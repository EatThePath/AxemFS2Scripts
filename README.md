# AxemFS2Scripts
Axem's Lua Scripts for FreeSpace2 Open

Some Lua scripts to make FreeSpace missions more fun and exciting by expanding the toolbox of the mission designers.

A lot of the scripts use a JSON formatted config file. It's highly recommended you use a JSON editor (like this one: https://jsoneditoronline.org/) to edit the files. Subtle syntax errors are a giant pain!

These scripts have been tested to work with a minimum version of FreeSpace Open 3.8.0. But it is recommended to use a newer build (anything past January 19, 2018) so that Lua SEXP functionality is available, making things *much* **much** ***much*** easier for the modder.

# AxMessage

A neat looking scripted message hud gauge. The text will scroll in on top of a graphic instead of being displayed all at once. There's a config file for editing position, speed, etc. v1.3 includes support for per-resolution settings.

# Base Files

These scripts contain some generic functions and libraries that are used in a number of the scripts. It's a good idea to have these installed if you're going to use any of the scripts here. (Otherwise they won't work!)

# BtA Scripts

A variety of scripts that I mostly didn't make, but added LuaSEXP functionality. There's some neat stuff thats very situational, but it may inspire you!

# Cloak

This script allows both the player and AI to be able to cloak. A config file (included) allows you to tweak the finer details, including if weapons or afterburner will kill the cloak, or if shields remain up. The script also includes a 'Cloaking Device' weapon that you can add to a ship's loadout, if a ship has this in their loadout they will get cloaking automatically. Otherwise a lua sexp is needed to give the cloaking ability.

2 sample missions are included

# Debug Tools

A few scripts meant to help you, the modder, with any sort of issues that may arise when making a mission or mod.

While in a mission pressing `5` will toggle a display of SEXP variables. `6` will inform you of their type, `7` will append bitmask information to the sexp variables. `8` will give some very verbose data about your current target. `9` will give that same batch of verbose data about the player's ship.

Also included is a PrintDebug() lua function for helping debug lua scripts. By inserting a table into the function, the function will recursively list the entire contents of the table. This is good to see what exactly your lua script is doing.

# Get Closest

Add a "lua-get-closest-from-team", which will return into a string variable, the closest ship to a given team. (Crazy!)

# In Mission Jump

This script will automatically do an in mission jump sequence to a selected waypoint for the player and AI. The lua sexp `lua-jump-to` is used to trigger this sequence. The first point on the waypoint path is used as the destination, the second point is used for orientation (relative to the first one). The sexp documentation for the sexp contains more specifics for how everything is timed. It is highly recommended that this be used with only fighters!

A sample mission is included

# Extended Loading Screen

This script will allow the modder to more finely customize mission loading screens. Added features include customizeable loading bars, randomized loading images, ability to automatically draw the mission's title, and random text (for tips or lore, as well as associated images). Care must be taken with the placement of the loading bar, random text and images, since they will **not** scale with the game's resolution (however, the background does have the ability to scale). This script only overrides missions that are inside the loading screen table. (A nightly after July 23, 2018 is needed to use this script)

# Mark Box

This script will allow the mission designer to **highlight** certain ships, wings and subsystems. This script does not do targetting, only highlighting. For ships and wings, brackets will be drawn around the ships at all times. An optional text string will be drawn over a ship if it has been targetted. For subsystems, brackets will only be drawn if the parent ship is targetted. A simple health bar is also drawn next to the subsystem.

A sample mission is included

# Misc Functions

A batch of LuaSEXPs that might come in handy for the industrious FREDder. Stuff like ProxyKill (self destruct a ship while giving credit to someone else), Lockdown (freeze a ship during cutscenes), and a bunch more.

# Prompt Box v2

Get a player response with the prompt box! This new version does away with ugly hud gauges and now draws bitmaps directly to the screen. The method to setting up the prompt box is now made much easier with a single lua sexp being able to initialize, set options, and populate the list of responses. Recalling player responses are now also much easier. Prompt Box v2 should be fully compatible with previous versions. See sexp documentation and the sample mission for more insight into how it all works.

A sample mission is included

# SaveLoadX

A new generation of checkpoint save system. This is in Beta right now and NOT READY FOR PRODUCTION. This works a bit different than the old one and will not be backwards compatible. The goal with this rewrite is to make a completely streamlined process.

# ScrollWrite

Like AxMessage, a system to write a subtitle-like text one character at a time, being a bit more dramatic and stuff for cutscenes.

# SpawnSystem

A system that will spawn a potentially infinite number of ships around an anchor ship. This is meant to be used for arcadey style mods and missions, where you'd rather not spend time placing down tons of fighters in FRED. This will do it all for you!

# Turret Hotkey

A simple script that allows a hotkey targetting functionality work for subsystems. Works pretty well with the MarkBox script!

# Waypoint Assist

A script that assists the FREDder guide a player through waypoints. The FREDder specifies a waypoint path and a marker object, and the system will keep moving the marker object to the next waypoint when the player gets close. There's also LUASexps for telling when the waypoint is done, or how far along they are.
