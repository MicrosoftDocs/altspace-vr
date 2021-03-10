---
title: Using a Mixed Reality Extension
description: 
author: hferrone
ms.author: v-hferrone
ms.date: 02/10/2021
ms.topic: article
ms.localizationpriority: high
keywords: 
---

# Using a Mixed Reality Extension

[Mixed Reality Extensions](https://developer.altvr.com/) (MREs) are apps you can use in your Worlds from [helmets](https://account.altvr.com/mres/1173667287173955931) to a working [Stargate](https://account.altvr.com/mres/1152987031857529562). This is how community members with programming experience can extend Altspace and one-way World Builders can make their Worlds more interactive. While MREs can be used by anyone in a World, only people in the World Building Program can browse and spawn MREs in their Worlds. 

1. Browse the MRE section of our [website](https://account.altvr.com/mres). By default you'll see your own MREs so select on "Altspace" to see official MREs and "Featured" to see MREs from the community. Get familiar with any MRE before you use it in your World. 
2. Navigate to the [Helmets](https://account.altvr.com/mres/1173667287173955931) MRE and select "Copy to Clipboard". 
3. Enter your World and open the World Editor to Basics > SDK App. Paste in the URL for Helmets into the Target URI field and select "Confirm". The MRE Object should appear and attempt to connect to the MRE that's running in the cloud. You should now see some helmets you can click on.
4. Move/rotate/scale the MRE just as you would any other World Object.

Congratulations! You're using MREs now--you're so cool!

## Troubleshooting

* **MRE is showing a frowning emoji** 
    * Verify that the URL is correct
    * Toggle "Is Playing" option on the Object and choose "confirm"
    * Try reentering
* **MRE is lagging**
    * Depending on where an MRE is hosted you may experience some network latency
* **Why do we have to paste URLs?**
    * In the future, you can manage and spawn MREs like you do Artifacts from Kits. Until then, we'll continue using URLs