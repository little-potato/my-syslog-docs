# **Settings**

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

## **AD Server**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| adserver_added | A new AD server has been added and saved. |
| adserver_ldap_updated | The LDAP address of an AD server has been updated. |
| adserver_name_updated | The name of an AD server has been updated. |
| adserver_removed | An existing AD server has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target AD server. |
| ldap_addr | String | The added/updated LDAP address of the AD server. |
| name | String | The updated name of the AD server. |

## **Unattended Access**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_grant_granular_file_transfer_download_updated | The admin-configurable value of the file transfer (download) has been updated for the team. |
| team_grant_granular_file_transfer_upload_updated | The admin-configurable value of the file transfer (upload) has been updated for the team. |
| team_grant_granular_remote_command_updated | The admin-configurable value of the remote command has been updated for the team. |
| team_grant_granular_remote_print_updated | The admin-configurable value of the remote print has been updated for the team. |
| team_grant_granular_request_permission_updated | The admin-configurable value of the request permission to connect has been updated for the team. |
| team_grant_granular_text_copy_paste_local_remote_updated | The admin-configurable value of the copy and paste (from local to remote) has been updated for the team. |
| team_grant_granular_text_copy_paste_remote_local_updated | The admin-configurable value of the copy and paste (from remote to local) has been updated for the team. |
| team_grant_granular_watermark_protection_updated | The admin-configurable value of the watermark protection has been updated for the team. |
| team_granular_file_transfer_download_admin_updated | The team’s granular control of the file transfer (download) for admins has been updated. |
| team_granular_file_transfer_download_member_updated | The team’s granular control of the file transfer (download) for members has been updated. |
| team_granular_file_transfer_upload_admin_updated | The team’s granular control of the file transfer (upload) for admins has been updated. |
| team_granular_file_transfer_upload_member_updated | The team’s granular control of the file transfer (upload) for members has been updated. |
| team_granular_remote_command_admin_updated | The team’s granular control of the remote command for admins has been updated. |
| team_granular_remote_command_member_updated | The team’s granular control of the remote command for members has been updated. |
| team_granular_remote_print_admin_updated | The team’s granular control of the remote print for admins has been updated. |
| team_granular_remote_print_member_updated | The team’s granular control of the remote print for members has been updated. |
| team_granular_request_permission_admin_updated | The team’s granular control of the request permission to connect for admins has been updated. |
| team_granular_request_permission_member_updated | The team’s granular control of the request permission to connect for members has been updated. |
| team_granular_text_copy_paste_local_remote_admin_updated | The team’s granular control of the copy and paste (from local to remote) for admins has been updated. |
| team_granular_text_copy_paste_local_remote_member_updated | The team’s granular control of the copy and paste (from local to remote) for members has been updated. |
| team_granular_text_copy_paste_remote_local_admin_updated | The team’s granular control of the copy and paste (from remote to local) for admins has been updated. |
| team_granular_text_copy_paste_remote_local_member_updated | The team’s granular control of the copy and paste (from remote to local) for members has been updated. |
| team_granular_watermark_protection_admin_updated | The team’s granular control of the watermark protection for admins has been updated. |
| team_granular_watermark_protection_member_updated | The team’s granular control of the watermark protection for members has been updated. |
| team_granular_request_permission_admin_updated | The team’s granular control of the request permission to connect for admins has been updated. |
| team_granular_request_permission_member_updated | The team’s granular control of the request permission to connect for members has been updated. |
| team_granular_centralized_session_recording_unattended_admin_updated | The team’s granular control of the centralized session recording (unattended) for admins has been updated. |
| team_granular_centralized_session_recording_unattended_member_updated | The team’s granular control of the centralized session recording (unattended) for members has been updated. |
| team_grant_granular_rcentralized_session_recording_unattended_updated | The admin-configurable value of the centralized session recording (unattended) has been updated for the team. |
| team_granular_system_tools_admin_updated | The team’s granular control of the system tools (unattended) for admins has been updated. |
| team_granular_system_tools_member_updated | The team’s granular control of the system tools (unattended) for members has been updated. |
| team_grant_granular_system_tools_updated | The admin-configurable value of the system tools (unattended) has been updated for the team. |
| team_granular_request_permission_rdp_admin_updated | The team’s granular control of the request permission to connect (RDP session) for admins has been updated. |
| team_granular_request_permission_rdp_member_updated | The team’s granular control of the request permission to connect (RDP session) for members has been updated. |
| team_grant_granular_request_permission_rdp_updated | The admin-configurable value of the  request permission to connect (RDP session) has been updated for the team. |
| team_remove_offline_computers_days_updated | The offline computer policy settings have been updated. |
| team_session_indicator_remote_session_type_updated | The display type of the remote session indicator has been updated. |
| team_session_indicator_background_action_type_updated | The display type of the background action session indicator has been updated. |
| team_centralized_session_recording_disabled | The centralized session recording function has been disabled for unattended access at the team level. |
| team_centralized_session_recording_enabled | The centralized session recording function has been enabled for unattended access at the team level. |
| team_concurrent_session_disabled | The concurrent session has been disabled for unattended access. |
| team_concurrent_session_enabled | The concurrent session has been enabled for unattended access. |
| team_device_redirect_disabled | The device redirection function has been disabled for unattended access at the team level. |
| team_device_redirect_enabled | The device redirection function has been enabled for unattended access at the team level. |
| team_file_transfer_disabled | The file transfer function has been disabled for unattended access. |
| team_file_transfer_enabled | The file transfer function has been enabled for unattended access. |
| team_keystroke_paste_disabled | The paste clipboard as keystrokes function has been disabled for unattended access. |
| team_keystroke_paste_enabled | The paste clipboard as keystrokes function has been enabled for unattended access. |
| team_mac_address_restriction_disabled | The MAC address restriction has been disabled at the team level. |
| team_mac_address_restriction_enabled | The MAC address restriction has been enabled at the team level. |
| team_mac_address_restriction_updated | The settings of the MAC address restriction have been updated. |
| team_rdp_computer_disabled | The RDP computer has been disabled at the team level. |
| team_rdp_computer_enabled | The RDP computer has been enabled at the team level. |
| team_remote_command_disabled | The remote command function has been disabled at the team level. |
| team_remote_command_enabled | The remote command function has been enabled at the team level. |
| team_remote_mic_disabled | The remote microphone function has been disabled at the team level. |
| team_remote_mic_enabled | The remote microphone function has been enabled at the team level. |
| team_remote_print_disabled | The remote print function has been disabled at the team level. |
| team_remote_print_enabled | The remote print function has been enabled at the team level. |
| team_remote_reboot_disabled | The remote reboot computer function has been disabled at the team level. |
| team_remote_reboot_enabled | The remote reboot computer function has been enabled at the team level. |
| team_remote_voice_call_disabled | Remote session voice call has been disabled. |
| team_remote_voice_call_enabled | Remote session voice call has been enabled. |
| team_remote_wakeup_disabled | The remote wakeup function for computers has been disabled at the team level. |
| team_remote_wakeup_enabled | The remote wakeup function for computers has been enabled at the team level. |
| team_remote_web_app_disabled | The Web app for unattended access has been disabled. |
| team_remote_web_app_enabled | The Web app for unattended access has been enabled. |
| team_remove_offline_computers_disabled | The offline computer policy has been disabled at the team level. |
| team_remove_offline_computers_enabled | The offline computer policy has been enabled at the team level. |
| team_session_chat_disabled | The pre-session chat function has been disabled at the team level. |
| team_session_chat_enabled | The pre-session chat function has been enabled at the team level. |
| team_session_recording_disabled | The local session recording has been disabled at the team level. |
| team_session_recording_enabled | The local session recording has been enabled at the team level. |
| team_ssh_session_disabled | The SSH computer has been disabled at the team level. |
| team_ssh_session_enabled | The SSH computer has been enabled at the team level. |
| team_text_copypaste_disabled | The copy and paste function has been disabled at the team level. |
| team_text_copypaste_enabled | The copy and paste function has been enabled at the team level. |
| team_vnc_session_disabled | The VNC computer has been disabled at the team level. |
| team_vnc_session_enabled | The VNC computer has been enabled at the team level. |
| team_wacom_bridge_disabled | The Wacom Bridge function has been disabled at the team level. |
| team_wacom_bridge_enabled | The Wacom Bridge function has been enabled at the team level. |
| team_watermark_disabled | The watermark function has been disabled for unattended access. |
| team_watermark_enabled | The watermark function has been enabled for unattended access. |
| team_system_tool_enabled | The system tools has been enabled for unattended access. |
| team_system_tool_disabled | The system tools has been disabled for unattended access. |
| team_close_banner_remote_session_enabled | The function of allowing users to close the indicator banner has been enabled for remote sessions. |
| team_close_banner_remote_session_disabled | The function of allowing users to close the indicator banner has been disabled for remote sessions. |
| team_close_banner_background_action_enabled | The function of allowing users to close the indicator banner has been enabled for background action sessions. |
| team_close_banner_background_action_disabled | The function of allowing users to close the indicator banner has been disabled for background action sessions. |
| team_save_off_session_chat_transcript_enabled | The save off-session chat transcript has been enabled at team level. |
| team_save_in_session_chat_transcript_enabled | The save in-session chat transcript has been enabled for unattended access. |
| team_save_off_session_chat_transcript_disabled | The save off-session chat transcript has been disabled at team level. |
| team_save_in_session_chat_transcript_disabled | The save in-session chat transcript has been disabled for unattended access. |
| system_tool_permission_updated | The roles that are allowed to use the system tools for unattended access have been updated. |
| team_sos_service_desk_system_tool_enabled | The system tools has been enabled for SOS and Service Desk sessions. |
| team_sos_service_desk_system_tool_disabled | The system tools has been disabled for SOS and Service Desk sessions. |
| team_srep_https_session_enabled | The HTTP/S computer has been enabled for unattended access at the team level. |
| team_srep_https_session_disabled | The HTTP/S computer has been disabled for unattended access at the team level. |
| team_srep_port_session_enabled | The port forwarding computer has been enabled for unattended access at the team level. |
| team_srep_port_session_disabled | The port forwarding computer has been disabled for unattended access at the team level. |
| team_redirect_cam_enabled | The redirect camera input function has been enabled for unattended access at the team level. |
| team_redirect_cam_disabled | The redirect camera input function has been disabled for unattended access at the team level. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| grant_granular_file_transfer_download | **on** or **off** | The admin has been granted or not granted the permission to configure file transfer (download). |
| grant_granular_file_transfer_upload | **on** or **off** | The admin has been granted or not granted the permission to configure file transfer (upload). |
| grant_granular_remote_command | **on** or **off** | The admin has been granted or not granted the permission to configure remote command. |
| grant_granular_remote_print | **on** or **off** | The admin has been granted or not granted the permission to configure remote print. |
| grant_granular_request_permission | **on** or **off** | The admin has been granted or not granted the permission to configure request-to-connect permission . |
| grant_granular_text_copy_paste_local_remote | **on** or **off** | The admin has been granted or not granted the permission to configure copy and paste (from local to remote). |
| grant_granular_text_copy_paste_remote_local | **on** or **off** | The admin has been granted or not granted the permission to configure copy and paste (from remote to local). |
| grant_granular_watermark_protection | **on** or **off** | The admin has been granted or not granted the permission to configure watermark protection. |
| granular_file_transfer_download_admin | **on** or **off** | The team’s granular control of the file transfer (download) for admins has been turned on or off. |
| granular_file_transfer_download_member | **on** or **off** | The team’s granular control of the file transfer (download) for members has been turned on or off. |
| granular_file_transfer_upload_admin | **on** or **off** | The team’s granular control of the file transfer (upload) for admins has been turned on or off. |
| granular_file_transfer_upload_member | **on** or **off** | The team’s granular control of the file transfer (upload) for members has been turned on or off. |
| granular_remote_command_admin | **on** or **off** | The team’s granular control of the remote command for admins has been turned on or off. |
| granular_remote_command_member | **on** or **off** | The team’s granular control of the remote command for members has been turned on or off. |
| granular_remote_print_admin | **on** or **off** | The team’s granular control of the remote print for admins has been turned on or off. |
| granular_remote_print_member | **on** or **off** | The team’s granular control of the remote print for members has been turned on or off. |
| granular_request_permission_admin | **on** or **off** | The team’s granular control of the request permission to connect for admins has been turned on or off. |
| granular_request_permission_member | **on** or **off** | The team’s granular control of the request permission to connect for members has been turned on or off. |
| granular_text_copy_paste_local_remote_admin | **on** or **off** | The team’s granular control of the copy and paste (from local to remote) for admins has been turned on or off. |
| granular_text_copy_paste_local_remote_member | **on** or **off** | The team’s granular control of the copy and paste (from local to remote) for members has been turned on or off. |
| granular_text_copy_paste_remote_local_admin | **on** or **off** | The team’s granular control of the copy and paste (from remote to local) for admins has been turned on or off. |
| granular_text_copy_paste_remote_local_member | **on** or **off** | The team’s granular control of the copy and paste (from remote to local) for members has been turned on or off. |
| granular_watermark_protection_admin | **on** or **off** | The team’s granular control of the watermark protection for admins has been turned on or off. |
| granular_watermark_protection_member | **on** or **off** | The team’s granular control of the watermark protection for members has been turned on or off. |
| granular_request_permission_admin | String | The team’s granular control of the request permission to connect for admins has been turned on or off. |
| granular_request_permission_member | String | The team’s granular control of the request permission to connect for members has been turned on or off. |
| granular_centralized_session_recording_unattended_admin | **on** or **off** | The team’s granular control of the centralized session recording (unattended) for admins has been turned on or off. |
| granular_centralized_session_recording_unattended_member | **on** or **off** | The team’s granular control of the centralized session recording (unattended) for members has been turned on or off. |
| grant_granular_rcentralized_session_recording_unattended | **on** or **off** | The admin has been granted or not granted the permission to configure centralized session recording (unattended). |
| granular_system_tools_admin | **on** or **off** | The team’s granular control of the system tools (unattended) for admins has been turned on or off. |
| granular_system_tools_member | **on** or **off** | The team’s granular control of the system tools (unattended) for members has been turned on or off. |
| grant_granular_system_tools | **on** or **off** | The admin has been granted or not granted the permission to configure system tools (unattended). |
| granular_request_permission_rdp_admin | String | The team’s granular control of the request permission to connect (RDP session) for admins has been turned on or off. |
| granular_request_permission_rdp_member | String | The team’s granular control of the request permission to connect (RDP session) for members has been turned on or off. |
| grant_granular_request_permission_rdp | **on** or **off** | The admin has been granted or not granted the permission to configure request permission to connect (RDP session). |
| remove_offline_computers_days | String | The computer offline day threshold for offline computer policy. |
| exec_at | String | The daily time of running the offline computer policy. |
| session_indicator_type | **Both** or **Pop-up** or **Banner** or **None** | The indicator type for remote session or background actions. |
| system_tool_permission | **Owner only** or **group managers, admins and owner** or **Members, group managers, admins and owner** | The roles that are allowed to use the system tools. |

