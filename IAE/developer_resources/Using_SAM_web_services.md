---
layout: dev_resources
title: Using the SAM Web Services
nav: using_SAM_web_services
---
### Using SAM Web Services 
SAM offers web services to search for both Entity data and Exclusions data.<br>

<b>Entity Management data can be searched by:</b><br>

* ```DUNSNumber``` (Both DUNS and DUNS + 4)
* ```CAGECode```
* ```taxpayerIdentificationNumber``` (requires addtional access  [Click here](/developer_resources/Access_SAM_data.html "Data Access") for more information.)<br>
* ```startDate``` & ```endDate``` (Maximum search time allowed between startDate and endDate is 24 hours.)
* ```registrationStatus```

The web service returns the Entity Management Record in XML format for you to consume into your local application. The Entity Management record has four areas:<br>
* ```coreData```<br>
* ```assertions```<br>
* ```repsAndCerts``` (Representations and Certifications)<br>
* ```POCs```(Points of Contact)<br>

You have to put a "Y" in any one of the above element tags to get a result from the web service. <br>

<b>EndPoint:</b> [https://gw.sam.gov/SAMWS/1.0/Entity](https://gw.sam.gov/SAMWS/1.0/Entity)<br>
<b>WSDL File:</b>[https://gw.sam.gov/SAMWS/1.0/Entity?wsdl](https://gw.sam.gov/SAMWS/1.0/Entity?wsdl)

Need more help? Click [here](https://github.com/GSA/IAE-Architecture/tree/master/as-is/tech-docs/SAM) for the SAM entity web service management tutorial.<br> <br>

<b>Exclusions can be searched by:</b> <br>
* ```Name``` (including Business Name, First/Last Name, Partial Name)<br>
* ```Social Security Number```<br>
* ```Taxpayer Identification Number```<br>
* ```Cage Code```<br>
* ```DUNS``` number.<br> <br>If there is a match the web service returns the Public Exclusion Record in XML for you to consume into your own system.<br>
<b>EndPoint:</b> [https://gw.sam.gov/SAMWS/1.0/ExclusionSearch](https://gw.sam.gov/SAMWS/1.0/ExclusionSearch) <br>
<b>WSDL File:</b>[https://gw.sam.gov/SAMWS/1.0/ExclusionSearch?wsdl](https://gw.sam.gov/SAMWS/1.0/ExclusionSearch?wsdl)


###Testing SAM Web Services

| Web Service | Endpoint in Test Environment |
|---|---|
| SAM Entity Management |[https://test.sam.gov/SAMWS/1.0/Entity](https://test.sam.gov/SAMWS/1.0/Entity)|
| SAM Exclusion |[https://test.sam.gov/SAMWS/1.0/ExclusionSearch](https://test.sam.gov/SAMWS/1.0/ExclusionSearch)|



<b>Test IDs:</b>

| ID Name | Password | Description | 
|---|---|---|---|
| SAMPublic | Contact IAETransparency@gsa.gov | The public Entity Management Web Service requires authentication |
| SAMFOUO | Contact IAETransparency@gsa.gov | For Official Use Only | 
| SAMSensitive | Contact IAETransparency@gsa.gov | Offers more secure data including banking information and MPIN. |

A test id is not needed for the SAM Exclusions XML web service. There is no role or authentication requirement.
For more information on SAM account access levels click [here](http://gsa.github.io/IAE-Transparency-Space/IAE/developer_resources/Access_SAM_data.html).
 

Tools available:

| Tool Name | Description |
|---|---|
| [Web Services tutorial](https://github.com/GSA/IAE-Architecture/tree/master/as-is/tech-docs/SAM) | Documents how to build an Entity Management web service. |
| [Sample XML request/response]() | Included in the web services tutorial. Various sample request and response for Entity Management. |
| [Soap UI project]() | Project ready for import into Soap UI. (http://www.soapui.org/) |
| [SAM Functional Data Dictionary](https://github.com/GSA/IAE-Architecture/blob/master/as-is/tech-docs/SAM/SAM%20Functional%20Data%20Dictionary%20v4.0.pdf) |All SAM field definitions and enumerations.|
| [Web Services Response Schema Documentation]() | Coming Soon! |

Comments? Questions?  [Talk to us](https://github.com/GSA/IAE-Transparency-Space/issues).



