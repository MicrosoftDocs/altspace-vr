---
title: Upgrading Old Unity Projects
description: Learn how to update your content to the latest version of Unity.
ms.date: 10/19/2021
ms.topic: article
keywords: kits, worlds, unity, updating, shaders, uploader, troubleshooting
---

Upgrading Old Unity Projects
=============================

Over the years, AltspaceVR has undergone several infrequent upgrades requiring users to change their content. If you find
that a template or kit that you've uploaded in the past is not accessible in the latest version of AltspaceVR, follow
this guide to get your content up and running again.

> [!NOTE]
> Before following any steps in this guide, you should create a full backup of your project in case the upgrade doesn't
> go smoothly. The simplest way is to create a second copy of the entire project folder. For a more advanced solution,
> consider using a version control system like Git and GitHub.

Overview
---------

As of this writing, the current version of AltspaceVR uses the following configuration:

* Game Engine: Unity 2020.3.18f1 (also acceptable: Unity 2020.3.9f1)
* Upload Tool: Uploader 2.2
* Rendering: Universal Render Pipeline (URP)
* Stereo Mode: Single-Pass Instancing (SPI), or Multiview on Quest

If your project Unity version is older than 2020.3, you probably need to take all of these updates at once, so follow
this guide from the beginning. If you are on Unity 2020.3 already, but with Uploader 0.9, start from step 6.

1. **BACK UP YOUR PROJECT** - Create a copy of your entire project directory, and put it somewhere safe. This upgrade
    is a destructive upgrade, so you will lose your original project files after you complete it.
    If you come across any problems during this upgrade, you'll NEED a clean copy of your project to fall back on.

2. **REMOVE OLD UPLOADER** - Do this step if your project is using the AltspaceVR Uploader 0.8 or earlier. With Unity closed,
    delete the following files/folders, and it's corresponding .meta files. If the file/folder doesn't exist, just skip
    it.

    * Assets/Altspace
    * Assets/Plugins
    * Assets/Prefabs/test-folder
    * Assets/Prefabs/Readme.txt
    * Assets/Resources/bg.jpeg
    * Assets/Resources/bg2.jpeg
    * Assets/Resources/logo.png
    * Assets/Resources/UserPreferences.asset
    * Assets/DFloor_v004.fbx

3. **REMOVE PROCESSED ASSETS** - Do this step if you are upgrading to a new Unity version. With Unity closed, delete
    the Library folder out of the project. This is a Unity system folder containing engine-specific assets and
    files that are automatically generated from the contents of the Assets folder (among other things).

4. **DOWNLOAD ENGINE VERSION** - Do this step if you are upgrading to a new Unity version. Open the Unity Hub, and
    install Unity 2020.3.18f1 from the download archive ([link to engine install](unityhub://2020.3.18f1/a7d1c678663c)).
    * If building on a Windows PC, check the boxes for Android and Mac Build Support.
    * If building on a Mac, check the boxes for Android and Windows Build Support.

5. **UPGRADE PROJECT** - Open your cleaned project in Unity 2020.3.18f1, and allow Unity to upgrade your project.
    This will take some time.

6. **DOWNLOAD THE UPLOADER** - Download the latest version of the Uploader [here](https://aka.ms/AvrUrpUploader),
    and save it in your project's Packages folder. This file should have a file extension of ".tgz".
    > [!NOTE]
    > If you are using the Safari browser to download, it will be auto-extracted to a ".tar" file, which Unity
    > can't use. You can either use a different browser to download, or use the "gzip" system utility to re-compress it.
    
7. **INSTALL THE UPLOADER** - Install the Uploader from within the Unity Editor's package manager:
    1. Open the Unity Package Manager window: Windows > Package Manager
    2. In the top-left of the window, click the "+" icon, and select "Add package from tarball".
    3. Select the tgz file you downloaded in the last step.
    4. Wait for Unity to unpack the package.

8. **OPEN THE UPLOADER** - If installation was successful, an "AltspaceVR" menu will be available in the top bar.
    This menu contains separate windows for Kits and Templates. Open the one most appropriate to your project.
    The first time the window opens, it will configure your project settings to match the Altspace game client:
    enabling the Universal Render Pipeline, and Single-Pass Instancing

9. **FIX SHADERS** - While that first-time setup is running, a powershell window may appear temporarily.
    You may be prompted to upgrade some of your custom/downloaded shaders. If you approve the prompt, the powershell
    script will attempt to upgrade your shaders automatically, but the odds of success are low. You will need to
    manually check if the shader still functions correctly in URP.

10. **FIX MATERIALS** - Some/all of your materials may turn pink/magenta during the upgrade process. This indicates
    an error in the shader used by that material. If you used the Unity built-in shaders, you can usually automatically
    migrate these to URP-compatible shaders from the menu: Edit > Render Pipeline > Universal Render Pipeline >
    Upgrade Project Materials to UniversalRP Materials.

11. **BUILD AND UPLOAD** - At this point, your project should be fully upgraded. Follow the instructions in the
    [Getting Started](world-building-toolkit-getting-started.md) guide to build and upload your kit/template.

Troubleshooting Tips
---------------------

1. If you discover that your content only appears in one eye in VR mode, it is likely that the custom
    shaders you use do not support SPI rendering. You’ll need to choose a different shader, or follow
    [Unity’s SPI upgrade guide](https://docs.unity3d.com/Manual/SinglePassInstancing.html) to manually edit the shader
    and add support.

2. If you discover that some of your content is pink/magenta in-game, or is totally invisible, this can be caused
    by a shader being incompatible with URP. You will need to either replace the shader, or upgrade it yourself.