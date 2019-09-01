# GdRtsCoopSpawnGroup.lua Editor
When you place a coop spawn on your map using Map Editor, you can specify the type of the spawn. Each spawn type must be defined in GdRtsCoopSpawnGroup.lua file found in **script** directory of your SpellForce game. This editor allows you to modify the file in an intuitive way.

## User interface
![enter image description here](https://lh3.googleusercontent.com/3BJq6yY-riD2P1ERI4P1OBaKtBOmyqz12Lwvp-fZfLirvfCbtDiecVggL9LxDNkwOEqLzFnUFRbI)
The editor is divided in 4 parts.
1. Spawn type list
2. Spawn type parameters
3. Spawn type wave list
4. Spawn type wave parameters

## Spawn type list
All types defined in the script are listed here. You are not allowed to remove any defined spawn type from within this editor - you can only add new types using **Add new spawn type** button, or edit existing spawn types. Select a type from the list to edit its parameters. 
Spawn types are automatically numbered sequentially from 1 onwards. While it is possible to add types numbered above 255, it is not advised so, because the game can only read types from 1 to 255.

## Spawn type parameters
### Name
Name of the spawn type, as displayed on the coop spawn list in Map Editor while in Miscellaneous objects editor mode.
### Level range
Not really used, but required. Displays level range of the units spawned from the map. You can set it to anything as it has no effect whatsoever.
### Goal
AI in game has many defined behaviors available to use. However, in the original script all camps are either **GoalCoopAggressive** or **GoalCoopDefensive**, so it is advised to use those.
### Max clan size
Maximum number of units allowed from a camp of this type. This includes units spawned initially in the camp. Units won't spawn if there are as many (or more) units in the camp than defined in this field.
### Starting units
You can define units which are created on map load. These units will stay in the camp no matter what and will protect it.
Type **unit ID** (as seen in **18. Unit general data/link with unit stats** in GameData Editor) in the gamedata link field below the **starting unit list** and click **Add** to add a new unit.
Select a unit from the list to either modify its unit ID or to remove it using **Remove** button.

### Spawn type wave list
Each spawn has defined several waves which generate units over time. A wave consists of start time, wave spawn period and units per wave spawn.

Example: a hypothetical spawn type has defined two waves: wave A and wave B.
Wave A starts 5 minutes into the game, has period of 2 minutes and generates two units: unit X and unit Y.
Wave B starts 8 minutes into the game,  has period of 1 minute and generates one unit: unit Z.
Here's timeline of events for your spawn:
Minute 5: spawn unit X and Y (wave A)
Minute 7: spawn unit X and Y (wave A)
Minute 8: spawn unit Z (wave B)
Minute 9: spawn unit X, Y and Z (wave A and B)
Minute 10: spawn unit Z (wave B)
Minute 11: spawn unit X, Y and Z (wave A and B)
And so on...

Select a wave from the **spawn type wave list** to edit its parameters. You can change **wave start time** below the list, you can add new wave at specified time using **Add** button, or you can remove selected wave with **Remove** button.

## Spawn type wave parameters
### Wave period
Set selected wave spawn period here. You can specify hour, minute and second.
### Units
You can define units which are created on wave spawn.
Type **unit ID** (as seen in **18. Unit general data/link with unit stats** in GameData Editor) in the gamedata link field below the **starting unit list** and click **Add** to add a new unit.
Select a unit from the list to either modify its unit ID or to remove it using **Remove** button.

## Apply
When you're done with the changes, click Apply button to save changes and close the editor. If the script is not found, it will be created. Closing this editor through any other method will **not** save the changes.

## Additional information
If you have GameData Editor open with GameData.cff loaded in, unit names will be displayed on the unit lists in this editor.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgzNDE2NTc0Ml19
-->