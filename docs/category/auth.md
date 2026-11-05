# **Auth**

## **Public Fields**

| Field | Value | **Explanation** |
| --- | --- | --- |
| timestamp | ISO 8601 timestamp format | The date and time the event has been triggered. |
| team_id | Integer | Splashtop Team ID. |
| category | String | Splashtop events category. |
| kind | String | Splashtop events kind under specific category. |
| action | **login** or **logout** | The event operating action type in the event. |
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

## **User**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| login | A user has attempted to log in to the Splashtop Gateway from the Business app or the web console. The result is **success** when the login has been completed, or **failure** when the login has been rejected; the reason of a failed login is recorded in the extra_result field. |
| logout | A user has logged out from the web console. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account that attempted to log in or log out. |
| method1 | **ad** or **local** or **sso** | The primary authentication method of the login: an AD account, a local account, or an SSO account. |
| method2 | **2fa_passcode** or **2fa_recovery_code** | The secondary authentication method of the login when two-factor authentication is in use: a 2FA passcode or a 2FA recovery code. This field is present only when the login has reached the 2FA step. |
| extra_result | String | The reason of a failed login. See the table below. This field is present only when the result is **failure**. |

### extra_result values

| **Value** | **Explanation** |
| --- | --- |
| account_disabled | The user account has been disabled. |
| account_lockout | The user account has been locked out due to too many failed login attempts. |
| pwd_incorrect | The password is incorrect. |
| need_resetpwd | The user is required to reset the password before logging in. |
| need_rotate_password | The password has expired and the user is required to change the password. |
| violate_policy_need_reset | The password does not meet the current password policy and the user is required to reset it. |
| need_2fa | The login requires two-factor authentication and the 2FA code has not been provided yet. |
| 2fa_code_incorrect | The 2FA passcode is incorrect. |
| 2fa_recovery_code_incorrect | The 2FA recovery code is incorrect. |
| need_device_auth | The login from the Business app requires device authentication and the device has not been authenticated yet. |
| need_browser_auth | The login from the web console requires browser authentication and the browser has not been authenticated yet. |
| web_access_disabled | The user account is not allowed to access the web console. |
| mac_address_restriction | The login has been rejected by the MAC address restriction. |
| out_of_seat | The login has been rejected because the team has no available license seat for the AD account. |
| user_count_limit_exceeded | The login has been rejected because the number of users in the team has reached the user count limit for the AD account. |
