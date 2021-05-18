---
title: Updating Content to the Latest Unity Version
description: Learn how to update your content to the latest version of Unity.
ms.date: 05/11/2021
ms.topic: article
keywords: kits, worlds, unity, updating, shaders, uploader, troubleshooting
---

# Moving to Unity 2020.3

AltspaceVR is upgrading to the latest version of Unity (2020.3). Beginning today, we're kicking off a content upgrade initiative. All creators are highly encouraged to begin to update their content (worlds, kits, etc.) to Unity 2020.3 as soon as possible. The content uploader has been updated for Unity 2020.3 and is ready for use.

It's highly important that all creator-owned content is updated as soon as possible. In the coming weeks, AltspaceVR will move to a new build, which will no longer support backwards-compatibility with content from 2019.4 and older. Any content that is not updated within this window will likely experience breaking changes.

> [!NOTE]
> If you are regularly using and are reliant upon content that is owned by someone else and has been shared with you, please reach out to the world/kit owner and work with them to understand their content update plan.
> If you are a content creator and you have questions or require assistance, please contact our support team for help: altvr.com/support

The update to Unity 2020.3 will include a change to "stereo render mode" as part of our move onto the new XR SDKs. This will ensure AltspaceVR runs on a more future-proof and supported format, which will enable greater performance and compatibility with the headsets of today and tomorrow.

## AltspaceVR Uploader v0.9.0 Upgrade Guide

Uploader 0.9 is packaged very differently than previous versions of the
Uploader. Simultaneous with this packaging change, the new Uploader requires a
new version of Unity. This guide is intended to make this upgrade process
smoother and safer for all involved.

1. **BACK UP YOUR PROJECT** - Create a copy of your entire project directory,
	and put it somewhere safe. This is a destructive upgrade, and you will no
	longer be able to create or upload bundles for Unity 2019.4 after you
	complete it. If you encounter any problems during this
	upgrade, you will NEED a clean copy of your project to fall back on. You
	will also need it to update any live kits or templates before
	Altspace officially upgrades to Unity 2020.3.

2. **REMOVE OLD UPLOADER** - With Unity closed, delete the following files/folders,
	and their corresponding .meta files:
	* `Assets/Altspace`
	* `Assets/Plugins`
	* `Assets/Prefabs/test-folder`, `Readme.txt`
	* `Assets/Resources/bg.jpeg`, `bg2.jpeg`, `logo.png`, `UserPreferences.asset`
	* `Assets/DFloor_v004.fbx`
	* `Library` (This is a Unity system folder, not an Uploader folder.
		Delete it anyway, and let it be rebuilt during the upgrade.)

3. **DOWNLOAD ENGINE VERSION** - Open the Unity Hub, and install the latest
	revision of Unity 2020.3 (5f1 as of this writing). 

4. **UPGRADE PROJECT** - Open your cleaned project in Unity 2020.3, and allow
	Unity to upgrade your project.

5. (PC Only) **DOWNLOAD MIXED REALITY FEATURE TOOL** - Follow the instructions to download the 
	[Mixed Reality Feature Tool](https://docs.microsoft.com/en-us/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool),
	which you will use to manage the installation of the Uploader package.

6. **INSTALL THE UPLOADER** - Use the MR Feature Tool to select your Unity project,
	and add the AltspaceVR Uploader feature (under the AltspaceVR heading).
	Follow the instructions in the tool.
	
	On MacOS, manually download the latest version
	from the [registry](https://dev.azure.com/aipmr/MixedReality-Unity-Packages/_packaging?_a=package&feed=Unity-packages&package=com.microsoft.altspacevr_uploader&protocolType=Npm&version=0.9.0&view=versions),
	and install it from within the Unity Editor's package manager (Windows >
	Package Manager > + > Add package from tarball).

Once the package finishes importing, the familiar Uploader window should be
available in the AltspaceVR menu item.
