# aws-iot-dragconnect-c

### Arrow DragonConnect

The DragonConnect project demonstrates recording events originating from the
DragonBoard&trade; and managing an LED.  The events are generated by pressing
the volume up and volume down keys on the DragonBoard&trade;.  When one of the
buttons is pressed, a client application written using the Amazon IoT C SDK
for embedded platforms uses MQTT to transfer the event to an Amazon data
center where it is stored in a DynamoDB table.

The LED is managed through the General Purpose IO (GPIO) of the
DragonBoard&trade; and uses AWS IoT Device Shadows.

The functionality of DragonConnect and how the application is configured is
detailed.  The documentation includes information on how to execute the client
and visit the dashboard.

# Getting Started
Please have the following information available:

* Amazon Account Number - (https://console.aws.amazon.com/billing/home#/account)
* Stage - Amazon API Gateway deploys to a stage, so it must be specified, By default 'dev' is used. (http://arrowelectronics.github.io/aws-iot-dragonconnect-c/admin/api.html)
* S3 Identifier - S3 is used to host the client, it would be best to give it something unique. By default the last 5 characters of the machine id is used. (http://arrowelectronics.github.io/aws-iot-dragonconnect-c/admin/dashboard.html)

After the setup has completed, there are a few urls that are provided. Please make note of them: AWS Endpoint, AWS API Gateway, and Dashboard

1. Navigate to the root of Arrow DragonConnect `/home/linaro/arrow/aws-iot-dragonnect-c`
2. Run the setup script
```sh
    $ cd scripts
    $ ./setup.sh
```
3. Start the Client
```sh
    $ cd DragonBoard/bin
    $ sudo ./aws_demo
```
4. Visit the DragonConnect Dashboard (http://arrowelectronics.github.io/aws-iot-dragonconnect-c/execution/dashboard.html)

## Uninstall and Cleanup

All the settings from the install are stored `scripts/.settings`
```sh
    $ cd scripts
    $ ./uninstall.sh 
```

For more information on the DragonConnect project, including how it is
deployed and configured, visit the
<a href="https://arrowelectronics.github.io/aws-iot-dragonconnect-c" target="_blank">DragonConnect Project Page</a>.

# License
This SDK is distributed under the
[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0),
see LICENSE.txt and NOTICE.txt for more information
