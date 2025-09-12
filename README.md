# FastbuilderDocs
An inofficial help document for the Fastbuilder Plugin from _MinusOne_

## What is this Doc about?
This Document is to help the people that bought MinusOne's Fastbuilder plugin but don't know how to set everything up. To me: I am Donut4GAMER and an early supporter of MinusOne's Fastbuilder Plugin.

## Requirements
- a Spigot 1.8.8 Minecraft server
- Java 8+

## Basic Setup
If you bought MinusOne's Fastbuilder make sure to join his Discord: https://discord.gg/tbQDeSZ3FU and open a support ticket and claim your License.

1. Drag the Fastbuilder Plugin into your `/plugins/` folder of your server
2. Start your server
3. Fastbuilder won't start since you need to fill in the license you got on his Discord server
4. Then restart your server
5. Configure everything you want to change (e.g. guis.yml or config.yml)
6. Reboot your server and you are ready to go

## Setup Arenas
Now we want to create a mode to play Fastbuilder. Please make sure that your map points to the south, also you can not set the deathhight yet. The finish will be golden pressure plates. 

1. Type: `/fb addmode <modename> <is diagonal (yes/no)>` Please note that Diagonal has bugs in it! MinusOne is fixing it soon
2. Go to the spawn of your island and type: `/fb set <modename> <islandnumber>`
3. _(optional)_ Go to your plugins folder and open the arenas.yml file. There you can configure where the Mode Switcher NPC should stand
4. Join the arena
- On a single server: Type: `/fb join <modename>`
- On a Bungeecord server: Rejoin your server or use the single server variant if you don't want to rejoin

## Other useful commands
Here you can see what every command does in detail.

- `/fb removemode <modename>` Remove a mode from Fastbuilder
- `/fb setcoins <user> <amount>` Set a users amount of coins (sertcoins sets the coins on top of the current amount of coins the user has)
- `/fb addcoins <user> <amount>` Add coins to an user (addcoins adds the coins on top of the current amount of coins the user has)

## Enable namecolors in the Scoreboard
For this you need to have Luckperms installed on your server. You also need to have ranks set up already.

1. Go into the config.yml
2. Find this: `luckperms-support: false` and set it to true
3. Restart your server and you are done

## Manage when you get tp'd back
You can setup where players should get tp'd back, so after how many blocks arount the map (this does NOT count for everything going to south)

1. Open the config.yml
2. Locate this: `max-distance: 4` and set it to an number you want (e.g. 6)
3. Save the config and reboot your server

## Setup GUI's correctly
If you want to customise the GUI's you need for this example an existing mode (if you don't know how to set it up read **Setup Arenas**.

1. Open the guis.yml
2. Search for this: `mode-changer-slots:`
3. Then you do this:
   ```mode-changer-slots:
  1: # the page number
    1: # the slotnumber
      name: "&6<modename>" # the display name in the gui
      material: SANDSTONE:0 # the item/block that should be there
      mode: "<modename>" # the mode players should join on interaction
      lore: # the text shown under this item in the gui
        - "&r&7A Fastbuilder Map"```
4. Click save and reboot your server.
