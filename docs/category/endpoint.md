# **Endpoint**

## **Public Fields**

| Field | Value | **Explanation** |
| --- | --- | --- |
| timestamp | ISO 8601 timestamp format | The date and time the event has been triggered. |
| team_id | Integer | Splashtop Team ID. |
| category | String | Splashtop events category. |
| kind | String | Splashtop events kind under specific category. |
| action | **authenticate** or **deploy** or **update** or **delete** or **disconnect** | The event operating action type in the event. |
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

## **Browser**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| browser_authenticated | A browser has been authenticated for a user to access the web console. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account that the browser has been authenticated for. |
| method | **email** or **web** | The method used to authenticate the browser: via the authentication link in the Email, or via the web console by an admin. |

## **Client**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| client_authenticated | A Business app (client) device has been authenticated for a user. |
| client_removed | An existing Business app (client) device has been removed from the authenticated device list of a user. |
| request_force_disconnected | A Business app (client) has been forced to disconnect all of its remote sessions. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account that the client has been authenticated for, or the name of the target client device. |
| method | **email** or **web** | The method used to authenticate the client: via the authentication link in the Email, or via the web console by an admin. |
| disconnected_streamer_list | String | The list of the computers whose sessions have been disconnected from the client. |

## **Streamer**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| streamer_deployed | A new computer (streamer) has been deployed and added to the team. |
| streamer_removed | An existing computer (streamer) has been removed from the team. |
| streamer_name_updated | The name of a computer has been updated. |
| streamer_note_updated | The note of a computer has been updated. |
| streamer_group_assigned | A computer has been moved to another computer group. |
| streamer_disconnected | All remote sessions of a computer have been disconnected. |
| request_wakeup_computer | A Wake-on-LAN request has been sent to a computer. |
| request_reboot_computer | A request to reboot a computer has been sent. |
| request_safe_mode_reboot_computer | A request to reboot a computer in safe mode has been sent. |
| request_restart_streamer | A request to restart the streamer service of a computer has been sent. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target computer. |
| old_name | String | The previous name of the computer. |
| new_name | String | The updated name of the computer. |
| old_group | String | The computer group that the computer belonged to previously. |
| new_group | String | The computer group that the computer has been moved to. |

## **SOS**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| support_session_device_associated | An end-user device has joined a support session via the SOS app. |
| service_desk_session_permission_requested | A technician has requested a permission (for example, elevated privilege) from the end-user in a support session. |
| service_desk_session_permission_accepted | The end-user has accepted the permission request in a support session. |
| service_desk_session_permission_refused | The end-user has refused the permission request in a support session. |
| service_desk_session_permission_revoked | The end-user has revoked a permission that was granted previously in a support session. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target support session. |
| channel | String | The name of the channel that the support session belongs to, or **Private(\<email\>)** for a private session created by the technician. |
| pemission | String | The permission that has been requested, accepted, refused, or revoked in the support session. |
