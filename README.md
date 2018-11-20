# Delegate365 Online Manual
Delegate365 is an Add-On for customers using Microsoft Office 365 and allows delegation, self-management, license-management and auditing. The software is provided as Software-as-a-Service solution in the Microsoft Cloud on Microsoft Azure and can be used instantly, see [Delegate365](https://www.Delegate365.com).


***Note: This manual is currently in work. atwork will complete this documentation in the next weeks. ***

Currently available modules:
- [Reports](./13-Reports/1-Reports.md)

 
## Synopsis
Welcome to the Delegate365 online manual. The following documents are available online here and describe the current status of the solution. In case of questions, pls. contact [atwork](https://www.atwork-it.com).

## Description
Delegate365 consists of a web portal and services, completely running on [Microsoft Azure](https://azure.microsoft.com/en-us/overview/what-is-azure/). It interacts with Microsoft Office 365 over API-calls and  secured channels using Azure Authentication. The whole product can be split into these parts:

- Delegate365 web interface. The web interface is an Azure website and is the interactive user interface for all admins. Only Delegate365 admins have the right to login here with their personal Office 365 login. The portal admins define the group of admins. This portal replaces the Office 365 portal for standard user management. Each customer gets his own website.
- Delegate365 Microsoft SQL Server database. The SQL database is running on an Azure SQL Database, see http://azure.microsoft.com/en-us/services/sql-database/. Delegate365 stores user object IDs and group memberships in a relational database. The entity model is also represented in the Delegate365 models and uses IDs for dependencies. Each customer gets his own database.
- Delegate365 cloud services. This is the counterpart for special operations against Microsoft Exchange Online and is running as an Azure cloud service. It´s the interface for actions that cannot be run in the Azure website because of technical or performance reasons. With Delegate365 version 2 and up the cloud service is part of a Delegate365 instance.
- Optional there exists a Delegate365 API which can be consumed by other web services, for example for external systems which want to create, update or delete users or their licenses in Office 365. The Delegate365 API is not part of a standard Delegate365 instance and not described here. For more information about the API interface pls. contact us.

With Delegate365 Portal Administrators can define users in a simple web portal that shall manage an office, a subsidiary, a department or any other organizational unit.
Common tasks like creation of users, distribution groups, assigning licenses or resetting passwords can easily be done with a minimum of effort. This is all restricted to the zone assigned to the local administrator (scope administrator).


## More information
For information about atwork pls. contact [**atwork**](https://www.atwork-it.com).

For information about Delegate365 pls. visit [**Delegate365**](https://www.Delegate365.com).

## Remarks
All information in this document, including Internet or other external references, is subject to change without notice. No part of this document may be reproduced or stored in a retrieval system or transmitted in any form or by any means without the express written permission of atwork gmbh (called "[atwork](https://www.atwork-it.com)" herein).
Any names of actual companies and products mentioned herein may be the trademarks of their respective owners.

(c) by [atwork](https://www.atwork-it.com)


[Next](1-About/1-Introduction.md)