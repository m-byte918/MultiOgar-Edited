# MultiOgar - Edited
Ogar game server with fast and smooth vanilla physics and multi-protocol support.

Since Barbosik stopped working on the original MultiOgar, I decided to continue it on this fork =D

Current version: **1.6.1**

## Project Info
![Language](https://img.shields.io/badge/language-node.js-yellow.svg)
[![License](https://img.shields.io/badge/license-APACHE2-blue.svg)](https://github.com/Barbosik/OgarMulti/blob/master/LICENSE.md)

MultiOgar code based on Ogar code that I heavily modified, and will continue to update.
Almost all physics and protocol code were rewritten and optimized.
The [OgarProject](https://ogarproject.com) owns Ogar, and I do not claim it as mine!
Original Ogar found [here](https://github.com/OgarProject/Ogar)

The goal is to make good and smooth physics and cleanup the code.

## Ogar Server Tracker

You can found active Ogar servers on http://ogar-tracker.tk
It updates server information in realtime with no need to refresh the page.

If you want to include your server in the list. Just install the latest version of MultiOgar server and enable server tracking with `serverTracker = 1` in gameserver.ini

If you have another tracker where you want to publish your server at, see [this function](https://github.com/Megabyte918/MultiOgar-Edited/blob/master/src/GameServer.js#L1244) for adding the functionality.

## Screenshot

MultiOgar console:

![Screenshot](http://i.imgur.com/PtKj86E.png)

Version 1.5.1 bottleneck test with bots:
* 1000 bots, 1 player, 50 viruses, 1000 pellets, map 14142x14142
* Update time: 34 milliseconds / 40 maximum
* CPU load: 84% (single core)
* Memory usage: 62 MB

![Screenshot](http://i.imgur.com/A2dBZPH.jpg)

*PC: Intel i5-6600k @ 4 x 3.5GHz, AMD Radeon R9 380 Series Crimson Edition, 16 GB DDR4 RAM, Gigabyte Z170-Gaming K3*

## Install

#### Windows:
* Download and install node.js: https://nodejs.org/en/download/ (64-bit recommended)
* Download MultiOgar code: https://github.com/Megabyte918/MultiOgar-Edited/archive/master.zip
* Unzip MultiOgar code into some folder.

*Method 1:*

* Run the win-Install_Dep.bat file. (It'll close automatically once it's done)
* Run run\win-Start.bat

*Method 2:*

Start command line and execute from MultiOgar folder.

```batch
npm install
```

and run the server:

```batch
cd src
node index.js
```

#### Linux:
```bash
# First update your packages:
sudo apt-get update

# Install git:
sudo apt-get install git

# Install node.js:
sudo apt-get install nodejs-legacy npm

# Clone MultiOgar:
git clone git://github.com/Megabyte918/MultiOgar-Edited.git

# Install dependencies:
cd MultiOgar
npm install

# Run the server:
```

*Method 1:*

```bash
cd run
sh lin-Start.sh
```

*Method 2:*

```bash
cd src
sudo node index.js
```

## Clients

This lists Ogar clients and server trackers that I found on internet.

###Ogar server trackers

URL | Description
--- | ---
http://ogar-tracker.tk | Ogar tracker
http://ogar.mivabe.nl/master | MivaBe, tracks a lot of servers
http://c0nsume.me/tracker.php | c0nsume.me server tracker

Now you can allow MultiOgar to be listed on a server tracker.
Just set `serverTracker = 1` in the gameserver.ini, and your server will appear
on these pages: http://ogar.mivabe.nl/master , http://c0nsume.me/tracker.php
If you don't want to include your server to tracker list,
just set `serverTracker = 0` and the server will not ping the server tracker.

###Ogar clients
URL | Protocol | Description
--- | --- | ---
http://agar.io/?ip=127.0.0.1:443 | 11 | Vanilla with no chat
http://ogar.mivabe.nl/?ip=127.0.0.1:443 | early 5 | MivaBe, pretty smooth, anime-like cells and overlay
http://old.ogarul.io/?ip=127.0.0.1:443 | 4 | OgarUL, old vanilla style with chat
http://c0nsume.me/private4.php?ip=127.0.0.1:443 | 5 | Vanilla style with chat
http://astr.io/?ip=127.0.0.1:443 | 6 | Extension like with chat
http://alis.io/?ip=127.0.0.1:443 | 5 | Extension like
