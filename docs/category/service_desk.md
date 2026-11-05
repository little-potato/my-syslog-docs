# **Service Desk**

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

## **Channel**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| channel_created | A new Service Desk channel has been created and saved. |
| channel_name_updated | The name of a channel has been updated. |
| channel_description_updated | The description of a channel has been updated. |
| channel_expiration_time_updated | The support session expiration time of a channel has been updated. |
| channel_enabled | A channel has been enabled. |
| channel_disabled | A channel has been disabled. |
| default_channel_set | A channel has been set as the default channel of the team. |
| channel_removed | An existing channel has been deleted. |
| technician_associated | A technician (user) has been associated with a channel. |
| technician_disassociated | A technician (user) has been disassociated from a channel. |
| technician_group_assicated | A technician group has been associated with a channel. |
| technician_group_disassociated | A technician group has been disassociated from a channel. |
| technician_support_session_permission_updated | The support session permission of a technician (user) in a channel has been updated. |
| technician_group_support_session_permission_updated | The support session permission of a technician group in a channel has been updated. |
| channel_sos_call_enabled | The SOS Call function has been enabled for a channel. |
| channel_sos_call_disabled | The SOS Call function has been disabled for a channel. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target channel. |
| name | String | The previous name of the channel. |
| new name | String | The updated name of the channel. |
| time | String | The previous support session expiration time of the channel. |
| new time | String | The updated support session expiration time of the channel. |
| user | String | The name of the technician (user) that has been associated with, disassociated from, or updated in the channel. |
| group | String | The name of the technician group that has been associated with, disassociated from, or updated in the channel. |
| permission | String | The updated support session permission of the technician or technician group in the channel. |

## **Support Session**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| support_session_created | A new support session has been created in a channel or as a private session. |
| support_session_name_updated | The name of a support session has been updated. |
| support_session_taken | A technician has taken a support session. |
| support_session_released | A technician has released a support session back to the channel. |
| support_session_closed | A support session has been closed. |
| support_session_deleted | A support session has been deleted. |
| support_session_transfered | A support session has been transferred to another technician. |
| support_session_expired | A support session has expired and been closed automatically by the system. |
| technician_invited | A technician has been invited to assist in a support session. |
| technician_assgined | A technician has been assigned to a support session. |
| comment_updated | The comment of a support session has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target support session. |
| channel | String | The name of the channel that the support session belongs to, or **Private(\<email\>)** for a private session created by the technician. |
| new name | String | The updated name of the support session. |
| user | String | The name of the technician that the support session has been transferred to or assigned to. |
| assistant | String | The name of the technician that has been invited to assist in the support session. |

## **SOS Call**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| sos_call_created | A new SOS Call has been created in a channel. |
| sos_call_name_updated | The name of an SOS Call has been updated. |
| sos_call_app_name_updated | The app name of an SOS Call has been updated. |
| sos_call_technician_assigned | A technician has been assigned to, or unassigned from, an SOS Call. |
| sos_call_resumed | A suspended SOS Call has been resumed. |
| sos_call_suspended | An SOS Call has been suspended. |
| sos_call_removed | An existing SOS Call has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target SOS Call. |
| channel | String | The name of the channel that the SOS Call belongs to. |
| new name | String | The updated name or app name of the SOS Call. |
| user | String or **Unassigned** | The name of the technician that the SOS Call has been assigned to, or **Unassigned** when the technician has been removed from the SOS Call. |

