---
title: Frequently asked questions about AltspaceVR audio
description: Troubleshooting and support for audio related issues.
ms.date: 8/23/2021
author: qianw211    
ms.author: v-qianwen
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

There is no push-to-talk button.  If you look to the lower left of your view, there is a microphone icon that can be used to toggle voice. Alternatively, you may use the keyboard shortcut, Space Bar to mute/un-mute your microphone.

If the icon blinks when you talk, your microphone is working!
 
## What do I do if my audio is choppy?

Some users have noticed that when another avatar is speaking the audio comes across as choppy, or with regular drop-outs. You may in other instances be informed by other users that your own audio is coming through choppy, or robotic.

The first thing to try is always reentering the space you are in, or even restarting AltspaceVR if this fails. Audio issues aren't common but when they do occur this is often an easy fix. 

If this fails these are some other things, you can investigate:

#### CPU Performance for desktop users

Review our [Recommended System Specifications](../getting-started/system-requirements.md) for hardware we suggest for running AltspaceVR. We've found that i3 or lower CPUs cause issues not only with the frame rates of the video, but can contribute to audio issues such as drop-outs and poor quality.

#### Internet Bandwidth and Network Connection

Users on slow internet connections (less than 5mbps) or on WiFi may have audio issues such as drop-outs. We recommend hardline connection of an Ethernet cable to your computer, and a connection faster than 5mbps. You may want to exit any programs that might be using internet connectivity in the background.

## What do I do if other users can't hear me?

First, determine if AltspaceVR is detecting the audio from your microphone. You can determine this by looking at whether the microphone icon in the lower left of your view is blinking when you're talking. If the icon blinks when you talk, your microphone is working. If the icon is red, you're muted. Select the icon to mute or unmute yourself.

If you don't see your microphone icon blinking after unmuting, then you may need to adjust your microphone settings in AltspaceVR, go to Menu / Settings / Audio / Audio Input Selection. Then using the arrow buttons to select the Mic you'd like to use.
 
### Oculus Quest/Quest 2

Make sure you give permissions to use your Mic audio when you're installing AltspaceVR. Another check you can do is looking in: Menu / Settings / Audio / Audio Input Selection and making certain it's set to Android audio input, which is Quest/Quest2's default mic.
 
### Windows Mixed Reality, Oculus Rift/Rift S, HTC Vive, or 2D Mode

Make sure you have the correct microphone settings in AltspaceVR: Menu / Settings / Audio / Audio Input Selection. Then using the arrow buttons to select the Mic you'd like to use.

Before starting AltspaceVR ensure that the proper microphone is set as your default recording device in Windows. The Oculus Rift/Rift S and HTC Vive both have a built-in microphone, if you have another microphone plugged in AltspaceVR may be trying to use that device.
 
To change your default recording device in Windows:

* Right-click on your Speaker Icon in Windows and select **Open Sound settings**.
* Navigate to the **Input/Choose your input device** drop down.
* Choose the microphone you'd like to use from the dropdown menu: 
    * The HTC Vive microphone will be labeled **Microphone - USB Audio Device**.
    * The Oculus Rift Microphone will be labeled **Headset Microphone (Oculus Virtual Audio Device)**.
* After restarting AltspaceVR your microphone will now be picked up
 
If after following these steps you're still having issues, things which may be affecting you can be:

* If you Alt-Tab away for more than 30 seconds, AltspaceVR will auto mute you. You can disable this in **Menu -> Settings -> Audio -> Mute when AltspaceVR is idle**.
* The AltspaceVR audio system has a volume threshold that you may be below. Set mic levels to max, set the mic closer to your mouth, and speak at normal volume.
* Exit VR, try plugging your USB cord from your headset into an alternative USB 3.0 port. In our experience, some USB 3.0 ports cause issues.

AltspaceVR may not recognize sound setting changes made while in game, so you may need to restart AltspaceVR for the above microphone changes to take effect.  When you re-enter the game, look at the microphone icon and see if it blinks when you talk. If the icon blinks, then your microphone is working.

## Support

Questions or feedback for the AltspaceVR team? 

> [!div class="nextstepaction"]
> [Click here to send a Support Request](https://help.altvr.com/hc/requests/new)