## **User Settings**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_group_manager_disabled | Group manager role has been disabled at the team level. |
| team_group_manager_enabled | Group manager role has been enabled at the team level. |
| team_member_connect_active_session_disabled | The function of allowing member roles to connect to the active session has been disabled. |
| team_member_connect_active_session_enabled | The function of allowing member roles to connect to the active session has been enabled. |
| team_member_create_multi_session_disabled | The function of allowing member roles to establish multiple sessions concurrently has been disabled. |
| team_member_create_multi_session_enabled | The function of allowing member roles to establish multiple sessions concurrently has been enabled. |
| team_member_disconnect_session_disabled | The function of allowing member roles to disconnect the active session has been disabled. |
| team_member_disconnect_session_enabled | The function of allowing member roles to disconnect the active session has been enabled. |
| team_member_reboot_disabled | The function of allowing member roles to reboot computers and Streamers has been disabled. |
| team_member_reboot_enabled | The function of allowing member roles to reboot computers and Streamers has been enabled. |
| team_member_see_group_disabled | The function of allowing member roles to see all groups has been disabled. |
| team_member_see_group_enabled | The function of allowing member roles to see all groups has been enabled. |
| team_remote_reboot_action_updated | The settings of allowing member roles to reboot computers and Streamers have been updated. |
| team_member_permission_for_computer_notes_updated | The settings of member’s permission for computer notes have been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| remote_reboot_member | String | Actions that member role is allowed to perform on the computers. |
| permission_for_computer_notes | **cannot view and edit** or **view only** or **view and edit** | Whether member role cannot view and edit the computer notes, can only view the computer notes, or can view and edit the computer notes. |

