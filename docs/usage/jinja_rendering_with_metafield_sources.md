| [Home](../../README.md) / [Usage](../usage.md) |
|------------------------------------------------|

# Jinja Rendering with Metafield Sources

Metafield sources are used to create dynamic Jinja variable input for Jinja templates. These can be leveraged in the following record types:
 - ZTP Profile Assignment Search Type = Jinja
 - Metafield Templates
 - Script Templates

When leveraging Jinja Templates from this framework you have Jinja Variables at your disposal and by default the attributes `record` and `devmeta`. You can see this info when rendering script templates or metafield templates by looking for the `get_jinja_variables` step or `jinja_vars` variable within the `Render Jinja` playbook execution logs. Once you have sample data you can open the `Tools > Jinja Editor` by editing any playbook and manually paste your Jinja Variables into the `JSON` section and then your `Jinja Template` to test the results of your script. 
```
{
  "jinja_vars": {
    "record": {
      "id": 258,
      "sn": "FG00001",
      "adom": "root",
      "vdom": "root",
      "devname": "FG00001",
      "firmware": "7.2.0-build1514",
      "hostname": null,
      "platform": "FortiGate-80F-POE",
      "meta_fields": {
        "Address": "",
        "Contact Email": "admin@test.com",
        "Company/Organization": "",
        "Contact Phone Number": ""
      },
      "connector_config": "FMG1-1"
    },
    "devmeta": {
      "site_id": 100,
      "site_subnet": "192.168.10.0/24"
    }
  }
}
```

When you add a Metafield Source you will append data to the defined `keynmame` as a new attribute with your additional custom data to then be used within your Jinja Template. 
```
{
  "jinja_vars": {
    "record": {},
    "devmeta": {},
    "metafield_source_keyname": {}
  }
}
```

# Metafield Source Types
Metafield source types describe how we can retrieve data to be used in a jinja template. 

 - fmg 
 - playbook 

Metafield sources can contain multiple sources and can be mixed of API and Playbooks. Source types have a different schema as different parameters are required to retrieve the Jinja variables. Below are details of the schema as well as examples that can be used in records that render Jinja. 

## Metafield Source Type: fmg

### Schema (fmg)

The following source type will leverage a FMG JSON-RPC `GET` action on the API endpoint defined in the `location`. Ideally this is for retrieving tables or objects from the FMG API. 

```
[
  {
    "source_type": "fmg",
    "source": "<fmg connector config_name>",
    "keyname": "<attribute name for data>",
    "location": "<api url>"
  }
]
```

### Example (fmg)

In this example we are grabbing the `interface` table for the device name from the record where we are rendering the Jinja. 

```
[
  {
    "source_type": "fmg",
    "source": "{{record.connector_config}}",
    "keyname": "interfaces",
    "location": "/pm/config/device/{{record.devname}}/global/system/interface"
  }
]
```

## Metadata Source Type: playbook

### Schema (playbook)

The following source type will leverage any custom playbook in FortiSOAR. This means you can create your own logic for building Jinja Variables that can come from any supported integration. 

```
[
  {
    "source_type": "playbook",
    "keyname": "<attribute name for data>",
    "playbook_id": "<custom playbook id found in url of playbook>",
    "payload": "<input data for playbook>"
  }
]
```

### Example (playbook)

The following example is used in the ZTP Flow Feature Examples. These playbooks perform simple logic and return data to showcase how custom playbooks can be leveraged. 

```
[
  {
    "source_type": "playbook",
    "keyname": "ip_table",
    "playbook_id": "9e6cff1f-0fe3-4c85-bf25-5cb409cea778",
    "argument": ""
  },
  {
    "source_type": "playbook",
    "keyname": "ip_table_lookup",
    "playbook_id": "1c6e570a-605e-46ac-9125-32f2af1877e7",
    "argument": "{{record.devname}}"
  }
]
```
