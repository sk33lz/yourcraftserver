---
title: "YourCraft is Now Running Spigot"
date:   2012-12-30 18:04:35 -0500
categories:
  - news
tags:
  - "server news"
  - Spigot
---

Let's face it, a vanilla Minecraft server, in it's current form, is a bit slow, memory hungry, and not very feature rich in terms of configuration. As a Minecraft server operator, I need to be able to provide a fast, memory efficient server with lots of features for both me to admin the server, and my users to have fun. I have been using Craftbukkit for almost a year now to provide that sort of funcationality for the Minecraft servers I manage. As I became more knowledeable about Craftbukkit, I soon realized that it was not the only server wrapper for running Bukkit mods, or alone in it's ability to provide different functionality to a Minecraft server.

As the owner of YourCraft Multiverse, I have always been looking for new ways to speed up my Minecraft server and use less resources. Currently YourCraft Multiverse is running the 2GB of RAM Skeleton plan from BeastNode, which is a fraction of the 12GB of RAM being used on our private THOR Multiverse server, but then again we aren't running SSD hard drives on THOR Multiverse either. Overall, the performance from the BeastNode Skeleton server has been outstanding! Since it's over $25/month, I'm trying to get everything I can out of that plan, and happened to stumble upon a high performance fork of CraftBukkit known as Spigot. It was formerly called Craftbukkit++, but has since evolved into what is now being called Spigot, which has it's own community over at Spigotmc.org.

Spigot has many features that come and go as needed, based on the specific Craftbukkit version, since it is a performance fork of Craftbukkit. If you aren't sure what a fork it is, bascially it's a copy of a piece of software, which may or may not have additional code added to change it's functionality. In this case, Spigot adds additional code to Craftbukkit's code to enable many performance enhancements and tweaks to allow server admins to reduce the amount of overall resources a Minecraft server uses. Here are a list of the features that aren't going anywhere.

## Spigot Server Changes

- Huge TPS increases
- Optimized growth, decay and chunk ticking
- Optimized, auto merging itemstacks and experience orbs.
- Chunk garbage collector, prevents chunk leaks
- Optimized tick loop -> perfect for GSPs, reduces idle load to nearly 0%
- Prevents insane CPU load caused by maps in item frames
- Disabling of random light updates
- Spamguard exceptions
- Customizable whitelist deny message
- Configuration options for command logging
- Configurable message on server stop
- Restart command
- Automatically stays up to date with latest CraftBukkit changes

I hope you enjoy the performance gains that Spigot enables for everyone, as it has shown great promise for extending the life of our server plan by allowing us to do more with less.
