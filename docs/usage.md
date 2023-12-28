| [Home](../README.md) |
|--------------------------------------------|

# Usage

The `FortiManager ZTP Flow` Solution Pack has a variety of uses. First, refer to the [installation and setup guide](setup.md) guide to get started. Use the example(s) found [below](#examples) to decide what provisioning options are available out of the box.

# Module Summary

## Managers
Manager records define the Fortimanagers, and the current firmware and status, used in your solution. Use this module to start the integration and/or simply report on the current status of your FortiMangers.

## Devices
Devices are synchronized from the FortiManager and stored in FortiSOAR. Then automation can occur on one or more devices based on operations and workflow needs. Once created in FortiSOAR they are not removed to preserve the last known status of the Device record even if the device has been removed, or moved, from your FortiManager. 

## Metafield Templates
Managing metafields is crucial to the success of any network deployment and provisioning.  Metafield Templates can be used to prompt required users to respond to unknown, but required, fields before deployment. Templates can be used to integrate external systems and retrieve key data requirements before deployment. Templates can be customized to create dynamic metadata based on a wide range of advanced and complex requirements. Metadata inside FortiSOAR can be exports to FortiManger to be used by already existing solutions with minimal effort. 

## Script Templates
Scripts in FortiSOAR for this Solution Pack can be used for creating customized FortiManager CLI, Device DB, Policy DB, and/or TCL Scripts per device. Scripts in FortiSOAR can also maintain and create Provisioning CLI Templates in FortiManager such as when new ADOMs are created and need to be setup with Templates. Device reporting script can also be used to create a custom dashboard with user defined content.  

## [ZTP Profiles](usage/ztp_profile.md)>
The ZTP Profiles module describes how to handle the provisioning of each device maintained by the respective FortiManager. As a device shows up in the FortiManager Device DB, unauthorized or modeled, when ZTP Profiles are assigned to those devices the defined device templates and provisioning steps are applied and reported per device. ZTP Profiles can be assigned on demand or automatically assigned when devices are created in FortiManger regardless of how the devices were created.

# Examples

 * [Example1](./usage/example1.md): Provision of 4x Unauthorized FortiGates VMs in FortiManager starting by simply assigning a ZTP Profile.

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|