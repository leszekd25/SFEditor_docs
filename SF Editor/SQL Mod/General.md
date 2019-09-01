# SQL Modifier general info
In addition to GameData.cff and various game assets, you can also add and edit scripts to alter the gameplay. SQL Modifier provides interface for modifying some of the important visual gameplay data - for example, coop game monster spawn types or item models displayed in game.

However, SpellForce.exe distributes its scripts in a compiled form, which means you're unable to edit the scripts in a text editor. To solve this problem, SpellForce Editor comes with Lua Decompiler 4.01, which can turn these compiled scripts into (relatively) readable and editable - but most importantly, *working* - Lua scripts.

See the following pages about SQL Lua scripts editable from the editor:
- GdRtsCoopSpawnGroup.lua
- sql_item.lua
- sql_object.lua
- sql_building.lua
- sql_head.lua

All of the above use scripts from game directory script folder. If the scripts are not found, they're first extracted and decompiled.

See the following page to understand how decompiler works:
- Lua Decompiler 4.01


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODk1MjY1MTFdfQ==
-->