-------------------------------------------------------------------------------
---Contents--------------------------------------------------------------------
-------------------------------------------------------------------------------

Section 1  - General Information
Section 2  - Preview
Section 3  - Install Instructions
Section 4  - What's New (Changelog)
Section 5  - Usage
Section 6  - Command List
Section 7  - Command Examples
Section 8  - Properties Files
Section 9  - Support
Section 10 - License

-------------------------------------------------------------------------------
---1. General Information------------------------------------------------------
-------------------------------------------------------------------------------

Created By: simo_415
Version: 2.12.1
Mincraft Version: Beta 1.8.1
Thread: http://bit.ly/spcmod
Official Channel: http://youtube.com/user/spcmod
Wiki: http://simo415.wikispaces.com/singleplayercommands

-------------------------------------------------------------------------------
---2. Preview------------------------------------------------------------------
-------------------------------------------------------------------------------

http://www.youtube.com/watch?v=P4qNc6FNLow

-------------------------------------------------------------------------------
---3. Install Instructions-----------------------------------------------------
-------------------------------------------------------------------------------

Automated Installation - http://www.youtube.com/watch?v=u6-qH763fiY
1. Double click the .JAR file to run it. Note that if double clicking the file doesn't
open it you can also run it from command line/console/terminal as described below:

>Open command line (Windows) /console (Unix/Linux) /terminal (MAC)
-Navigate to where the installer is, for example it might be: 
cd C:\Users\Example\MyDocuments\Downloads
-Type in the following: java -cp SPCInstaller.jar com.sijobe.installer.Installer
2. Once the installation screen is up verify that the filepath that is displayed is
pointing to where Minecraft is installed.
3. Click the Install button and the installation will start, a popup message will
appear when the installation is finished. 

Manual Installation
1. Go to the minecraft bin directory and backup minecraft.jar
2. Using 7zip or equally capable ZIP viewer open minecraft.jar
3. Delete the META-INF folder
4. Copy ALL the ".class" files contained within the mod to minecraft.jar, replacing the existing files.
Note: The SPCInstall.JAR can be opened up the same way as Minecraft.jar and you can install the mod manually by dragging the files from there into Minecraft.jar as you usually would.
5. Close minecraft.jar
6. Copy ALL the ".jar" files contained within the mod to the minecraft/bin directory (the same directory as minecraft.jar)

Note: If you have problems installing this mod, refer to help on the thread.

-------------------------------------------------------------------------------
---4. What's New---------------------------------------------------------------
-------------------------------------------------------------------------------

---V2.12.1---------------------------------------------------------------------

Fixed the damage command
Fixed WorldEditCUI compatability
Fixed noclip damage in walls

---V2.12-----------------------------------------------------------------------

V2.12 is now compatiable with Minecraft 1.8.1

Changes:
/flymode <dynamic|standard|minecraft|reset> - Allows you to specify which flying mode to use
/hunger <empty|full|infinite> - Sets your hunger level to predefined figures
/food <QTY> - Adds the specified quantity to your food bar
/gamemode <creative|survival|1|0> - Changes the World game mode to creative or survival

---V2.11.1---------------------------------------------------------------------

Fixed glitch which made redstone off-by-one tick

---V2.11-----------------------------------------------------------------------

New Installer
Update checker (tells you when updates are available)
Improved compatibility with other mods such as Zombes and ShockAhPI (Aether)

/textcolor <<normal|error> <0-f|random>>|<setrandom COLORS> - Allows you to configure output text colors
/update <enable|disable> - Turns update checking on/off
/time speed - Allows you to change the speed which time goes by
/stacklimit - Turns stack limiting on/off
/stackcombine - When run combines all of the same stack types into the same stack
/chest clear - Allows you to clear the contents of a chest
/flymode standard - Allows you to turn on standard flying mode
/repeat - Repeats the last used command (useful command to bind)
/freezecam - Freezes the players camera at the current location
/itemname - Now provides item damage information

Fixed /keepitems
Fixed /infiniteitems
Fixed /itemdamage

And a handful of other things...

For more information on commands use /help <COMMANDNAME>

---V2.10_2---------------------------------------------------------------------

Compatible with Minecraft 1.7.3

---V2.10_1---------------------------------------------------------------------

This release is mainly a bugfix release. Fixes the below mentioned known bugs:

/music
/achievement
WorldEdit air block doesn't work
/ascend and /descend should now work more reliably.

ShockAhPI compatability integrated into SPC

---V2.10-----------------------------------------------------------------------

This new release is now compatible with Minecraft 1.7.2 among all the content added here are the highlights

New commands:
/freecam - Allows you to freecam around the map
/moveplayer <DISTANCE> <DIRECTION> - Moves the player the specified distance (in blocks) in the specified direction, (neswup)

Improvements/Bugfixes:
rewrote the noclip command so it works again
fixed resize
WorldEdit now supports custom blocks (ids only)

---V2.9_1----------------------------------------------------------------------

Now compatible with Minecraft 1.6.5

No new features, no bug fixes.

---V2.9------------------------------------------------------------------------

Added a few new commands:

