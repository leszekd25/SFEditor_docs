# Units, Buildings, Objects editor modes
Anyone who played SpellForce at least once knows what each of those three are. Here they will be collectively referred to as **entities**. Entities are the main aspect of gameplay. Map Editor allows you to do anything with entities.

User interfaces of all 3 modes are similar, but there are slight differences. Therefore, these symbols will signalize which mode a particular feature belongs to:
- (U) - units
- (B) - buildings
- (O) - objects

## User interface
![enter image description here](https://lh3.googleusercontent.com/AKpvJTvpLviXGKbRHfNAaccEemlmlgDgD8Iz8pq0fhkL2Vzk9ZD34sA13xtT_eaKfPOGdCqW_8PA)
1. Placement panel
2. Selected entity panel
3. Entity list

### Placement panel
#### Entity to place
You can specify entity ID to place on the map using this field. As you can see, it is a gamedata link field - right clicking it will display the entity data in GameData Editor, but only if it's already open.
#### (U) Race, (U) Unit
Units editor mode allows you to specify entity ID in a more friendly way. Select race from the Race menu, and select any unit that belongs to selected race using the Unit menu. Entity ID will be automatically specified.

### Selected entity panel
All entities share some of the parameters.
#### Entity ID
Changing this will reload the entity, which will become apparent in 3D display.
#### NPC ID
Each entity can be optionally assigned NPC ID. You can do this in two ways.
1. Simply set the NPC ID manually in this field.
2. If the NPC ID is not set (value is 0), you can right-click this field to assign a new, non-colliding NPC ID. An entry will be created in GameData.

If NPC ID is assigned to the entity, you can right-click the field to move to NPC inspector.
#### Position
Read only, the XY coordinates of currently selected entity are displayed here. To move the unit, see 3D display controls.
#### Angle
You can change initial angle of selected entity by changing this value You can assign angle manually, or you can use the slider.

The following parameters are unique to specific entity type.
#### (U) Group
It is not yet known what this parameter is supposed to do...
#### (B) Building level
Depending on the level, the building will have more HP. Level range is the same as usual units.
#### (B) Race
You can optionally assign custom race to the building. Useful when you want to make sure units on the map don't attack this building accidentally.

Additionally, there are unknown paramaters, of which functionality is yet to be determined.

### Entity list
When you switch editor mode to any entity mode, a list of all entities of given type is displayed. You can click on any entity on the list to select it and move the 3D display to the position of the entity. Additionally, a simple search tool is provided.
#### Find next
Searches for a next entity on the list, searching forward, of which name matches the search string.
#### Find previous
Searches for a next entity on the list, searching backward, of which name matches the search string.

## 3D display controls
Click with LMB to select an entity under the 3D cursor. If no entity is under the cursor, a new entity will be created at the 3D cursor position, accordingly with placement panel parameters.
Click with LMB over a selected entity and drag the mouse to move entity around the map.
Click with RMB over any entity to remove it from the map. If the entity is assigned an NPC ID, it will also be removed from map data (but not from GameData, unless this NPC was created before GameData.cff was saved).

## Additional information
Buildings and some objects have additional collision mesh assigned, but it is currently not taken into account when determining whether you can place an entity in a given place or not. Take extra care when placing buildings.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg3MzEyNTMxNV19
-->