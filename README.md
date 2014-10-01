<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>PagerDuty Action Plugin</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
    <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
    <meta content="Scroll Wiki Publisher" name="generator"/>
    <link type="text/css" rel="stylesheet" href="css/blueprint/liquid.css" media="screen, projection"/>
    <link type="text/css" rel="stylesheet" href="css/blueprint/print.css" media="print"/>
    <link type="text/css" rel="stylesheet" href="css/content-style.css" media="screen, projection, print"/>
    <link type="text/css" rel="stylesheet" href="css/screen.css" media="screen, projection"/>
    <link type="text/css" rel="stylesheet" href="css/print.css" media="print"/>
</head>
<body>
                <h1>PagerDuty Action Plugin</h1>
    <div class="section-2"  id="159187800_PagerDutyActionPlugin-Overview"  >
        <h2>Overview</h2>
    <p>
            <img src="images_community/download/attachments/159187800/icon.png" alt="images_community/download/attachments/159187800/icon.png" class="confluence-embedded-image" />
            </p>
    <p>
Allows dynaTrace incidents to be forwarded to PagerDuty via PagerDuty API.    </p>
    <p>
Checks the API URL first using a GET request then processes the incident using POST.    </p>
    </div>
    <div class="section-2"  id="159187800_PagerDutyActionPlugin-PluginDetails"  >
        <h2>Plugin Details</h2>
    <div class="tablewrap">
        <table>
<thead class=" "></thead><tfoot class=" "></tfoot><tbody class=" ">    <tr>
            <td rowspan="1" colspan="1">
        <p>
Author    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
Josh Cho (<a href="mailto:josh.cho@compuware.com">josh.cho@compuware.com</a>)    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
dynaTrace Versions    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
5.5, 5.6    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
License    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
<a href="attachments_5275722_2_dynaTraceBSD.txt">dynaTrace BSD</a>    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
Support    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
Community Supported    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
Known Problems    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
None (Yet...)    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
Release History    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
2014-03-14 Initial Release    </p>
            </td>
        </tr>
    <tr>
            <td rowspan="1" colspan="1">
        <p>
Download    </p>
            </td>
                <td rowspan="1" colspan="1">
        <p>
<a href="attachments_160761820_1_com.dynatrace.pagerduty_1.0.0.jar.zip">com.dynatrace.pagerduty_1.0.0.jar.zip</a>    </p>
            </td>
        </tr>
</tbody>        </table>
            </div>
    </div>
    <div class="section-2"  id="159187800_PagerDutyActionPlugin-Installation"  >
        <h2>Installation</h2>
    <p>
Import the Plugin into the dynaTrace Server. For details how to do this please refer to the <a href="https://community/display/DOCDT56/Plugin+Management">Online Documentation on Plugin Management</a>.    </p>
    </div>
    <div class="section-2"  id="159187800_PagerDutyActionPlugin-Configuration"  >
        <h2>Configuration</h2>
<ol class=" "><li class=" ">    <p>
Select the incident you want to set up PagerDuty alerting against and open the edit dialog.    </p>
</li><li class=" ">    <p>
In the 'Actions' tab, ensure the PagerDuty Plugin is added and set to fire 'on incident begin'.    </p>
</li><li class=" ">    <p>
Ensure correct API key is added from your PagerDuty services. Optionally set URL and/or TCP timeout.    </p>
</li></ol>    <p>
The following screenshot shows an example configuration:    </p>
    <p>
            <img src="images_community/download/attachments/159187800/Capture.PNG" alt="images_community/download/attachments/159187800/Capture.PNG" class="confluence-embedded-image" />
            </p>
    <p>
            <img src="images_community/download/attachments/159187800/image2014-3-14_9_9_45.png" alt="images_community/download/attachments/159187800/image2014-3-14_9_9_45.png" class="confluence-embedded-image" />
            </p>
    <p>
            <img src="images_community/download/attachments/159187800/image2014-3-14_9_33_34.png" alt="images_community/download/attachments/159187800/image2014-3-14_9_33_34.png" class="confluence-embedded-image" />
            </p>
    <p>
Logs should indicate each incident that is forwarded:    </p>
    <p>
2014-03-14 09:07:51 INFO [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Successfully forwarded incident to PagerDuty for incident: URL Monitor/HostReachable : HostReachable (easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound exceeded. The incident key is: bba7de8b04364ab2874802eb7c0442a4    </p>
    <p>
    </p>
    <p>
Set logs to FINE if more detail is required:    </p>
    <p>
2014-03-14 09:07:50 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Checking connectivity...<br/>2014-03-14 09:07:50 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Sending 'GET' request to URL : <a href="https://events.pagerduty.com/generic/2010-04-15/create_event.json">https://events.pagerduty.com/generic/2010-04-15/create_event.json</a><br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Response Code : 400<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Incident URL Monitor/HostReachable : HostReachable (easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound exceeded triggered.<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Using API KEY - 67316670793b407e897ad09263b179a5<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Measure HostReachable (easyTravel Availability Monitor@localhost) violoated threshold.<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Measure HostReachable violoated threshold.<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] JSON String is: {&quot;service_key&quot;:&quot;67316670793b407e897ad09263b179a5&quot;,&quot;details&quot;:{&quot;Severity&quot;:&quot;Informational&quot;,&quot;Incident Rule&quot;:&quot;easyTravel Availability&quot;,&quot;Violation&quot;:&quot;HostReachable violated threshold&quot;},&quot;client&quot;:&quot;dynaTrace&quot;,&quot;description&quot;:&quot;URL Monitor\/HostReachable : HostReachable (easyTravel Availability Monitor@localhost) easyTravel Availability Monitor lower bound exceeded&quot;,&quot;event_type&quot;:&quot;trigger&quot;,&quot;client_url&quot;:&quot;slo124829n01&quot;}<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Trying to get output stream...<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Trying to write to output stream<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Trying to connect...<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Response Code : 200<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Status: success<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Message: Event processed<br/>2014-03-14 09:07:51 FINE [<a href="mailto:PagerDutyActionPlugin@com.dynatrace.pagerduty.action">PagerDutyActionPlugin@com.dynatrace.pagerduty.action</a>] Incident Key: bba7de8b04364ab2874802eb7c0442a4    </p>
    <p>
    <span style="color: #505050;">
Feedback    </span>
    </p>
    <p>
Please provide feedback on this plugin either by commenting on this page or by comments on the <a href="https://community/display/DTFORUM/Community+Plugins+and+Extensions">Community Plugins and Extensions</a>    </p>
    </div>
            </div>
        </div>
        <div class="footer">
        </div>
    </div>
</body>
</html>