/achievement <list|unlock> - Allows you to list or unlock all achievements
/alias <NAME> <COMMAND> {ARGS} - Allows you to assign an alias to one or more words
/ralias <NAME> - Removes the specified alias
/resize [1080p|720p|480p|setdefault [WIDTH HEIGHT]|<WIDTH HEIGHT>] - Resizes the Minecraft window, no arguments sets it to default
/startup <COMMAND> {ARGS} - Specifies a command to run on startup

Changes:
/weather sun
/give command now puts items into inventory rather than droping them
/give you can now specify damage using : or ^ an example: /give 35:12 or /give wool:10 or /give 35^8
/spawn mob no longer freezes minecraft

Known Bugs:
/noclip doesn't work correctly due to Minecraft 1.6

A BIG thankyou to all the support since 1.6 came out, it is really appreciated!

---V2.8_2----------------------------------------------------------------------

More bugfixes...

Fixed SMP issues, you can now break blocks, place blocks, open and close chests
and a bunch of other stuff.
Fixed the longerlegs problem.

---V2.8_1----------------------------------------------------------------------

BUGFIXES!!!

/freeze and /mobdamage makes enemies stay on the ground sideways and red
/freeze freezes the player as well
/longerlegs doesn't work
/phelp doesn't work
Some people are having problems with infinite items
WorldEdit super pickaxe doesn't work
//wand tool doesn't give player a wand
TFC mod manager doesn't appear to work
Water damage is buggy
No hurt sounds
itemdamage is buggy
/explode can cause game crash - Can't reproduce.
/world seed needs to be fixed
/removedrops doesn't work
/slippery 0 causes problems (crash?)
/defuse not working

Other:
Forgot to add a class to the ZIP which can cause problems with plugins

---V2.8------------------------------------------------------------------------

This release now works with Minecraft 1.5! Yay. 

It also introduces a heap of new commands, mainly thanks to 303. Go say thanks
and check out his thread: http://goo.gl/aX9bv

helmet [ITEM] [QTY] [DAMAGE] - Specifies the helmet the player wears
slippery <BLOCK> [SLIPPERYNESS] - Makes the specified block slippery
longerlegs - Makes your legs longer so you can walk up 1 block high 
atlantis - Toggles atlantis mode on/off 
spawnportal - Spawns a portal nearby the player
clone [QUANTITY] - Clones the NPC which you are looking at
killall <MOBTYPE> - Kills all of the specified mob type, 
flammable <BLOCK> [CATCH] [SPREAD] - Sets the specified block at the flammability level
clearwater - Toggles water clarity on/off
confuse [DISTANCE] - Confuses nearby mobs
confusesuicide - ?
cyclepainting - Cycles through the painting which you are pointing at
bring [ENTITY] - Brings the specified entity to you.

superpunch [DISTANCE|reset] - Hit that NPC with a punch like no other 
phelp [COMMAND] - Provides help for plugins
bindid <ID> <COMMAND> {ARGS} - Binds a command to a keyboard key using the key id 
unbindid <ID> - Unbinds a command from a keyboard key using the key id
reskin <FILENAME> - Reskins the NPC which you are pointing at to the specified skin 
weather <lightning|thunder|rain> - Toggles weather on/off

A heap of other stuff was added as well... but they are the main ones.

---V2.7_1 V2.7_2---------------------------------------------------------------

Bug fix releases, if you aren't experiencing issues with V2.7 or V2.7_1 you
don't need to upgrade.

Fixed:
/ride
/exterminate
and the crash on world load

---V2.7------------------------------------------------------------------------

This release introduces 8 new commands and a number of changes to existing
functionality, as well as a detection system which will let you know if you
have installed Single player commands wrong and a little bit of information on
how to fix it.

New Commands:
/biome - Tells you what biome you are currently in
/cannon [STRENGTH] - Shoots a primed TNT in the direction you are pointing.
/chest <drop|get|fill|swap> - Allow access of chests
/config <setglobal [reset]> - Allows you to set the global configuration file as your current configuration
/exterminate [SIZE] - KillNPC with style, kills the NPC you are pointing at
/killnpc [monster|animal] - You can now just kill the agressive or friendly NPCs if you like.
/output - This just toggles SPC messages on/off, useful for macros/scripts.
/platform - Puts a glass square under your feet
/plugin [dlist] - Shows you all the disabled plugins.
/ride - Allows you to ride any NPC which you point at
/unbind [all] - Unbind all your currently bound keys at once
/world [backup] - Allows you to backup your current world into .minecraft/backup

Other Changes:
-/bind : You can no longer use IDs, use the key name instead, for example: /bind e /cannon 5
-/unbind : You can no longer use IDs, use the key name instead, for example: /unbind e
-If you didn't install the core SPC correctly you should get a helpful popup error
-Better scripting support, will now pickup the .JAR script engines from .minecraft/bin
-WorldEdit 4.3 now included with release
-A global configuration is now loaded into new worlds if it is set

Scripting support has now been added to access and use scripting you need to
use the "/sc" command, see SPC help for more information. By default the 
scripts should be written in Javascript but using the "/sc engine <NAME>" 
command you can specify another script language to write in, you will need to
have this engine installed correctly or the .JAR should be in .minecraft/bin

