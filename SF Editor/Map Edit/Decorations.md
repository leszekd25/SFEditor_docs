# Decorations editor mode
Decorations (decals) are those small patches of grass, mushrooms and flowers on the ground. They are different from textures in that they're 3D models. In this mode, you can manage decoration groups and add/remove decorations on the map.

## User interface
![enter image description here](https://lh3.googleusercontent.com/VLxXw75ti0uc4d5-SyqYLmuwQItU3XLwWePivHOOtExxgWhF0o_s9Hs4JBk7SWuM3zQ5WMKpfxsI)
1. Decal brush
2. Decoration group manager

### Decal brush
You use brush to paint on terrain - whether it's height paint, texture paint, or anything else.
#### Size
Radius of the brush. The larger the size, the bigger the area affected by brush.
#### Shape
Currently, brush supports 3 shapes: **Square**, **Circle**, **Diamond**. Circle is the default shape, and is usually enough for most cases.
#### Interpolation mode
This is unused.

### Decoration group manager
There are 255 decoration groups available. Each decoration group contains at most 30 decoration types.
#### Decoration group list
Selecting a group from the list will display all decoration types for this decoration group on the decoration type list. It will also mark all places where the selected group is used on the map with a **magenta** color.
 If the group has no types assigned to it, the group is marked as **Unused**. 
First group (**No group**) is special - it denotes areas where no decoration group is assigned.
#### Decoration type list
Selecting a type from the list will allow you to modify type parameters. You can add an empty type to the list using **Add** button, and remove selected type using **Remove** button.
#### Decoration ID
Decorations use the same ID as objects. Check **34. Environment objects data** in GameData editor for available objects.
#### Weight
Currently unused in Map Editor, since it's not known what exactly this is for. Leave at 255 for a good measure.

## 3D display controls
Use LMB to paint areas with decoration brush. If you want to clear decorations, select the **No group** group.
Use RMB to select the group that's used on the map at the 3D cursor position.

## Additional information
Editor Status shows decoration group used on the map at the 3D cursor position while you're in Decorations editor mode.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA2NzgxOTY3Nl19
-->