## **General**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_name_updated | The name of the team has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| name | String | The updated name of the team. |

## **Security**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_pwd_min_len_updated | The minimum password length of the password policy has been updated. |
| team_pwd_expiration_enabled | The password expiration has been enabled at the team level. |
| team_pwd_expiration_disabled | The password expiration has been disabled at the team level. |
| team_pwd_exp_duration_updated | The password expiration duration has been updated. |
| team_force_apply_pwd_policy_enabled | Forcing all users to apply the password policy has been enabled at the team level. |
| team_force_apply_pwd_policy_disabled | Forcing all users to apply the password policy has been disabled at the team level. |
| team_lockout_policy_enabled | The account lockout policy has been enabled at the team level. |
| team_lockout_policy_disabled | The account lockout policy has been disabled at the team level. |
| team_lockout_policy_updated | The settings of the account lockout policy have been updated. |
| team_idle_timeout_hours_updated | The idle timeout for the web console has been updated (in hours). |
| team_idle_timeout_minutes_updated | The idle timeout for the web console has been updated (in minutes). |
| team_idle_user_logout_from_client_hours_updated | The idle timeout for logging out users from the Business app has been updated (in hours). |
| team_idle_user_logout_from_client_minutes_updated | The idle timeout for logging out users from the Business app has been updated (in minutes). |
| team_device_timeout_enabled | The device timeout (idle timeout for the Business app) has been enabled at the team level. |
| team_device_timeout_disabled | The device timeout (idle timeout for the Business app) has been disabled at the team level. |
| team_remember_app_login_enabled | Allowing users to stay logged in to the Business app has been enabled at the team level. |
| team_remember_app_login_disabled | Allowing users to stay logged in to the Business app has been disabled at the team level. |
| team_client_device_auth_enabled | The device authentication for the Business app has been enabled at the team level. |
| team_client_device_auth_disabled | The device authentication for the Business app has been disabled at the team level. |
| team_client_device_auth_duration_updated | The validity duration of the device authentication for the Business app has been updated. |
| team_client_device_auth_request_expiration_time_updated | The expiration time of the device authentication request for the Business app has been updated. |
| team_browser_device_auth_enabled | The browser authentication for the web console has been enabled at the team level. |
| team_browser_device_auth_disabled | The browser authentication for the web console has been disabled at the team level. |
| team_browser_device_auth_duration_updated | The validity duration of the browser authentication for the web console has been updated. |
| team_browser_device_auth_request_expiration_time_updated | The expiration time of the browser authentication request for the web console has been updated. |
| team_turn_on_device_auth_when_2FA_on | Keeping the device authentication on for users who have enabled 2FA has been turned on. |
| team_turn_off_device_auth_when_2FA_on | Keeping the device authentication on for users who have enabled 2FA has been turned off. |
| team_allow_trust_device_enabled | Allowing users to trust devices for 2FA has been enabled at the team level. |
| team_allow_trust_device_disabled | Allowing users to trust devices for 2FA has been disabled at the team level. |
| team_2FA_trust_device_exp_updated_days | The expiration of trusted devices for 2FA has been updated to a number of days. |
| team_2FA_trust_device_exp_updated_forever | The expiration of trusted devices for 2FA has been updated to never expire. |
| team_granular_require_2fa_admin_updated | The team’s granular control of the require 2FA for admins has been updated. |
| team_granular_require_2fa_member_updated | The team’s granular control of the require 2FA for members has been updated. |
| team_grant_granular_require_2fa_updated | The admin-configurable value of the require 2FA has been updated for the team. |
| team_granular_remote_control_admin_updated | The team’s granular control of the remote control for admins has been updated. |
| team_granular_remote_control_member_updated | The team’s granular control of the remote control for members has been updated. |
| team_grant_granular_remote_control_updated | The admin-configurable value of the remote control has been updated for the team. |
| save_credential_enabled | Allowing users to save the computer login credentials in the Business app has been enabled at the team level. |
| save_credential_disabled | Allowing users to save the computer login credentials in the Business app has been disabled at the team level. |
| save_security_code_enabled | Allowing users to save the security code of computers in the Business app has been enabled at the team level. |
| save_security_code_disabled | Allowing users to save the security code of computers in the Business app has been disabled at the team level. |
| team_conditional_access_enabled | The conditional access has been enabled at the team level. |
| team_conditional_access_disabled | The conditional access has been disabled at the team level. |
| team_granular_conditional_access_admin_updated | The team’s default granular control of the conditional access for admins and group managers has been updated. |
| team_granular_conditional_access_member_updated | The team’s default granular control of the conditional access for members has been updated. |
| team_grant_granular_conditional_access_updated | The admin-configurable value of the conditional access has been updated for the team. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| pwd_min_len | String | The updated minimum password length. |
| pwd_exp_duration | String | The updated password expiration duration. |
| lockout_threhold | String | The updated number of failed login attempts before the account is locked out. |
| lockout_duration | String | The updated duration that the account stays locked out. |
| idle_timeout | String | The updated idle timeout for the web console, in hours or minutes according to the event. |
| client_logout_ttl | String | The updated idle timeout for logging out users from the Business app, in hours or minutes according to the event. |
| device_auth_duration | String | The updated validity duration of the device authentication for the Business app. |
| device_auth_request_exp_time | String | The updated expiration time of the device authentication request for the Business app. |
| browser_auth_duration | String | The updated validity duration of the browser authentication for the web console. |
| browser_auth_request_exp_time | String | The updated expiration time of the browser authentication request for the web console. |
| 2fa_ttl | String | The updated number of days before a trusted device for 2FA expires. |
| granular_require_2fa_admin | **on** or **off** or **verification with Authenticator app** or **verification with Email** | The team’s granular control of the require 2FA for admins. |
| granular_require_2fa_member | **on** or **off** or **verification with Authenticator app** or **verification with Email** | The team’s granular control of the require 2FA for members. |
| grant_granular_require_2fa | **on** or **off** | The admin has been granted or not granted the permission to configure require 2FA. |
| granular_remote_control_admin | **on** or **off** | The team’s granular control of the remote control for admins has been turned on or off. |
| granular_remote_control_member | **on** or **off** | The team’s granular control of the remote control for members has been turned on or off. |
| grant_granular_remote_control | **on** or **off** | The admin has been granted or not granted the permission to configure remote control. |
| granular_conditional_access_admin | Policy name or **off** | The conditional access policy applied to admins and group managers by default, or **off** when no policy is applied. |
| granular_conditional_access_member | Policy name or **off** | The conditional access policy applied to members by default, or **off** when no policy is applied. |
| grant_granular_conditional_access | **on** or **off** | The admin has been granted or not granted the permission to configure conditional access. |

