---
title: Finding the AltspaceVR app version
description: 
author: hferrone
ms.author: v-hferrone
ms.date: 02/10/2021
ms.topic: article
ms.localizationpriority: high
keywords: 
---

# Finding the AltspaceVR app version

In the course of troubleshooting an issue, you may be asked what version of the AltspaceVR app you are currently running.

## In AltspaceVR

To find the app version in AltspaceVR, navigate to the **settings menu** and select **About** in the left navigation bar. The 'App Version' is reported here, as shown in the screenshot below.

![Settings menu open with about panel open]()

## In Windows System Settings

If you installed AltspaceVR via the Microsoft Store, you can additionally find the app version via Windows system settings.  This would be a good option to report the app version if you are unable to successfully log into the client.

To find the app version in Windows system settings, open the **Start Menu** and type **Apps & Features**. Select this, and navigate to **AltspaceVR** in the list of apps. Left click AltspaceVR and select **Advanced Options** from the menu that appears.

![Apps and features menu open with advanced option highlighted]()

In the **Advanced Options**, under the **Specifications** header, the **App Version** should be listed to the right of the **Version** label.

![Advanced options open with app version highlighted]()

## In Client Logs

AltspaceVR reports the app version in the client logs file as "Altspace Version" during application startup. This would be a good option to get the app version if you cannot successfully log into the client, but it did attempt to start before failing.

## Windows

On Windows, the client logs file can be found via Windows Explorer at:

```
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player.log
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player-prev.log
```

This file is overwritten each time you launch AltspaceVR. 'Player.log' represents your latest session, and 'Player-prev.log' represents the previous session.

## Via PowerShell

Advanced users can search the client logs for this string via PowerShell as follows:

Input:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Output:

[2.047] AltspaceVR Version: 3.2.23.e66c2