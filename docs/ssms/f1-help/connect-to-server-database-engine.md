---
title: "Connect to Server (Database Engine) | Microsoft Docs"
ms.custom: 
  - "SQL2016_New_Updated"
ms.date: "01/30/2017"
ms.prod: "sql-non-specified"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "tools-ssms"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "sql13.swb.connectoserverunknownservertype.f1"
  - "sql13.swb.connection.login.sqlce.f1"
  - "sql13.swb.connecttoce.f1"
  - "SQL13.SWB.CONNECTION.LOGIN.SQLSERVER.F1"
  - "sql13.swb.connection.login.sqlserver.f1"
  - "sql13.swb.manageSS2k.f1"
ms.assetid: ee9017b4-8a19-4360-9003-9e6484082d41
caps.latest.revision: 6
author: "stevestein"
ms.author: "sstein"
manager: "jhubbard"
---
# Connect to Server (Database Engine)
Use this dialog to view or specify options when connecting to [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion_md.md)]. In most cases, you can connect by entering the computer name of the database server in the **Server name** box and then clicking **Connect**. If you are connecting to [!INCLUDE[ssExpress](../../includes/ssexpress_md.md)], use the computer name followed by **\sqlexpress**.  
  
Many factors can affect your ability to connect to [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)].  
  
## Options  
**Server type**  
When registering a server from Object Explorer, select the type of server to connect to: [!INCLUDE[ssDE](../../includes/ssde_md.md)], [!INCLUDE[ssASnoversion](../../includes/ssasnoversion_md.md)], [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion_md.md)], or [!INCLUDE[ssISnoversion](../../includes/ssisnoversion_md.md)]. The rest of the dialog shows only the options that apply to the selected server type. When registering a server from Registered Servers, the **Server type** box is read-only, and matches the type of server displayed in the Registered Servers component. To register a different type of server, select [!INCLUDE[ssDE](../../includes/ssde_md.md)], [!INCLUDE[ssASnoversion](../../includes/ssasnoversion_md.md)], [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion_md.md)], [!INCLUDE[ssEW](../../includes/ssew_md.md)], or [!INCLUDE[ssISnoversion](../../includes/ssisnoversion_md.md)] from the Registered Servers toolbar before starting to register a new server.  
  
**Server name**  
Select the server instance to connect to. The server instance last connected to is displayed by default.  
  
> [!NOTE]  
> To connect to an active user instance of [!INCLUDE[ssExpress](../../includes/ssexpress_md.md)] connect using named pipes protocol specifying the pipe name, such as np:\\\\.\pipe\3C3DF6B1-2262-47\tsql\query For more information, see the [!INCLUDE[ssExpress](../../includes/ssexpress_md.md)] documentation.  
  
**Authentication**  
Three authentication modes are available when connecting to an instance of the [!INCLUDE[ssDE](../../includes/ssde_md.md)].  
  
**Windows Authentication**  
[!INCLUDE[msCoName](../../includes/msconame_md.md)] Windows Authentication mode allows a user to connect through a Windows user account.  
  
**SQL Server Authentication**  
When a user connects with a specified login name and password from a non-trusted connection, [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] performs the authentication itself by checking to see if a [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] login account has been set up and if the specified password matches the one previously recorded. If [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] does not have a login account set, authentication fails, and the user receives an error message.  
  
> [!IMPORTANT]  
> When possible, use Windows Authentication or Active Directory Password Authentication.  
  
**Active Directory Universal Authentication**  
Active Directory Universal Authentication is an interactive work flow that supports Azure Multi-Factor Authentication (MFA). Azure MFA helps safeguard access to data and applications while meeting user demand for a simple sign-in process. It delivers strong authentication with a range of easy verification options—phone call, text message, smart cards with pin, or mobile app notification—allowing users to choose the method they prefer. When the user account is configured for MFA the interactive authentication work flow requires additional user interaction through pop-up dialog boxes, smart card use, etc. When the user account is configured for MFA, the user must select Azure Universal Authentication to connect. If the user account does not require MFA, the user can still use the other two Azure Active Directory Authentication options. For more information, see [SSMS support for Azure AD MFA with SQL Database and SQL Data Warehouse](https://azure.microsoft.com/documentation/articles/sql-database-ssms-mfa-authentication/). Requires at least SSMS version 16.3 (August 2016).

**Active Directory Password Authentication**  
Azure Active Directory Authentication is a mechanism of connecting to [!INCLUDE[msCoName](../../includes/msconame_md.md)][!INCLUDE[ssSDSfull](../../includes/sssdsfull_md.md)] by using identities in Azure Active Directory (Azure AD).  Use this method for connecting to [!INCLUDE[ssSDS](../../includes/sssds_md.md)] if you are logged into Windows using credentials from a domain that is not federated with Azure, or when using Azure AD authentication using Azure AD based on the initial or the client domain. For more information, see [Connecting to SQL Database By Using Azure Active Directory Authentication](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**Active Directory Integrated Authentication**  
Azure Active Directory Authentication is a mechanism of connecting to [!INCLUDE[msCoName](../../includes/msconame_md.md)][!INCLUDE[ssSDSfull](../../includes/sssdsfull_md.md)] by using identities in Azure Active Directory (Azure AD). Use this method for connecting to [!INCLUDE[ssSDS](../../includes/sssds_md.md)] if you are logged into Windows using your Azure Active Directory credentials from a federated domain. For more information, see [Connecting to SQL Database By Using Azure Active Directory Authentication](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**User name**  
The Windows user name to connect with. This option is only available if you have selected to connect using **Active Directory Password Authentication**. It is read-only when you selecting **Windows Authentication**.  
  
**Login**  
Enter the login to connect with. This option is only available if you have selected to connect using [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Authentication or or Active Directory Password Authentication.  
  
**Password**  
Enter the password for the login. This option is only editable if you have selected to connect using [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Authentication or or Active Directory Password Authentication.  
  
**Connect**  
Click to connect to the server selected above.  
  
**Options**  
Click to display additional server connection options, such as registering a server and remembering the password.  
  
