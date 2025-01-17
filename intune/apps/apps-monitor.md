---
# required metadata

title: Monitor app information and assignments
titleSuffix: Microsoft Intune
description: After you've assigned an app to users or devices, use this information to help you monitor the app's status.
keywords:
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 07/22/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: apps
ms.localizationpriority: high
ms.technology:
ms.assetid: 64e5133d-1e23-4ee6-b556-f5d32c0e95da

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: mghadial
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Monitor app information and assignments with Microsoft Intune

[!INCLUDE [azure_portal](../includes/azure_portal.md)]

Intune provides several ways to monitor the properties of apps that you manage and to manage app assignment status.

1. Sign in to [Intune](https://go.microsoft.com/fwlink/?linkid=2090973).
3. In the **Intune** pane, select **Client apps**.
4. In the **Manage** section of the menu, select **Apps**.
5. In the list of apps, select an app to monitor. You'll then see the app pane, which includes an overview of the device status and the user status.

> [!NOTE]
> Android Store apps that are deployed as **Available** do not report their installation status.

## App overview pane

In the app pane, you can review details about the status of an app in your environment.

### Essentials
The **Essentials** section contains the following information about the app:

 | **App details**            | **Description**                                                      |
|------------------------|------------------------------------------------------------------|
| **Publisher**          | The publisher of the app.                                            |
| **Operating system**   | The app operating system (Windows, iOS, Android, and so on). |
| **Created**             | The date and time when this revision was created. <b>**Note**: This date value is updated when an IT admin changes app metadata, such as changing the app category or app description.                        |
| **Assigned**           | Whether the app has been assigned (**Yes** or **No**).                  |

### Device and user status graphs
The graphs show the number of apps for the following status:

| **Device status**       | **Description**                                       |
|-----------------------|-------------------------------------------------------|
| **Installed**         | The number of apps installed.                         |
| **Not Installed**     | The number of apps not installed.                     |
| **Failed**            | The number of failed installations.                   |
| **Install Pending**   | The number of apps that are in the process of being installed. |
| **Not Applicable**           | The number of apps for which status is not applicable.            |

> [!NOTE]
> Be aware that Android LOB apps (.APK) deployed as **Available with or without enrollment** only report app installation status for enrolled devices. App installation status is not available for devices that are not enrolled in Intune.

### Device install status

A device status list is shown when you select **Device install status** in the **Monitor** section of the menu. The details table includes the following columns:

| **Device column**      | **Description**                                                                                                                                                                                                                                            |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Device name**      | The name of the device on platforms that allow naming a device. On other platforms, Intune creates a name from other properties. This attribute isn't available to any other device.                                                                       |
| **User name**        | The name of the user.                                                                                                                                                                                                                                      |
| **Platform**         | The operating system of the device (Windows, iOS, Android, and so on).                                                                                                                                                                                           |
| **Version**          | The version number of the app. For line-of-business (LOB) apps and Microsoft Store for Business apps, the full version number of the app is shown. The full version number identifies a specific release of the app. The number appears as _Version_(_Build_). For example,  2.2(2.2.17560800). For standard Store apps, no versions are shown. |
| **Status**           | The status of the app.                                                                                                                                                                                                                                     |
| **Status details**   | The details of the status.                                                                                                                                                                                                                                     |
| **Last check-in**    | The date of the device's last sync with Intune.                                                                                                                                                                                                                  |


### User install status

A user status list is shown when you select **User install status** in the **Monitor** section of the menu. The details table includes the following columns:

| **User column**     | **Description**                           |
|---------------------|-------------------------------------------|
| **Name**            | The name of the user in Azure Active Directory.         |
| **User name**       | The unique name of the user.              |
| **Installations**   | The number of apps installed by the user. |
| **Failures**        | The number of failed app installations for the user.     |
| **Not installed**   | The number of apps not installed by the user. |


## Next steps

- To learn more about working with your Intune data, see [Use the Intune Data Warehouse](../reports-nav-create-intune-reports.md).
- To learn about app configuration policies, see [App configuration policies for Intune](app-configuration-policies-overview.md).
