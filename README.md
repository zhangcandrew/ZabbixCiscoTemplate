# ZabbixCiscoTemplate
Generic template for low-level-discovery of Cisco Devices to return Device Model Name, Serial Number, Fans, Temperature Monitoring and other items. The code was adapted to work with Zabbix 3.0. Based off the work presented [here](https://github.com/jjmartres/Zabbix/tree/master/zbx-templates/zbx-cisco/zbx-cisco-envmon) which previously only supported up to Zabbix 2.4.

Updated SNMPv2 OID discovery to work with Zabbix 3.0 since there are syntax changes in Low Level Discovery

##Default Configuration
Information from the two device prototypes under the Device Name discovery rule is set to update **daily**.  
Fan and Power Supply Discovery Rules are set to update every **5 minutes**.  
Temperature Discovery Rules are set to update every **30 minutes**.   
All discovered devices are set to remain in history for **30 days**.  
Make sure the SNMP community key is correctly configured in your Macros to allow Zabbix to talk to SNMPv2 Devices.  
Device Serial Number and Device Model Name under template items, not item prototypes, should both be disabled and only used when lower level discovery fails for some reason.   

## Implementing a Local Copy
Download the .xml file by clicking the raw button in the top right corner. 
Import the .xml template into Zabbix 3.0 

## Built for Use With
Zabbix 3.0

## Contributing
JJMartres seems to have discontinued the merging of pull requests circa 3 years ago. Still worth trying though. 

## Authors

* **jjMartres** - *Initial work* - [Zabbix Templates](https://github.com/jjmartres/Zabbix/tree/master/zbx-templates)
