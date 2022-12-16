# PotionGames

> A Minecraft minigames plugin for PaperMC servers!

PotionGames is a minigames plugin that works like SurvivalGames but with potions and effects!

## Functions

* Set up your own loot table for the normal chest type
* Set up your own potion effects for looting the normal chests
* Set up your own chest types
* Airdrops (Activate with redstone torch)
* Loot coins and glass bottles to use in the shop
* Setup 27 potions for the shop
* Setup 26 kits to give sale prices for certain potions from the shop
* Setup 27 lobbies with 26 arenas to vote for every round
* Setup teams with your own team size
* Use milk buckets to clear all of your potion effects
* Eat soups with one click to also heal some health
* Use stats with SQLite or MySQL
* Use the stats wall to show the best three players
* Use startOnJoin option to use this plugin with BungeeCord
* Use GUI or sign to join a lobby
* Deathmatch
* Rewards (Vault needed)
  * [Download the latest release here!](https://www.spigotmc.org/resources/vault.34315/)

## Installation

1. Download the plugin
  * [Download the latest release here!](https://github.com/andersspielen/PotionGamesIssues/releases/latest)
2. Put the .jar in your plugins folder
3. Download Multiverse-Core
  * [Download the latest release here!](https://www.spigotmc.org/resources/multiverse-core.390/)
4. Put the .jar in your plugins folder
5. Add `mv.bypass.gamemode.*: true` to your permissions.yml
6. Start your server
7. Import your worlds with `/mv import [worldname] NORMAL`
8. Change `lobbySystem` to `false` or `true`
9. Change the .yml files in the PotionGames folder like you want them
10. Restart your server to reload the changed plugin files

## Usage

### Setup

#### Use `/pg setup` to set up the plugin!

#### Multi-Lobby-System

1. You need to be op or have the permission `pg.setup`
2. Create lobby `/pg setlobby [lobbynumber]`
3. Create arena `/pg addarena [lobbynumber] [arenaname]`
4. Add arena spawns `/pg addspawn [lobbynumber] [arenaname]`
5. Add chests to your arena
6. Add deathmatch spawns `/pg adddeathmatch [lobbynumber] [arenaname]` (activateDeathmatch = true)

#### Single-Lobby-System

1. You need to be op or have the permission `pg.setup`
2. Create lobby `/pg setlobby`
3. Create arena `/pg addarena [arenaname]`
4. Add arena spawns `/pg addspawn [arenaname]`
5. Add chests to your arena
6. Add deathmatch spawns `/pg adddeathmatch [arenaname]` (activateDeathmatch = true)

#### Chest-Types

* End Portal Frame: Normal chest like in SurvivalGames (With different item probabilities)
  * food1 20%
  * food2 10%
  * armour1 15%
  * armour2 15%
  * armour3 7%
  * armour4 5%
  * armour5 3%
  * weapons1 20%
  * weapons2 5%
* Target: A special chest with Flame-Bow and Arrows
* Netherite Block: A special chest with Netherite Ingots
  * Smithing Table: Upgrade Diamond- to Netherite Items (Build a Beacon next to the Smithing Table to make it shown on
    the whole map)
* Composter: Shop with potions (Build a Beacon under the Composter to make it shown on the whole map)

#### Create Join and Stats Signs

* Join Sign
  * Place a Sign and look at it, then use the command for your Lobby-System type
* Stats Sign
  * Place a Sign and type in the second line `PotionGames` and in the third line `Stats`

#### Create Stats-Wall

1. Place 3 Player Heads on a block next to each other
2. Place 3 Signs at the front of the block
3. Now use the commands listed below to create a podium
4. Look at the head of the 1(2;3) player on the podium and do: `/pg headp1(2;3)`
5. Look at the sign of the 1(2;3) player on the podium and do: `/pg signp1(2;3)`

### Commands and Permissions

#### Multi-Lobby-System

* `/pg` or `/pg help` or `/pg commands` - Get list of commands + permissions - Permission: `none`
* `/pg setlobby [lobbynumber]` - Set lobby - Permission: `pg.setup`
* `/pg dellobby [lobbynumber]` - Remove lobby - Permission: `pg.setup`
* `/pg addarena [lobbynumber] [arenaname]` - Add an arena - Permission: `pg.setup`
* `/pg addspawn [lobbynumber] [arenaname]` - Add a spawn - Permission: `pg.setup`
* `/pg adddeathmatch [lobbynumber] [arenaname]` - Add a deathmatch spawn - Permission: `pg.setup`
* `/pg delarena [lobbynumber] [arenaname]` - Remove an arena - Permission: `pg.setup`
* `/pg delspawn [lobbynumber] [arenaname]` - Remove last spawn - Permission: `pg.setup`
* `/pg deldeathmatch [lobbynumber] [arenaname]` - Remove last deathmatch spawn - Permission: `pg.setup`
* `/pg build` - Activate build mode - Permission: `pg.build`
* `/pg pause` - Pause timer/countdown - Permission: `pg.pause`
* `/pg force [arenaname]` - Force an arena - Permission: `pg.force`
* `/pg start` - Set lobby countdown to 10 - Permission: `pg.start`
* `/pg join [lobbynumber]` - Join the game (`startOnJoin = false`) - Permission: `pg.join`
* `/pg list` - Open GUI with all lobbies (`startOnJoin = false`) - Permission: `pg.join`
* `/pg leave` - Leave the game (`startOnJoin = false`)
* `/pg stats [player]` - Show player stats - Permission: `pg.stats`
* `/pg version` - Show your and latest version of plugin - Permission: `pg.update`
* `/pg reload` - Reload all config files - Permission: `pg.setup`
* `/pg headp1(2;3)` - Add Player Head to Stats-Wall - Permission: `pg.setup`
* `/pg signp1(2;3)` - Add Player Sign to Stats-Wall - Permission: `pg.setup`
* `/pg joinsign [lobbynumber]` - Set Join-Sign - Permission: `pg.setup`
* `/pg setup` - Set up the plugin - Permission: `pg.setup`

####

* Colored name in player and spectator chat - Permission: `pg.admin`
* Error messages - Permission: `pg.admin`
* Update Checker - Permission: `pg.update`

#### Single-Lobby-System

* `/pg` or `/pg help` or `/pg commands` - Get list of commands + permissions - Permission: `none`
* `/pg setlobby` - Set lobby - Permission: `pg.setup`
* `/pg addarena [arenaname]` - Add an arena - Permission: `pg.setup`
* `/pg addspawn [arenaname]` - Add a spawn - Permission: `pg.setup`
* `/pg adddeathmatch [arenaname]` - Add a deathmatch spawn - Permission: `pg.setup`
* `/pg delarena [arenaname]` - Remove an arena - Permission: `pg.setup`
* `/pg delspawn [arenaname]` - Remove last spawn - Permission: `pg.setup`
* `/pg deldeathmatch [arenaname]` - Remove last deathmatch spawn - Permission: `pg.setup`
* `/pg build` - Activate build mode - Permission: `pg.build`
* `/pg pause` - Pause timer/countdown - Permission: `pg.pause`
* `/pg force [arenaname]` - Force an arena - Permission: `pg.force`
* `/pg start` - Set lobby countdown to 10 - Permission: `pg.start`
* `/pg join` - Join the game (`startOnJoin = false`) - Permission: `pg.join`
* `/pg leave` - Leave the game (`startOnJoin = false`)
* `/pg stats [player]` - Show player stats - Permission: `pg.stats`
* `/pg version` - Show your and latest version of plugin - Permission: `pg.update`
* `/pg reload` - Reload all config files - Permission: `pg.setup`
* `/pg headp1(2;3)` - Add Player Head to Stats-Wall - Permission: `pg.setup`
* `/pg signp1(2;3)` - Add Player Sign to Stats-Wall - Permission: `pg.setup`
* `/pg joinsign` - Set Join-Sign - Permission: `pg.setup`
* `/pg setup` - Set up the plugin - Permission: `pg.setup`

####

* Colored name in player and spectator chat - Permission: `pg.admin`
* Error messages - Permission: `pg.admin`
* Update Checker - Permission: `pg.update`

### Config

* `activateMySQL: false` - Change between SQLite `false` and MySQL `true` database
* `mysql:` - Setup your mysql database
* `gameServer: true` - Change between Game-Server `true` and Hub-Server `false`
* `lobbySystem: false` - Change between Single-Lobby `false` and Multi-Lobby `true`
* `countdown: 60` - Set the lobby countdown
* `maxPlayers: 24` - Set the amount of maximum amount of players
* `minPlayers: 12` - Set the amount of minimal amount of players to start the game
* `teamSize: 2` - Set amount of players in one team
* `roundTime: 30` - Set duration of the round in minutes
* `activateTeams: true` - Teams allowed `false` or `true`
* `activateKits: true` - Kits allowed `false` or `true`
* `activateShop: true` - Shop allowed `false` or `true`
* `activateAirdrops: true` - Airdrops allowed `false` or `true`
* `startOnJoin: false` - Join the lobby when joining the server `false` or `true` (Example: BungeeCord)
* `language: en_US` - Change language to one of the defined ones in the `messages.yml` file
* `activePotions: 19` - Change amount of used slots in the Potion-Shop (Maximum: `27`)
* `activeKits: 6` - Change amount of used slots in the Kit-Chooser (Maximum: `26`)
  * `Rich Kid` is hard coded and can only be deactivated
* `compassOnSpawn: false` - Add Player-Finder to inventory on round start `false` or `true`
* `allowOutsideChat: false` - Allows chatting with all players on the server `false` or `true`
* `changeGamerules: true` - Decide if the plugin changes gamerules `true` or `false`
* `activateScoreboard: true` - Activate scoreboard `true` or `false`
* `friendlyFire: false` - Allows friendly fire on teammates `true` or `false`
* `joinStarted: true` - Allows joining a match that has already started `true` or `false`
* `activateDeathmatch: true` - Activate deathmatch when only two players are left `true` or `false`
* `enableRewards: true` - Enable rewards `true` or `false`
* `winningReward: 100` - Set reward amount for winning
* `killReward: 10` - Set reward amount for kills (Vault needed)
  * [Download the latest release here!](https://www.spigotmc.org/resources/vault.34315/)
* `broadcastStarting: false` - Broadcast when a lobby reached minimal amount of players `false` or `true`

### Messages

* To change a message just change the text in the `messages.yml` file
* To add a language copy the existing lines and paste them below it and change the `en_US` to your language.
* Also change the `en_US` in the `config.yml` to your language.
  * [Download the latest German and Chinese translation here!](https://github.com/andersspielen/PotionGamesIssues/releases/latest)

## Release History

* 6.0
  * ADD: Airdrops
* 5.2
  * ADD: Sounds
* 5.1
  * ADD: Rewards for kills and winning (Vault)
* 5.0
  * ADD: Deathmatch
* 4.9.5
  * ADD: Team-Mode
* 4.9
  * ADD: Scoreboard
* 4.8
  * ADD: One arena lobbies
* 4.7
  * ADD: Primed TNT to loot table
* 4.6
  * ADD: /pg reload command
* 4.5
  * ADD: /pg version command
* 4.4
  * ADD: Join lobby via gui
* 4.3
  * ADD: Support for 1.17
* 4.2
  * ADD: Bungee Hub-Server setting
* 4.1
  * ADD: Option to change all chest blocks
* 4.0
  * ADD: Option to add own blocks with their own loot table
* 3.1
  * ADD: Own settings per a lobby (Now every setting)
* 3.0
  * ADD: Inventory set up
* 2.3
  * ADD: Round-Time
* 2.2
  * ADD: Own settings per a lobby
* 2.1
  * ADD: Join-Sings with updating information
* 2.0
  * ADD: Multi-Arena-System
* 1.0
  * ADD: Option to change chest items and effects
* 0.9
  * ADD: Option to change database type between MySQL and SQLite
* 0.8.5
  * ADD: Option to deactivate mysql/stats
* 0.8
  * ADD: Option to change kits
* 0.7
  * ADD: Option to change shop items
* 0.6
  * ADD: Option to turn Teams, Kits and Shop on or off
* 0.5
  * ADD: Teams
* 0.4
  * ADD: Kits
* 0.3
  * ADD: Shop
* 0.2
  * ADD: ArenaVote-System
* 0.1
  * ADD: SurvivalGames-System with chests giving PotionEffects

## TODO

## Issues / Ideas

[Report bugs / request features here!](https://github.com/andersspielen/PotionGamesIssues/issues)
