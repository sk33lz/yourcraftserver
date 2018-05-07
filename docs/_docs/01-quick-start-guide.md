---
title: "Quick-Start Guide"
permalink: /docs/quick-start-guide/
excerpt: "How to quickly install and setup a Minecraft Server."
last_modified_at: 2018-03-20T15:58:49-04:00
toc: true
---

YourCraftServer has been building and running Java Minecraft servers since mid-beta. We have also been building and running other game servers since Counter-strike Beta 1.0 in 1999. We have gone through many different types of game server setups, game server wrappers, and game server hosting companies over the years for Minecraft. We hope with our years of experience running Minecraft server and game servers in general we can provide some helpful documentation and 

This Quick-Start Guide was designed to help new Java Minecraft server owners, or those looking to start a Java Minecraft server in an easy to understand guide.

**Notice:** This guide is specifically written for Java Minecraft Server. We may write other quick-start guides in the future, but this is the version we know best. This guide should be helpful for server owners using other versions of Minecraft, but some details will differ based on the version you are using. Thanks!
{: .notice--notice}

## Choosing a Server Location

Choosing a location for your Minecraft server is probably one of the most important decisions you will make, especially if you are trying to build a large community. We will go over some various ways to host a Minecraft server, including paid hosting solutions, and self-hosted solutions.

### Minecraft Hosting Companies

There are many Minecaft server hosting companies out there, and each have their pros and cons. We are not going to compare all the hosting companies out there in this guide, as that will fill up the whole guide. What we will do is provide you with a list of important features you should look for when purchasing Minecraft server hosting.

#### Important Features for Hosting Companies

Below are some key features you should look for in any Minecraft server hosting company you are looking to use.

##### SSD Storage

Make sure the hosting company uses Solid State Drives. Minecraft reads and writes often to disk and using a older spindle based hard drives is a huge impact on server performance. Nobody wants to play on a slow server. Some companies are even starting to officer NVMe SSD storage, which is an even faster SSD technology. Instead of transferring data at hundreds of MB/s, NVMe SSDs can transfer data at thousands of MB/s.

##### DDOS Protection

Minecraft servers are constantly a target of Denial of Service attacks and Distributed Denial of Service attacks. You will want to make sure you have DDOS Protection available if you are going to have a Minecraft server where you or an admin might ban someone for not following the rules. This is the sort of time that a malicious player would attack the server with a DDOS attack. During the attack server performance will be degraded, or it might appear offline completely.

##### Backups

Make sure the hosting company has some sort of backup system available. Backups are key for any large server community, as it will allow you to revert to a working state of your server if something goes wrong with it. Your players won't stick around if you lose their items or XP because of a failure of some sort on the host's servers.

##### Voice Chat

Voice Chat is an important feature for Minecraft servers, as it allows your community to communicate easier. Minecraft itself does not include any sort of voice chat out of the box. Many hosting companies include some sort of voice chat server for free on their hosting, so it's easier to find than some other features. You may need to pay for a voice chat server depending on how big your community is. You can also run your own voice chat server for free with something like Teamspeak, which we use for YourCraftServer.  

### VPS Minecraft Hosting

Some Minecraft server owners want to have more control over their server than what most Minecraft Hosting Companies allow. There are some that allow full SSH access to the server, but not many. Typically you would need to rent a fully dedicated box from a hosting company for this sort of access, which can be quite expensive. Hosting Minecraft on a VPS requires a bit more work, but you ultimately have the same control as a dedicated server, with comparable resources and cost to Managed Minecraft Hosting solutions that Minecraft Hosting Companies provide.

### Home Minecraft Server Hosting

Sometimes players are looking to try hosting their own Minecraft server, or want to host a small server for friends on their home network to play together on the LAN. Casual players who want to just play with a few friends or test out running their own server typically don't want to pay for Minecraft Sever Hosting or VPS hosting. In this guide we will show you a few ways how to run a Minecraft server at home on a dedicated server computer, or on your local machine along side your Minecraft client.

**WARNING:** Make sure if you are going to host a Minecraft server on your home network that you are only hosting for a few friends. Minecraft can use a ton of bandwidth on high population servers, and most residential ISPs do not want you running servers on their networks. If you start getting warnings from your ISP, then you should probably start looking for a hosted solution on either VPS or a Minecraft Hosting company. 
{: .notice--warning}

---

## Choosing the Minecraft Server Version

Minecraft Server comes in a few different flavors depending if you want to run Minecraft Server Plugins, or just run a Vanilla Minecraft server with no plugins. This section will outline each type of server flavor available, so you can choose which server version you want to run. 

**Notice:** Each server version requires that you have Java installed, so make sure to install that prior to getting started. 
{: .notice--notice}

### Install Java First

Minecraft and Minecraft Server require Java to be installed to run. Depending on your operating system, installing Java will differ.

#### Install Oracle Java on Windows, Mac, and Linux

Install Java SE Development Kit 8 from the following URL for your OS:

http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

Install Java SE JRE 8 from the following URL for your OS:

http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html

