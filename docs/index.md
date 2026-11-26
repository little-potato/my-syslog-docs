In addition to access logs from web console, Splashtop log events can also be sent to a Syslog server or SIEM tool that supports Syslog in your local environment. The auditing of Splashtop event logs can be accessed both from Gateway web console, download as CSV or Syslog collectors simultaneously.

### 1. Configuration

1. To configure Splashtop Gateway as Syslog source, log in web console as Team Owner, go to **Settings** → **Syslog**.

2. You can configure Gateway to send Syslog messages up to two Syslog servers.

3. Click add to configure your target Syslog server.

4. Syslog Settings

<table>
  <tr><th align="left">Name</th><td>Required display label for this syslog destination in the Gateway console.</td></tr>
  <tr><th align="left">Syslog Server address</th><td>Required hostname or IP address of the syslog server that will receive Gateway log messages.</td></tr>
  <tr><th align="left">Port</th><td>Destination port on the syslog server, default 514, range 1–65535.</td></tr>
  <tr><th align="left">Syslog Protocol</th><td>Transport used for delivery — UDP (default, lowest overhead, no delivery confirmation) or TCP (retransmits lost messages, preferred for audit trails).</td></tr>
  <tr><th align="left">Message Format</th><td>Message structure — RFC 5424 (default, recommended) or RFC 3164 BSD (legacy, for collectors that cannot parse RFC 5424).</td></tr>
  <tr><th align="left">Facility</th><td>Syslog facility for Gateway log messages, local0 by default; select a facility no other log source is using so Gateway traffic can be routed separately on your syslog server.</td></tr>
  <tr><th align="left">Severity</th><td>Syslog severity carried by Gateway log messages, Notice by default; select the level that matches how your log management system classifies remote access audit events.</td></tr>
  <tr><th align="left">Status</th><td>Enables forwarding to this destination, enabled by default.</td></tr>
  <tr><th align="left">Test Message</th><td>Sends a test message using the settings shown, without saving the configuration, to confirm the syslog server is reachable; enter custom text or leave blank to use the default.</td></tr>
</table>

### 2. Syslog Message Format

**Header**

<table>
  <tr><th align="left">Date/Time</th><td>Syslog event time</td></tr>
  <tr><th align="left">PRI</th><td>Local0.Notice</td></tr>
  <tr><th align="left">Hostname</th><td>IP/FQDN</td></tr>
  <tr><th align="left">APP-Name</th><td>onpremise.exe</td></tr>
  <tr><th align="left">PROCID</th><td>Process ID</td></tr>
  <tr><th align="left">MSGID</th><td>SOP</td></tr>
</table>

**Message Payload**

| **Parameters** | **Values** | **Description** |
| --- | --- | --- |
| **timestamp** | ISO 8601 timestamp format | The date and time the event has been triggered. |
| **team_id** | Integer | Splashtop Team ID. |
| **event** | String | The specific event was triggered. |
| **account** | String | The user account that initiated the specific event. |
| **source_address** | String | The origin IP address in the specific event. |
| **source_agent** | String | The origin client of the specific event. |
| **source_version** | String | The origin client version in the specific event. |
| **source_os** | String | The origin operating system in the specific event. |
| **source_name** | String | The origin client name in the specific event. |
| **target_address** | String | The target IP address in the event. |
| **target_version** | String | The target agent version in the event. |
| **target_os** | String | The target agent platform in the event. |
| **target_agent** | String | The target device type in the event. |
| **target_name** | String | The target device name in the event. |
| **target_account** | String | The target user account in the event. |
| **category** | String | Splashtop events category. |
| **kind** | String | Splashtop events kind under the specific category. |
| **action** | String | The event operating action type in the event. |
| **result** | String | Success or failure of the event |
| **extra_result** | String | The detailed failure reason in the event |
| **target** | String | The target object in the event. |
| **property** | String | Additional property in the event |
| **value** | String | Additional values in the event. |

### 3. Syslog message examples

Splashtop syslog message examples following standard RFC 5424 format are showing below.

**Example 1.**

```
05-13-2022 14:44:54 Local0.Notice 192.168.70.75 1 2022-05-13T14:44:54+05:00 Test-Vistro onpremise.exe 3292 SOP - timestamp=2022-05-13T09:44:54Z;team_id=1;event=team_file_transfer_enabled;account=john.doe@example.com;source_agent=browser;source_address=192.168.67.22;source_name=IE;source_version=110.0.1587;source_os=Windows;category=settings;kind=team;action=update;result=success;target=unattended_access;desc:file_transfer=enabled;

```

The example indicates event of enabling file transfer function from Team Settings occurred at a given time by what account with specific IP address and device information.

**Example 2.**

Below syslog messages were generated by a login attempt to Splashtop web console resulted in failure (2) because a privileged account has enabled browser authentication in an earlier time (1). Then the re-login succeeded (4) after the privileged account authenticated this login request from web console (3).

```
1. 08-22-2022 09:12:35 Local0.Notice 192.168.70.75 1 2022-08-22T09:12:35+05:00 Test-Vistro onpremise.exe 3292 SOP - timestamp=2022-05-13T04:12:35Z;team_id=1;event=team_browser_device_auth_enabled;account=john.doe@example.com;source_agent=browser;source_address=192.168.67.22;source_name=IE;source_version=111.0.1661;source_os=Windows;category=settings;kind=team;action=update;result=success;target=security;desc:browser_device_auth=enabled;

2. 08-22-2022 09:14:02 Local0.Notice 192.168.70.75 1 2022-08-22T09:14:02+05:00 Test-Vistro onpremise.exe 3292 SOP - timestamp=2022-05-13T04:12:35Z;team_id=1;event=login;account=mary.doe@example.com;source_agent=browser;source_address=192.168.89.176;source_name=Chrome;source_version=110.0.0;source_os=Mac;target_account=mary.doe@example.com;category=auth;kind=user_mgmt;action=login;result=failure;extra_result=need_device_auth;target=mary.doe@example.com;desc:=;

3. 08-22-2022 10:00:37 Local0.Notice 192.168.70.75 1 2022-08-22T10:00:37+05:00 Test-Vistro onpremise.exe 3292 SOP - timestamp=2022-05-13T05:00:37Z;team_id=1;event=client_authenticated;account=john.doe@example.com;source_agent=browser;source_address=192.168.67.22;source_name=IE;source_version=111.0.1661;source_os=Windows;target_address=192.168.89.176;target_agent=browser;target_version=110.0.0;target_os=Mac;target_name=Chrome;target_account=mary.doe@example.com;category=endpoint;kind=browser;action=authenticate;result=success;desc:method=web console;

4. 08-22-2022 10:08:22 Local0.Notice 192.168.70.75 1 2022-08-22T10:08:22+05:00 Test-Vistro onpremise.exe 3292 SOP - timestamp=2022-05-13T05:08:22Z;team_id=1;event=login;account=mary.doe@example.com;source_agent=browser;source_address=192.168.89.176;source_name=Chrome;source_version=110.0.0;source_os=Mac;target_account=mary.doe@example.com;category=auth;kind=user;action=login;result=success;extra_result=;target=mary.doe@example.com;desc:=;

```
