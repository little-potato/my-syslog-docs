# **System**

## **Public Fields**

| Field | Value | **Explanation** |
| --- | --- | --- |
| timestamp | ISO 8601 timestamp format | The date and time the event has been triggered. |
| team_id | Integer | Splashtop Team ID. |
| category | String | Splashtop events category. |
| kind | String | Splashtop events kind under specific category. |
| action | **add** or **update** or **delete** | The event operating action type in the event. |
| account | String | The user account that initiated the specific event. |
| source_agent | **browser** or **client** or **streamer** or **openapi** or **scim** or **system** | The origin client of the specific event. |
| source_address | String | IPv4 format. The origin IP address in the specific event. |
| source_version | String | The origin client version in the specific event. |
| source_os | String | The origin operating system in the the event. |
| source_name | String | The origin client name in the specific event. |
| target_agent | **browser** or **client** or **streamer** | The target device type in the event. |
| target_address | String | IPv4 format. The target IP address in the event. |
| target_version | String | The target agent version in the event. |
| target_os | String | The target agent platform in the event |
| target_name | String | The target device name in the event. |
| target_account | String | The target user account in the event. |
| result | String | Success or failure of the event. |

## **Network**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| gateway_url_updated | The Splashtop Gateway URL has been modified and saved. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | **gateway_url** | The target configuration item of the event. |
| old_url | String | The previous Gateway URL. |
| new_url | String | The updated Gateway URL. |

## **SMTP Server**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| smtp_server_added | A new SMTP server has been added and saved. |
| smtp_server_enabled | An SMTP server has been enabled. |
| smtp_server_disabled | An SMTP server has been disabled. |
| smtp_server_updated | An existing SMTP server has been modified and saved. The modified item (address or email) is recorded in the target field. |
| smtp_server_removed | An existing SMTP server has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The target SMTP server address, or the specific configuration item that has been updated: **address** or **email**. |
| old_addr | String | The previous SMTP server address. |
| new_addr | String | The updated SMTP server address. |
| old_email | String | The previous sender Email address. |
| new_email | String | The updated sender Email address. |

## **Syslog Server**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| syslog_server_added | A new syslog server has been added and saved. |
| syslog_server_updated | An existing syslog server has been modified and saved. |
| syslog_server_removed | An existing syslog server has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target syslog server. |
| FQDN | String | The address (FQDN) of the added syslog server. |
