# **Management**

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
| extra_result | String | The reason of a failed event. This field is present only when the result is **failure**. See the extra_result values table under each kind. |

## **User**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| user_added | A new local user has been added to the team. |
| user_added_csv | A new local user has been added to the team by importing a CSV file. |
| user_removed | An existing local user has been deleted from the team. |
| ad_user_added | A new AD user has been added to the team. |
| ad_user_added_csv | A new AD user has been added to the team by importing a CSV file. |
| ad_user_removed | An existing AD user has been deleted from the team. |
| ad_group_added | A new AD group has been added to the team. |
| ad_group_added_csv | A new AD group has been added to the team by importing a CSV file. |
| ad_group_removed | An existing AD group has been deleted from the team. |
| ad_group_member_added | A member of an AD group has been added to the team. |
| ad_group_member_removed | A member of an AD group has been removed from the team. |
| sso_user_added | A new SSO user has been added to the team. |
| sso_user_added_csv | A new SSO user has been added to the team by importing a CSV file. |
| sso_user_removed | An existing SSO user has been deleted from the team. |
| sso_group_added | A new SSO group has been added to the team via SCIM provisioning. |
| sso_group_removed | An existing SSO group has been deleted from the team. |
| sso_group_name_updated | The name of an SSO group has been updated via SCIM provisioning. |
| sso_group_member_assigned | A user has been assigned to an SSO group via SCIM provisioning. |
| sso_group_member_unassigned | A user has been unassigned from an SSO group via SCIM provisioning. |
| sso_group_member_removed | A member of an SSO group has been removed from the team. |
| user_enabled | A user account has been enabled. |
| user_disabled | A user account has been disabled. |
| user_locked | A user account has been locked. |
| user_unlocked | A user account has been unlocked. |
| user_auth_method_updated | The authentication method of a user has been changed. |
| user_email_updated | The Email address of a user has been updated. |
| account_name_updated | The account name of a user has been updated. |
| display_name_updated | The display name of a user has been updated. |
| pwd_updated | The password of a user has been changed. |
| pwd_reset | The password of a user has been reset by an admin. |
| 2fa_enabled | Two-factor authentication has been enabled for a user. |
| 2fa_disabled | Two-factor authentication has been disabled for a user. |
| trust_device_added | A device has been added to the trusted device list of a user. |
| trust_device_removed | A device has been removed from the trusted device list of a user. |
| admin_granted | A user has been granted the admin role. |
| member_granted | A user has been granted the member role. |
| managed_group_added | A user has been granted the group manager role of a group. |
| managed_group_removed | The group manager role of a group has been withdrawn from a user. |
| user_group_assigned | A user has been moved to another group. |
| access_permission_updated | The access permission of a user has been updated. |
| access_permission_updated_csv | The access permission of a user has been updated by importing a CSV file. |
| user_accessed_group_added | A computer group has been added to the access list of a user. |
| user_accessed_group_added_csv | A computer group has been added to the access list of a user by importing a CSV file. |
| user_accessed_group_removed | A computer group has been removed from the access list of a user. |
| user_accessed_group_removed_csv | A computer group has been removed from the access list of a user by importing a CSV file. |
| user_accessed_streamer_added | A computer has been added to the access list of a user. |
| user_accessed_streamer_added_csv | A computer has been added to the access list of a user by importing a CSV file. |
| user_accessed_streamer_removed | A computer has been removed from the access list of a user. |
| user_accessed_streamer_removed_csv | A computer has been removed from the access list of a user by importing a CSV file. |
| web_access_enabled | Web console access has been enabled for a user. |
| web_access_disabled | Web console access has been disabled for a user. |
| sos_enabled | SOS (attended access) has been enabled for a user. |
| sos_disabled | SOS (attended access) has been disabled for a user. |
| user_granular_remote_control_updated | The granular control of the remote control for a user has been updated. |
| user_granular_file_transfer_download_updated | The granular control of the file transfer (download) for a user has been updated. |
| user_granular_file_transfer_upload_updated | The granular control of the file transfer (upload) for a user has been updated. |
| user_granular_remote_command_updated | The granular control of the remote command for a user has been updated. |
| user_granular_remote_print_updated | The granular control of the remote print for a user has been updated. |
| user_granular_request_permission_updated | The granular control of the request permission to connect for a user has been updated. |
| user_granular_request_permission_rdp_updated | The granular control of the request permission to connect (RDP session) for a user has been updated. |
| user_granular_text_copy_paste_local_remote_updated | The granular control of the copy and paste (from local to remote) for a user has been updated. |
| user_granular_text_copy_paste_remote_local_updated | The granular control of the copy and paste (from remote to local) for a user has been updated. |
| user_granular_watermark_protection_updated | The granular control of the watermark protection for a user has been updated. |
| user_granular_centralized_session_recording_unattended_updated | The granular control of the centralized session recording (unattended) for a user has been updated. |
| user_granular_centralized_session_recording_attended_updated | The granular control of the centralized session recording (attended) for a user has been updated. |
| user_granular_system_tools_updated | The granular control of the system tools for a user has been updated. |
| user_granular_require_2fa_updated | The granular control of the require 2FA for a user has been updated. |
| user_grant_granular_remote_control_updated | The admin-configurable value of the remote control has been updated for a user (admin role). |
| user_grant_granular_file_transfer_download_updated | The admin-configurable value of the file transfer (download) has been updated for a user (admin role). |
| user_grant_granular_file_transfer_upload_updated | The admin-configurable value of the file transfer (upload) has been updated for a user (admin role). |
| user_grant_granular_remote_command_updated | The admin-configurable value of the remote command has been updated for a user (admin role). |
| user_grant_granular_remote_print_updated | The admin-configurable value of the remote print has been updated for a user (admin role). |
| user_grant_granular_request_permission_updated | The admin-configurable value of the request permission to connect has been updated for a user (admin role). |
| user_grant_granular_request_permission_rdp_updated | The admin-configurable value of the request permission to connect (RDP session) has been updated for a user (admin role). |
| user_grant_granular_text_copy_paste_local_remote_updated | The admin-configurable value of the copy and paste (from local to remote) has been updated for a user (admin role). |
| user_grant_granular_text_copy_paste_remote_local_updated | The admin-configurable value of the copy and paste (from remote to local) has been updated for a user (admin role). |
| user_grant_granular_watermark_protection_updated | The admin-configurable value of the watermark protection has been updated for a user (admin role). |
| user_grant_granular_centralized_session_recording_unattended_updated | The admin-configurable value of the centralized session recording (unattended) has been updated for a user (admin role). |
| user_grant_granular_centralized_session_recording_attended_updated | The admin-configurable value of the centralized session recording (attended) has been updated for a user (admin role). |
| user_grant_granular_system_tools_updated | The admin-configurable value of the system tools has been updated for a user (admin role). |
| user_grant_granular_require_2fa_updated | The admin-configurable value of the require 2FA has been updated for a user (admin role). |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The target user account. |
| ad_server | String | The name of the AD server that the AD user or AD group belongs to. |
| csv | String | The file name of the imported CSV file. |
| SSO group | String | The name of the SSO group that the user has been assigned to or unassigned from. |
| old_name | String | The previous name of the SSO group. |
| new_name | String | The updated name of the SSO group. |
| old_method | String | The previous authentication method of the user. |
| new_method | String | The updated authentication method of the user. |
| old_email | String | The previous Email address of the user. |
| new_email | String | The updated Email address of the user. |
| account_name | String | The updated account name of the user. |
| display_name | String | The updated display name of the user. |
| 2fa_method | **Authenticator app** or **Email** | The two-factor authentication method that has been enabled for the user. |
| device_name | String | The name of the device that has been added to or removed from the trusted device list. |
| group | String | The name of the group: the group that the group manager role has been granted or withdrawn for, or the computer group that has been added to or removed from the access list of the user. |
| old_group | String | The group that the user belonged to previously. |
| new_group | String | The group that the user has been moved to. |
| access_permission | String | The updated access permission of the user. |
| streamer | String | The name of the computer that has been added to or removed from the access list of the user. |
| granular_remote_control | **default** or **follow group** or **off** or **on** | The updated granular control of the remote control for the user. |
| granular_file_transfer_download | **default** or **follow group** or **off** or **on** | The updated granular control of the file transfer (download) for the user. |
| granular_file_transfer_upload | **default** or **follow group** or **off** or **on** | The updated granular control of the file transfer (upload) for the user. |
| granular_remote_command | **default** or **follow group** or **off** or **on** | The updated granular control of the remote command for the user. |
| granular_remote_print | **default** or **follow group** or **off** or **on** | The updated granular control of the remote print for the user. |
| granular_request_permission | **reject connection after request expires (at login screen, reject automatically)** or **reject connection after request expires (at login screen, allow automatically)** or **allow connection after request expires** or **off** | The updated granular control of the request permission to connect for the user. |
| granular_request_permission_rdp | **reject connection after request expires (at login screen, reject automatically)** or **reject connection after request expires (at login screen, allow automatically)** or **allow connection after request expires** or **off** | The updated granular control of the request permission to connect (RDP session) for the user. |
| granular_text_copy_paste_local_remote | **default** or **follow group** or **off** or **on** | The updated granular control of the copy and paste (from local to remote) for the user. |
| granular_text_copy_paste_remote_local | **default** or **follow group** or **off** or **on** | The updated granular control of the copy and paste (from remote to local) for the user. |
| granular_watermark_protection | **default** or **follow group** or **off** or **on** | The updated granular control of the watermark protection for the user. |
| granular_centralized_session_recording_unattended | **default** or **follow group** or **off** or **on** | The updated granular control of the centralized session recording (unattended) for the user. |
| granular_centralized_session_recording_attended | **default** or **follow group** or **off** or **on** | The updated granular control of the centralized session recording (attended) for the user. |
| granular_system_tools | **default** or **follow_group** or **off** or **on** | The updated granular control of the system tools for the user. |
| granular_require_2fa | **default** or **follow group** or **off** or **on** or **verification with Authenticator app** or **verification with Email** | The updated granular control of the require 2FA for the user. |
| grant_granular_remote_control | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure remote control. |
| grant_granular_file_transfer_download | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure file transfer (download). |
| grant_granular_file_transfer_upload | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure file transfer (upload). |
| grant_granular_remote_command | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure remote command. |
| grant_granular_remote_print | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure remote print. |
| grant_granular_request_permission | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure request permission to connect. |
| grant_granular_request_permission_rdp | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure request permission to connect (RDP session). |
| grant_granular_text_copy_paste_local_remote | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure copy and paste (from local to remote). |
| grant_granular_text_copy_paste_remote_local | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure copy and paste (from remote to local). |
| grant_granular_watermark_protection | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure watermark protection. |
| grant_granular_centralized_session_recording_unattended | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure centralized session recording (unattended). |
| grant_granular_centralized_session_recording_attended | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure centralized session recording (attended). |
| grant_granular_system_tools | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure system tools. |
| grant_granular_require_2fa | **default** or **off** or **on** | The admin has been granted or not granted the permission to configure require 2FA. |

