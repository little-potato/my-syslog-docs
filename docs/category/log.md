# **Log**

## **Public Fields**

| Field | Value | **Explanation** |
| --- | --- | --- |
| timestamp | ISO 8601 timestamp format | The date and time the event has been triggered. |
| team_id | Integer | Splashtop Team ID. |
| category | String | Splashtop events category. |
| kind | String | Splashtop events kind under specific category. |
| action | **delete** | The event operating action type in the event. |
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

## **Events and triggers**

| **Event** | **Trigger** |
| --- | --- |
| remote_session_recording_removed | A remote session recording has been deleted from the session logs in the web console. |
| sos_session_recording_removed | An SOS session recording has been deleted from the session logs in the web console. |

## **Fields**

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account that the deleted session recording belongs to. |
| start_time | String | The start time of the session that the deleted recording belongs to. |
| end_time | String | The end time of the session that the deleted recording belongs to. |
