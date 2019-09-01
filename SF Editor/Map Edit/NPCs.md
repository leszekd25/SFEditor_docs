# NPCs editor mode
For coop-type maps you don't usually need to deal with any NPC stuff. However, if you want your entities to exhibit special behavior, you need to provide a script for that entity. Such script will only be executed if the entity has assigned NPC ID. This editor mode allows you to view all NPCs on the map and manage them.

## User interface
![enter image description here](https://lh3.googleusercontent.com/9SnQi-97XLUXnkQLtMinvXcut0j3epV0_5QHakdddGTSB50gQlgnSOZCn8oPabI6WBze8Q_mGjWF)

## Open platform script
When SpellForce loads a map, it must first determine its platform ID. Platform contains all scripts that can be executed on the map, including all scripts assigned to NPCs on the map. If you want to see what's your map's platform ID, search for your map name in category **38. Map data** in GameData Editor. Map ID corresponds directly to its platform ID.

Using this button will load in a list of all scripts which belong to the platform. Select any of them to open the script in your favorite Lua editor. If the script is not found in game directory where it's supposed to be, it is extracted from game PAKs, decompiled using Lua 4.01 Decompiler, and placed in the expected place in game directory.

## NPC ID
You can change NPC ID of any NPC on the map. Be wary though - the previously assigned NPC script will no longer work, unless you rename it to reflect the NPC ID.
This is a gamedata link field - right-click it to see the NPC data in GameData Editor, provided that you have the editor already open.

## Create new ID
Using this option, you can replace selected entity's NPC ID with a new, unassigned NPC ID. This modifies the currently loaded in GameData.cff.

## Go to properties
Depending on the entity type of selected NPC, this option will change editor mode to **Units**, **Buildings** or **Objects**, and select the entity in the inspector.

## Remove
Removes NPC ID from the map. Does not remove the selected entity from the map! It only changes its NPC ID to 0.
This also does not remove the NPC entry in GameData.cff, unless the NPC was created before GameData.cff was saved.

## Open NPC script
Opens the script for selected NPC in your Lua editor. If the script is not found in game directory where it's supposed to be, it is extracted from game PAKs, decompiled using Lua 4.01 Decompiler, and placed in the expected place in game directory. If the script also does not exist in game PAKs, you will be asked whether to create a new script for the NPC (usually the case for newly assigned NPC IDs).
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ5Nzc1ODc3OF19
-->