### extra_result values

| **Value** | **Explanation** |
| --- | --- |
| user_existed | The user or group already exists in the team. |
| out_of_seat | The team has no available license seat for the user. |
| out_of_sos_seat | The team has no available SOS license seat for the user. |
| user_count_limit_exceeded | The number of users in the team has reached the user count limit. |
| group_limits_exceeded | The number of users in the group has reached the enabled user limit of the group. |
| invalid_email_domain | The Email domain of the user is not allowed by the team. |
| duplicated_name | The updated Email address is already in use by another user. |
| upn_not_found | The user principal name (UPN) of the AD user has not been found on the AD server. |
| ldap_verify_failed | The AD user or AD group has failed the LDAP verification against the AD server. |
| sso_profile_disabled | The SSO profile that the user belongs to has been disabled. |
| invalid_format | The imported CSV file is not in a valid format. |
| max_characters_exceeded | A value in the imported data has exceeded the maximum number of characters. |

## **Group**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| group_added | A new group has been added to the team. |
| group_added_csv | A new group has been added to the team by importing a CSV file. |
| group_removed | An existing group has been deleted from the team. |
| group_name_updated | The name of a group has been updated. |
| group_connection_pool_enabled | The connection pool has been enabled for a group. |
| group_connection_pool_disabled | The connection pool has been disabled for a group. |
| group_access_permission_enabled | The access permission setting of a group has been enabled. |
| group_access_permission_disabled | The access permission setting of a group has been disabled. |
| group_access_permission_updated | The access permission of a group has been updated. |
| group_access _permission_updated | The access permission of a group has been updated by importing a CSV file. |
| group_accessed_group_added | A computer group has been added to the access list of a user group. |
| group_accessed_group_added_csv | A computer group has been added to the access list of a user group by importing a CSV file. |
| group_accessed_group_removed | A computer group has been removed from the access list of a user group. |
| group_accessed_group_removed_csv | A computer group has been removed from the access list of a user group by importing a CSV file. |
| group_accessed_streamer_added | A computer has been added to the access list of a user group. |
| group_accessed_streamer_added_csv | A computer has been added to the access list of a user group by importing a CSV file. |
| group_accessed_streamer_removed | A computer has been removed from the access list of a user group. |
| group_accessed_streamer_removed_csv | A computer has been removed from the access list of a user group by importing a CSV file. |
| group_granular_remote_control_updated | The granular control of the remote control for a group has been updated. |
| group_granular_file_transfer_download_updated | The granular control of the file transfer (download) for a group has been updated. |
| group_granular_file_transfer_upload_updated | The granular control of the file transfer (upload) for a group has been updated. |
| group_granular_remote_command_updated | The granular control of the remote command for a group has been updated. |
| group_granular_remote_print_updated | The granular control of the remote print for a group has been updated. |
| group_granular_request_permission_updated | The granular control of the request permission to connect for a group has been updated. |
| group_granular_request_permission_rdp_updated | The granular control of the request permission to connect (RDP session) for a group has been updated. |
| group_granular_text_copy_paste_local_remote_updated | The granular control of the copy and paste (from local to remote) for a group has been updated. |
| group_granular_text_copy_paste_remote_local_updated | The granular control of the copy and paste (from remote to local) for a group has been updated. |
| group_granular_watermark_protection_updated | The granular control of the watermark protection for a group has been updated. |
| group_granular_centralized_session_recording_unattended_updated | The granular control of the centralized session recording (unattended) for a group has been updated. |
| group_granular_centralized_session_recording_attended_updated | The granular control of the centralized session recording (attended) for a group has been updated. |
| group_granular_system_tools_updated | The granular control of the system tools for a group has been updated. |
| group_granular_require_2fa_updated | The granular control of the require 2FA for a group has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target group. |
| name | String | The updated name of the group. |
| csv | String | The file name of the imported CSV file. |
| access_permission | String | The updated access permission of the group. |
| group | String | The name of the computer group that has been added to or removed from the access list of the user group. |
| streamer | String | The name of the computer that has been added to or removed from the access list of the user group. |
| granular_remote_control | **default** or **off** or **on** | The updated granular control of the remote control for the group. |
| granular_file_transfer_download | **default** or **off** or **on** | The updated granular control of the file transfer (download) for the group. |
| granular_file_transfer_upload | **default** or **off** or **on** | The updated granular control of the file transfer (upload) for the group. |
| granular_remote_command | **default** or **off** or **on** | The updated granular control of the remote command for the group. |
| granular_remote_print | **default** or **off** or **on** | The updated granular control of the remote print for the group. |
| granular_request_permission | **reject connection after request expires (at login screen, reject automatically)** or **reject connection after request expires (at login screen, allow automatically)** or **allow connection after request expires** or **off** | The updated granular control of the request permission to connect for the group. |
| granular_request_permission_rdp | **reject connection after request expires (at login screen, reject automatically)** or **reject connection after request expires (at login screen, allow automatically)** or **allow connection after request expires** or **off** | The updated granular control of the request permission to connect (RDP session) for the group. |
| granular_text_copy_paste_local_remote | **default** or **off** or **on** | The updated granular control of the copy and paste (from local to remote) for the group. |
| granular_text_copy_paste_remote_local | **default** or **off** or **on** | The updated granular control of the copy and paste (from remote to local) for the group. |
| granular_watermark_protection | **default** or **off** or **on** | The updated granular control of the watermark protection for the group. |
| granular_centralized_session_recording_unattended | **default** or **off** or **on** | The updated granular control of the centralized session recording (unattended) for the group. |
| granular_centralized_session_recording_attended | **default** or **off** or **on** | The updated granular control of the centralized session recording (attended) for the group. |
| granular_system_tools | **default** or **off** or **on** | The updated granular control of the system tools for the group. |
| granular_require_2fa | **default** or **off** or **on** or **verification with Authenticator app** or **verification with Email** | The updated granular control of the require 2FA for the group. |