To run a script: "/sc SCRIPTNAME.EXT"

By default these objects are passed into the script:
player - The player object
helper - The SPC main class, to run a command use method processCommand(String)
world - The Minecraft world object
minecraft - The main Minecraft class

More information soon.

---V2.6_1----------------------------------------------------------------------

This build purely fixes all the issues which occurred in V2.6

/skin now works correctly
/repair works
/removedrops works
/maxstack now works
WorldEdit commands should now work as they did

A few other things "under the hood" were also fixed which should allow SPC to 
run nicer.

---V2.6------------------------------------------------------------------------

After numerous hours, it's finally updated! Woot!

As for features -

Commands:
/infiniteitems - Toggles infinite items on/off
/instantkill - Toggles instant kill on/off (kill any NPC in one hit)
/macro <edit|create|dir|folder|delete|list> - Added additional commands
/plugin <enable MODNAME|disable MODNAME> - Added enable/disable
/sc <FILENAME> - Added scripting support (more information coming soon)
/skin <USERNAME> - Change your players skin to ANY minecraft players

Problems:
The update broke these commands - 
/maxstack
/itemdamage

---V2.5_1----------------------------------------------------------------------

Added another plugin method which allows WorldEditGUI to work on single player
now, go check it out! 

The skeleton bug was fixed as well.

For WorldEdit commands which aren't working correctly use an extra slash in 
front of it for it to work correctly.

For example:
///expand

---V2.5------------------------------------------------------------------------

Plugin support is now here. What does this mean? Well it means mod developers 
can write their own commands for SPC and SPC will load them and use those
commands when they are installed. Cool eh? More information will be available 
in the developer pack which will include some example plugins, some 
documentation and some JavaDocs. Note that the developer pack may not be 
available until V2.6.

As well as the plugin support a few new commands were added (thanks to trunksbomb):
itemdamage - Turn item damage on/off. This means you will never have to repair an item again
keepitems - Turn this on and you will keep your items when you die. 
instantkill - Instantly kills any NPC you hit
instantplant [grow] - Instantly plants saplings into the ground, if grow is specified the tree will when instantly grow
plugin <list|enable|disable> - Lists all loaded plugins and also allows you to enable/disable plugins

Bug Fixes:
You can now kill enemies when they are frozen
If WorldEdit isn't installed correctly - only error once
Furnace turns wood into charcoal now, rather than wood

Many other things were changed but they are the things you will notice.

Big Thanks to Trunksbomb for writing some of the commands.

---V2.4------------------------------------------------------------------------

This release brings some bugfixes, commands and a few other changes. Also, 
earlier this week it a new video also came out detailing all the commands that 
are in V2.3

Video: http://www.youtube.com/watch?v=U1whd_KO5og

BugFixes:
/listwaypoints doesn't cause occasional game crash anymore

Commands:
/drops - Turns item drops on/off, having them turned off will make the game run
a little bit faster, and also stop your inventory from filling.
/freeze - Freezes mobs so that they cannot move or attack you
/light - Turns permanent lighting on and off
/mobdamage - Mobs cannot give you damage 
/rename <COMMANDNAME> <NEWNAME> - Allows you rename a command to a new name
/superheat [all] - Turns items which are furnace-able into their furnaced form

Other Changes:
A startup message is now displayed on startup of Minecraft when SPC is installed
correctly. 

---V2.3_01---------------------------------------------------------------------

This build only has bugfixes - no new features.

Bug Fixes:
-Can now connect to multiplayer servers again
-WorldEdit 4 now works
-WorldEdit 4 now packaged with SPC
-Illegal Keys which are bound shouldn't cause crashes anymore

---V2.3------------------------------------------------------------------------

This build is now compatible with Minecraft V1.3

It also introduces the /bind and /unbind commands which allow you to bind a 
command to a keyboard button.

Syntax:
/bind <KEYCODE> <COMMAND> {COMMANDPARAMS}
/unbind <KEYCODE>

Example:
/bind 22 /give stone 64
/bind 23 /fly
/bind 24 /macro mycommands

/unbind 24
/unbind 22
/unbind 23

---V2.2------------------------------------------------------------------------

This build fixes issues people were having opening the chat and using the fly 
command, where they wouldn't work correctly. As a result I totally re-wrote the
flying command and also the keyboard processing.

New Commands:
/world <load|save|seed|new|exit|list> - Allows you to explicitly, have control over your world.

load <FILENAME> - Loads the specified FILE, this allows you to play ANY save on your computer, not just World1-5, and can have any name
save - Explicitly saves your game then returns to it
seed [SEED] - Allows you to see and change the seed of the map, so it will generate custom terrain
new [FILENAME] [SEED] - Creates a new map at the specified location 
exit - Lets you exit a game without saving (perfect from when a creeper blows something up)
list - Lists all the saves which you can load from ".minecraft/saves"

/macro <FILENAME> {PARAMS} - Allows you to pass in parameters to your macros, see Wiki for more information

Macro's now MUST end with a ".txt" extension.

I have also started creating a Wiki which will begin to contain all the information contained in this readme.

http://simo415.wikispaces.com/singleplayercommands