## **Attended Access**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_sos_use_granular_settings_enabled | Using the granular settings for attended access has been enabled at the team level. |
| team_sos_use_granular_settings_disabled | Using the granular settings for attended access has been disabled at the team level. |
| team_sos_concurrent_session_enabled | The concurrent session has been enabled for attended access. |
| team_sos_concurrent_session_disabled | The concurrent session has been disabled for attended access. |
| team_sos_web_app_enabled | The Web app for attended access has been enabled. |
| team_sos_web_app_disabled | The Web app for attended access has been disabled. |
| team_sos_file_transfer_enabled | The file transfer function has been enabled for attended access. |
| team_sos_file_transfer_disabled | The file transfer function has been disabled for attended access. |
| team_sos_file_transfer_direction | The allowed direction of the file transfer for attended access has been updated. |
| team_sos_text_copypaste_enabled | The copy and paste function has been enabled for attended access. |
| team_sos_text_copypaste_disabled | The copy and paste function has been disabled for attended access. |
| team_sos_text_copypaste_direction | The allowed direction of the copy and paste for attended access has been updated. |
| team_sos_keystroke_paste_enabled | The paste clipboard as keystrokes function has been enabled for attended access. |
| team_sos_keystroke_paste_disabled | The paste clipboard as keystrokes function has been disabled for attended access. |
| team_sos_voice_call_enabled | The voice call has been enabled for attended access. |
| team_sos_voice_call_disabled | The voice call has been disabled for attended access. |
| team_sos_watermark_enabled | The watermark function has been enabled for attended access. |
| team_sos_watermark_disabled | The watermark function has been disabled for attended access. |
| team_sos_session_indicator_type_updated | The display type of the session indicator for attended access has been updated. |
| team_sos_close_banner_enabled | The function of allowing users to close the indicator banner has been enabled for attended access. |
| team_sos_close_banner_disabled | The function of allowing users to close the indicator banner has been disabled for attended access. |
| team_sos_centralized_session_recording_enabled | The centralized session recording function has been enabled for attended access at the team level. |
| team_sos_centralized_session_recording_disabled | The centralized session recording function has been disabled for attended access at the team level. |
| team_granular_centralized_session_recording_attended_admin_updated | The team’s granular control of the centralized session recording (attended) for admins has been updated. |
| team_granular_centralized_session_recording_attended_member_updated | The team’s granular control of the centralized session recording (attended) for members has been updated. |
| team_grant_granular_centralized_session_recording_attended_updated | The admin-configurable value of the centralized session recording (attended) has been updated for the team. |
| team_sos_save_in_session_chat_transcript_enabled | The save in-session chat transcript has been enabled for attended access. |
| team_sos_save_in_session_chat_transcript_disabled | The save in-session chat transcript has been disabled for attended access. |
| service_desk_transcripts_name_display_updated | The name type displayed in the Service Desk chat transcripts has been updated. |
| team_sos_global_invitation_template_enabled | The global invitation template for attended access has been enabled at the team level. |
| team_sos_global_invitation_template_disabled | The global invitation template for attended access has been disabled at the team level. |
| team_sos_global_invitation_template_updated | The global invitation template for attended access has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| file_transfer_direction | String | The updated allowed direction of the file transfer for attended access. |
| text_copy_paste_direction | String | The updated allowed direction of the copy and paste for attended access. |
| session_indicator_type | **Banner** or **None** | The indicator type for attended access sessions. |
| granular_centralized_session_recording_attended_admin | **on** or **off** | The team’s granular control of the centralized session recording (attended) for admins has been turned on or off. |
| granular_centralized_session_recording_attended_member | **on** or **off** | The team’s granular control of the centralized session recording (attended) for members has been turned on or off. |
| grant_granular_rcentralized_session_recording_attended | **on** or **off** | The admin has been granted or not granted the permission to configure centralized session recording (attended). |
| name_type | **account name** or **display name** | The name type displayed in the Service Desk chat transcripts. |

