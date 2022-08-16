---
title: Recording and live streaming
description: Learn how to record and live stream your AltspaceVR events from your PC to promote and share with your users.
author: qianw211    
ms.author: v-qianwen
ms.date: 11/1/2021
ms.topic: article
keywords: streaming, recording, video, audio, youtube, obs, live
---

# Recording and live streaming

Recording and Live Streaming your AltspaceVR experience to show others around the world is a great way to promote your event, AltspaceVR, and VR in general! Take a look below to see how to get started.

In this article, you'll learn how to:

* [Record AltspaceVR in 2D mode on PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Live stream to YouTube in AltspaceVR in 2D mode on PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## Recording AltspaceVR in 2D mode on PC

### The short version

1. Have AltspaceVR and OBS (Open Broadcaster Software) installed. Launch AltspaceVR in 2D mode, launch OBS, set OBS up to record AltspaceVR and record away!

### The slightly longer version

1. Visit [https://obsproject.com/](https://obsproject.com/)
2. Select **Windows** to download OBS. This post is using **OBS v26.1.1**
3. Install OBS

### Have AltspaceVR running BEFORE you run OBS

1. Download and install AltspaceVR from our website: [altvr.com/get](https://altvr.com/get-altspacevr/)
2. If you'd like to stabilize your VR video and eliminate jerky head movements, make sure you either use the 2D client, or launch AltspaceVR in 2D mode by unplugging your headset’s USB cable from your PC. If you have a Rift, press Ctrl+Alt+Del, select **Services**, **Oculus VR Runtime Service**, right-click, and select **Stop**. This will disable Oculus and start AltspaceVR in 2D mode. Repeat these steps and use Start to get VR mode back.
3. You can also record your experience in VR mode, using Game Capture with OBS

Now, Alt-Tab over to OBS:

1. Under **Scenes**, select **+** and name your new scene
2. Next, under **Sources**, select: **+ > Game Capture > Create new**
2. Edit text to 'AltspaceVR Capture', tick **Make source visible**, and select **OK**
3. Double-click **AltspaceVR Capture** under **Sources**
4. Change **Mode** to **Capture specific window**
5. Window: [AltspaceVR.exe]: AltspaceVR
6. Window Match Priority: Match title, otherwise find window of the same executable
7. Scroll down to **Capture Cursor**: untick
8. Select **OK**
9. This should make AltspaceVR show up in OBS.

Now to set the following properties in OBS, go to **File > Settings**:

|Tab|Settings|
|---|---|
| **General** | Leave default |
| **Stream** | Leave default |
| **Output** | Switch to Advanced |
| **-Streaming tab** | Audio Track 1 <br> Encoder: x264 <br> Rescale Output: unticked <br> Rate Control: CBR <br> Bitrate: 6000 (6000 for 30 fps or 9000 for 60 fps) <br> Keyframe Interval = 2 <br> CPU Usage Preset = veryfast |
| **-Recording tab** | Type: Standard <br> Recording Path: D:/Video (Browse to where you'd like the video files saved) <br> Recording Format: mp4 (If you get some crashing while recording, try flv here instead of mp4, if you crash, the video will still be usable with flv) <br> Audio Track 1 <br> Encoder: Use stream encoder |
| **-Audio tab** | Audio Bitrate: 160 (for all Tracks) |
| **-Replay buffer tab** | Leave default |
| **Audio** | Sample Rate: 44.1khz <br> Channels: Stereo <br> Desktop Audio: Default <br> Desktop Audio 2: Disable <br> Mic/Aux Audio: Default |
| **Video** | Base (Canvas) Resolution: 1920x1080 <br> Output (Scaled) Resolution: 1920x1080 <br> Downscale Filter: Bicubic (Sharpened scaling, 16 samples) <br> Common FPS Values: 30 (or 60) |
| **Hotkeys** | Leave default |
| **Advanced** | Process Priority: Normal | <br>

<br>Alright, now make sure to select **Apply**, then **OK** to save all your OBS settings. 

1. Alt-Tab over to AltspaceVR, get into the correct space/world/event and line up your camera (that is, your Avatar) we're about to record a video!
2. Alt-Tab over to OBS and when you're ready click **Start Recording**.

You'll see at the bottom right of OBS that **REC:** will start counting up and the dot is red, which means you're recording!

Make a test recording out of this: 
1. In AltspaceVR open/close/rollover the menus to make UI sounds
2. Make sure you are unmuted, say 'Sibilance, Sibilance' or get another user to talk to you at a normal volume.
3. Look at the **Desktop Audio** and **Mic/Aux** levels as you do this to see if it's properly picking up audio.

We usually mute the Mic/Aux when recording. Go ahead and select the speaker icon for Mic/Aux and it will turn red with an X.

* It’s VERY difficult to match your mic audio levels to the other user’s audio, so the Mic is best muted when you are recording an event.
* Another issue with audio is the way OBS is set up. It captures ALL audio from your computer, so if you're watching YouTube or get notification sounds on your PC it will record that audio.
* To record just the audio from AltspaceVR, go into **Open Volume mixer** (right-click on the Speaker icon on the bottom right of Windows) and mute System Sounds, browsers, and so on, but don't mute OBS or AltspaceVR.

> [IMPORTANT]
> Don't forget to unmute these Volume mixer settings after recording.

Now, navigate back to OBS and select **Stop Recording**. To find the video you just recorded go to **File>Show Recordings**. This opens up the folder with your OBS video files, double-click the test video.

Sometimes the recording is quite loud, so lower the slider for Desktop Audio in OBS and make another recording to test.

Pro-tip: use Ctrl+Alt+P to toggle on Photography Mode, it will remove the UI from your view to get a nice clean shot.

Congrats you're an AltspaceVR video recorder!

## Live streaming to YouTube in AltspaceVR 2D mode on PC

### The short version

Have AltspaceVR and OBS installed. Launch AltspaceVR and OBS. You can either live stream 'Right Now' or on a 'Later date'. On YouTube, set up OBS with your YouTube Stream Key. Start streaming in OBS and on YouTube, and you're off to the races!

### The slightly longer version

See the [Recording AltspaceVR in 2D mode on PC](#recording-altspacevr-in-2d-mode-on-pc) section at the top of this page for instructions on how to test recording using a local recording instead of the live stream, and how to get your camera shot set up.

## Setting up Live Streaming on YouTube

You can either get a live stream going 'Right Now' or set up a future live stream with 'Later date'.

1. Open your browser and sign into [https://www.youtube.com/](https://www.youtube.com/) and then go to [https://studio.youtube.com/](https://studio.youtube.com/)
2. Look to the top right and select **CREATE** then **Go live**

**'Right now'** method:

1. Select **Right now / START**
1. Select **Streaming software / GO**
1. Choose **EDIT**, top right, to edit your video details and customizations
1. Under **Stream Settings**, keep the defaults
1. Beside **Stream key (paste in encoder)**, **COPY** the key so you can paste it into OBS
1. Open OBS / **Settings** / **Stream**
1. In the **Service** drop-down menu, select **YouTube - RTMPS**
1. Paste the Stream key from YouTube into the **Stream Key** field in OBS
1. Click **Apply**, then **OK**
1. Select **Start Streaming** in OBS
1. Switch over to YouTube and you will see you are now LIVE on YouTube!
1. To see your actual YouTube live stream video page, you'll need to select the SHARE icon at the top right
1. Click the 'Video link' and you will see and hear your YouTube live stream 
1. This URL is your live stream link and can be shared out to all your Social channels :)
1. To stop the live stream, select END STREAM on YouTube then Stop Streaming on OBS

'**Later date**' method:
1. Top left, choose the **Manage** icon
1. Select **SCHEDULE STREAM**, top right
1. Add Title, Description, Category, Thumbnail (1280x720), then **NEXT**
1. Live chat options, then **NEXT**
1. Private, Unlisted or Public (choose Public)
1. Schedule the Date and Time you want to go live, then **DONE**

 **When you are ready to start your live stream in the future:**
1. Under Stream Settings, keep the defaults
1. Beside **Stream key (paste in encoder)**, **COPY** the key so you can paste it into OBS
1. Open OBS / **Settings** / **Stream**
* In the **Service** drop-down menu, select **YouTube - RTMPS**
1. Paste the Stream key from YouTube into the **Stream Key** field in OBS
1. Click **Apply**, then **OK**
1. Select **Start Streaming** in OBS
1. Switch over to YouTube and you will see you are now LIVE on YouTube!
1. To see your actual YouTube live stream video page, you'll need to select the SHARE icon at the top right
1. Click the 'Video link' and you will see and hear your YouTube live stream 
1. This URL is your live stream link and can be shared out to all your Social channels :)
1. To stop the live stream, select **END STREAM** on YouTube then **Stop Streaming** on OBS

For bonus points, share your videos on social and make sure to tag us @AltspaceVR :)