---V2.1------------------------------------------------------------------------

This build mainly fixes the WorldEdit commands which weren't working in V2.0. 
Now you are able to use //wand and //rbrush and a bunch of other cool commands.
Check out the WorldEdit wiki for more information.

It also fixes the in-game help so that all in-built commands are now listed 
(this does not yet include WorldEdit, sorry). And adds a file which you can 
configure the item names if you don't like them, note that this only changes 
the commands which use item names such as /item, /itemstack and /maxstack

Commands:
/maxstack [ITEMID|ITEMNAME|all] [STACKSIZE] - Configures the maximum stack size
   of that item between 1 and 64.
/itemstack <ITEMID|ITEMNAME> [QTY] - Gives the player the specified number of
   that itemstack
/reset - Provides a better reset mechanism
/help [COMMAND] - Should now be easier to use even if you change command names
/reach [reset] - Allows you to specify the reach distance (and reset it)

To Change Item Names:
1. Install mod then run minecraft and load a world
2. Close minecraft
3. Go to .minecraft/mods/sppcommands/itemnames.properties
4. Change the itemnames as required
5. Save file and load up minecraft.
6. Commands which use ITEMNAME now use the new specified itemname. 

---V2.0------------------------------------------------------------------------

This build introduces support for the SMP version of WorldEdit. Now what does
this mean? It means that most of the commands in the world edit mod will now 
work in single player. You can read about the mod here:

http://www.minecraftforum.net/viewtopic.php?f=1023&t=45396#p747338

And you can view all the current world edit commands here:

http://wiki.sk89q.com/wiki/WorldEdit

As these world edit commands have been introduced there is no further need for
the in-built WorldEdit commands. Therefore from V2.0 onwards the in-built 
worldedit commands have been removed.

In other news a few other things were added/changed:
/reach - Allows you to set your players reach distance
/reset - Allows you to reset your settings
/item - Now has a damage specifier "/item <ITEM> [QTY] [DAMAGE]"
/item - Now allows you to specify a quanity with an itemname
/grow - Now grows cactus and reeds
/fly - Now has better control
/fly - crouching will now descend you
/fly - If experiencing weird problems, turning fly on then off should reset it
/noclip - Still annoying sounds, but you shouldn't be damaged by anything
/fly-noclip - Both revert to previous settings before issuing commands.

Also! Minecraft.class no longer needs to be modded by this mod, this now makes
it compatible with SDK's and Xau's mods without compatibility patches.

---V1.9_02---------------------------------------------------------------------

Fixes minor issue of the version number.

---V1.9_01---------------------------------------------------------------------

This build just fixes the bugs that were introduced in V1.9

/home now doesn't delete inventory
/spawn mob now doesn't crash minecraft
/spawnstack now actually stacks the NPCs
/defuse now defuses TNT
/fly now turns falldamage off
/noclip now turns damage off

---V1.9------------------------------------------------------------------------

Compatible with Minecraft Beta 1.2

Added fly and no clip commands...

/fly - Allows you to fly
/noclip - Allows you to go through walls

Note: Minecraft Beta V1.2 breaks the repair command.

---V1.8------------------------------------------------------------------------

This release has a number of changes from the previous releases, the command 
set has now been broken up into two distinct sets, standard commands (such as
set, tele, instantmine, damage, etc) and world edit commands (previously known
as cuboid commands). 

The world edit commands are accessed by hitting '//' before your command name.

The list of current world edit commands is as follows (these are exactly the 
same as the "cuboid" commands in V1.6 and V1.7):
//box <BLOCKID> - Creates a box between the two specified points
//contract <n|s|e|w|u|d> [DISTANCE] - Reduces the selected area in the direction specified
//copy - Copies the selected area
//expand <n|s|e|w|u|d> [DISTANCE] - Expands the selected area in the direction specified
//fill <BLOCKID> - Fills the selected area
//help [COMMAND] - Specific world-edit help
//load <FILENAME> - Loads a saved config file so that it can be pasted
//paste - "Pastes" the copied (or loaded) region to the south-west of you
//remove - Removes the selected region
//reset - Resets the selected region
//save [FILENAME] - Saves the selected region to file
//set1 - Sets one corner of the region
//set2 - Sets one corner of the region
//walls <BLOCKID> - Puts walls around the selected region

Also added in this release is error messaging. The mod will now tell you if you
don't have enough parameters, your formatting is wrong or if the command you
typed in doesn't exist, just to name a few. This should help in debugging any
problems you have with commands. 

Along with the error messaging there is better error handling, so now the mod 
should NEVER cause the game to crash, and there should be an error log written 
if a problem occurs.

The new commands in this release are as follows:
/dropstore - This command transfers everything in your inventory into a chest 
   that it creates next to you.
/grow [all] - Grows all saplings/wheat on the map.
/itemname - Use this command to discover the itemname and ID of your currently 
   selected item.
/msg <MESSAGE> - This commands adds a message to the console.
/removedrops [all] - This command removes item drops from the world.
/replenish [all] - Re-stocks your items in your inventory to the maximum ammount
/search <SEARCHTERM> - Allows you to search for items using a name
/spawn <NAME|ID|random> [QTY] - Allows you to spawn an individual creature.
/spawnstack <NAME|ID|random>... - Same as /spawn in previous releases
/useportal - Instantly transfers you to the nether, use it again to go back.

