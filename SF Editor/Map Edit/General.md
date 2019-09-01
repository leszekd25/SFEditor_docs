# Map Editor general information
While there already exists an official Map Editor, it can't be run on modern Intel CPUs (i3 and later). Moreover, it can't modify maps provided within SpellForce installation (which means you can't edit campaign maps, for example - only open and view). At least not without special modification. SpellForce Editor comes with **Map Editor**, which bypasses both issues completely. 

## User Interface
Here's a short description of the Map Editor interface.
![enter image description here](https://lh3.googleusercontent.com/tcg3QTpubEoVU1n90MZsk1pvIp8_tTXOzq6Xf6IhgEiLaGX5WwDsYGEnXardQ5ivV4m-SgBl-_AS)
1 - Opened map file
2 - Menu bar
3 - Editor mode selection
4 - Inspector
5 - 3D display
6 - Editor Status

## Menu bar
Menu bar contains the following menus: File, Tools.
### File
#### Create new map
Choosing the option will bring **Map Creator** tool into view. More on creating maps on page **Creating maps**.
#### Load map
Loads selected map into the editor. If you have a map already open, you will be prompted to save the current map.
Loaded maps are stored in-memory, so there's no risk of _accidentally_ overwriting existing maps.

After you load a map, and only if GameData Editor is open, Map Editor attempts to synchronize with GameData Editor. If you have another game data open in GameData Editor already, you will be prompted to save it. Cancelling this operation fails the synchronization attempt and closes the currently loaded map. After synchronization succeeds, you can edit GameData.cff currently in data folder of your SpellForce directory.
#### Save map
Saves currently open map under specified name. If GameData.cff was modified meanwhile, it will also be saved.
#### Close map
Closes currently open map. You will be prompted to save the map before closing.
#### Exit
Closes the editor. You will be prompted to save the map before closing.

### Tools
There's currently only one tool available.
#### Slope-based paint
This tool allows you to automatically texture the map, depending on the local slope. It's meant to speed up the process of painting the map, as they might grow large in size and painting every bit of terrain manually might be tedious work. More on this tool in **Textures** page.

## Editor mode selection
Map Editor allows you to edit nearly every aspect of the map, and it would quickly get bothersome to have to constantly keep everything in mind while editing. There are currently 11 editor modes, each helping you perform a specific task. The modes are listed below, and each mode has a dedicated page.
### Heightmap
Every map is build upon a terrain generated from a heightmap. This mode enables you to edit the terrain height with a variety of tools.
### Textures
In addition to height data, each map is provided with texture data. In this mode, you can paint terrain with a variety of textures.
### Terrain flags
In this mode, you may optionally designate some parts of the terrain to become impassable and/or to obstruct vision of in-game units.
### Lakes
All maps are surrounded by an all-encompassing ocean, but you can place additional water bodies on the map, called lakes. This mode serves as a lake tool.

The next 3 modes are similar to each other, so they will share the same page.
### Units, objects, buildings
Without units, objects and buildings, maps would become barren, and the game probably boring, as you couldn't be able to do anything of interest. These three modes allow you to edit these entities on the map-level.
### Decorations
While textures paint the map terrain, decorations - mushrooms, patches of grass, plants - give it a lively look. You can place and edit them in this mode.
### NPCs
Campaign maps are full of NPCs - if you want a unit or an object to exhibit unusual or special behavior, you must assign it a NPC ID. This mode serves as a manager of all NPCs on the map.
### Miscellaneous objects
This mode allows you to edit monster camps, bindstones, hero and army monuments, and portals.
### Metadata
In here you will find everything that functions over the usual gameplay - global spawn parameters, player starting locations, and multiplayer team compositions.

## Inspector
Each mode uses a different inspector, which usually contains parameters you can edit to alter appearance of selected entities, or behavior of **3D cursor**. Each editor mode page describes its own inspector.

## 3D display
Taking over half of the editor interface, 3D display shows you what your map looks like at the given moment. You can move around the map by holding Middle Mouse Button and moving mouse around. You can also zoom in and out by using Mouse Scroll.
While Mouse Cursor hovers over the 3D display, 3D cursor (a **bright yellow** beam) is shown on the map, which indicates where an operation will take place.

## Editor Status
Usually it shows you 3D cursor position on the map. Depending on editor mode, it will show additional information.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY4NzQwNzk2Nl19
-->