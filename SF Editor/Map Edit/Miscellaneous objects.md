# Miscellaneous objects editor mode
In Spellforce, there are special objects which are interactive, but not scripted in usual Lua way. These are: **Coop camps**, **Bindstones**, **Portals** and **Monuments**. This editor mode manages them all.

## User interface
![enter image description here](https://lh3.googleusercontent.com/bUFF0TvzeSUkONZwtgAw3wMPLR_F-MW_-zrzCr9Xek-ntmFCU9X-z-msSJFSgEcEQ4d_BSJWMaaE)
### Edit mode
You need to select edit mode to be able to place these special objects.

Each of the following panels always contains **Object list**. Selecting an object from such list allows you to edit its parameters. It also centers the 3D display on the object, and switches the edit mode to an appropriate one.
Each object type has a read only **Position** parameter, which is modified through 3D display controls.

### Coop camps
Coop camps should only be placed on Coop type maps. They are displayed as **purple** circles on the map. Any building within that circle is automatically assigned to the coop camp, and in game you must destroy all assigned buildings to remove the camp from the map.
#### Type
Sets a type of the selected coop camp. Types can be viewed and edited through the **Edit types** option, which is the same as **GdRtsCoopCampSpawns.lua** option in the SQL Modifier.

The remaining 3 edit modes all share the **Angle** parameter, which modifies the angle of selected object.
### Bindstones
In campaign mode, bindstones are used as checkpoints, means of fast travel. In coop and multiplayer mode, bindstones are used as player spawns.

### Portals
Portals are two-way bridge between maps. A special **Portal to Exit** exists, which is used exclusively in Coop maps.
#### ID
Sets the portal ID of the selected portal. To see available portal IDs, check category **39. Portal locations** in the GameData editor. 

### Monuments
Monuments are the core of RTS part of SpellForce. You spawn army and hero units at monuments.
#### Type
There are 7 monument types available: **Humans**, **Elves** , **Dwarves**, **Orcs**, **Trolls**, **Dark Elves** and **Heroes**. Changing the type of selected monument will reload it.

## 3D display controls.
"Object" here refers to an object of type that matches the currently selected edit type.

Click with LMB to select an object under the 3D cursor. If no entity is under the cursor, a new object will be created at the 3D cursor position, accordingly with placement panel parameters.
Click with LMB over a selected object and drag the mouse to move the object around the map.
Click with RMB over any object to remove it from the map.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg3MjA3Mjg1NF19
-->