#### Install OpenJDK8 Java on Linux

Those more comfortable using Linux command line can use the following commands based on your operating system version.

##### Install OpenJDK8 on Ubuntu 16.04 (Xenial Xerus) & Debian 9 (Stretch)

```
sudo apt update && sudo apt upgrade
sudo apt install openjdk-8-jre-headless
```

##### Ubuntu OpenJDK8 on Ubuntu 14.04 (Trusty Tahr) & Debian 8 (Jessie)

```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install openjdk-8-jre-headless
```

### Vanilla Minecraft Server

Minecraft Server has a Vanilla version, which is just a `server.jar` file which can be loaded on Windows, Mac, or Linux machines. The Vanilla version of Minecraft Server is easiest to setup, but does not allow plugins.

#### Installing a Vanilla Minecraft Server

Vanilla Minecraft Server can be downloaded from at the following URLs:

https://minecraft.net/en-us/download/server

https://launcher.mojang.com/mc/game/1.12.2/server/886945bfb2b978778c3a0288fd7fab09d315b25f/server.jar

Using command line? Use `wget`:

`wget https://s3.amazonaws.com/Minecraft.Download/versions/1.12/minecraft_server.1.12.jar`

Once downloaded, you should copy the `server.jar` file to a directory that you control to use as your Minecraft Server root directory. Depending on your operating system, this directory will vary. It is also recommended that you rename the `server.jar` file to add the current version that Minecraft Server it is. This helps keep track of when you want to update the server.

Some examples:

Windows: `C:\minecraft-server\minecraft_server.1.12.jar`
Mac: `/Users/username/minecraft-server/minecraft_server.1.12.jar`
Linux: `/home/username/minecraft-server/minecraft_server.1.12.jar`

#### Running a Vanilla Minecraft Server

Once you have the `server.jar` installed and/or renamed to what you want, you can start up your server. The command is basically the same on all operating systems, as long as java is in  your path.

`java -Xmx1024M -Xms1024M -jar minecraft_server.1.12.2.jar nogui`

You can also remove the `nogui` flag to start the server with the included GUI. 

**WARNING:** Make sure java executable is in your path, or you will have to provide the full path to the java executable in your command.
{: .notice--warning}

### Spigot Minecraft Server

[Spigot](https://www.spigotmc.org/wiki/about-spigot/) is a high performance fork of Craftbukkit. Spigot it is mostly based on the original Craftbukkit project source code. Spigot mainly adds some enhancements to improve the performance of the server, especially in high traffic servers. The Spigot team has actually made some enhancements that have been picked up and added into Minecraft Server itself. Without Spigot the Minecraft Server modding community would have died with a DMCA takedown request. Thanks for your hard work and dedication to the community guys!

[Spigot](https://www.spigotmc.org/wiki/about-spigot/) is a modified Minecraft server based on Craftbukkit, which was for a long time used to run Minecraft with Plugins or Mods. Craftbukkit ran into some licensing issues and received a DMCA takedown request, so it is no longer available as a downloadable package. Because of the licensing issues that Craftbukkit has, Spigot would have the same issues if the Spigot executable was made available online for download.

#### BuildTools

[BuildTools](https://www.spigotmc.org/wiki/buildtools/) was created by the Spigot team to get around this licensing problem. BuildTools builds not only the Spigot executable, but also the classic Craftbukkit and Bukkit API executables from publicly available source code without breaking any copyright laws. BuildTools allows server owners to continue to use Craftbukkit or Bukkit API for their servers, as well as build the Spigot executable.

**Notice:** More information on BuildTools can be found on the [Official BuildTools Wiki](https://www.spigotmc.org/wiki/buildtools/). 
{: .notice--notice}

#### Installing BuildTools

The Spigot team created BuildTools to allows servers owners to build all the required files for Spigot, Craftbukkit, and the Bukkit API.

The `BuildTools.jar` is available from the Spigot Jenkins server found at the following URL:

https://hub.spigotmc.org/jenkins/job/BuildTools/

The latest successful build can be downloaded from the following URL directly:

https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar

Those using command line can use the following command to download the latest BuildTools.jar file:

`wget https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar`

I would copy this file to a location that you have full access to and put it in a specific directory to run out of.

**Notice:** Make sure to have git installed. 
{: .notice--notice}

#### Installing Spigot with BuildTools

The Spigot .jar file, along with the Craftbukkit and Bukkit API .jar files will be generated by the BuildTools.jar file.

Build the latest version of Spigot, Craftbukkit, and Bukkit API with the following command:

`java -jar BuildTools.jar`

Specific versions of Spigot and Craftbukkit can be installed using the following command:

`java -jar BuildTools.jar --rev 1.12.2`

**Notice:** Replace --rev 1.12.2 with the version you want to build for your server. 
{: .notice--notice}

#### Running a Spigot Minecraft Server

Once the Spigot .jar file has been built by BuildTools you can start up the server with the following command:

`java -Xms1G -Xmx1G -XX:+UseConcMarkSweepGC -jar spigot.jar`
