# Terrain flags editor mode
While terrain tiles can have optionally set movement and visibility flags, you can set custom flags in this editor mode. This is sometimes a necessity - many objects in game don't have built-in collision mesh and units would simply pass through these objects, were it not for the custom flags.

## User interface
![enter image description here](https://lh3.googleusercontent.com/-km0wvF6E_KUniRlcuy25Azqv5JU8vAstJ3XVurZEW3hc0LirYEPh1UFj9Xq0p8dZeFIqPv0Aaxk)
1. Flag visibility
2. Flag brush
3. Flag mode

### Flag visibility
You can turn on and off flag display for both movement and visibility flags. Tile movement flags are **maroon**. Custom movement flags are **bright red**. Custom visibility flags are **bright yellow**.
As for now, there are no tile visibility flags - it appeared that not a single official map uses those.

### Flag brush
You use brush to paint on terrain - whether it's height paint, texture paint, or anything else.
#### Size
Radius of the brush. The larger the size, the bigger the area affected by brush.
#### Shape
Currently, brush supports 3 shapes: **Square**, **Circle**, **Diamond**. Circle is the default shape, and is usually enough for most cases.
#### Interpolation mode
Unused.

### Flag mode
There are two modes: **Movement** and **Visibility**. You can set custom flags depending on which flag mode you are in.

## 3D display controls
Use LMB to set custom flags on terrain according to flag mode. Use RMB to remove custom flags from terrain according to flag mode.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3MDI2MjQzMDldfQ==
-->