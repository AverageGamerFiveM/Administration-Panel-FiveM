<p align="center">
	<h1 align="center">
		Administration Panel for FiveM
	</h1>
	<p align="center">
		<img width="420" height="237" src="https://i.imgur.com/acV0dfO.png">
	</p>
	<h4 align="center">
		txAdmin FiveM Forum Post: &nbsp; <a href="https://forum.fivem.net/t/530475"><img src="https://img.shields.io/badge/dynamic/json.svg?color=green&label=txAdmin&query=views&suffix=%20views&url=https%3A%2F%2Fforum.fivem.net%2Ft%2F530475.json"></img></a>  <br/>
		txAdmin Discord: &nbsp; <a href="https://discord.gg/f3TsfvD"><img src="https://discordapp.com/api/guilds/577993482761928734/widget.png?style=shield"></img></a>
	</h4>
	<p align="center">
		<b>Administration Panel</b> is a <b>full featured</b> web panel to Manage & Monitor your FiveM Server remotely.
	</p>
</p>

<br/>



## Features
- Start/Stop/Restart your server instance or resources
- Access control via multiple credentials and action logging
- Discord Integration:
	- Server status command (`/status`)
	- Custom static commands
	- Command spam prevention
- Monitor server’s CPU/RAM consumption
- Real-time playerlist with ping + steam-linked accounts (when available)
- OneSync Support (more than 32 slots server)
- Linux Support
- Live Console
- Auto Restart on failure detection or schedule
- Password brute-force protection
- FXServer process priority setter
- Hitch Detection
- New settings page
- Save console to file
- Restart warning announcements
- Admin Management system
- Permissions system ([more info](docs/permissions.md))
- (BETA) SSL Support ([more info](docs/ssl_support.md))
- Translation Support ([more info](docs/translation.md))
- (BETA) Server Activity Log (connections/disconnections, kills, chat and explosions)
- (BETA) Player Management System
	- (BETA) Online Players List
	- (BETA) Player Search
	- (BETA) Warnings List
	- (BETA) Kicks List
	- (BETA) Bans List
- FiveM's Server CFG editor


## Installing & Running

**Video Tutorial [ENGLISH]:** https://youtu.be/S0tBq7Q8YaQ  
**Video Tutorial [PT_BR]:** https://youtu.be/vcM75_E6wmU

**Requirements**:
- NodeJS v10 LTS (or v12)
- FXServer build 1543+ [(duh)](https://runtime.fivem.net/artifacts/fivem/)
- One TCP listen port opened for the web server (default is 40120)
- Git (only for installs and updates)

**1 -** In the terminal (cmd, bash, powershell & etc) execute the following commands:
```bash
# Download Administration Panel, Enter folder and Install dependencies
git clone https://github.com/AverageGamerFiveM/Administration-Panel-FiveM
cd AdminPanel
npm i

# Add admin
node src/scripts/admin-add.js

# Setup default server profile
node src/scripts/setup.js default

# Start default server
node src/index.js default
```

**2 -** Then open `http://public-ip:40120/` in your browser and login with the credentials created and go to the settings page to configure the remaining settings.   
**If on Windows, you can start the Administration Panel by executing `start.bat` in your server profile's folder (example `data/default/start.bat`).**  

> **Note:** You should run FXServer **through** the Administration Panel, and not in parallel (ie in another terminal).  

> **Note2:** To configure your Discord bot, follow these two guides:  [Setting up a bot application](https://discordjs.guide/preparations/setting-up-a-bot-application.html) and [Adding your bot to servers](https://discordjs.guide/preparations/adding-your-bot-to-servers.html).  

> **Note3:** Although **not recommended**, you can set FXServer processes priorities. To do so, change `fxRunner.setPriority` in the `config.json` to one of the following: LOW, BELOW_NORMAL, NORMAL, ABOVE_NORMAL, HIGH, HIGHEST.  

> **Note4:** To create more server profiles, execute `node src/scripts/setup.js <profile name>`. You can run multiple Administration Panel instances in the same installation folder. 

## Troubleshooting
### If you run into any problem, check our [Troubleshooting Guide](docs/troubleshooting.md).   
If you are having trouble starting the FXServer via the Administration Panel, run `node src/scripts/config-tester.js default` and see which test is failing.  

## Updating
To **UPDATE** the Administration Panel execute the following commands inside AdminPanel folder:
```bash
git pull
npm i
``` 
If you have any problems with `package-lock.json`, just delete it and try again.  
> **Note:** This will only work if you downloaded the Administration Panel using the `git clone` command.  


  
## TODO:
The next major things:
- [ ] N/A

Minor things:
- [ ] N/A

Ideas:
- [ ] N/A 

## License, Credits and Thanks
- This project is licensed under the MIT License.
- Favicons made by Freepik from [www.flaticon.com](www.flaticon.com) are licensed under [CC 3.0 BY](http://creativecommons.org/licenses/by/3.0/)
- Special thanks to everyone that contributed to this project.
- Also this Administration Panel was based of [txAdmin](https://github.com/tabarra/txAdmin) by [Tabarra](https://github.com/tabarra/)
