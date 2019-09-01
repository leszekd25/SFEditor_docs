# sql_item.lua Editor
sql_item.lua contains visual information for every wearable item in the game, as well as additional info of unclear purpose...

## User interface
![enter image description here](https://lh3.googleusercontent.com/nHfpJBzBpEXHmJMH0jpTEDl5h9fXW0Jxb2IWdGfbP8BWfJr2knM6jSSS058EYRNk_GlhZE1aO8u1)
### Item list
All items in the game are listed here. Select an item to edit its parameters.
You can change **item ID** in the field below the list (though it isn't advised for existing items), add new item using **Add** button, or remove selected item using **Remove** button.

### Mesh
Each item has defined up to 4 variants of its mesh. It should be the filename of the mesh file in **mesh** and, in some cases, **mesh\\skinning** directory, without the .msb suffix. If the item isn't a chest piece, leg piece, head piece, weapon or shield, it should be left empty, which is indicated by **\<undefined\>**.
These are the variants:
- Mesh (male cold)
- Mesh (female cold)
- Mesh (male warm)
- Mesh (female warm)

Army units specify all 4 variants for their chest piece. It determines which color the unit is. Useful for team colouring.
Chest pieces and leg pieces (wearable by the avatar and rune heroes) have Mesh (male cold) and Mesh (male warm) specified with the male version of the mesh, and Mesh (female cold) and Mesh (female warm) specified with female version of the mesh.
Other items only have Mesh (male cold) and Mesh (male warm) specified, with one mesh.

### Animation set
If your item is a chest piece or leg piece, you must provide the animation set name. For example, animation set for the avatar is figure_hero. Each enemy type has a different animation set.

## Additional information
If you have GameData Editor open with GameData.cff loaded in, item names will be displayed on the item list in this editor.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ0NjQ0MzkxM119
-->