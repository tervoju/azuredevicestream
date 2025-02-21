# Azure IoT Hub - DeviceStreams Sample
**Example how to work with Azure IoT Hub Device Streams**


-------------------------------------

This example shows how to work with Azure IoT Hub - Device Streams when using SSH to connect to a IoT device via Internet/IoT Hub.

`DeviceProxy` represents local proxy for IoT device which acts as client for the local SSH daemon. It's responsible for authenticating against IoT Hub as well as creating a WebSocket connection to streaming endpoint of Azure IoT Hub.

`ServiceProxy` represents proxy for service which acts as a server for a local SSH client. It's responsible for authenticating against IoT Hub as well as creating a WebSocket connection to streaming endpoint of Azure IoT Hub.

`DeviceProxy` and `ServiceProxy` communicates with each other using created WebSocket via streaming endpoint of Azure IoT Hub.

Further information: https://www.fzankl.de/en/blog/remote-access-for-iot-devices-using-azure-iot-hub

## How to run this sample

To run this example you have to provide valid IoT Hub configuration via *launchSettings.json* for DeviceProxy and ServiceProxy.

## microsoft material
https://learn.microsoft.com/en-us/azure/iot-hub/iot-hub-device-streams-overview


https://github.com/Azure-Samples/azure-iot-samples-csharp/tree/preview/iot-hub/Samples/service/DeviceStreamingSample
https://www.nuget.org/packages/Microsoft.Azure.Devices.Client/1.41.0-preview-001 - seems not to have the device stream feature


netstandard2.1
- Microsoft.Azure.Devices.Client contains devicestream
https://nuget.info/packages/Microsoft.Azure.Devices.Client/1.32.0-preview-001 - seems to have the device stream feature
