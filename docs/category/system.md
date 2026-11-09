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
| source_agent | **browser** or **client** or **streamer** or **openapi** or **scim** or **system** or **cli** | The origin client of the specific event. |
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
| port_updated | The Splashtop Gateway port has been modified and saved. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | **gateway_url** | The target configuration item of the event. Empty for the port_updated event. |
| old_url | String | The previous Gateway URL. |
| new_url | String | The updated Gateway URL. |
| old_port | String | The previous Gateway port. |
| new_port | String | The updated Gateway port. |

## **SMTP Server**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| smtp_server_added | A new SMTP server has been added and saved. |
| smtp_server_enabled | An SMTP server has been enabled. |
| smtp_server_disabled | An SMTP server has been disabled. |
| smtp_server_updated | An existing SMTP server has been modified and saved. The modified item (address, email, or the limit general emails setting) is recorded in the target field. |
| smtp_server_removed | An existing SMTP server has been deleted. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The target SMTP server address, or the specific configuration item that has been updated: **address**, **email**, **Limit general emails status**, or **Limit general emails value**. |
| old_addr | String | The previous SMTP server address. |
| new_addr | String | The updated SMTP server address. |
| old_email | String | The previous sender Email address. |
| new_email | String | The updated sender Email address. |
| old_status | String | The previous status of the limit general emails setting. |
| new_status | String | The updated status of the limit general emails setting. |
| old_value | String | The previous limit value of the limit general emails setting. |
| new_value | String | The updated limit value of the limit general emails setting. |

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

## **Security**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| ssl_cert_imported | An SSL certificate has been imported to the Gateway. |
| ssl_cert_removed | The SSL certificate has been removed from the Gateway. |
| tls_setting_updated | The TLS version setting of the Gateway has been updated. |
| web_ip_restriction_enabled | The IP restriction for web console access has been enabled. |
| web_ip_restriction_disabled | The IP restriction for web console access has been disabled. |
| web_ip_restriction_ip_updated | The allowed IP ranges for web console access have been updated. |
| web_ip_restriction_access_deny_updated | The response displayed when the web console is accessed from an IP address without permission has been updated. |
| web_ip_restriction_allow_access_download_updated | Allowing access to the support session app download pages (SOS, Service Desk, PIN Code) from all IP ranges has been enabled or disabled. |
| client_ip_restriction_enabled | The IP restriction for On-Prem app (Business app and streamer) access has been enabled. |
| client_ip_restriction_disabled | The IP restriction for On-Prem app (Business app and streamer) access has been disabled. |
| client_ip_restriction_ip_updated | The allowed IP ranges for On-Prem app access have been updated. |
| openapi_ip_restriction_enabled | The IP restriction for Open API access has been enabled. |
| openapi_ip_restriction_disabled | The IP restriction for Open API access has been disabled. |
| openapi_ip_restriction_ip_updated | The allowed IP ranges for Open API access have been updated. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| old_tls | **1.0 or 1.1+** or **1.2+** | The previous minimum TLS version. |
| new_tls | **1.0 or 1.1+** or **1.2+** | The updated minimum TLS version. |
| old_access_deny | **HTTP 404** or **Access forbidden** | The previous response displayed for an access without permission. |
| new_access_deny | **HTTP 404** or **Access forbidden** | The updated response displayed for an access without permission. |
| status | **enabled** or **disabled** | Whether access to the support session app download pages from all IP ranges is allowed. |
| IPs | String | The updated allowed IP ranges, separated by commas. |

## **Certificate**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| certificate_installed_web | A new certificate for an FQDN has been installed via the web console. |
| certificate_installed_acme | A new certificate for an FQDN has been installed via ACME, either requested by a user from the web console or renewed automatically by the system. |
| certificate_installed_cli | A new certificate for an FQDN has been installed via the CLI. |
| acme_renewal_failed | A certificate request via ACME for an FQDN has failed. The result of this event is **failed**. |
| certificate_removed | The certificate for an FQDN has been removed. |
| certificate_notification_enabled | The certificate expiration notification for an FQDN has been enabled. |
| certificate_notification_disabled | The certificate expiration notification for an FQDN has been disabled. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The FQDN that the certificate is issued for. |
| terms_url | String | The URL of the ACME terms of service accepted at setup. |
| reason | String | The error returned by the ACME server when the certificate request failed. |

## **License**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| online_license_imported | An online license has been imported. |
| online_license_removed | An online license has been removed. |
| offline_license_imported | An offline license has been imported. |
| offline_license_removed | An offline license has been removed. |
| license_expiration_notification_enabled | The license expiration notification has been enabled. |
| license_expiration_notification_disabled | The license expiration notification has been disabled. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| license | String | The masked license key of the online license that has been imported or removed. |

## **Maintenance**

### Events and triggers

| **Event** | **Trigger** |
| --- | --- |
| database_restored | The system has been restored from a database backup file. |
| logs_remove | The logs up to (and including) a month have been removed. The result is **success** when all logs have been removed, or **failure** with extra_result **partial failure** when some logs could not be removed. |
| inventory_remove | The inventories up to (and including) a month have been removed. The result is **success** when all inventories have been removed, or **failure** with extra_result **partial failure** when some could not be removed. |
| patches_remove | The patches up to (and including) a month have been removed. The result is **success** when all patches have been removed, or **failure** with extra_result **partial failure** when some could not be removed. |
| centralized_session_recording_storage_path_updated | The storage path of the centralized session recording has been updated, by a user or by the system. |
| centralized_session_recording_retention_period_updated | The retention period of the centralized session recording has been updated, by a user or by the system. |

### Fields

| **Field** | **Value** | **Explanation** |
| --- | --- | --- |
| target | String | The name of the backup file that the system has been restored from. Present only in the database_restored event. |
| extra_result | **partial failure** | The reason of a failed removal. Present only when the result is **failure**. |
| removal_up_to | String | The month (in **yyyy-mm** format, UTC) up to which the items have been removed. Present only when the result is **success**. |
| success_count | Integer | The number of items that have been removed successfully. Present only when the result is **failure**. |
| failure_count | Integer | The number of items that could not be removed. Present only when the result is **failure**. |
| old_path | String | The previous storage path of the centralized session recording. |
| new_path | String | The updated storage path of the centralized session recording. |
| old_retention | Integer | The previous retention period of the centralized session recording, in days. |
| new_retention | Integer | The updated retention period of the centralized session recording, in days. |
