# Textures editor mode
Using this mode, you can bring color to your freshly built. barren terrain. You can set up which textures will be used, define custom tiles made by mixing textures together, and mode.

## User interface
![enter image description here](https://lh3.googleusercontent.com/NHbQ8fW-S4ymdEcd7iN3-BK22cRLQKeeZreFmFMe9fFc6NLXGHEuu_7_sqqddXKYDUf4NAwgoqdd)
1. Base textures panel
2. Tile panel
3. Paint brush

### Base textures panel
Maps come with predefined 32 textures used to paint the terrain with and create custom tiles from. Click any of the textures, then edit "Texture ID" field to change the base texture. Texture ID can take values from 0 to 119. If you provide invalid value, the field will turn **red**, and the texture will not be changed.

If you want to preview all available base textures, right now there's no option to do that in editor. You can use Dragon UnPacker to open file pak\\sf1.pak, and look at all textures named landscape_island_*.dds, as those are used in editor and in game to paint terrain.

You should not change the first of 32 base textures, as it's used by game to denote areas submerged in ocean. Changing it might give unpredictable results.

### Tile panel
When you paint the terrain, you don't use textures, but **tiles**.
#### Tile list
There is a total of 255 tiles defined in map file. Each tile contains texture data, texture weighting and whether the tile blocks movement/vision or not. However, SpellForce gives special meaning to some tiles.
- Tile 0 is the ocean tile.
- Tiles from 1 to 31 are base tiles, each made up of exactly one base texture corresponding to the ones in base texture panel.
- Tiles from 32 to 223 are custom tiles, and are made of up to 3 base textures mixed together.
- Tiles from 224 to 254 are hidden on the list, but they are internally the ones painted on the map whenever you use tiles 1-32. They are just copies of tiles 1-32, so don't worry about it.
#### Tile mixing
Tiles from 32 to 223, as denoted above, are custom tiles, and only those can use tile mixer. You can specify up to 3 base textures, together with weights, to mix the textures and define a new tile. Weights should sum up to 255.
Note: Currently tile preview only shows mix of two first textures. The textures are still correctly mixed in game.
#### Tile flags
Tiles can be set up to block movement and/or vision. You can create natural walls using impassable tiles, which is pretty useful.

### Paint brush
You use brush to paint on terrain - whether it's height paint, texture paint, or anything else.
#### Size
Radius of the brush. The larger the size, the bigger the area affected by brush.
#### Shape
Currently, brush supports 3 shapes: **Square**, **Circle**, **Diamond**. Circle is the default shape, and is usually enough for most cases.
#### Interpolation mode
This is unused.
#### Match movement flags
A special property of paint brush, it allows you to paint only on terrain which blocks movement, or only on terrain which doesn't block it, depending on whether the tile you paint with blocks movement or not. Very useful when you have already painted mountains with one tile, but want to change the tile to another type.

## 3D display controls
Use LMB to paint the terrain with chosen tile. Press RMB to set tile to paint with based on tile at the 3D cursor position.

## Slope-based paint
A special painting tool exists for modifying the look of the map. Slope-based paint tool can be found under **Tools->Slope-based paint**. It is used to paint whole map depending on how steep the terrain is.
![enter image description here](https://lh3.googleusercontent.com/l4cqFrwZmxyd2W0yCD9Xb6RlMxNW1Oy1DCT3BvkyOrwC3r4lH4GAxDLGS1YMXeL3UHN1s5lQr0mi)
### Slope threshold
You can set threshold for the paint tool, which is used to determine which one of the groups will be used to paint on the specific parts of the map. Angle varies between 0 and 90 - 0 meaning only the **tiles above threshold** group will be used for painting, 90 meaning the same but for the **tiles below threshold** group, and anything inbetween will use both of the groups depending on terrain slope.

The two groups share the same parameters. Click the **+** button to add a new tile type to the group, click on tile to remove it from the group.
### Tile ID
The ID of the particular tile in the group. It can take values from 1 to 223, just as the tiles on tile list.
### Weight
The weight of the particular tile in the group. It can take any integer value greater than 0.

When you're done setting up groups, click on **Apply** button to paint the terrain. The process goes as follows:
- If the angle between terrain and the horizontal plane is lower than slope threshold, **Tiles below threshold** group is used to paint the terrain. Otherwise, **Tiles above threshold** group is used.
- When a group is determined, a tile type is chosen randomly from the group, depending on weights. In the example above, tile ID 19 has weight 1, and tile ID 2 has weight 3. This means that the terrain will be painted using tile ID 19 with probability 1/4 = 25%, and tile ID 2 - with probability 3/4 = 75%.
![enter image description here](https://lh3.googleusercontent.com/MDv8VBGZTX2BUcY51fmy-ygYfJHgrtCuDH_vYyYk_tnXyJJ_4seSf3pmMutuHON_jA1bD_jTxNCX)

## Additional information
Editor Status shows terrain tile at the 3D cursor position while you're in Textures editor mode.

You can't paint terrain with height set to 0 - it will be automatically painted with tile 0.

In addition to assigning visibility flag to tiles, SpellForce determines visibility by checking if terrain itself obstructs vision of a unit. You don't _need_ to set the flag - simply modify the heightmap.
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExODA3NDY1MTFdfQ==
-->