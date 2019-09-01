# Lakes editor mode
Compared to previous modes, this one is very simple. It allows you to add and remove lakes, and to change lake types.

## User interface
![enter image description here](https://lh3.googleusercontent.com/E9NtasRPpbsaShuSfvsOs9WPpSHeZHU6gVBSBO9D1IOHkpO5pDHU3Be8sq2cl9k7SKoxlostd5gq)
1. Selected lake panel

### Selected lake panel
This panel is enabled only when a lake is selected.
#### Internal depth
Read-only. Depth of the lake at its deepest point.
#### Lake type
You can change appearance of the lake by changing its type. Available types: **Water**, **Swamp**, **Lava**, **Ice**.

## 3D Display controls
Use LMB on a terrain which is not submerged in lake to create a new lake. The lake will flood all neighbouring terrain below the terrain at 3D cursor position. If the terrain is flat as a pancake, the water will have nowhere to go, and the lake will not be created. Therefore, you should click on sloped terrain for desired results.
Any existing lakes which make contact with the new lake are assimilated into the latter.

Use LMB on a terrain submerged in lake to select that lake.

Use RMB on a terrain submerged in lake to remove that lake.

Use RMB anywhere else to deselect any selected lake.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk5NDE3Njk5MV19
-->