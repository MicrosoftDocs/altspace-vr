---
title: Frequently asked questions about AltspaceVR audio
description: Troubleshooting and support for audio-related issues.
ms.date: 8/23/2021
author: qianw211    
ms.author: qianwen
ms.topic: article
keywords: vr, audio, troubleshooting, support
---

# Frequently asked questions about audio

## Does my VR headset have a built-in mic?

### Oculus Rift/Rift S, Oculus Quest/Quest 2, Windows Mixed Reality and HTC Vive

Yes, these VR headsets have built-in microphones.

### Windows

For headsets used with Windows, you should be able to find the microphone listed under your **Recording Devices** while you have the headset plugged in.

### Further Troubleshooting

* [AltspaceVR Support - Other users cannot hear me](#what-do-i-do-if-other-users-cant-hear-me)
* [AltspaceVR Support - Managing permissions for Oculus Quest](../getting-started/oculus-controls.md#managing-permissions)

## Is there a push-to-talk button?

There is no push-to-talk button. If you look to the lower left of your view, use the microphone icon to toggle the voice. Alternatively, you may use the keyboard shortcut Space Bar to mute/un-mute your microphone.

If the icon blinks when you talk, your microphone is working!
 
## What do I do if my audio is choppy?

Some users have found the audio choppy or have regular drop-outs when another avatar speaks. Your audio may come through choppy or robotic for other users in other instances.

If this fails, the first thing to try is always reentering your space or even restarting AltspaceVR. Audio issues aren't common, but this is often an easy fix when they do occur. 

If this fails, there are some other things you can investigate:

#### CPU Performance for desktop users

Review our [Recommended System Specifications](../getting-started/system-requirements.md) for hardware we suggest for running AltspaceVR. We've found that i3 or lower CPUs cause issues with the frame rates of the video but can contribute to audio issues such as drop-outs and poor quality.

#### Internet Bandwidth and Network Connection

Users on slow internet connections (less than 5mbps) or WiFi may have audio issues such as drop-outs. We recommend a hardline connection of an Ethernet cable to your computer and a link faster than 5mbps. You may want to exit any programs using internet connectivity in the background.

## What do I do if other users can't hear me?

First, determine if AltspaceVR is detecting the audio from your microphone. You can determine this by looking at whether the microphone icon in the lower left of your view is blinking when you're talking. A blinking icon when you talk indicates your microphone is working. If the icon is red, you're mute. Select the icon to mute or unmute yourself.

If you don't see your microphone icon blinking after unmuting, you may need to adjust your microphone settings in AltspaceVR. Go to Menu / Settings / Audio / Audio Input Selection. Then use the arrow buttons to select the mic you'd like to use.
 
### Oculus Quest/Quest 2

Make sure you give permission to use your Mic audio when installing AltspaceVR. Another check you can do is look in **Menu / Settings / Audio / Audio Input Selection** and make sure to set to Android audio input, which is Quest/Quest2's default mic.
 
### Windows Mixed Reality, Oculus Rift/Rift S, HTC Vive, or 2D Mode

Ensure you have the correct microphone settings in AltspaceVR: Menu / Settings / Audio / Audio Input Selection. Then use the arrow buttons to select the mic you'd like to use.

Before starting AltspaceVR, set the proper microphone as your default recording device in Windows. The Oculus Rift/Rift S and HTC Vive have built-in microphones. If you have another microphone plugged in, AltspaceVR may be trying to use that device.
 
To change your default recording device in Windows:

* Right-click on your Speaker Icon in Windows and select **Open Sound settings**.
* Navigate to the **Input/Choose your input device** dropdown.
* Choose the microphone you'd like to use from the dropdown menu: 
    * The HTC Vive microphone will be labeled **Microphone - USB Audio Device**.
    * The Oculus Rift Microphone will be labeled **Headset Microphone (Oculus Virtual Audio Device)**.
* After restarting, AltspaceVR will now pick up your microphone.
 
If after following these steps you're still having issues, things that may be affecting you can be:

* If you Alt-Tab away for more than 30 seconds, AltspaceVR will automute you. You can disable this in **Menu -> Settings -> Audio -> Mute when AltspaceVR is idle**.
* The AltspaceVR audio system has a volume threshold that you may be below. Set mic levels to the max, put the mic closer to your mouth, and speak at average volume.
* Exit VR, try plugging your USB cord from your headset into an alternative USB 3.0 port. In our experience, some USB 3.0 ports cause issues.

AltspaceVR may not recognize sound setting changes made in-game, so you may need to restart AltspaceVR for the above microphone changes. When you reenter the game, look at the microphone icon and see if it blinks when you talk. If the icon blinks, then your microphone is working.

## Support

Questions or feedback for the AltspaceVR team? 

> [!div class="nextstepaction"]
> [Click here to send a Support Request](https://help.altvr.com/hc/requests/new)