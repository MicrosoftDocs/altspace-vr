---
title: Uploading custom Skyboxes
description: 
author: hferrone
ms.author: v-hferrone
ms.date: 02/10/2021
ms.topic: article
ms.localizationpriority: high
keywords: 
---

# Uploading custom Skyboxes

A Skybox is a way to create a "background" for your World that makes the experience more immersive. There are different kind of Skyboxes but we currently support "equirectangular". Here's an example taken with a 360 camera (more example [here](http://moments.mankindforward.com/)): 

![]()

You can also use the [Unity Uploader](world-building-toolkit-getting-started.md) but this approach is simpler.

1. Navigate to [Worlds > Skyboxes](https://account.altvr.com/skyboxes) and press the "Create" button on the right

![]()

2. Fill in a name and specify your 360 image (It doesn't have to be a photo. There are programs that can allow you to draw your own or you can search for some online). Then, click "Create". 

![]()

4. Enter your World and open the World Editor. Under Skyboxes, click your new Skybox. In a few seconds the sky will literally change. Others in your World will also see the sky change. To switch back, click the "default" skybox in that same list. 

## Troubleshooting

* There's a seam or line in the sky :-(. 
    * It's a bug that we'll fix soon
* Upload failed
    * try uploading just the 360 image on its own
    * try with another, smaller file as a test
* I can't find a 360 photo
    * Flickr is a good source (change the filters to find creative commons ones)
    * Take your own! We've had success with Ricoh's cameras. 
* The sky looks grainy or blocky
    * You may need to find a higher-resolution image. Typically around 2-5MB and ~5000px x 2000px
* It hurt my World's framerate!
    * The image is probably too large. Some generated skyboxes can be 8k. They usually come with mobile-friendly 2k versions--use that.
* Help me with the ambient audio
    * Use free software like Audacity to lower the volume or create your own loops. Remember that the audio will be repeated and playing in people's ears so keep it very low and not annoying
    * [Free Sound](https://freesound.org/) is a good source of royalty-free sounds
