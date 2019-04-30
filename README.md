# Byzantine-config

GUI based executable application that allows Hyperledger Fabric (HLF) configuration blocks to be viewed and updated transactions created for channel configuration, adding new organizations, and generating crypto material.

### Installation 

Download desired platform installation binary and execute. `Note`, it you `CLONE` this repo executable binaries will not work, since we are using the large file plugin to handle. Download desired platform binary. 

### Source Code 

Source code can be found at this repository [https://github.com/hyperledger-labs/byzantine-config](https://github.com/hyperledger-labs/byzantine-config)

### Usage 

Updating a Hyperledger Fabric network configuration and adding/updating organizations requires a configuration block to be defined, signed and then executed as an update config transaction. Doing this manually with CLI tools can be complex and cumbersome.   

Byantine-config provides an executable `GUI` application that greatly simplifies updating and adding Organizations. When invoked an initial connect screen will appear.  You will need a network peer node address, Userid, access to your private key, and Fabric Binaries 

![](images/connect.png)


Once connected the current configuration block is displayed... 

![](images/config-block.png)


Clicking the `add` and an org link will prompt for new Org name and properties, input desired values then click generate. You can also click `edit` to change current configuration

![](images/add-org.png)


Crypto artifacts for the new Org and an `updated config block `<your org>_update_in_envelop.pb` will be generated. This config PB will need to besigned by the consortium based upon policy settings. 

![](images/generated-pb.png)













