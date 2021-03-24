---
title: Granting world roles
description: Get step-by-step instructions for giving users roles in your AltspaceVR worlds.
ms.date: 03/11/2021
ms.topic: article
keywords: roles
---

# Granting world roles

Altspace has a Roles and Abilities system. Each person can have multiple roles and their roles can be different depending on where they are. Each role, in turn, gives you one or more abilities. For example, when you're in your own event, you automatically receive the **presenter** and **moderator** roles. With those two roles you can kick unruly users, be on stage, and maybe release the confetti. 

1. Edit your World and scroll down to the **In VR** section ([How to manage Worlds](managing-worlds.md))

![Changing roles in VR section of worlds](images/granting-roles.png)

2. Edit the **Roles** field if you want to grant specific roles to specific users just for this World. For example, if you want to give me **presenter** + **moderator** and give Calen **moderator**, you would add the following and select **Save**. The format is **{role},{username or email}** on each line. Username is case-insensitive. 

```
presenter,jimmy
moderator,jimmy
moderator,calen
```

3. If you select **Edit** again, you should see the following above the Roles field. That's how you know updated in the database.

```
Presenters: jimmy
Moderators: jimmy,calen
```

* In order for the change to take effect in Altspace, you should reset the world, forcing everyone to rejoin. There's a full list of roles below.

4. Edit the **Contextual Roles** field if you want to grant a role to every one that joins your World. For example, if you want to let people fly and use the megaphone so they can hear each other while far part, add the following:

```
pilot,megaphone_only
```

After you select **Update**, reset the World. This will only affect this World. If you want to grant roles to an entire Universe, edit the same fields on the Universe. 

## Roles 

* **Presenter** - abilities like being able to be on stage
* **Moderator** - abilities like **kick** to maintain decorum
* **Terraformer** - ability to use the World Editor
* **Pilot** - ability to toggle fly mode and spawn the 6DOF flight tool
* **Megaphone_only** - ability to speak into users' ears wherever they are in the World
* **Showcase_new_sdk** - ability to spawn MRE SDK apps

## Troubleshooting

**Can I delete roles?**
Not from the form right now so file a Support request at help.altvr.com and we'll take care of it for you

**Are roles copied when a World is importing from another?**
No, roles aren't copied