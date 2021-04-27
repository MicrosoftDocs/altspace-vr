---
title: Recording and live streaming
description: Learn how to record and live stream your AltspaceVR events from your PC to promote and share with your users.
ms.date: 04/26/2021
ms.topic: article
keywords: streaming, recording, video, audio, youtube, obs
---

# Recording and live streaming

Recording and Live Streaming your AltspaceVR experience to show others around the world is a great way to promote your event, AltspaceVR, and VR in general! Take a look below to see how to get started:

In this article, you'll learn how to:

* [Record AltspaceVR in 2D mode on PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Live stream to YouTube in AltspaceVR in 2D mode on PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## Recording AltspaceVR in 2D mode on PC

### The short version

1. Have AltspaceVR and OBS installed. Launch AltspaceVR in 2D mode, launch OBS, set OBS up to record AltspaceVR and record away!

### The slightly longer version

1. Visit [https://obsproject.com/](https://obsproject.com/)
2. Select **Windows** to download OBS. This post is using **OBS v22.0.2**
3. Install OBS

### Have AltspaceVR running in 2D mode BEFORE you run OBS

1. Download and install AltspaceVR from our website: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Make sure you launch AltspaceVR in 2D mode by unplugging your HMD’s USB cable from your PC or if you have a Rift: Ctrl+Alt+Del, Services, Oculus VR Runtime Service, right-click, Stop. 
    * This will disable Oculus and start AltspaceVR in 2D mode, repeat these steps and use Start to get VR mode back.

Now, Alt-Tab over to OBS:

1. Under Sources, select: **+ > Game Capture > Create New**
2. Edit text to 'AltspaceVR Capture', tick **Make source visible**, and select OK
3. Double-click **AltspaceVR Capture** under Sources
4. Change **Mode** to **Capture specific window**
5. Window: [AltspaceVR.exe]: AltspaceVR
6. Window Match Priority: Match title, otherwise find window of the same executable
7. Scroll down to Capture Cursor: untick
8. Select OK

This should make AltspaceVR show up in OBS. Now to set the following properties in OBS, go to **File > Settings**:

| Tab | Settings |
|---|---|
| **General** | Leave default |
| **Stream** | Leave default |
| Output mode | Switch to Advanced |
| Streaming tab | Audio Track 1 <br> Encoder: x264 <br> Rescale Output: unticked <br> Rate Control: CBR <br> Bitrate: 6000 (6000 for 30 fps or 9000 for 60 fps) <br> Keyframe Interval = 2 <br> CPU Usage Preset = veryfast |
| Recording tab | Type: Standard <br> Recording Path: D:/Video (Browse to where you'd like the video file saved to) <br> Recording Format: mp4 (If you get some crashing while recording, try flv here instead of mp4, if you crash the video will still be usable with flv) <br> Audio Track 1 <br> Encoder: Use stream encoder |
| Audio tab | Audio Bitrate: 160 (for all Tracks) |
| Replay buffer tab | Leave default |
| **Audio** | Sample Rate: 48khz <br> Channels: Stereo <br> Desktop Audio Device: Default <br> Desktop Audio Device 2: Disable <br> Mic/Aux Audio Device: Default |
| **Video** | Base (Canvas) Resolution: 1920x1080 <br> Output (Scaled) Resolution: 1920x1080 <br> Downscale Filter: Bicubic (Sharpened scaling, 16 samples) <br> Common FPS Values: 30 |
| **Hotkeys** | Leave default |
| **Advanced** | Process Priority: Normal | <br>

<br>Alright, now make sure to select **Apply**, then **OK** to save all your OBS settings. 

1. Alt-Tab over to AltspaceVR, get into the correct space/world/event and line up your camera (that is,, your Avatar) we're about to record a video!
2. Alt-Tab over to OBS and when you're ready click **Start Recording**.

You'll see at the bottom right of OBS that REC: will start counting up and the dot is red, which means you're recording!

Make a test recording out of this: 
1. In AltspaceVR open/close/rollover the menus to make UI sounds
2. Make sure you are unmuted, say 'Sibilance, Sibilance' or get another user to talk to you at a normal volume.
3. Look at the Desktop Audio and Mic/Aux levels as you do this to see if it's working.

We usually mute the Mic/Aux when recording. Go ahead and select the speaker icon for Mic/Aux and it will turn red with an X.

* It’s VERY difficult to match your audio and the other user’s audio so the Mic is best muted when you are recording an event.
* Another issue with audio is the way OBS is set up. It captures ALL audio from your computer, so if you're watching YouTube on your PC it will record that audio, or Discord notifications.
* To record just the audio from AltspaceVR, go into Volume Mixer (right-click on the Speaker icon on the bottom right of Windows) and mute System Sounds, browsers, and so on, but don't mute OBS or AltspaceVR.

> [!IMPORTANT]
> Don't forget to turn these Volume Mixer settings back on after recording.

Now, navigate back to OBS and select **Stop Recording** from **File>Show Recordings**. This opens up the folder with your OBS video files, double-click the test video.

Sometimes the recording is quite loud, so lower the slider for Desktop Audio and make another recording to test.


## Live streaming to YouTube in AltspaceVR 2D mode on PC

### The short version

Have AltspaceVR and OBS installed. Launch AltspaceVR in 2D mode, launch OBS, either live stream or create a 'New Live Event' on YouTube, set up OBS with your YouTube Stream Key, start streaming in OBS, start streaming on YouTube and you're off to the races!

### The slightly longer version

1. Visit [https://obsproject.com/](https://obsproject.com/)
2. Select **Windows** to download OBS (this post is using OBS v22.0.2)
3. Install OBS

Have AltspaceVR running in 2D mode BEFORE you run OBS
1. Download AltspaceVR from our Website: [https://account.altvr.com/downloads](https://account.altvr.com/downloads)
2. To make sure you launch AltspaceVR in 2D mode, either unplug your HMD’s USB cable from your PC or if you have a Rift: Ctrl+Alt+Del, Services, Oculus VR Runtime Service, right-click, Stop. This will disable Oculus Home and start AltspaceVR in 2D mode, repeat these steps and Start to get VR mode again.

3. Alt-Tab over to OBS

4. Under Sources, select **+**, Select Game Capture, Create new, Edit text to 'AltspaceVR Capture', tick Make source visible, OK
5. Double-click AltspaceVR Capture
6. Mode: Capture specific window
7. Window: [AltspaceVR.exe]: AltspaceVR
8. Window Match Priority: Match title, otherwise find window of the same executable
9. Scroll down to Capture Cursor: untick OK

This should make AltspaceVR show up in OBS. Nice!

Now in OBS goes to File>Settings:

| Tab | Settings |
|---|---|
| General | Tick Automatically record when streaming (this records a video file to your computer in addition to live streaming) |
| Stream | Stream Type: Streaming Services <br> Service: YouTube / YouTube Gaming (Can also stream to Twitch, Mixer, Facebook Live, etc.)<br>Server: Primary YouTube ingest server <br>Stream key: Paste your Stream Key from YouTube*** (See ‘Setting up Live Streaming on YouTube’ below) |
| Output | Output Mode: switch to Advanced |
| Streaming | Audio Track 1 <br>Encoder: x264 <br>Enforce streaming service encoder settings: tick <br>Rescale Output: unticked <br>Rate Control: CBR <br>Bitrate: 6000 (6000 for 30 fps or 9000 for 60 fps) <br>Keyframe Interval = 2 <br>CPU Usage Preset = veryfast |
| Recording | Type: Standard <br>Recording Path: D:/Video (Browse to where you'd like the video file saved to if you selected 'Automatically record when streaming' earlier) <br>Recording Format: mp4 (If you get some crashing while recording, try flv here instead of mp4, if you crash the video will still be usable with flv) <br>Audio Track 1 <br>Encoder: Use stream encoder |
| Audio | Audio Bitrate: 160 (for all Tracks) Sample Rate: 48khz <br>Channels: Stereo <br>Desktop Audio Device: Default <br>Desktop Audio Device 2: Disable <br>Mic/Aux Audio Device: Default |
| Replay buffer | Leave default |
| Video | Base (Canvas) Resolution: 1920x1080 <br>Output (Scaled) Resolution: 1920x1080 <br>Downscale Filter: Bicubic (Sharpened scaling, 16 samples) <br>Common FPS Values: 30 |
| Hotkeys | Leave default |
| Advanced | Process Priority: Normal |
|||

<br>Alright, now make sure to click Apply, then OK, then close and reopen OBS. That will save your all your OBS settings. Looking good :)

See the 'How to record AltspaceVR in 2D mode on PC' section above for instructions on how to test recording using a local recording instead of the live stream and also how to get your camera shot setup first before recording.

Another issue with audio is the way OBS is set up. It captures ALL audio from your computer, so if you're watching YouTube it will record that audio, or Teams messages, or notification sounds.

To record just the audio from AltspaceVR, go into Volume Mixer (right-click on the Speaker icon on the bottom right of Windows) and Mute System Sounds, Browsers, and so on, but don't Mute OBS or AltspaceVR.

Don't forget to turn the audio back on after recording ;)

Congrats you're an AltspaceVR video recorder!

## Setting up Live Streaming on YouTube

You can either quickly get a live stream going (**Stream**) or set up a future live stream event (**Manage**). I might suggest you set it up the 'Manage' way.

1. Open your browser and sign into [https://www.youtube.com/](https://www.youtube.com/) and then go to [https://www.youtube.com/my_live_events](https://www.youtube.com/my_live_events)
2. Select on your Account icon, top right, select Creator Studio from the drop-down
3. LIVE STREAMING on the left side of the page.

'**Stream now**' method:

* Select EDIT to enter your live stream info<br>
* Under Stream Settings, keep the defaults<br>
* Stream key (paste in encoder), select 'Reveal' and copy this key so you can paste it into OBS<br>
* Open OBS / Settings / Stream<br>
* Paste the Stream Key from YouTube into the Stream Key field in OBS<br>
* Apply, then OK<br>
* Select Start Streaming in OBS<br>
* Switch over to YouTube and you will see you are now LIVE on YouTube!<br>
* To see your actual YouTube live stream video page, you'll need to select the SHARE icon at the top right.<br>
* Copy and paste the 'Video link' into a new browser tab, you will see your YouTube live stream page.<br>
* This URL is your live stream link and can be shared out to all your Social channels :)<br>
* To stop the live stream, select Stop Streaming on OBS, this will end the live stream on YouTube.<br>
* Then stop stream on YouTube<br>

'**Manage**' method:
* Select 'Schedule Stream'
* Create New or Reuse Settings if you've already set up a previous managed live stream
* Add Title, Date, Start time, Description, Upload Thumbnail and Tags – Don’t forget to tag AltspaceVR :)
* Choose Public from the drop-down menu (default is 'Unlisted')
* Use defaults
* Copy Stream key (paste in encoder)
* To see your actual YouTube live stream video page, you'll need to select  the SHARE icon at the top right. This is your YouTube live stream event link, this can be shared on Social way ahead of your actual event!
* Now open OBS
* File / Settings
* Stream
* Paste the Stream Key you copied into the Stream Key field
* Apply, then OK
* Select  'Start Streaming'
* Back to YouTube, you'll see the 'Preview' window is showing your stream and GO LIVE is now lit up at the top right.
* Select GO LIVE
* You're now LIVE!
* Go to your browser tab with the 'View on Watch Page' link open to make sure the video looks good. REMEMBER you won’t hear the audio because you’ve turned off audio from your browsers when you muted them in Windows Volume Mixer. Check the audio on your phone or ask a friend to check the audio for you.
* Looking good!
* Alt-Tab back to AltspaceVR to move your camera (that is, your Avatar) around in your event.
* When you're done with your live stream go back to the YouTube 'Live Control Room' page
* Select 'Stop Streaming'
* Dialog box opens, asking if you want to stop streaming the live event, OK
* Go to OBS and select Stop Streaming as well.
* Congrats, you're now an AltspaceVR streamer!

For bonus points share your videos with the world on social media and make sure to tag us @AltspaceVR :)