Changed Functionality:
/item Allows you to enter an Item name rather than ID. The item name is found
   by hovering over the item in your inventory.
/spawn has changed to /spawnstack
/spawn now allows a number of the specified NPC to spawn

Bugs Fixed:
/explode now works as expected (tip: after big blasts use /removedrops).

---V1.7------------------------------------------------------------------------

This version adds a few new commands and a number of changes to the mod which
should allow for further expansion in the future. The new commands in this 
release are:

/damage - Turns player damage on/off
/explode [SIZE] - Sets off an explosion in your current location.
/extinguish|ext [all] - Puts out all nearby fire (or all fire)
/firedamage - Turns fire damage on/off
/timeschedule <reset | <TIME1> <TIME2>> - Sets a period of time (HH:MM format), 
   this will make minecraft always within this time.
/waterdamage - Turns water damage on/off

Also in this release a few other things were fixed/added:
/spawn <NAME> now does not have to be case-sensitive
/cuboid now has expand and contract options.

---V1.6------------------------------------------------------------------------

This version adds a "cuboid" type command to the mod:

To use cuboid you first need to specify the corners of the region that you want
to use cuboid with. To do this use:

/cuboid set1
/cuboid set2

Once both positions are set these commands become accesible:

/cuboid fill <BLOCKID> - This fills the selected region with the BLOCKID
/cuboid remove - This removes the selected region (same as /cuboid fill 0)
/cuboid box <BLOCKID> - This creates a box around the selected region with the 
   specified BLOCKID.
/cuboid copy - This copies the selected region to memory
/cuboid paste - This "pastes" the copied region to the map - to the immediate
   north east of the player.
/cuboid save [FILENAME] - This saves the copied region to file. These files are
located at ".minecraft/mods/sppcommands/saves". The files are uncompressed and
in later versions of this mod probably won't be compatible.
/cuboid load <FILENAME> - This loads the specified file to memory. The files 
should be in the same format that "/cuboid save" saves them as.

/cuboid get - This will return the two points which set1 and set2 are at. 
/cuboid reset - This will reset the two points set1 and set2.

See the examples for sample usage.

---

Other than /cuboid this version also comes with a number of new commands which 
should come in handy:

/falldamage - Turns fall damage on/off
/instantmine - Turns instant mining on/off
/jump - Moves you from where you are to where your mouse is pointing. Note: 
   This command is buggy and may put you in the block you move to.
/return - Moves the player to the last position before teleport
/setjump [JUMP|reset] - Sets the height that you jump. Note: Turns fall damage off
   if the jump is configured to move than 1.
/setspeed [SPEED|reset] - Sets the speed that the player moves

Use /help <COMMANDNAME> to find out information about each command. For example - /help falldamage

There is now a spc.settings file saved by the mod to the level save - this 
contains information which the mod uses and is configurable. This allows 
your settings to be saved, such as playerspeed and instantmine. 

This also release has a fix for the "/time day" command affecting redstone.

---V1.5------------------------------------------------------------------------

This version adds a number of new commands which are outlined below:

/ascend - Moves you to the next platform above your position
/descend - Moves you to the next platform below your position
/repair [all] - Repairs the currently selected item to full health
/duplicate [all] - Duplicates and drops the currently selected item stack
/destroy [all] - Destroys the current item
/itemstack <ITEMID> [QUANTITY] - Gives the player the specified quantity of maximum item stacks of the item.
/defuse [all] - Defuses any TNT nearby which has been hit, drops 1 tnt in its place
/killall [all] - Added [all] functionality which will remove all NPCs nearby
/killnpc [all] - Same as killall (killall to be removed in a later release).

Use /help <COMMANDNAME> to find out information about each command. For example - /help ascend

Made readme clearer

---V1.4------------------------------------------------------------------------

Single Player Commands mod now compatible with BETA 1.1.X

Added the ability to spawn custom mobs. This new feature changes the way /spawn works,
and changes all the NPC codes. Use /spawn list to find monster names and associated codes.
Please note that monster names ARE case sensitive.

You can now change the command names through a properties file, refer to the help
below for more information about this.

Fixed the bugs which were introduced in the last release

---V1.3------------------------------------------------------------------------

Single Player Commands mod now compatible with BETA 1.0.X

/health inf == /health infinite
/health now provides a message when used
Fixed bug where if you die you lose your waypoints

---V1.2------------------------------------------------------------------------

New Commands - 

difficulty
killall
music

Use /help <COMMANDNAME> to find out information about each command. For example - /help music

Added some extra functionality to /spawn
Moved the majority of the mod's functionality into a new class, PlayerHelper. This will help with compatability of other mods.
Fixed /time day and /time night to work like they should
Added more content to the readme

---V1.1------------------------------------------------------------------------

New commands -
clear
heal
health
help
listwaypoints
spawn
time

Use /help <COMMANDNAME> to find out information about each command. For example - /help time

