# Change Log
- 202306300429
  - Add custom playbook for reading spreadsheet files attached as metadata types.

- 202306290520
  - Add Retrieve Device Config Phase and Tested.

- 202306140940
  - Add monitor metadata support.

- 202306130429
  - Add support for custom playbook metadata sources. 

- 202306070550
  - Add metadata monitor regex fields and logic. Fixed device in device group bug. 

- 202306010456
  - Add script error handling. ZTP Phases now go to "Fail" if a joining step has errors. 

- 202305310506
  - Add error passing on script run to implement error handling. 

- 202305300523
  - Add support for Report Script Templates. 

- 202305190255
  - Create Packages if not defined and packages will be named by the device if not defined. 

- 202305150505
  - First addition to prompting user for metafield on create.
  - Updated the auto assign profile. 

- 202305120526
  - Add toggle for profile removals.
  - Add new playbooks for metafield handling and for auto assign options.

- 202305110404
  - Add logic to allow for chainint ZTP Profiles together. 

- 202305090500
  - Tweak ZTP Auto Assignment and add Step Configuration. 

- 202305080458
  - Added ZTP Trigger master playbook and implemented first assumed update path. 

- 202305041112
  - Add new ZTP Phases and begin the ZTP Phase trigger system. 

- 202304280608
  - Add ZTP Assignment and Mode picklists.

- 202304270403
  - Rename lots of buttons.
  - Added ZTP Phase data fields. 

- 202304251159
  - Running Provisioning Templates now assigns devices to groups and uses the ZTP Profile Template Group Name if set...otherwise use the devname. 

- 202304240533
  - Added lots of provision template playbooks. 

- 202304190457
  - ZTP Profiles run a link and metadata merge on change. 

- 202304170507
  - Metdata templates now also support rendering per device.

- 202304140318
  - Add Metafield Templates and ZTP Profiles.
  - Add RPC Set to Connector.
  - Add playbooks for managing variables. 

- 202304131036
  - Add record link from managers to devices. 

- 202304120915
  - Synch Managers now...also now can communicated with FortiCloud. 
  - Can manage metadata keys using records.
  - Support import and export of metafields

- 202304110456
  - Added metadata key add and delete functions. 

- 202304100415
  - Add device fields for provisioning and pkg.

- 202304070423
  - Add script to run on device option. 

- 202304070904
  - Add script to do dynamic var lookups.

- 202304060914
  - Tweak the create and execute script to function as desired. 

- 202304050458
  - Export wizard always leaves off new fields.
  - Missing some script module fields now added.

- 202304050456
  - Create new Script Module and Handle Create/Exec Script

- 202304051158
  - Add run script button. 
  - Migrate install and run script to handle one or more devices.

- 202303310447
  - Post upgrade 7.4.0.
  - Add spinner to install too.
  - Cleanup of some playbook views.

- 202303290444
  - Add status spinner.
  - 2x ways to API to FOS.
  - Set devices to delete if no longer found. 

- 202303280400
  - FOS Helper playbooks now use the util http instead of the http connector. 

- 202303270503
  - Add config management dashboard. 
 
- 202303240300
  - Add connection status as html.

- 202303231141
  - Repair missing fields from Export wizard. 

- 202303231115
  - Add new button to FMG devices that have been deleted.

- 202303231100
  - Add new playbook, FOS Helpers, for bootstrapping the FMG config on the FG. 

- 202303220454
  - Move status fields to an html and text version. 
  - Add source data field to devices. 
  - Change button logic to match status fields. 

- 202303201042
  - Support comma seperated configs on db synch.
  - Delete now also clears status fields. 

- 202303170601
  - Add synch with status in the playbook.

- 202303170332
  - Multitenant support. 
  - Device Records with comments.
  - Playbooks inclue synch, auth, and delete.
