# **Session**

## **Public Fields**

| Field | Value | **Explanation** |
| --- | --- | --- |
| timestamp | ISO 8601 timestamp format | The date and time the event has been triggered. |
| team_id | Integer | Splashtop Team ID. |
| category | String | Splashtop events category. |
| kind | String | Splashtop events kind under specific category. For session events the kind is the same as the session type of the event. |
| action | String | Not applicable to session events. |
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

Session events are logged when a session between a Business app (client) and a computer (streamer) has ended. The computer that the session was connected to is recorded in the target_* public fields.

| **Event** | **Trigger** |
| --- | --- |
| remote_session | A remote control session to a computer has ended. |
| file_transfer_session | A file transfer session (without remote control) to a computer has ended. |
| file_transfer | A file has been transferred between the Business app and a computer, in a remote control session or in a file transfer session. |
| chat_session | A chat session with a computer has ended. |
| remote_cmd_session | A remote command session to a computer has ended. |
| remote_cmd | A command has been executed on a computer in a remote command session. |
| system_tool_session | A system tools session to a computer has ended. |
| rmm_session | An RMM session to a computer has been established. |
| sos_remote_session | An SOS (attended) remote control session to an end-user device has ended. |
| sos_file_transfer | A file has been transferred between the Business app and an end-user device in an SOS session. |
| sos_system_tool_session | An SOS (attended) system tools session to an end-user device has ended. |

## **Fields**

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account of the RMM session. Present only in the rmm_session event; for the other session events the target computer is recorded in the target_* public fields. |
| duration | String | The duration of the session. |
| type | **lan** or **wan** or **rdp_lan** or **rdp_wan** or **vnc_lan** or **vnc_wan** | The connection type of the session: whether the session was established over the local network (lan) or over the Internet via the Gateway (wan), and whether the session was a native streamer session, an RDP session (rdp_*), or a VNC session (vnc_*). The rdp_* and vnc_* values apply to remote_session only; the rdp_* values also apply to file_transfer. |
| file_name | String | The name of the file that has been transferred. |
| cmd | String | The command that has been executed in the remote command session. |
