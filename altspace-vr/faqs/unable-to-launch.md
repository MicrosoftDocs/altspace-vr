---
title: I can't launch AltspaceVR
description: Learn how to fix issues relating to launching the AltspaceVR environment.
author: hferrone
ms.author: v-hferrone
ms.date: 02/10/2021
ms.topic: article
keywords: faq
---

# I can't launch AltspaceVR

There are several reasons why AltspaceVR may not launch for you. Try out the following steps to ensure the application is installed correctly with the necessary third-party software.

## If you're trying to launch AltspaceVR for the first time:

1. Verify that your device is supported and meets the [minimum specified requirements](../getting-started/system-requirements.md).
2. Make sure you have the latest [Oculus Software](https://www.oculus.com/setup) installed, and that Settings-> General-> Unknown Devices is set to ON. If launching in 2D mode, you don't need Oculus installed.
3. Make sure that you have a working internet connection. If you're attempting to launch Altspace from within a network firewall, open UDP ports 5055 and 5056, and TCP ports 80 and 443. If you are within the network of a corporate or educational firewall, you may need to contact the network administrator or IT department.
4. See also:
    * [Installing AltspaceVR for Oculus Quest](../getting-started/oculus-installation.md)
    * [Installing AltspaceVR for Windows Mixed Reality](../getting-started/wmr-installation.md)

## If AltspaceVR reports that the current version is out of date:

* The version of the application you're using is no longer supported. If you downloaded AltspaceVR through a storefront, the update may have launched recently before your store was able to update your client.
* If you would like to force update, you may do so through the various storefronts:
    * **Microsoft Store:** [Microsoft Store Support - Get updates for apps and games in Microsoft Store](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f)
    * **Oculus:** Open your Oculus Library and navigate to 'Updates' in the left navbar.
    * **Steam:** [Steam Support - Update & Installation Issues](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

## If the program was working, but ceased to launch after update:

* Do a 'Clean Reinstall' of the software. This requires you to uninstall or remove existing versions of the Application. Once fully removed from your system, install Altspace via Steam, Oculus, or Microsoft Store.
* If you do have a problem launching AltspaceVR, let us know via a [support ticket](https://help.altvr.com/hc/requests/new). Include a [log file](uploading-client-logs.md) from your session.

## If AltspaceVR fails to launch after customizing your home space:

* Navigate to your [home space's website](https://account.altvr.com/users/sign_in).
* Verify that your world's template still exists. If the template was shared with you, it may have been deleted by the owner, which would cause your home space to fail to load.
    * If the template has been deleted, simply 'Edit' the world from the left 'World Tools' panel, replace the existing template with another template, and 'Update' to save changes.
* Remove any objects that may be failing to load by selecting 'Objects' from the left 'World Tools' panel. Problematic objects may include:
    * Objects from deleted kits, or objects deleted from kits, that are still present in your world.
    * Experimental GLTFs.
* After addressing the items above, attempt to reenter AltspaceVR.