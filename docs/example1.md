# [README](../README.md) -> Example1

## Unauthorized Devices
Devices in FortiManager are synchronized to FortiSOAR for handling. 

![](./images/ex1-001.png)

## Assign ZTP Profile
We will manually select these devices and manually assign the ZTP Profile `Report-and-Onboard`. 

![](./images/ex1-002.png)
![](./images/ex1-003.png)

## Authorize Devices
The ZTP Profile kicks off the first ZTP Phase defined which is `Authorize` the device(s). We can see FortiSOAR performing these steps via the API in FortiManager. 

![](./images/ex1-004.png)