# SpellForce Editor
Welcome to **SpellForce Editor**, a set of tools made with the intention of enabling users to modify and enhance their experience with **SpellForce: The Order of Dawn** and its two expansions - **Breath of Winter** and **Shadow of the Phoenix**. This page will shortly describe each tool available in the application.

## GameData Editor
**GameData Editor** allows you to modify the main database of the game - **GameData.cff**. This file contains, among others, information about all text entries in the game, all unit stats, their equipment and spells, spell data itself, available races, and more. All data in the database can be modified.

## Asset Viewer
You can use **Asset Viewer** to preview 3D models, animations, music and sounds contained in the game files. This tool browses **game PAKs** to find and display game content, and it allows you to extract the content from the PAKs.

## Map Editor
There already exists an official map editor, but only computers with AMD processors and Intel processors pre-i3 era can run it, which means that many of modern PCs can't run it. This **Map Editor** is guaranteed to run on any PC which meets requirements at the end of this page - and it can open and edit official campaign maps!

## Mod Manager
**Mod Manager**'s purpose is to allow you to painlessly switch between original version of the game and any installed mods. **Mod Creator** allows you to create mods that can be managed by this Manager.

## SQL Modifier
A complementary tool for GameData Editor, **SQL Modifier** allows you to edit some of the **Lua scripts** responsible for additional per-entity data (for example, chest item appearance in the game). It also comes with **Lua 4.01 Decompiler**, for when you want to edit scripts manually.

## Requirements
.Net Framework 4 or higher
OpenGL 3.3 or higher
2 GB of RAM
It is recommended that you have **[Dragon UnPacker](https://www.elberethzone.net/dragon-unpacker.html)** extraction tool - while SpellForce Editor is able to extract files from the game PAKs, it doesn't have an option to do this explicitly.
Some of the tools require you to **specify game directory** - simply provide it with the path to the game folder, and the application will do the rest.

## Additional information
When you run the SpellForce Editor, the application checks whether there's a new version available - it will signalize you if that's the case.

After you specify game directory, **pakdata.dat** will be generated. Don't remove this file, as it speeds up loading files from game PAKs substantially.

**config.txt** contains various settings for many different things in the editor. Check it out, maybe you'll find something interesting there!

After you close the SpellForce Editor, **UserLog.txt** is generated, which contains details on nearly every operation the editor performs. When the editor closes unexpectedly due to an error, it will also contain details of the error.
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTQ2NzEwNDA2XX0=
-->