### extra_result values

| **Value** | **Explanation** |
| --- | --- |
| group_existed | The group already exists in the team. |
| max_characters_exceeded | A value in the imported CSV file has exceeded the maximum number of characters. |
| missing_required_entry | A required entry is missing in the imported CSV file. |
| invalid_value_of_connection_pool | The connection pool value in the imported CSV file is invalid. |
| invalid_value_of_enabled_user_limit | The enabled user limit value in the imported CSV file is invalid. |

## **Resource**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| resource_added | A new scheduled access resource has been added. |
| resource_updated | An existing scheduled access resource has been modified and saved. |
| resource_removed | An existing scheduled access resource has been deleted. |
| resource_manager_associated | A user has been assigned as the manager of a resource. |
| resource_manager_disassociated | A user has been removed from the managers of a resource. |
| schedule_added | A new schedule has been added to a resource. |
| schedule_updated | An existing schedule of a resource has been modified and saved. |
| schedule_removed | An existing schedule has been deleted from a resource. |
| schedule_manager_associated | A user has been assigned as the manager of a schedule. |
| schedule_manager_disassociated | A user has been removed from the managers of a schedule. |
| streamer_associated | A computer has been added to a resource. |
| streamer_disassociated | A computer has been removed from a resource. |
| streamer_group_associated | A computer group has been added to a resource. |
| streamer_group_disassociated | A computer group has been removed from a resource. |
| user_associated | A user has been added to a resource. |
| user_disassociated | A user has been removed from a resource. |
| user_group_associated | A user group has been added to a resource. |
| user_group_disassociated | A user group has been removed from a resource. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target resource. |
| user | String | The account of the user that has been associated with or disassociated from the resource or schedule. |
| streamer | String | The name of the computer that has been associated with or disassociated from the resource. |
| group | String | The name of the computer group or user group that has been associated with or disassociated from the resource. |

