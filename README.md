# Delegate365 Manual for Reports

Delegate365 is an Add-On for customers using Microsoft Office 365 and allows delegation, self-management, license-management and auditing. The software is provided as Software-as-a-Service solution in the Microsoft Cloud on Microsoft Azure and can be used instantly, see [Delegate365](https://www.Delegate365.com).

## Reports

Delegate365 allows to run instant reports and time triggered reports. All Admins with permission to the reports module can run the reports. **By default, the reports are filtered just for the entitled OU's of the admin.** If a user has report administration permission, there are more reports available and there is no OU filter applied, so data is reported tenant-wide.

## Run a report

The "Available reports" box shows the list of reports that can be run from Delegate365. The reports are grouped by category: Azure Active Directory, Risk Events, Microsoft 365, Microsoft Teams, Skype for Business, Yammer, SharePoint, OneDrive, Exchange and Delegate365. Select the desired report. Below the list, a short description is shown. The date filter becomes active if a date filter can be applied. By default, all reports are filterd just for the entitled data. Only report administrators see data from the whole Microsoft 365 tenant.

[![link](./Samples/reports-selection.png)](./Samples/reports-selection.png "Click to enlarge")

Optionally, you can be notified when the report has been generated. The Schedule dropdown allows to run an instant report, or generate a recurring report. There, weekly (each Monday) or monthly (each 1st) can be chosen. Once you submit the report, the report generation job will show up in the corresponding box below. The report engine checks the reports in the queue and generates the output. Once the generation is completed, the user will get an email with a link to this page, and the report will show up in the "Finished reports" box at the page end. Alternatively, a user can click the "Refresh" button to check if the report was already generated.

The reports are generated as CSV file and as Excel file. The filename is the job number plus the file type. There are just some exceptions for reports that can be very large, where only a CSV file is generated. Click on the CSV icon or on the Excel icon to download the generated report for further processing.

[![link](./Samples/reports-completed.png)](./Samples/reports-completed.png "Click to enlarge")

The report generation can take some minutes, depending on the size of data. The generated reort files are available for 7 days are are automatically deleted after that time. If the configuration is set to send a direct download link, this link is valid for 24 hours. Users can directly open the generated report as shown in the email notification sample here.

[![link](./Samples/report-notification.png)](./Samples/report-notification.png "Click to enlarge")

There is no file backup of reports. So, download the files if needed within the valid time frame. Find a list of all available reports with sample report files below.

## Report Overview

The following graphics shows an overview of the available reports in the current version of Delegate365.

[![link](./Samples/delegate365-reports-overview.png)](./Samples/delegate365-reports-overview.png "Click to enlarge")

## Report List

This list includes an enumeration of currently available reports in Delegate365. Reports that are marked with Admin-Only are only available for users who have the *report administration permission* assigned. Click on the sample link to see a sample output in CSV or Excel format with some records to understand the fields that are included. 

| Nr | Category                      | Report                                            | Admin | Sample                                                                                    | Description
|:---|:------------------------------|:--------------------------------------------------|:------|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------
| 001| Azure AD                      | Directory role users                              | -     | [CSV](./Samples/AAD-Directory-role-users.csv)                                             | Retrieve a list of the users that are assigned to the directory role.
| 002| Azure AD                      | Last Sign-ins                                     | -     | [CSV](./Samples/AAD-Last-Sign-ins.csv)                                                    | Retrieve the Azure AD user sign-ins for your tenant. To access this report through the reporting API, you must have an Azure Active Directory Premium P1 or P2 edition.
| 003| Azure AD                      | Directory audits                                  | yes   | [CSV](./Samples/AAD-Directory-audits.csv)                                                 | Get the list of audit logs such as users, apps, devices, PIM, and more logs generated by Azure Active Directory. 
| 004| Intune                        | Managed devices                                   | -     | [CSV](./Samples/Intune-Managed-devices.csv)                                               | List properties and relationships of the managed device objects.
| 005| Intune                        | Managed devices (simple)                          | -     | [CSV](./Samples/Intune-Managed-devices.csv)                                               | List properties and relationships of the managed device objects.
| 006| Intune                        | Unmanaged devices                                 | yes   | [CSV](./Samples/Intune-UnmanagedDevices.csv)                                              | List of device objects that are registered in the organization but not assigned to any user, including the device ID, DeviceVersion TrustType, LastSignInDateTime, Operating System and version, and other metadata.
| 007| Risk Events                   | Anonymous IP                                      | -     | [CSV](./Samples/Risk-Events-Anonymous-IP.csv)                                             | Show successful logins from anonymous proxy IP addresses that could be used to hide a device's IP address, and may be used for malicious intent.
| 008| Risk Events                   | Impossible travel                                 | -     | [CSV](./Samples/Risk-Events-Impossible-travel.csv)                                        | Get sign-ins from geographically distant locations, that are also atypical for the user (after an initial learning period of 14 days).
| 009| Risk Events                   | Leaked credentials                                | -     | [CSV](./Samples/Risk-Events-Leaked-credentials.csv)                                       | Get stolen credentials. Microsoft leaked credentials service checks stolen username and password pairs by monitoring public and dark web sites.
| 010| Risk Events                   | Malware                                           | -     | [CSV](./Samples/Risk-Events-Malware.csv)                                                  | Get sign-ins from devices infected with malware that are known to actively communicate with a malicious bot by correlating IP addresses.
| 011| Risk Events                   | New country                                       | -     | [CSV](./Samples/RiskEvents-newcountry.csv)                                                | This detection is discovered by Microsoft Cloud App Security (MCAS). The sign-in occurred from a location that wasn't recently or never visited by the given user.
| 012| Risk Events                   | Suspicious browser                                | -     | [CSV](./Samples/RiskEvents-suspiciousbrowser.csv)                                         | Suspicious sign-in activity across multiple tenants from different countries in the same browser.
| 013| Risk Events                   | Anomalous Token                                   | -     | [CSV](./Samples/RiskEvents-anomaloustoken.csv)                                            | Indicates that there are abnormal characteristics in the token such as an unusual token lifetime or a token that is played from an unfamiliar location.
| 014| Risk Events                   | Activity from anonymous IP address                | -     | [CSV](./Samples/RiskEvents-riskyipaddress.csv)                                            | This detection is discovered by Microsoft Cloud App Security (MCAS). Users were active from an IP address that has been identified as an anonymous proxy IP address.
| 015| Risk Events                   | Atypical travel                                   | -     | [CSV](./Samples/RiskEvents-unlikelytravel.csv)                                            | Identifies two sign-ins originating from geographically distant locations, where at least one of the locations may also be atypical for the user, given past behavior.
| 016| Risk Events                   | Malicious IP address                              | -     | [CSV](./Samples/RiskEvents-maliciousipaddress.csv)                                        | Indicates sign-ins from a malicious IP address. An IP address is considered malicious based on high failure rates because of invalid credentials received from the IP address or other IP reputation sources.
| 017| Risk Events                   | Suspicious inbox manipulation rules               | -     | [CSV](./Samples/RiskEvents-suspiciousinboxmanipulation.csv)                               | Discovered by Microsoft Defender for Cloud Apps (MDCA). Identifies suspicious email forwarding rules, for example, if a user created an inbox rule that forwards a copy of all emails to an external address.
| 018| Risk Events                   | Suspicious inbox forwarding                       | -     | [CSV](./Samples/RiskEvents-suspiciousinboxforwarding.csv)                                 | This detection is discovered by Microsoft Cloud App Security (MCAS). It looks for suspicious email forwarding rules, for example, if a user created an inbox rule that forwards a copy of all emails to an external address.
| 019| Risk Events                   | Unfamiliar sign-in properties                     | -     | [CSV](./Samples/RiskEvents-unfamiliarfeatures.csv)                                        | Indicates sign-ins with characteristics that deviate from past sign-in properties.
| 020| Risk Events                   | Azure AD threat intelligence                      | -     | [CSV](./Samples/RiskEvents-threatintelligence.csv)                                        | Indicates a sign-in activity that is unusual for the given user or is consistent with known attack patterns based on Microsoft's internal and external threat intelligence sources.
| 021| Risk Events                   | Password spray                                    | -     | [CSV](./Samples/RiskEvents-passwordspray.csv)                                             | Indicates that multiple usernames are attacked using common passwords in a unified brute force manner to gain unauthorized access.
| 022| Risk Events                   | Token Issuer Anomaly                              | -     | [CSV](./Samples/RiskEvents-tokenissueranomaly.csv)                                        | Indicates that The SAML token issuer for the associated SAML token is potentially compromised. The claims included in the token are unusual or match known attacker patterns.
| 023| Identity                      | Registration details                              | -     | [CSV](./Samples/Identity-Registration-details.csv)                                        | Get a list of credential user registration details objects for the tenant.
| 024| Identity                      | Usage details                                     | -     | [CSV](./Samples/Identity-Usage-details.csv)                                               | Get a list of user credential usage details objects for a given tenant. Details include user information, status of the reset, and the reason for failure.
| 025| Identity                      | Registration count                                | yes   | [CSV](./Samples/Identity-Registration-count.csv)                                          | Report the current state of how many users in your organization are registered for self-service password reset and multi-factor authentication (MFA) capabilities.
| 026| Identity                      | Credential usage summary                          | yes   | [CSV](./Samples/Identity-Credential-usage-summary.csv)                                    | Get a list of credential user registration details objects for a given tenant.
| 027| Security                      | Alerts                                            | yes   | [CSV](./Samples/Security-alerts.csv)                                                      | Represents potential security issues within a customer's tenant that Microsoft or partner security solutions have identified.
| 028| M365                          | Active user detail                                | -     | [CSV](./Samples/Office365-Active-user-detail.csv)                                         | Get all active users and their current licenses status including the last activity date.
| 029| M365                          | Active user counts                                | yes   | [CSV](./Samples/Office365-Active-user-counts.csv)                                         | Get the count of daily active users in the reporting period by product.
| 030| M365                          | Services user counts                              | yes   | [CSV](./Samples/Office365-Services-user-counts.csv)                                       | Get the count of users by activity type and Microsoft 365 service.
| 031| M365                          | Groups activity detail                            | -     | [CSV](./Samples/Office365-Groups-activity-detail.csv)                                     | Get an Microsoft 365 groups statistics and size of stored data per Microsoft 365 group.
| 032| M365                          | Groups activity counts                            | yes   | [CSV](./Samples/Office365-Groups-activity-counts.csv)                                     | Get the number of group activities across Microsoft 365 group workloads.
| 033| M365                          | Groups activity group counts                      | yes   | [CSV](./Samples/Office365-Groups-activity-group-counts.csv)                               | Get the daily total number of Microsoft 365 groups and how many of them were active based on email conversations, Yammer posts, and SharePoint file activities.
| 034| M365                          | Groups activity storage                           | yes   | [CSV](./Samples/Office365-Groups-activity-storage.csv)                                    | Get the total storage used across all Microsoft 365 group mailboxes and group sites.
| 035| M365                          | Groups activity file counts                       | yes   | [CSV](./Samples/Office365-Groups-activity-file-counts.csv)                                | Groups activity file counts.
| 036| M365                          | Activations user detail                           | -     | [CSV](./Samples/Office365-Activations-user-detail.csv)                                    | Get the activated Microsoft 365 licenses by user.
| 037| M365                          | Activation counts                                 | yes   | [CSV](./Samples/Office365-Activation-counts.csv)                                          | Get the count of Microsoft 365 activations on desktops and devices.
| 038| M365                          | Activations user counts                           | yes   | [CSV](./Samples/Office365-Activations-user-counts.csv)                                    | Get the count of users that are enabled and those that have activated the Office subscription on desktops or other devices.
| 039| Teams                         | Device usage user detail                          | -     | [CSV](./Samples/Microsoft-Teams-Device-usage-user-detail.csv)                             | Get the devices used for accessing Microsoft Teams by user.
| 040| Teams                         | Device usage user counts                          | yes   | [CSV](./Samples/Microsoft-Teams-Device-usage-user-counts.csv)                             | Get the number of Microsoft Teams daily unique users by device type.
| 041| Teams                         | Device usage distribution user counts             | yes   | [CSV](./Samples/Microsoft-Teams-Device-usage-distribution-user-counts.csv)                | Get the number of Microsoft Teams unique users by device type over the selected time period.
| 042| Teams                         | User activity user detail                         | -     | [CSV](./Samples/Microsoft-Teams-User-activity-user-detail.csv)                            | Get the users and when they last accessed Microsoft Teams.
| 043| Teams                         | User activity counts                              | yes   | [CSV](./Samples/Microsoft-Teams-User-activity-counts.csv)                                 | Get the number of Microsoft Teams activities by activity type. The activity types are team chat messages, private chat messages, calls, and meetings.
| 044| Teams                         | User activity user counts                         | yes   | [CSV](./Samples/Microsoft-Teams-User-activity-user-counts.csv)                            | Get the number of Microsoft Teams users by activity type. The activity types are number of teams chat messages, private chat messages, calls or meetings.
| 045| SFB                           | Activity user detail                              | -     | [CSV](./Samples/Skype-Activity-user-detail.csv)                                           | Get the a Skype for Business statistics by user, number of conferences, minutes, participations and more.
| 046| SFB                           | Activity counts                                   | yes   | [CSV](./Samples/Skype-Activity-counts.csv)                                                | Get the SFB trends on how many users organized and participated in conference sessions held in your organization and the number of peer-to-peer sessions through Skype for Business.
| 047| SFB                           | Activity user counts                              | yes   | [CSV](./Samples/Skype-Activity-user-counts.csv)                                           | Get the SFB trends on how many unique users organized and participated in conference sessions held in your organization and the number of peer-to-peer sessions through Skype for Business.
| 048| SFB                           | Device usage user detail                          | -     | [CSV](./Samples/Skype-Device-usage-user-detail.csv)                                       | Get details about Skype for Business device usage by user.
| 049| SFB                           | Device usage distribution user counts             | yes   | [CSV](./Samples/Skype-Device-usage-distribution-user-counts.csv)                          | Get the number of SFB users using unique devices in your organization. The report will show you the number of users per device including phones and iPad.
| 050| SFB                           | Device usage user counts                          | yes   | [CSV](./Samples/Skype-Device-usage-user-counts.csv)                                       | Get the SFB usage trends on how many users in your organization have connected using the Skype for Business app device including phones and iPad.
| 051| SFB                           | Organizer activity counts                         | yes   | [CSV](./Samples/Skype-Organizer-activity-counts.csv)                                      | Get SFB usage trends on the number and type of conference sessions held and organized by users in your organization including IM, audio/video, application sharing, web, dial-in/out - 3rd party, and Dial-in/out Microsoft.
| 052| SFB                           | Organizer activity user counts                    | yes   | [CSV](./Samples/Skype-Organizer-activity-user-counts.csv)                                 | Get SFB usage trends on the number of unique users and type of conference sessions held and organized by users in your organization including IM, audio/video, application sharing, web, dial-in/out - 3rd party, and dial-in/out Microsoft.
| 053| SFB                           | Organizer activity minute counts                  | yes   | [CSV](./Samples/Skype-Organizer-activity-minute-counts.csv)                               | Get usage trends on the number of unique users and type of conference sessions held and organized by users in your organization including IM, audio/video, application sharing, web, dial-in/out - 3rd party, and dial-in/out Microsoft.
| 054| SFB                           | Participant activity counts                       | yes   | [CSV](./Samples/Skype-Participant-activity-counts.csv)                                    | Get SFB usage trends on the number and type of conference sessions that users from your organization participated in including IM, audio/video, application sharing, web, and dial-in/out - 3rd party.
| 055| SFB                           | Participant activity user counts                  | yes   | [CSV](./Samples/Skype-Participant-activity-user-counts.csv)                               | Get SFB usage trends on the number of unique users and type of conference sessions that users from your organization participated in including IM, audio/video, application sharing, web, and dial-in/out - 3rd party.
| 056| SFB                           | Participant activity minute counts                | yes   | [CSV](./Samples/Skype-Participant-activity-minute-counts.csv)                             | Get SFB usage trends on the length in minutes and type of conference sessions that users from your organization participated in including audio/video.
| 057| SFB                           | Peer to peer activity counts                      | yes   | [CSV](./Samples/Skype-Peer-to-peer-activity-counts.csv)                                   | Get SFB peer-to-peer usage trends on the number and type of sessions held in your organization including IM, audio, video, application sharing, and file transfer.
| 058| SFB                           | Peer to peer activity user counts                 | yes   | [CSV](./Samples/Skype-Peer-to-peer-activity-user-counts.csv)                              | Get SFB peer-to-peer usage trends on the number of unique users and type of peer-to-peer sessions held in your organization including IM, audio, video, application sharing, and file transfers.
| 059| SFB                           | Peer to peer activity minute counts               | yes   | [CSV](./Samples/Skype-Peer-to-peer-activity-minute-counts.csv)                            | Get SFB peer-to-peer usage trends on the number of unique users and type of peer-to-peer sessions held in your organization including IM, audio, video, application sharing, and file transfers.
| 060| Viva Engage                   | Activity user detail                              | -     | [CSV](./Samples/Yammer-Activity-user-detail.csv)                                          | Get the last Yammer activity date by user, number of posts written, read and liked.
| 061| Viva Engage                   | Activity counts                                   | yes   | [CSV](./Samples/Yammer-Activity-counts.csv)                                               | Get the trends on the amount of Yammer activity in your organization by how many messages were posted, read, and liked.
| 062| Viva Engage                   | Activity user counts                              | yes   | [CSV](./Samples/Yammer-Activity-user-counts.csv)                                          | Get the trends on the number of unique users who posted, read, and liked Yammer messages.
| 063| Viva Engage                   | Device usage user detail                          | -     | [CSV](./Samples/Yammer-Device-usage-user-detail.csv)                                      | Get device usage user details.
| 064| Viva Engage                   | Device usage distribution user counts             | yes   | [CSV](./Samples/Yammer-Device-usage-distribution-user-counts.csv)                         | Get the number of Yammer users by device type.
| 065| Viva Engage                   | Device usage user counts                          | yes   | [CSV](./Samples/Yammer-Device-usage-user-counts.csv)                                      | Get the number of daily Yammer users by device type.
| 066| Viva Engage                   | Groups activity detail                            | yes   | [CSV](./Samples/Yammer-Groups-activity-detail.csv)                                        | Get details about Yammer groups activity by group.
| 067| Viva Engage                   | Groups activity group counts                      | yes   | [CSV](./Samples/Yammer-Groups-activity-group-counts.csv)                                  | Get the total number of Yammer groups that existed and how many included group conversation activity.
| 068| Viva Engage                   | Groups activity counts                            | yes   | [CSV](./Samples/Yammer-Groups-activity-counts.csv)                                        | Get the number of Yammer messages posted, read, and liked in groups.
| 069| SharePoint                    | Activity user detail                              | -     | [CSV](./Samples/SharePoint-Activity-user-detail.csv)                                      | Activity user detail of SharePoint Online.
| 070| SharePoint                    | Activity file counts                              | yes   | [CSV](./Samples/SharePoint-Activity-file-counts.csv)                                      | Get the number of unique and licensed users who interacted with files stored in SharePoint sites.
| 071| SharePoint                    | Activity user counts                              | yes   | [CSV](./Samples/SharePoint-Activity-user-counts.csv)                                      | Get the trend in the number of active SharePoint users. Active users are counted by a file activity or a page visit within the specified time period.
| 072| SharePoint                    | Activity pages                                    | yes   | [CSV](./Samples/SharePoint-Activity-pages.csv)                                            | Get the number of unique SharePoint pages visited by users.
| 073| SharePoint                    | Site usages detail                                | yes   | [CSV](./Samples/SharePoint-Site-usages-detail.csv)                                        | Get details about the SharePoint sites usage.
| 074| SharePoint                    | Site usage file counts                            | yes   | [CSV](./Samples/SharePoint-Site-usage-file-counts.csv)                                    | Get the total number of SharePoint files across all sites and the number of active files within the specified time period.
| 075| SharePoint                    | Site usage site files counts                      | yes   | [CSV](./Samples/SharePoint-Site-usage-site-files-counts.csv)                              | Get the total number of SharePoint sites usage across all sites within the specified time period.
| 076| SharePoint                    | Site usage storage                                | yes   | [CSV](./Samples/SharePoint-Site-usage-storage.csv)                                        | Get the trend of SharePoint storage allocated and consumed during the reporting period.
| 077| SharePoint                    | Site usage pages                                  | yes   | [CSV](./Samples/SharePoint-Site-usage-pages.csv)                                          | Get the number of SharePoint pages viewed across all sites.
| 078| OneDrive                      | Activity user detail                              | -     | [CSV](./Samples/OneDrive-Activity-user-detail.csv)                                        | Get the last OneDrive activity date by user and the number of files accessed and shared.
| 079| OneDrive                      | Activity user counts                              | yes   | [CSV](./Samples/OneDrive-Activity-user-counts.csv)                                        | Get the trend in the number of active OneDrive users.
| 080| OneDrive                      | Activity file counts                              | yes   | [CSV](./Samples/OneDrive-Activity-file-counts.csv)                                        | Get the number of unique and licensed users that performed file interactions against any OneDrive account.
| 081| OneDrive                      | Usage account detail                              | yes   | [CSV](./Samples/OneDrive-Usage-account-detail.csv)                                        | Get details about OneDrive usage by account.
| 082| OneDrive                      | Usage account counts                              | yes   | [CSV](./Samples/OneDrive-Usage-account-counts.csv)                                        | Get the trend of active OneDrive for Business sites including the number of viewed, modified, uploaded, downloaded, shared, or synced files.
| 083| OneDrive                      | Usage file counts                                 | yes   | [CSV](./Samples/OneDrive-Usage-file-counts.csv)                                           | Get the total number of OneDrive files across all sites and how many are active files in the given time period. 
| 084| OneDrive                      | Usage storage                                     | yes   | [CSV](./Samples/OneDrive-Usage-storage.csv)                                               | Get the trend on the amount of storage that is being used in OneDrive for Business.
| 085| Exchange                      | Activity user detail                              | -     | [CSV](./Samples/Exchange-Activity-user-detail.csv)                                        | Get the last email activity date per user, emails sent, received and read.
| 086| Exchange                      | Activity counts                                   | yes   | [CSV](./Samples/Exchange-Activity-counts.csv)                                             | Understand the trends of email activity and see how many emails were sent, read, and received in your organization.
| 087| Exchange                      | Activity user counts                              | yes   | [CSV](./Samples/Exchange-Activity-user-counts.csv)                                        | Understand trends on the number of unique email users who are performing activities like email send, read, and receive.
| 088| Exchange                      | App usage user detail                             | -     | [CSV](./Samples/Exchange-App-usage-user-detail.csv)                                       | See which apps and protocols users are using for accessing their mailbox.
| 089| Exchange                      | App usage apps user counts                        | yes   | [CSV](./Samples/Exchange-App-usage-apps-user-counts.csv)                                  | Get the count of unique users by email app.
| 090| Exchange                      | App usage user counts                             | yes   | [CSV](./Samples/Exchange-App-usage-user-counts.csv)                                       | Get the count of unique users that connected to Exchange Online using any email app.
| 091| Exchange                      | App usage versions user counts                    | yes   | [CSV](./Samples/Exchange-App-usage-versions-user-counts.csv)                              | Get the count of unique users by Outlook desktop version.
| 092| Exchange                      | Usage detail                                      | -     | [CSV](./Samples/Exchange-Usage-detail.csv)                                                | Get detailed information about mailbox usage as the mailbox size, the number of items, quotas and more.
| 093| Exchange                      | Usage mailbox counts                              | yes   | [CSV](./Samples/Exchange-Usage-mailbox-counts.csv)                                        | Get the total number of user mailboxes in your organization and how many are active each day during the given time period.
| 094| Exchange                      | Usage quota status mailbox counts                 | yes   | [CSV](./Samples/Exchange-Usage-quota-status-mailbox-counts.csv)                           | Get the count of user mailboxes by each quota category.
| 095| Exchange                      | Usage storage                                     | yes   | [CSV](./Samples/Exchange-Usage-storage.csv)                                               | Get the amount of storage used by mailboxes in your organization.
| 096| Exchange                      | User forwarding                                   | -     | [CSV](./Samples/Exchange-User-forwarding.csv)                                             | Get a list of all users within your OU's with information if email forwarding is activated.
| 097| Exchange                      | Litigation hold user mailboxes                    | -     | [CSV](./Samples/Exchange-Litigation-hold-user-mailboxes.csv)                              | Get the litigation hold information of your user mailboxes.
| 098| Exchange                      | Litigation hold shared mailboxes                  | -     | [CSV](./Samples/Exchange-Litigation-hold-shared-mailboxes.csv)                            | Get the litigation hold information of your shared mailboxes.
| 099| Exchange                      | Litigation hold resource mailboxes                | -     | [CSV](./Samples/Exchange-Litigation-hold-resource-mailboxes.csv)                          | Get the litigation hold information of your resource mailboxes.
| 100| Delegate365                   | Report Services                                   | -     | [CSV](./Samples/Delegate365-Report-Services.csv)                                          | Report the count of active users in the services, such as Exchange, OneDrive, SharePoint, Teams, Skype and Yammer
| 101| Delegate365                   | Groups governance                                 | yes   | [CSV](./Samples/Delegate365-Groups-governance.csv)                                        | All Office 365 groups at a glance with visibility, classification, renewed date, type, owner count, members and guests.
| 102| Delegate365                   | User                                              | -     | [CSV](./Samples/Delegate365-User.csv)                                                     | A list of all users the admin can manage.
| 103| Delegate365                   | Security groups                                   | -     | [CSV](./Samples/Delegate365-Security-groups.csv)                                          | A list of all security groups the admin can manage.
| 104| Delegate365                   | Office 365 groups                                 | -     | [CSV](./Samples/Delegate365-Office365-groups.csv)                                         | A list of all Office 365 groups the admin can manage.
| 105| Delegate365                   | Distribution groups                               | -     | [CSV](./Samples/Delegate365-Distribution-groups.csv)                                      | A list of all distribution groups the admin can manage.
| 106| Delegate365                   | Dynamic groups                                    | -     | [CSV](./Samples/Delegate365-Dynamic-groups.csv)                                           | A list of all dynamic groups the admin can manage. 
| 107| Delegate365                   | Shared mailboxes                                  | -     | [CSV](./Samples/Delegate365-Shared-mailboxes.csv)                                         | A list of all shared mailboxes the admin can manage. 
| 108| Delegate365                   | Resources                                         | -     | [CSV](./Samples/Delegate365-Resources.csv)                                                | A list of all resource mailboxes the admin can manage. 
| 109| Delegate365                   | Contacts                                          | -     | [CSV](./Samples/Delegate365-Contacts.csv)                                                 | A list of all contacts the admin can manage. 
| 110| Delegate365                   | License-statistics                                | -     | [CSV](./Samples/Delegate365-License-statistics.csv)                                       | Shows a list of used Microsoft 365 licenses and license quotas for each OU and license.
| 111| Delegate365                   | OU overview                                       | -     | [CSV](./Samples/Delegate365-OU-overview.csv)                                              | A list of objects that are assigned to an OU the admin can manage. 
| 112| Premium                       | User Last Logon                                   | -     | [CSV](./Samples/Premium-UserLastLogon.csv)                                                | A list of all users in their assigned OUs, including last login date, days since last login, account enabled, employee ID, assigned licenses, and other metadata. Use this report to identify users who have been inactive for a long time.
| 113| Premium                       | User missing data                                 | -     | [CSV](./Samples/Premium-UserMissingData.csv)                                              | A list of all users in their assigned OUs, including last login date and department, company, business phone, job title, zip code, city, state, country and other metadata. Use this report to find users with empty fields to fill in this information.
| 114| Premium                       | Deleted Users                                     | yes   | [CSV](./Samples/Premium-DeletedUsers.csv)                                                 | A list of all deleted users in the M365 tenant. This includes the last login date, account enabled, and other metadata.
| 115| Premium                       | Deleted Groups                                    | yes   | [CSV](./Samples/Premium-DeletedGroups.csv)                                                | A list of all deleted groups in the M365 tenant. This includes creation date, deletion date, group type and other metadata.


## Remarks

This is a consolidated version of the previous versions in this repository. The ReadMe shows a quick overview of all reports that are available in Delegate365. This list will change with newer versions and will be updated continuously. All information in this reporistory, including Internet or other external references, is subject to change without notice.

These reports are available with Delegate365 version 9.1 and later.  

**Update June 2023:**  
Reports in the **Premium** section are only available for customers who have the Governance Toolkit 365 (GT365) in production. Find more information about GT365 at [**governancetoolkit365.com**](https://governancetoolkit365.com/).  

## More information

For information about atwork pls. contact [**atwork**](https://www.atwork-it.com).  

For information about Delegate365 pls. visit [**Delegate365**](https://www.Delegate365.com).  

(c) by [atwork](https://www.atwork-it.com)
