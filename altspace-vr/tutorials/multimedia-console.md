---
title: Using the multimedia console
description: Learn how to start configuring, publishing, and controling the multimedia console in your AltspaceVR experiences.
ms.date: 03/11/2021
ms.topic: article
keywords: console, multimedia
---

# Using the multimedia console

The Multimedia Console is a tool that enables media sharing in events and worlds. You can use it to share things like images, presentation slides, livestreams, videos, playlists, and more. Below is a step-by-step instruction on how to use the Multimedia Console **v0.5.0+**. 

## Getting started

Getting started with the Multimedia Console is a two part process.  First there's the web portal that you'll use to generate and publish a configuration for the Multimedia Console session you place in your environment.  Second is the placement of the actual Multimedia Console app in your environment and setting the configuration code it should use.

### Configuring the Multimedia console with the web portal

1. First, you'll need to make sure your content is hosted online because you'll need a URL. (You can upload photos to altvr.com, host a video .mp4 file online or use a Dlive live stream link: https://dlive.tv/yourlivestream) 
2. Navigate to the web portal for the Multimedia Console at [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)
3. From the web portal, you can generate and publish a configuration for the Multimedia Console.  (See below for details about the various properties).
4. Once you've entered the media into the media list and have configured the general settings, select the publish button in the top-right part of the app.
5. Once the publish has completed, a dialog will pop up with a two word code for you to enter in to the Multimedia Console you placed.
  
### Placing the Multimedia console in your environment

1. Select on **World Editor > Editor Panel > SDK Apps > Multimedia Console**. (Don't go to **World Editor > Basics > SDK App**--that's for unregistered apps.)  
2. Position the Multimedia Console to best suite your space and audience.
3. Get out of Edit Mode by clicking the orange Edit Mode button.
4. You'll be prompted **Are you the media player owner?** If you're the person who should be the official owner of this Multimedia Console session, confirm and continue. (Other permissioned roles are available as well. See below for a detailed list.)
5. Select Yes to confirm that you are the primary host.  
6. A dialog should pop up that asks you to enter a code from the web portal or valid JSON.  Enter the two word code from the web portal including the dash and hit OK. (JSON is an advanced configuration described below)
7. The Multimedia Console should load after a few seconds with the configuration you built in the web portal.

### Controlling the Multimedia console

1. After you input your code and complete the configuration process, you'll see control buttons appear below a media display. 
    * **Play** starts the media viewer (or restarts at current entry, if previously stopped) 
    * **Stop** stops the media viewer, and hides current media.  
    * **Next/Prev** skips to next or previous media 
    * **x/x** shows the current index into the media list, and allows you to jump to any point in the list
    * **Config** allows reentering a new code from the web portal to set a new configuration in the console. 

Now you're set to begin sharing via the Multimedia Console!  
 
## Working with the web portal

The web portal is a web app that enables configuring the various features of the Multimedia Console.  These features fall in to two categories; general media console settings, and the media play list.

### Multimedia console general settings

**Playback Settings**

General playback settings for the media list

* **Loop Media List**- Determines whether the media list should loop around once you reach the end of the list.
* **Start Method** - Selects the method by which the multimedia console should start.
    * Manual - Waits for the play button to be pressed before starting the media
    * Auto Start from Beginning - Auto start the media list from the beginning of the list
    * Auto Start Random - Auto starts the media from a random starting point in the list

**Roles**

Role assignments for controlling and configuring the Multimedia Console.    These roles are broken down in to the following set:

* **Owner Only** - The user that is the owner of the Multimedia Console Session
* **Elevated Users** - Users that have moderator, host, or presenter roles in the space that the Multimedia Console is configured in originally
* **All Users** - All users

These roles stack in the sense that all roles above the one chosen in this list will also be granted permission to use that feature.  Example: **Elevated Users** includes the **Owner** even if they aren't a moderator, host, or presenter** in AltspaceVR. Features that are controlled by role assignments are as follows

* **Can control media player** - Determines what roles can control the media playback buttons for the Multimedia Console
* **Can configure the media player** - Determines what roles can configure the Multimedia Console by being granted access to the **Config** button

### Adding photos and videos to the media list

Media is the heart of the Multimedia Console.  Images and video links are supported as media types within the Multimedia Console.  To add new media, select either the **Add Image** or **Add Video** icons to have a dialog pop up to enter the media information and settings.  Below is the breakdown of the media types and associated settings

**Image**

Images should be a standard image type such as jpeg, png, and son on. They need to be hosted somewhere with a public link.

* **Name** - (Required) Name that you wish to identify the image with.
* **Image URL** - (Required) The public url of the image
* **Skip After** - The number of seconds that the image should be skipped after

**Video**

Videos can be hosted videos or live streams through Twitch and DLive.  (Other support may function with extra work to get the proper stream url, but aren't fully supported within the Multimedia Console)

* **Name** - (Required) Name that you wish to identify the video with.
* **Video URL** - (Required) The public url that the video is hosted at or the live stream is served from.
* **Skip After** - The number of seconds that the video should be skipped after
* [!NOTE]
> REQUIRED: Put in the time that matches the length of the video to enable videos to properly forward. For example, if your video is 5 minutes long put 300 seconds, otherwise your video won't skip to the next piece of content.
* **Volume** - The volume of the video from 0 (min) - 1 (max) values.
* **Start Time** - The number of seconds from the beginning of the video start from.
* **Roll Off Start Distance** - The distance in meters in world that the volume begins to fall off at as you move away from the Multimedia Console
* **End of Video Action** - The action to take once the end of the video is reached.
    * Stop - The media list stops after the video has ended
    * Loop - The video will loop until manually skipped
    * Play Next - The next media in the media list will be started after the current video ends.

## Working with JSON directly (advanced/optional)

The Multimedia Console supports entering JSON directly in to the prompt of the console in AltspaceVR.  JSON is the internal mechanism with which we enable media player configurations. Exposing the ability to set JSON directly is something that allows for more advanced users to build their own workflows that suites their needs and familiarity with JSON.  The following is a brief description of the JSON structure and the schema by which the JSON is validated. For more detailed descriptions of the properties below, see the above sections that talk about configuring the Multimedia Console.  This section is focused primarily on the schema examples and structuring for the JSON data.

### Global media settings

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### Media list

The media list is a property set at the root of the JSON structure like the Roles and Playback Settings.  It's a simple array that can contain one of the following media configuration structures. (See property descriptions above for details on what each does.)

**Image example**

*Required fields: "name" and "imageUrl"*

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

**Video example**

*Required fields: "name" and "videoUrl"*

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### Example JSON

```json
{
  "loopMediaList": false,
  "startMethod": "autostart-beginning",
  "controlMediaPlayer": "everyone",
  "configureMediaPlayer": "elevated",
  "mediaList": [
    {
      "videoUrl": "https://www.twitch.tv/ninja",
      "volume": 0.2,
      "startTime": 0,
      "endOfVideoAction": "play-next"
    },
    {
      "imageUrl": "http://www.hypergridbusiness.com/wp-content/uploads/2016/09/AltspaceVR-highrise.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://d1qb2nb5cznatu.cloudfront.net/startups/i/333629-6ffd7199b9bcf34d8957e8e09d974a38-medium_jpg.jpg?buster=1423092095",
      "skipAfter": 5
    },
    {
      "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://altvr-wpengine.netdna-ssl.com/wp-content/uploads/2019/05/Educators-in-VR-Social-VR-AltspaceVR.png",
      "skipAfter": 10
    },
    {
      "videoUrl": "https://www.twitch.tv/shroud",
      "volume": 1,
      "startTime": 0,
      "endOfVideoAction": "stop"
    }
  ]
}
```

### Schema

```json
{
  "$schema": "https://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": [
    "mediaList"
  ],
  "properties": {
    "loopMediaList": {
      "type": "boolean",
      "description": "Whether to loop through the media list when reaching the beginning or end of the list."
    },
    "controlMediaPlayer": {
      "type": "string",
      "enum": [
        "everyone",
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are able to control the media player. (Owner can always control player)"
    },
    "configureMediaPlayer": {
      "type": "string",
      "enum": [
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are allowed to configure the media play list.  Note: This role needs to be able to control the media player in order to configure it. (Owner can always configure media)"
    },
    "startMethod": {
      "type": "string",
      "enum": [
        "manual",
        "autostart-beginning",
        "autostart-random"
      ],
      "default": "manual",
      "description": "The method by which the media player should start"
    },
    "mediaList": {
      "description": "A list of images or videos to configure the media player to operate on.",
      "type": "array",
      "items": {
        "oneOf": [
          {
            "title": "Image",
            "type": "object",
            "description": "Configuration for an image media.",
            "properties": {
              "imageUrl": {
                "type": "string",
                "description": "The url for the image to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              }
            },
            "required": [
              "imageUrl"
            ]
          },
          {
            "title": "Video",
            "type": "object",
            "description": "Configuration for a video media.",
            "properties": {
              "videoUrl": {
                "type": "string",
                "description": "The url of the video to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              },
              "volume": {
                "type": "number",
                "minimum": 0,
                "maximum": 1,
                "default": null,
                "description": "The volume to play the video at. (Minimum 0, maximum 1)"
              },
              "startTime": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The time in seconds from the start of the video to begin playing the video at. (Minimum of 0)"
              },
              "rolloffStartDistance": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The distance in meters away from the media player that the volume will begin to fall off. (Minimum 0)"
              },
              "endOfVideoAction": {
                "type": "string",
                "enum": [
                  "stop",
                  "loop",
                  "play-next"
                ],
                "default": null,
                "description": "The type of action to take at the end of the video."
              }
            },
            "required": [
              "videoUrl"
            ]
          }
        ]
      }
    }
  }
}
```

> [!NOTE]
> Up to date with Multimedia Console v0.5.0