## **Policy**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| preference_policy_added | A new preference policy has been added. |
| preference_policy_updated | An existing preference policy has been modified and saved. |
| preference_policy_removed | An existing preference policy has been deleted. |
| policy_manager_associated | A user has been assigned as the manager of a preference policy. |
| policy_manager_disassociated | A user has been removed from the managers of a preference policy. |
| policy_streamer_added | A computer has been added to a preference policy. |
| policy_streamer_removed | A computer has been removed from a preference policy. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target preference policy. |
| user | String | The account of the user that has been associated with or disassociated from the policy. |
| streamer | String | The name of the computer that has been added to or removed from the policy. |

## **1-to-Many Action**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| 1_to_many_action_added | A new 1-to-Many action has been added. |
| 1_to_many_action_updated | An existing 1-to-Many action has been modified and saved. |
| 1_to_many_action_removed | An existing 1-to-Many action has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target 1-to-Many action. |
| action_kind | String | The action kind of the 1-to-Many action. |

## **1-to-Many Schedule**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| 1_to_many_schedule_added | A new 1-to-Many schedule has been added. |
| 1_to_many_schedule_updated | An existing 1-to-Many schedule has been modified and saved. |
| 1_to_many_schedule_removed | An existing 1-to-Many schedule has been deleted. |
| 1_to_many_streamer_associated | A computer has been added to a 1-to-Many schedule. |
| 1_to_many_streamer_disassociated | A computer has been removed from a 1-to-Many schedule. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target 1-to-Many schedule. |
| action_kind | String | The action kind of the 1-to-Many schedule. |
| streamer | String | The name of the computer that has been associated with or disassociated from the schedule. |

## **Deployment**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| deploy_package_added | A new deployment package has been created. |
| deploy_package_removed | An existing deployment package has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the target deployment package. |

## **RMM**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| rmm_secret_created | A new RMM API secret (token) has been created for a user. |
| rmm_secret_updated | An existing RMM API secret (token) of a user has been updated. |
| rmm_secret_removed | An existing RMM API secret (token) of a user has been deleted. |
| rmm_setting_updated | An RMM setting has been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The user account that owns the RMM API secret, or the name of the RMM setting key that has been updated. |
| api_token | String | The RMM API token that has been created, updated, or removed. |
| setting_key | String | The updated value of the RMM setting. |

## **OAuth**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| access_token_added | An Open API access token has been issued. |
| access_token_removed | An Open API access token has been revoked. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | **access_token** | The target item of the event. |
| token | String | The Open API access token that has been issued or revoked. |
| grant_type | String | The OAuth grant type used to issue the access token. |
