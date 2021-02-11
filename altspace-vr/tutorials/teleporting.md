---
title: Using the teleporter
description: 
author: hferrone
ms.author: v-hferrone
ms.date: 02/10/2021
ms.topic: article
ms.localizationpriority: high
keywords: 
---

# Using the teleporter

Being able to travel from one Event to another or from one World to another is a great way for you, or the community in general, to explore what AltspaceVR has to offer.

## The short version:

![Teleporting steps from editor panel to setting a teleportation destination]()

## The slightly longer version:

You'll want to make sure you are in your Homespace, in an Event or World that you've created or have been given the Terraformer role in. If you are in 2D Mode and don't see the World Editor button toward the bottom right of your UI, right click the mouse button to toggle that on/off. If you still don't see the World Editor button you may be in someone else's space and you'll have to ask them to give you the Terraformer role.

It will also help to 1. create the Events (eg Event A and B) or Worlds first, then 2. go to where you want to spawn the Teleporter, so your Events / Worlds will populate in the Teleporter Destination panel and make it faster/easier for you to connect them.


Now move to the location where you'd like to spawn a Teleporter and click on World Editor / Editor Panel / Basics / Teleporter.

This will bring up the Teleporter Destination panel. You'll see 3 categories to choose from:

* **MY SPACES** - List of Worlds that you've created.
* **RECENT** - List of recent Events you've been to. Use this option if you want to travel to an Event, this is the only option that will take you to an Event, the other 2 only let you travel between Worlds. NOTE: See Advanced below if you are connecting Front Row Events that have Imported Worlds, you'll need to spawn/setup the Teleporters in the Imported World and not in the actual Event.
* **FEATURED** - List of Featured Worlds you can set the Teleporter to travel to.

Select the Event / World you'd like to use, this will spawn the Teleporter and also put a text Label of the Event / World name slightly behind. So you could click the Gear icon in Present Objects section to change the Label name.

You can either click on the Teleporter with your cursor (you'll be asked if it's OK to go there, in case it was a misclick) or move your avatar right into the Teleporter and, presto, you're travelling to your destination. Tell them we say hi!

## Advanced features

If you are creating a conference, summit or larger event using Front Row with a custom World (eg a Foundation World, Unity Uploader Space Template, Re-Import World) you'll need to setup the Teleporter in your Foundation World, and NOT in the actual Event. Make sure you are setting up the Teleporter to travel to the correct Event (must be from the Recent list) in your Foundation World, then Re-Import World in the Event to get the Teleporters to show up in all the Front Row event spaces.

## FAQs

**Error: 'Sorry, we'd like to, but we just can't let you in there'**

Event might have a Group attached to it, so only usernames in the Group can get into that Teleporter to get to that private Group Event.

**How many teleporters can I use in one space?**

Teleporters are using transparent textures with animated particle effects, so it's best to not have too many all in the same spot/overlapping as this might impact performance. Try not to have more than 4 in the same area or more than 10 if they are all spread out in your space.