## **Endpoint Management**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_os_patch_enabled | The OS patch function has been enabled for endpoint management at the team level. |
| team_os_patch_disabled | The OS patch function has been disabled for endpoint management at the team level. |
| team_os_patch_scan_schedule_updated | The default scan schedule of the OS patch has been updated. |
| team_os_patch_install_schedule_updated | The default install schedule of the OS patch has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| mode | **Daily** or **Weekly** or **Monthly** | The recurrence mode of the schedule. |
| days | String | The days of the schedule: the day of the week (**Monday** to **Sunday**) for a weekly schedule, or the day of the month (**1** to **31**, or **last day**) for a monthly schedule. Empty for a daily schedule. |
| time | String | The time of day of the schedule, in **HH:MM** format (00:00 to 23:59). |

## **Others**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| team_notification_computer_online_enabled | The Email notification for computers going online has been enabled at the team level. |
| team_notification_computer_online_disabled | The Email notification for computers going online has been disabled at the team level. |
| team_notification_computer_online_recipient_updated | The recipients of the Email notification for computers going online have been updated. |
| team_notification_computer_offline_enabled | The Email notification for computers going offline has been enabled at the team level. |
| team_notification_computer_offline_disabled | The Email notification for computers going offline has been disabled at the team level. |
| team_notification_computer_offline_recipient_updated | The recipients of the Email notification for computers going offline have been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| recipient | **Owner** or **Admins and owner** | The updated recipients of the Email notification. |

