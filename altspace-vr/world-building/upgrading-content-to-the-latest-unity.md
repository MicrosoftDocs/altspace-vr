---
title: Updating Content to the Latest Unity Version
description: Learn how to update your content to the latest version of Unity.
ms.date: 06/4/2021
ms.topic: article
keywords: kits, worlds, unity, updating, shaders, uploader, troubleshooting
---

# Updating Content to the Latest Unity Version

## Moving to Unity 2020.3.9

Starting today, AltspaceVR has upgraded to a recent version of Unity (2020.3.9). In addition to some performance improvements, this update future-proofs us for forthcoming features that we're excited to incorporate. This change should be compatible with all existing content. If it isn't, feel free to contact support: altvr.com/support

Though this move to 2020.3.9 hasn't affected user-generated content, in a few weeks we're making a change to AltspaceVR's [stereo rendering mode that will require users to update their content]( https://docs.unity3d.com/Manual/SinglePassStereoRendering.html). This upgrade to [Single Pass Instancing](https://docs.unity3d.com/Manual/SinglePassInstancing.html) will allow for significant performance improvements in your worlds. Keep in mind that this new build will no longer support backwards-compatibility with content from 2019.4 and older. It's urgent that all creator-owned content is updated as soon as possible to avoid breaking changes. Follow the guide below to update your content and ensure a smooth transition to Single Pass Instancing on Unity 2020.3.9.

> [!NOTE]
> If you are regularly using content that is owned by someone else and has been shared with you, contact the world/kit owner and make sure they are planning to update their content.

> If you are a content creator and you have questions or require assistance, please contact our support team for help: altvr.com/support

## Testing your SPI content

Use the following preview versions of AltspaceVR to test your newly updated content in VR. The preview versions are for testing purposes only, and shouldn't be used for a general use of the platform.

* [AltspaceVR SPI Preview for Windows Mixed Reality](https://aka.ms/AvrSpiMr)
* [AltspaceVR SPI Preview for SteamVR](https://aka.ms/AvrSpiSteam)
* [AltspaceVR SPI Preview for Oculus Rift](https://aka.ms/AvrSpiRift)

> Note: Only PC VR previews have been provided. Single pass instanced rendering is not available on Android, and is not needed on non-VR platforms like Mac. Thus, you can use the general release version to test these devices.


## Store Compatibility Check

The upgrade to Unity 2020.3.9 will also affect headset and store-build compatibility. It's now a requirement that you download AltspaceVR from the store that is compatible with your headset. As an example: For a WinMR or Oculus headset, download AltspaceVR from the Windows Store or Oculus Store, respectively. Windows Mixed Reality users should download AltspaceVR from the Windows Store, SteamVR users from Steam, and Oculus Rift users from the Oculus Store.

## AltspaceVR Uploader v0.9.0 Upgrade Guide 

Uploader 0.9 is packaged differently than previous versions of the Uploader. Simultaneous with this packaging change, the new Uploader requires a new version of Unity. This guide is intended to make this upgrade process smoother and safer for all who are involved.

1. **BACK UP YOUR PROJECT** - Create a copy of your entire project directory, and put it somewhere safe. This upgrade is a destructive upgrade, so you won't be able to create or upload bundles for Unity 2019.4 after you complete it. If you come across any problems during this upgrade, you'll NEED a clean copy of your project to fall back on. You'll also need it to update any live kits or templates before AltspaceVR officially upgrades to Unity 2020.3.9.

2. **REMOVE OLD UPLOADER** - With Unity closed, delete the following files/folders, and it's corresponding .meta files:

    ```console
    * Assets/Altspace

    * Assets/Plugins

    * Assets/Prefabs/test-folder, Readme.txt

    * Assets/Resources/bg.jpeg, bg2.jpeg, logo.png, UserPreferences.asset

    * Assets/DFloor_v004.fbx

    * Library (This is a Unity system folder, not an Uploader folder. Delete it anyway, and let it be rebuilt during the upgrade.)
    ```

3. **DOWNLOAD ENGINE VERSION** - Open the Unity Hub, and install Unity 2020.3.9 (or [click here](https://unity3d.com/ru/unity/whats-new/2020.3.9) to install directly).

4. **UPGRADE PROJECT** - Open your cleaned project in Unity 2020.3.9, and allow Unity to upgrade your project.

5. (PC Only) **DOWNLOAD MIXED REALITY FEATURE TOOL** - Follow the instructions to download the [Mixed Reality Feature Tool](/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool), which you'll use to manage the installation of the Uploader package.

6. **INSTALL THE UPLOADER** - Use the MR Feature Tool to select your Unity project, and add the AltspaceVR Uploader feature (under the AltspaceVR heading). Follow the instructions in the tool.

On macOS, manually download the latest version from the [registry](https://dev.azure.com/aipmr/MixedReality-Unity-Packages/_packaging?_a=package&feed=Unity-packages&package=com.microsoft.altspacevr_uploader&protocolType=Npm&version=0.9.0&view=versions), and install it from within the Unity Editor's package manager (Windows > Package Manager > + > Add package from tarball).

Once the package finishes importing, the familiar Uploader window should be available in the AltspaceVR menu item.

## Troubleshooting Tips

1. If you're having controller or input issues on your WinMR headset, ensure it's positioned on your head to properly engage the presence sensor. This is a known issue and Microsoft is actively working to resolve it.

2. Check your headset and store-build compatibility. If you're using a WinMR headset, for example, make sure that your AltspaceVR build was acquired through the Windows Store.

3. If during testing you discover that your content only appears in one eye in VR mode, it is likely that the custom shaders you use do not support SPI rendering. You’ll need to choose a different shader, or follow [Unity’s SPI upgrade guide](https://docs.unity3d.com/Manual/SinglePassInstancing.html) to manually edit the shader and add support.

4. For those on WinMR, please remember that before you can access VR mode in AltspaceVR, you must: 
    1. Download and install OpenXR for Windows Mixed Reality from the Microsoft Store.
        1. Open the Mixed Reality Portal app
        2. On the lower-left corner of the app select "See More"
        3. In the menu that appears select Set Up OpenXR. Doing this will cause the Windows Store to launch from where you can install the runtime. If this menu item does not appear, OpenXR may already be installed on your PC.