---
title: AltspaceVR for Business frequently asked questions
description: Troubleshooting and support for AltspaceVR for Business.
ms.date: 8/27/2021
author: qianw211    
ms.author: v-qianwen
ms.topic: article
keywords: vr, business, troubleshooting, support
---

# AltspaceVR for Business frequently asked questions

## Frequently asked questions

### What is Mesh? 

Microsoft Mesh is a new platform built on Microsoft Azure.  Microsoft Mesh allows you to build collaborative mixed reality experiences across platforms and devices. Using Mesh, you can build immersive 3D and multi-user experiences, where people come together virtually to create and collaborate on 3D content.  Customers can use Mesh to enhance virtual meetings, conduct virtual design sessions, assist remotely better, learn together virtually, host virtual social gatherings and meet-ups. Learn more [here](https://aka.ms/meshdocs).

### Who should use AltspaceVR for Business? 

Enterprise companies who are looking for a secure way to collaborate with presence. The platform offers the ability to provide an organizational view to your employees so that they only see and interact with the worlds and events specific to your organization. 

### Which platforms and devices does AltspaceVR for Business support?

AltspaceVR for Business is available on Windows Mixed Reality devices, HTC Vive, Oculus Rift/Rift-S, Oculus Quest/Quest 2, and on PC in 2D mode.

### What are the system requirements?  

See [minimum system requirements](../getting-started/system-requirements).

### Where can I find AltspaceVR Terms of Service? 

See https://altvr.com/terms-of-service/.

### Where can I find AltspaceVR Privacy Policy?

See [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).

### What are the advantages to having meeting/events in VR? 

Virtual reality allows you to engage with your team members with more presence, making collaboration and socialization easier using many features including spatial audio. There is no travel, which saves time, money, carbon footprints.

### How many people can attend a large scale event?  

Events can hold up to 1,000+ users in any given event using our [Front Row feature](/windows/mixed-reality/altspace-vr/faqs/scaling-audiences). 

### What are the mechanisms/protocols in place regarding IT security? 

We comply with Azure Cloud Security.  See [Azure Security Overview](https://azure.microsoft.com/en-us/overview/security).

### What type of encryption do you support?

We encrypt all End User Identifiable Information (EUII), End user Pseudonymized Information (EUPI), Organizational Identifiable Information (OII) and customer content using FIPS 140-2 (Azure Database for PostgreSQL) for Encryption at Rest and HTTPS (TLS 1.2) Encryption in Transit.

### Are the messages between users encrypted in transit?  

Messages are encrypted using HTTPS.

### Does Altspace store voice data?

No. Voice data is not stored.

### How do I manage employees within my organization?

Business users get access to an **Org View** dashboard where they can manage user accounts within their organization.

### What level of support do we get from Microsoft for creating and hosting events within our organization? 

We have created documentation to help you create and host events, however if additional support is needed, please contact us for support at https://help.altvr.com/hc/en-us/requests/new.

### Will you support a standalone build so we can easily distribute Altspace across our devices at scale? 

Yes, we have a standalone MSIX package available in the Microsoft Store that will work with your organization's device management solution like Intune, SCCM, etc.

### Can people outside of my organization attend events?  

Yes! You can allow guests to access your event by selecting <mark> this setting upon event creation (link?)</mark>. They'll gain access by using the event's custom entry code. 

### How much does it cost to use Altspace? 

A Mesh subscription will be required to use Altspace. The subscription will be free during the Public Preview and then roll into a paid subscription by the time the product hits General Availability. You can sign up for [Microsoft Mesh-enabled AltspaceVR](https://altvr.com/mesh/) and get notified as it becomes available.

### Can we rebrand the Altspace menus/UI with our company logo? 

Yes. Altspace for Business supports the ability to add a company logo and customized loading screen tips.

### Can we create our own 3D environments or objects with Unity? 

Yes! Users can upload Unity world builds and add custom kit objects. We also have our [Mixed Reality Extensions (MREs)](/windows/mixed-reality/altspace-vr/world-building/using-mixed-reality-extensions), this is our SDK to create games/apps that you can make using a Node.js server.

### Can I share my desktop or browser in Altspace? 

Yes! You can use our Mesh enabled Desktop sharing feature to share content in world from any Edge browser tab.

### How can I measure the success of my events? 

After you complete your event, you may view the event's user turnaround and other metrics on the event page at altvr.com.

### Can I make a custom avatar? 

Mesh supports an Avatar customization feature which will be available shortly.

### Will my company mix with non-organizational users? Will my company be able to see other Altspace public events/worlds? 

To protect your users and IP, your employees will have a gated experience which will not allow them to interact with regular users or events. They may however log into a personal account within the same app to access public user content. 

### Is there a web portal where the IT Admin can configure our Organization? 

Yes! Enteprise users are able to access an Organization Console where they can manage events, users and privacy.

### Does Altspace for Business work with Oculus for Business? 

Yes! Part of our enterprise package is the ability to launch our app on Oculus for Business headsets.  Instructions for signing up for Oculus for Business will be provided upon Altspace for Business signup.

### What customizations can we make to our own Altspace Org instance?

You can have your own logo, choose templates, and community.

### What customizations can we make in AltspaceVR? 

Branding (photos, 3d objects), create environments with Unity, interactable 3d objects (Kits), SDK (MRE) to create your own games/apps that work in AltspaceVR and beyond.

### Can I whiteboard? Take notes? Use stickynotes? (Do we want a 'no we don't have this' section?) 

Coming soon!

### Why do I need a Mesh subscription to use Altspace for Business?

Altspace for Business is a Mesh enabled app leveraging the Mesh Developer Platform which is built on the Azure infrastructure.

### Can you provide us with specific DNS names or an IP range to allow through our firewall to use Altspace? The ones you provide are too generic and our security team will not open ports without a destination address or range. 

Open UDP ports 5055 and 5056, and TCP ports 80 and 443". <mark> At the bottom: "More advanced support for network administrators or IT departments, including Azure IP Ranges and Service Tags, can be found in our download details."</mark>

### What will my employees see when they enter AltspaceVR?  

Your employees will be able to see the events and worlds you pre-select for them. 

### Can I use Microsoft 365 Groups to create different groups so only Marketing can access a Marketing specific meeting? 

Yes! Once you set up your M365 group, you can add the group ID to any event you wish them to have access to. 

### How many different AltspaceVR environments are there to choose from for event locations? 

There will be roughly 20 venues to choose from not including ones designed and built by your organization.

### Can you recommend to us a 3rd party to create custom environments?

Absolutely. Please write our helpdesk to receive recommendations. 

### Will you support other VR headsets like the Vive Focus, Pico or Valve Index in the future?

Though we don't have a public date around availability, we aim to deploy AltspaceVR on as many different platforms as possible. Altspace will run on many devices, but some issues may exist. 

### What if I already have a personal Altspace Microsoft Account? Can I continue to use both a work and personal account?

Yes. You can log in with your personal MSA to access our consumer version of Altspace, and then log in with your AAD account  to access  Altspace for Business which is specific to your organization. Note - the consumer and enterprise versions of Altspace are mutually exclusive so you will not be able to access consumer content when you are logged in with your AAD account. 

### Account issues

Link, unlink account. <mark>Is it the responsibility of users or IT admins?</mark>

## Support

Questions or feedback for the AltspaceVR team? 

> [!div class="nextstepaction"]
> [Click here to send a Support Request](https://help.altvr.com/hc/requests/new)