## **SSO**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| sso_method_added | A new SSO method has been added and saved. |
| sso_method_updated | An existing SSO method has been modified and saved. The modified item is recorded in the corresponding field. |
| sso_method_removed | An existing SSO method has been deleted. |
| default_sso_method_updated | The default SSO method of the team has been updated. |
| set_sso_saml_entity_id | The SAML entity ID of the team has been set. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target SSO method, or **sso_settings** for the team-level SSO settings. |
| name | String | The added or updated name of the SSO method. |
| status | **enabled** or **disabled** | The updated status of the SSO method. |
| note | String | The updated note of the SSO method. |
| web_dev_auth | **enabled** or **disabled** | Whether the browser authentication is required for users of the SSO method. |
| src_dev_auth | **enabled** or **disabled** | Whether the device authentication for the Business app is required for users of the SSO method. |
| idp_sso_url | String | The updated IdP SSO URL of the SSO method. |
| idp_sso_issuer | String | The updated IdP issuer of the SSO method. |
| idp_sso_cert | String | The updated IdP certificate of the SSO method. |
| entity_id | String | The updated entity ID of the SSO method. |
| force_auth | **enabled** or **disabled** | Whether forcing re-authentication at the IdP is enabled for the SSO method. |
| add_subject_in_authreq | **enabled** or **disabled** | Whether adding the subject in the authentication request is enabled for the SSO method. |
| login_hint | **enabled** or **disabled** | Whether the login hint is enabled for the SSO method. |
| default_sso_method | String | The updated default SSO method of the team. |
| sso_saml_entityid | String | The SAML entity ID of the team. |

## **API**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| api_application_added | A new Open API application has been added and saved. |
| api_application_enabled | An Open API application has been enabled. |
| api_application_disabled | An Open API application has been disabled. |
| api_application_removed | An existing Open API application has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target Open API application. |
