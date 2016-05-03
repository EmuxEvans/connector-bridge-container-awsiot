mbed Device Connector integration bridge image importer for AWS IoT Device Gateway 

Date: May 3, 2016

LOG:
    5/03/2016: Initial checkin

Container Bridge source (Apache 2.0 licensed - Enjoy!): https://github.com/ARMmbed/connector-bridge.git


Container Bridge Instance Installation:

1). Clone this repo into a Linux instance that supports docker images

2). cd into the cloned repo and run: ./run-reload-bridge.sh

3). Note the public IP address of your linux runtime - update "start-bridge.sh" and replace "192.168.1.230" with yours

4). invoke: ./start-bridge.sh

Once the container instance is live, you must configure the bridge and bind it between your mbed Connector account and your IoT Account in AWS

<<< TBD>>>

3). Next go to https://connector.mbed.com and create your mbed Connector Account

4). Once your Connector account is created, you need to "Access Keys" to create an API Key/Token

Now that you have your:

    - AWS Access Key ID

    - AWS Secret Access Key

    - Connector API Key/Token generated

Go to:  https://[[your containers public IP address]]:8234

    - username: "admin" (no quotes)

    - password: "admin" (no quotes)

Enter each of Key ID, Access Key, and Connector API Token

    - Please press "SAVE" after *each* is entered... 

    - After all 3 are entered and saved, press "RESTART"

Your AWSIoT-Connector bridge should now be configured and operational. 

For your mbed endpoint, you can clone and build (via yotta) this: https://github.com/ARMmbed/mbed-ethernet-sample

    - This sample assumes you are using the NXP K64F + mbed Application Shield

Enjoy!
