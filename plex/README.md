# Plex Media Server

![ ](https://shadow.coffee/bucket/plex/plex-logo-flat.png)

> This guide details setup for a Plex Media Server. In the context of this guide, this will be used to host media that **you own**, rather than otherwise obtained media.  
> Legalities regarding licencing of media differ on a per country basis, please refer to the laws in your area.

## Intro

## Setup & Configuration

### Setup

My server is currently running on Ubuntu, and was installed using a binary. The downside to this method is that there is no ability to update the server from the console, all updates are manual.

In future, I will probably roll my server using Docker, or use the snap version of Plex Media Server.  
For Windows/macOS, I would use the .exe/.dmg version.

#### Hardware

My server is running on an Intel NUC (tall boi) with:

- i5-10210U Frost Canyon
- 16GB Corsair Vengeance DDR4 SO-DIMM
- 250GB WD Blue M2 SSD (Operating System)
- 1TB Samsung 860 EVO (Server Operations)
- 4TB WD Red HDD (External to NUC - Media Drive)

### Configuration

#### General

![Plex General Settings Panel](https://shadow.coffee/bucket/plex/plex-general.png)

#### Remote Access

![Plex Remote Access Settings Panel](https://shadow.coffee/bucket/plex/plex-remote-access.png)

#### Agents

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-1.png)

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-2.png)

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-3.png)

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-4.png)

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-5.png)

![Plex Agents Settings Panel](https://shadow.coffee/bucket/plex/plex-agents-6.png)

#### Library

![Plex Library Settings Panel](https://shadow.coffee/bucket/plex/plex-library.png)

#### Plugins

![Plex Plugins Settings Panel](https://shadow.coffee/bucket/plex/plex-plugins.png)

#### Network

![Plex Network Settings Panel](https://shadow.coffee/bucket/plex/plex-network.png)

#### Transcoder

![Plex Transcoder Settings Panel](https://shadow.coffee/bucket/plex/plex-transcoder.png)

#### Languages

![Plex Languages Settings Panel](https://shadow.coffee/bucket/plex/plex-languages.png)

#### DLNA

![Plex DLNA Settings Panel](https://shadow.coffee/bucket/plex/plex-dlna.png)

#### Scheduled Tasks

![Plex Scheduled Tasks Settings Panel](https://shadow.coffee/bucket/plex/plex-scheduled-tasks.png)

#### Extras

![Plex Extras Settings Panel](https://shadow.coffee/bucket/plex/plex-extras.png)

## Importing Media

> In this section, we will be **backing up** a legally purchased disc, and importing it into Plex using MakeMKV.

**Note**: DVD's come out in a great size, usually ~700MB. Blu-ray's are considerably larger (~40GB), and will likely need re-encoding into a smaller filesize for ease of use/storage.

## Media Customisation

### Collections

### Posters

![The best trilogy, with sweet posters!](https://shadow.coffee/bucket/plex/plex-posters.png)

There are a couple of places to get great collections of posters, for that ultimate aesthetic library.

- [theposterdb](https://theposterdb.com/)
- [/r/PlexPosters](https://reddit.com/r/plexposters)

### Prerolls

![A Netflix Originals style preroll](https://shadow.coffee/bucket/plex/plex-preroll-small.gif)

It's possible to set custom intros which will play before a movie. Prerolls are set in the *Extras settings panel*. Setting a directory will force Plex to randomly choose a preroll video from the directory, else setting semi-colon separated paths will use those specific files.

A great source for video prerolls is [prerolls.video](https://prerolls.video/plex/) - it's where the one above is from!

## Playback

## Links

- [Plex](https://plex.tv)
- [/r/PlexPosters](https://reddit.com/r/plexposters)
- [theposterdb](https://theposterdb.com/)
- [MakeMKV](https://makemkv.com)
