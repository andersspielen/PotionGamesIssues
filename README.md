# PotionGames

> A Minecraft Minigames Plugin for Bukkit Servers!

PotionGames is a minigames plugin that works like SurvivalGames but with potions and effects!

## Installation

1. Download the plugin
2. Put the .jar in your plugins folder
3. Download Multiverse-Core
4. Put the .jar in your plugins folder
5. Add `mv.bypass.gamemode.*: true` to your permissions.yml
5. Start your server
6. Change the config.yml in the PotionGames folder like you want it
7. (Optional) Change or add languages to the messages.yml in the PotionGames folder

## Usage

### Setup

0. You need to be op or have the permission pg.setup
1. Create lobby `/pg setlobby`
2. Create arena `/pg addarena [arenaname]`
3. Add arena spawns `/pg addspawn [arenaname]`
4. Add chests to your arena

#### Chest-Types

* End Portal Frame: Normal chest like in SurivalGames
* Target: Special chest with Flame-Bow and Arrows
* Netherite Block: Special chest with Netherite Ingots
* Composter: Shop with potions (Build a Beacon under the Composter to make it shown on the whole map)
    
#### Create Stats-Wall

1. Place 3 Player Heads on a block next to each other
2. Place 3 Signs at the front of the block
3. Now use the commands listed below to create a podium
    * Look at the head of the 1(2;3) player on the podium and do: `/pg headp1(2;3)`
    * Look at the sign of the 1(2;3) player on the podium and do: `/pg signp1(2;3)`
    
### Commands and Permissions

* `/pg help` or `/pg commands` - Get list of commands + permissions - Permission: `none`
* `/pg setlobby` - Set waiting lobby - Permission: `pg.setup`
* `/pg addarena [arenaname]` - Add arena - Permission: `pg.setup`
* `/pg addspawn [arenaname]` - Add spawn - Permission: `pg.setup`
* `/pg delarena [arenaname]` - Remove arena - Permission: `pg.setup`
* `/pg delspawn [arenaname]` - Remove last added spawn - Permission: `pg.setup`
* `/pg build` - Activate build mode - Permission: `pg.build`
* `/pg pause` - Pause timer/countdwon - Permission: `pg.pause`
* `/pg force [arenaname]` - Force arena - Permission: `pg.force`
* `/pg start` - Set lobby countdown to 10 - Permission: `pg.start`
* `/pg join` - Join the game - When `startOnJoin = false` - Permission: `pg.join` 
* `/pg leave` - Leave the game - When `startOnJoin = false` - Permission: `pg.leave` 
* `/pg stats` - Show your stats - Permission: `pg.stats`
* `/pg headp1(2;3)` - Add Player Head to Stats-Wall - Permission: `pg.setup`
* `/pg signp1(2;3)` - Add Player Sign to Stats-Wall - Permission: `pg.setup`

### Config

* `mysql:` - Setup your mysql database
* `countdown: 60` - Set the lobby countdown
* `maxPlayers: 24` - Set the amount of maximum amount of players
* `minPlayers: 12` - Set the amount of minimal amount of players to start the game
* `teamSize: 2` - Set amount of players in one team
* `activateTeams: false` - Teams allowed `false` or `true`
* `startOnJoin: false` - Automatically joining the lobby when joining the server `false` or `true` (Example: BungeeCord)
* `language: en_US` - Change language to one of the defined ones in the `messages.yml` file

### Messages

* To change a massege just change the text in the language you use.
* To add a language copy the existing lines and paste them below it and change the `en_US` to your language.

## Release History

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

* ADD: Option to deactivate mysql (file database) - (Version 1.0)
* ADD: Kits in config (remove, add, deactivate) - (Version 1.0)
* ADD: Shop items in config - (Version 1.0)
* ADD: Chest items in config - (Version 1.0)
* ADD: Multiple lobbys per server - (Version 2.0)


## Issues

[linky](https://github.com/andersspielen/PotionGamesIssues/issues)Report bugs here!