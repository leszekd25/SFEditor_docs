# Creating maps
Using Map Editor, you can create your own maps from scratch. Click **File->Create new map** to do it.

## User interface
You can specify parameters which alter the base look of the map.
![enter image description here](https://lh3.googleusercontent.com/Gl252KLxitrhw3DeCmu_Jj6QbAHcjAFn7kErjCAjuY5lK_ndVcQgbcJ1a5JjSRW4A8E2AY_h0jsV)
### Size
There are 3 sizes available: **256**, **512**, **1024**. Each describes dimensions of the map - NxN, N being size. It doesn't really matter though - SpellForce automatically clips map size to its minimum upon loading. Just make sure the size is big enough to fit all you want to place on the map. Usually there's no need to use size bigger than 512.
### Generate base for terrain
You can optionally request a base terrain for the island that your map is going to be. It's a simple process, which nevertheless allows you to modify a variety of parameters to change the look of the base.
Note that it is just a base for the terrain - no mountains, no lakes, no entities placed on the map. And no textures.
#### Base terrain height
You can specify base height of your map - it sets height of all terrain on the map to specified value.
#### Erosion cell size
After setting base height, generator will attempt to erode edges of the map to make the terrain look more like a natural island. Erosion happens in blocks, and cell size determines how big a single block is.
#### Erosion offset
Generates a square ring of ocean around the island, equal in size to block size multiplied by offset value. Setting to 0 generates no ring, so you might want to leave it at a non-zero value.
#### Erosion strength
Defines how strong the erosion will be on each axis. Erosion happens randomly, but this parameter allows you to set how strong _on average_ the erosion will be. Erosion size on map is on average equal to erosion strength multiplied by block size.
#### Erosion variance
The higher this value is, the more the particular erosion values are likely to deviate from average erosion strength.
#### Erosion blur size
After erosion is generated, the generated erosion grid is layered over the heightmap of the terrain to affect the terrain. You can blur the erosion grid prior to this operation to make the erosion look more smoothly. Blur affects erosion grid on block level, so the blur size value should be small (1 is usually enough, more than 3 can be slow).
#### Erosion blur strength
The higher this value, the more the grid is blurred. Usually 1.0 is a good value, though nothing stops you from experimenting.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMjM1OTI2NjddfQ==
-->