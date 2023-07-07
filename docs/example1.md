[README](../README.md)

# Example 1

## Unauthorized Devices
Devices in FortiManager are synchronized to FortiSOAR for handling. 

![](./images/ex1a.png)

## Assign ZTP Profile
We will manually select these devices and manually assign the ZTP Profile `Report-and-Onboard`. 

![](./images/ex1b.png)

## Authorize Devices
The ZTP Profile kicks off the first ZTP Phase defined which is `Authorize` the device(s). We can see FortiSOAR performing these steps via the API in FortiManager. 

![](./images/ex1c.png)