# PagerDuty Action Plugin

## Overview

![images_community/download/attachments/159187800/icon.png](images_community/download/attachments/159187800/icon.png)

Allows dynaTrace incidents to be forwarded to PagerDuty via PagerDuty API.

Checks the API URL first using a GET request then processes the incident using POST.

## Plugin Details

| Name | PagerDuty Action Plugin
| :--- | :---
| Author | Josh Cho ([josh.cho@compuware.com](mailto:josh.cho@compuware.com))
| Supported dynaTrace Versions | >= 5.5
| License | [dynaTrace BSD](dynaTraceBSD.txt)
| Support | Community Supported (https://community.compuwareapm.com/community/display/DL/Support+Levels)
| Release History | 2014-03-14 Initial Release
| Download | [com.dynatrace.pagerduty_1.0.0.jar.zip](com.dynatrace.pagerduty_1.0.0.jar.zip)

## Installation

Import the Plugin into the dynaTrace Server. For details how to do this please refer to the [Online Documentation on Plugin Management](https://community.compuwareapm.com/community/display/DOCDT56/Plugin+Management).

## Configuration

  1. Select the incident you want to set up PagerDuty alerting against and open the edit dialog. 

  2. In the 'Actions' tab, ensure the PagerDuty Plugin is added and set to fire 'on incident begin'. 

  3. Ensure correct API key is added from your PagerDuty services. Optionally set URL and/or TCP timeout. 

The following screenshot shows an example configuration:

![images_community/download/attachments/159187800/Capture.PNG](images_community/download/attachments/159187800/Capture.PNG)

![images_community/download/attachments/159187800/image2014-3-14_9_9_45.png](images_community/download/attachments/159187800/image2014-3-14_9_9_45.png)

![images_community/download/attachments/159187800/image2014-3-14_9_33_34.png](images_community/download/attachments/159187800/image2014-3-14_9_33_34.png)

Logs should indicate each incident that is forwarded:

2014-03-14 09:07:51 INFO [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Successfully forwarded incident to PagerDuty for
incident: URL Monitor/HostReachable : HostReachable (easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound exceeded. The incident key is:
bba7de8b04364ab2874802eb7c0442a4

Set logs to FINE if more detail is required:

2014-03-14 09:07:50 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Checking connectivity...  
2014-03-14 09:07:50 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Sending 'GET' request to URL :
<https://events.pagerduty.com/generic/2010-04-15/create_event.json>  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Response Code : 400  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Incident URL Monitor/HostReachable : HostReachable
(easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound exceeded triggered.  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Using API KEY - 67316670793b407e897ad09263b179a5  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Measure HostReachable (easyTravel Availability
Monitor@localhost) violoated threshold.  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Measure HostReachable violoated threshold.  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] JSON String is:
{"service_key":"67316670793b407e897ad09263b179a5","details":{"Severity":"Informational","Incident Rule":"easyTravel Availability","Violation":"HostReachable violated
threshold"},"client":"dynaTrace","description":"URL Monitor\/HostReachable : HostReachable (easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound
exceeded","event_type":"trigger","client_url":"slo124829n01"}  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Trying to get output stream...  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Trying to write to output stream  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Trying to connect...  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Response Code : 200  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Status: success  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Message: Event processed  
2014-03-14 09:07:51 FINE [[PagerDutyActionPlugin@com.dynatrace.pagerduty.action](mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action)] Incident Key: bba7de8b04364ab2874802eb7c0442a4

## Feedback

Please provide feedback on this plugin either by commenting on this page or by comments on the [Community Plugins and Extensions](https://community.compuwareapm.com/community/display/DTFORUM/Community+Plugins+and+Extensions)

