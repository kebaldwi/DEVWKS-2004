# DevNet Cisco DNA Center Advanced REST API with Postman 

This set of Cisco Learning Labs is developed around a set of simple use cases to show both the power of DNA Center, the APIs, and easy methodologies for execution through Postman. This is an advanced lab. While not mandatory it is recommended that you first complete the [DNE DNA Center REST API with Postman](https://testing-developer.cisco.com/learning/tracks/dna-devnet-express/dnac-dne-postman/)

| Module ID | PubHub Link |
|-----------|-------------|
| dnac-dne-postman | https://pubhub.cisco.com/detail/4500 |

| Lab ID | PubHub link |
|--------|-------------|
| dnac-0-orientation | https://pubhub.cisco.com/detail/ |
| dnac-1-hierarchy | https://pubhub.cisco.com/detail/ |
| dnac-2-settings | https://pubhub.cisco.com/detail/ |
| dnac-3-discovery | https://pubhub.cisco.com/detail/ |
| dnac-4-templates | https://pubhub.cisco.com/detail/ |
| dnac-5-archive | https://pubhub.cisco.com/detail/ |
| dnac-6-inventory | https://pubhub.cisco.com/detail/ |
| dnac-7-cmd-run | https://pubhub.cisco.com/detail/ |
| dnac-8-pythonapp | https://pubhub.cisco.com/detail/ |
| dnac-9-ansible | https://pubhub.cisco.com/detail/ |

> **Note**: The following section of the README contains information for DevNet Express instructors.

## The DCLOUD environment

For DevNet Express events, use this environment: 

> **LAB Environment**: [Cisco Enterprise Networks Hardware Sandbox](https://dcloud2-sjc.cisco.com/content/catalogue?search=Enterprise%20Networks%20Hardware%20Sandbox&screenCommand=openFilterScreen)

The DCLOUD session includes the following equipment.

### Virtual Machines:
  * DNA Center 2.2.3.4 or better
  * Identity Services Engine (ISE) 3.0 Patch 4 or better (deployed)
  * Identity Services Engine (ISE) 3.0 (Not deployed)
  * Stealthwatch 7.4.0 or better
  * FlowCollector 7.4.0 or better
  * Cisco Prime Infrastructure 3.10  or better
  * Script Server - Ubuntu 20.04  or better
  * Wireless LAN Controller - C9800 running IOS-XE Bengaluru 17.5.1 code or better
  * Windows 10 Jump Host 
  * Windows Server 2019 - Can be configured to provide identity, DHCP, DNS, etc.
  * Windows 10 Clients

### Hardware Devices:
  * ISR 4451 Router - 17.06.01a IOS-XE Code
  * Catalyst 9300 Switch - 17.06.01 IOS-XE Code with Embedded Wireless Controller (EWC) and ThousandEyes Enterprise Agent
  * 9130AX Access Points
  * Silex Controllers (3 Wired NIC's and 1 Wireless NIC)

The following diagram shows the dCloud topology.

![](./assets/DCLOUD_Topology2.png?raw=true)

### dCLOUD VPN Connection

Use AnyConnect VPN to connect to dCLOUD. When connecting, look at the session details and copy the credentials from the session booked into the client to connect.

![](./assets/VPN-to-dCLOUD.png?raw=true)

> **Documentation**: For AnyConnect Documentation visit: <a href="https://dcloud-cms.cisco.com/help/android_anyconnect" target="_blank">dCloud AnyConnect Documentation</a>

> **Download**: Get AnyConnect here: <a href="https://dcloud-rtp-anyconnect.cisco.com" target="_blank">⬇︎ AnyConnect Download Site ⬇︎</a>

### dCLOUD Service Optimization

The dCLOUD environment must be optimized prior to the session, and to do this, we need to disable the following settings:

![](./assets/ShutdownUnused.png?raw=true)

Use the drop-down menu item by each that is shutdown in the image and click the shutdown link.

### SSL Settings and disabling Validation
For lab purposes, DNA Center uses a self-signed certificate which would fail any validation precheck. Disable the setting to proceed with the Labs.

Follow these steps:

1. Click the settings gear icon on the top right of Postman to select settings.

   ![](./assets/Postman-Settings-Menu.png?raw=true)

2. Deselect the `SSL certificate verification`

   ![](./assets/Postman-Settings-SSL-Validation-On.png?raw=true)

### Postman Collection and Environment Import

Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration so you can create better APIs—faster.

Once Postman has been downloaded to your desktop, it is advisable to set up an account and sign in so that all your changes can be used within any system with the client or a web browser, much in the same way as a chrome or firefox profile work. This additional capability I have found instrumental when working in multiple environments. 

> **Download**: Get Postman here: <a href="https://www.postman.com/downloads/" target="_blank">⬇︎ Postman Download ⬇︎</a>

> **Documentation**: For an understanding of postman, please visit: <a href="https://learning.postman.com/docs/getting-started/introduction/" target="_blank">Postman Documentation</a>

To prepare Postman for the Lab, download the following student collection and environment zip file and upload them into Postman. The file includes six collections and one environment. Right-click and open this link in a new tab to download them:
   
> **Download**: Please download the following lab bundle. [⬇︎ Lab-Bundle ⬇︎](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/kebaldwi/DNAC-TEMPLATES/blob/master/LABS/LAB-I-Rest-API-Orchestration/postman/DNACenter-UseCase-API-Collection.zip)

> **Download**: Please download the accompanying CSV: [⬇︎ CSV-Bundle ⬇︎](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/kebaldwi/DNAC-TEMPLATES/blob/master/LABS/LAB-I-Rest-API-Orchestration/csv/DNAC-Design-Settings.csv)

Once the files have been downloaded, uncompress/unzip it and import all the files into Postman. Walk students through the lab as a student using the lab within the LLC.

## Summary

DNA Center should be set up and ready for the attendees.

> **Disclaimer**: Various labs are designed for use in the **DCLOUD** environment but can but are for use elsewhere. The environment allows for use with a web-based browser client for VPN-less connectivity, access as well as AnyConnect VPN client connectivity for those who prefer it. The labs are hosted out of our San Jose and RTP Facilities so that you would choose sessions from either US East or US West. Choose the Cisco Enterprise Network Sandbox v4 or greater To access this or any other content, including demonstrations, labs, and training in dCloud, please work with your Cisco Account team or Cisco Partner Account Team directly. Your Account teams will make sure the session is scheduled and shared for you to use. Once booked, follow the guide within Github to complete the tasks adhering to the best practices of the dCLOUD environment.

> **Feedback**: If you found this set of Labs helpful, please fill in comments and [give feedback](https://app.smartsheet.com/b/form/f75ce15c2053435283a025b1872257fe) on how it could be improved.