Removed changes to cy.class so only TWO classes needed for mod to function correctly.
Fixed player skin bug.
Seperated waypoint save from level.dat into a seperate file named waypoints.dat
Cleaned up code and made more robust
More detailed readme

-------------------------------------------------------------------------------
---5. Usage--------------------------------------------------------------------
-------------------------------------------------------------------------------

1. After applying mod open minecraft.
2. Start a saved world or new world (as per usual).
3. Type 't' (by default) to bring up the chat console.
4. Type in the command and hit enter; a list of commands can be found below.

View the preview video for more information.

-------------------------------------------------------------------------------
---6. Commands-----------------------------------------------------------------
-------------------------------------------------------------------------------

---Normal Commands-------------------------------------------------------------

ascend - Moves you to the next platform above your position
biome - Tells you what biome you are currently in
bind <KEYCODE> <COMMAND> {COMMANDPARAMS} - Binds a key to a command
cannon [STRENGTH] - Shoots a primed TNT in the direction you are pointing.
chest <drop|get|fill|swap> - Allow access of chests
clear - Clears the console
config <setglobal [reset]> - Allows you to set the global configuration file as your current configuration
damage - Turns player damage on/off
descend - Moves you to the next platform below your position
destroy [all] - Destroys the current item
defuse [all] - Defuses any TNT nearby which has been hit, drops 1 tnt in its place
diff <VALUE> - Same as /difficulty
difficulty <VALUE> - Sets the difficulty of the game, valid range is 0-3.
dropstore - This command transfers everything in your inventory into a chest that it creates next to you.
drops - Turns item drops on/off, having them turned off will make the game run a little bit faster, and also stop your inventory from filling.
dupe [all] - Same as /duplicate
duplicate [all] - Duplicates and drops the currently selected item stack
explode [SIZE] - Sets off an explosion in your current location.
exterminate [SIZE] - KillNPC with style, kills the NPC you are pointing at
extinguish [all] - Puts out all nearby fire (or all fire)
ext [all] - Same as extinguish 
falldamage - Turns fall damage on/off
firedamage - Turns fire damage on/off
fly - Allows the player to fly
*freecam - Allows you to freecam around the map
freeze - Freezes mobs so that they cannot move or attack you
give <ITEMCODE> [QUANTITY] - Same as /item
goto <NAME> - Goto a waypoint
grow [all] - Grows all saplings/wheat on the map.
h [COMMAND] - Same as /help
heal <HEALTH> - Heals a player the specified number of points
health <MIN|MAX|INFINITE> - Sets the health of a player to pre-defined figures
help [COMMAND] - Gives general help when COMMAND isn't specified, gives specific help when COMMAND is specified.
home – Teleport to spawn point
i <ITEMCODE> [QUANTITY] - Same as /item
infiniteitems - Toggles infinite items on/off
instantkill - Toggles instant kill on/off (kill any NPC in one hit)
instantmine - Turns instant mining on/off
item <ITEMCODE|ITEMNAME> [QUANTITY] [DAMAGE] – Gives player item, if quantity isn’t specified maximum amount of that item
itemname - Use this command to discover the itemname and ID of your currently selected item.
itemstack <ITEMCODE> [QUANTITY] - Gives the player the specified quantity of maximum item stacks of the item.
kill – Kills the current player
jump - Moves you from where you are to where your mouse is pointing. Note: This command is buggy and may put you in the block you move to.
killnpc [all|monster|animal] - Kills all nearby living creatures except for yourself.
l - Same as /listwaypoints
light - Turns permanent lighting on and off
listwaypoints - Lists all waypoints
macro <edit|create|dir|folder|delete|list|FILENAME {PARAMS}> - Allows a macro to be run.
maxstack [ITEMID|ITEMNAME|all] [QTY] - Sets the maximum stack size of an item.
mobdamage - Mobs cannot give you damage 
*moveplayer <DISTANCE> <DIRECTION> - Moves the player the specified distance (in blocks) in the specified direction, (neswup)
msg <MESSAGE> - This commands adds a message to the console.
music [VOLUME] - Requests a music track to be played (max 2 per day, won't always work), if volume is specified, sets the volume
noclip - Allows the player to go through walls
output - This just toggles SPC messages on/off, useful for macros/scripts.
p - Same as /pos
platform - Puts a glass square under your feet
plugin <enable MODNAME|disable MODNAME|list|dlist> - Added enable/disable
pos – Gives current player position
reach <DISTANCE> - Sets the player reach distance.
return - Moves the player to the last position before teleport
rem <NAME> - Removes the specified waypoint
removedrops [all] - This command removes item drops from the world.
rename <COMMANDNAME> <NEWNAME> - Allows you rename a command to a new name
replenish [all] - Re-stocks your items in your inventory to the maximum ammount
repair [all] - Repairs the currently selected item to full health
reset - Resets your settings to default
ride - Allows you to ride any NPC which you point at
s <NAME> - Same as /set
sc <FILENAME|engine NAME> - Added scripting support (more information coming soon)
search <SEARCHTERM> - Allows you to search for items using a name
set <NAME> - Mark a waypoint on the world
setjump [JUMP|reset] - Sets the height that you jump. Note: Turns fall damage off if the jump is configured to move than 1.
setspawn [<X> <Y> <Z>] – Set the current position as the spawn point, if X Y Z are specified sets that position as spawn point
setspeed [SPEED|reset] - Sets the speed that the player moves
skin <USERNAME> - Change your players skin to ANY minecraft players
spawn <NAME|ID|random|list> [QTY] - Allows you to spawn an individual creature.
spawnstack <NAME|ID|random|list> {NAME|ID|random} - Spawns a stack of NPCs
superheat [all] - Turns items which are furnace-able into their furnaced form
t <X> <Y> <Z> - Same as /tele
tele <X> <Y> <Z> - Teleport to X Y Z coordinates.
time [set|get|day|night [minute|hour|day [TIME]]] - Set and get the time within minecraft.
timeschedule <reset | <TIME1> <TIME2>> - Sets a period of time (HH:MM format), this will make minecraft always within this time.
unbind <KEYCODE|all> - Unbinds a key from a command
useportal - Instantly transfers you to the nether, use it again to go back.
waterdamage - Turns water damage on/off
world <load|save|seed|new|exit|list> - Allows you to explicitly, have control over your world.
	world load <FILENAME> - Loads the specified FILE, this allows you to play ANY save on your computer, not just World1-5, and can have any name
	world save - Explicitly saves your game then returns to it
	world seed [SEED] - Allows you to see and change the seed of the map, so it will generate custom terrain
	world new [FILENAME] [SEED] - Creates a new map at the specified location 
	world exit - Lets you exit a game without saving (perfect from when a creeper blows something up)
	world list - Lists all the saves which you can load from ".minecraft/saves"
	world backup - Allows you to backup your current world into .minecraft/backup

* = New Command

---World Edit Commands---------------------------------------------------------

You can read about the WorldEdit mod here:

http://www.minecraftforum.net/viewtopic.php?f=25&t=156902#p2251803

And you can view all the current world edit commands here:

http://wiki.sk89q.com/wiki/WorldEdit


-------------------------------------------------------------------------------
---7. Examples-----------------------------------------------------------------
-------------------------------------------------------------------------------

---Normal Commands-------------------------------------------------------------

/ascend - Moves you to the platform above (if there is one)
/bind 22 /give stone 64 - Binds key 22 to the command /give stone 64
/bind 23 /fly - Binds the key 23 to /fly
/bind 24 /macro mycommands - Binds the key 24 to a macro
/clear - Clears the console.
/damage - Turns player damage off
/defuse - Defuses primed TNT in close radius of you
/defuse all - Defuses all primed TNT in the map.
/descend - Moves you to the platform below (if there is one)
/destroy - Destroys the current item
/destroy all - Destroys everything in your inventory
/difficulty 0 - Sets the difficulty to peaceful
/difficulty 3 - Sets the difficulty to hard
/drops - Turns off drops
/dropstore - transfers everything in your inventory into a chest that it creates next to you.
/duplicate - Duplicates and drops the current item
/duplicate all - Duplicates and drops your entire inventory
/explode - Creates an explosion at your current location
/explode 10 - Creates an explosion at your current location of size 10.
/extinguish - Gets rid of all fire nearby
/extinguish all - Gets rid of all fire in the map
/falldamage - Turns fall damage off. /falldamage again will turn it on.
/firedamage - Turns fire damage off
/fly - Player now flies
/freeze - Freeze NPCs where they are standing
/goto example - Teleports the player to the waypoint named "example"
/grow - Grows nearby plants
/grow all - Grows everything in the world
/heal 10 - Heals a player 10 health
/heal -10 - Removes 10 health from the player
/health min - Sets the players health to half a heart health
/health max - Sets the players health to ten full hearts
/health infinite - Sets the players health to 65565 (maximum ammount of health allowed).
/help goto - Provides an ingame help message about the goto command
/help spawn - Provides an ingame help message about the spawn command
/help - Provides a generic help message.
/instantmine - Turns instant mine on. /instantmine again will turn it off.
/item 1 - Gives the player 64 stone
/item 278 - Gives the player 1 diamond pickaxe
/item 278 64 - Gives the player 64 diamond pickaxe's
/item wool 64 12 - Gives the player 64 wool at 12 damage (different colour).
/item diamond sword - Gives the player a diamond sword
/itemname - Gives you the current items name and ID.
/itemstack 1 64 - Gives the player 64 stacks of 64 stone
/itemstack 278 10 - Gives the player 10 diamond pickaxes
/jump - Will teleport the player to the block where the mouse is pointing.
/kill - Kills the current player
/killall - Kills all nearby living creatures.
/killall all - Kills every living creature that is currently on the map.
/listwaypoints - Lists all waypoints that have been set on the given map
/macro give 1 - Runs the macro script give.txt with parameter "1"
/maxstack stone 32 - Sets the maximum stack of stone to 32
/maxstack boat - Sets the maximum stack of boats to 64
/maxstack - Sets the currently selected item to have a maxstack of 64
/maxstack all - Sets all items in inventory to have a maxstack of 64
/mobdamage - Turns mob damage off
/msg hello world - Puts a message on the console "hello world"
/music - Requests a music track to be played. Note that only one or two tracks can be player per day.
/music 10 - Sets the volume of music to 10.
/noclip - Player now able to go through walls
/pos - Gives the players position in X Y Z coordinates
/reach 10 - Sets the player reach distance to 10
/rem example - Removes the waypoint named "example"
/removedrops - Removes items that are on the ground nearby
/removedrops all - Removes all items on the ground in the world
/rename goto warp - Renames the command "goto" to "warp"
/rename warp goto - Renames the command "warp" to "goto"
/repair - Repairs the current item
/repair all - Repairs every item in your inventory
/replenish - Makes the current stack maximum again
/replenish all - Makes all stacks maximum
/reset - Resets the player settings to default
/return - Teleports the player to the position they were before they teleported. 
/search pick - Searchs items for the name "pick" and returns all matches.
/set example - Sets a waypoint at the current position named "example"
/setjump 5 - Sets the player jump to 5.
/setjump reset - Resets the player jump to default.
/setspawn - Sets the current position as the spawn point
/setspawn 0 66 0 - Sets the spawn point at (0,66,0)
/setspeed 5 - Sets the player speed to 5.
/setspeed reset - Resets the player speed to default.
/spawn list- Prints a list of monsters and monster codes to screen
/spawn random - Spawns a random monster
/spawn random 10 - Spawns 10 random monsters
/spawn creeper 20 - Spawns 20 creepers
/spawn 92 - Spawns creature #92
/spawn 92 5 - Spawns 5 of creature 92.
/spawnstack list - Prints a list of monsters and monster codes to screen
/spawnstack Zombie - Spawns a zombie nearby
/spawnstack 92 - Spawns the creature with id = 92, a cow in this case.
/spawnstack random - Spawns a random creature
/spawnstack r r - Spawns two random creatures ontop of one another
/spawnstack 92 Creeper 56 - Spawns creature 92 ontop of a creeper ontop of creature 56 (ghast > creeper > cow)
/superheat - Superheats the current item if it's furnacable
/superheat all - Superheats all the items in your inventory
/tele 0 66 0 - Teleports the player to the coordinates (0,66,0)
/time - Gives the player the current time
/time day - Sets the time to the morning, ie: hour = 0, same as /time set hour 0
/time night - Sets the time to night, ie: hour = 13, same as /time set hour 13
/time get hour - Gets the current hour
/time get minute - Gets the current minute
/time set day 1 - Sets the current day as 1
/time set hour 10 - Sets the current hour as 10
/timeschedule 12:00 0:00 - Sets a time schedule of 12:00 to 0:00. This means that once the time hits 12:00 it will go to 0:00
/unbind 24 - Removes the key 24 from the binding
/useportal Puts you in the nether, run again to go back to the normal world.
/waterdamage - Turns water damage off
/world new - Creates a new world
/world new world6 - Creates a new world, World6
/world new World6 1111 - Creates a new world, World6 with seed 1111
/world list - Lists all the saves
/world load World1 - Loads World1
/world save - Saves the current world
/world exit - Exits from the current world - without saving.
/world seed - Shows the current world's seed
/world seed 111 - Sets the current world's seed to '111'


---World Edit Commands---------------------------------------------------------

Please read the Wiki for more information.

http://wiki.sk89q.com/wiki/WorldEdit

-------------------------------------------------------------------------------
---8. Properties Files---------------------------------------------------------
-------------------------------------------------------------------------------

To change command names from what they are to alternate versions you need to 
add this file to your .minecraft directory.

.minecraft/mods/sppcommands/sppcommands.properties

Within this properties file should be key value pairs seperated by an equals "=" 
sign. Where the key is the command name and the value is the new value.

For example to change /goto to /warp

goto = warp

Example sppcommands.properties file
#START OF FILE

give =
goto = warp
item = 
pos = 
p = 
spawn = q

/set1 = /s1
/set2 = /s2

#END OF FILE

-------------------------------------------------------------------------------

To Change Item Names:
1. Install mod then run minecraft and load a world
2. Close minecraft
3. Go to .minecraft/mods/sppcommands/itemnames.properties
4. Change the itemnames as required
5. Save file and load up minecraft.
6. Commands which use ITEMNAME now use the new specified itemname. 

-------------------------------------------------------------------------------
---9. Support------------------------------------------------------------------
-------------------------------------------------------------------------------

If you are having any trouble with this mod please post on this forum thread, I check it regularly:
http://www.minecraftforum.net/viewtopic.php?f=25&t=100267

That way when I help you with your problem, people with the same problem can also find the solution.

Bugs Reports/Bug Fixes/Feature requests/Problems should all be posted on that forum thread.

I love hearing feedback, so any feedback so greatly appreciated, if you like the mod please tell me!

-------------------------------------------------------------------------------
---10. License-----------------------------------------------------------------
-------------------------------------------------------------------------------

This software is Copyright ©(2011) of simo_415 (hereafter referred to as "The Owner") 
and is the intellectual property of The Owner. Only Minecraftforum.net is able to host 
any of The Owner's material without the consent of The Owner. It may not be placed on 
any other web site or otherwise distributed publicly without advance written 
permission. (Electronic mail is acceptable as long as you wait for a response.) 