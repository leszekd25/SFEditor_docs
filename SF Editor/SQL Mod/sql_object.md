# sql_object.lua Editor
sql_object.lua contains visual information about all objects in the game - mainly which meshes they consist of. You can edit it in this editor.

## User interface
![enter image description here](https://lh3.googleusercontent.com/YioWF5nPPKNvZozAJ7qMpnuS5k68_I8ZBOdsLvjYk3gGppjmYo69dKX8hR-_8FtlITQ7iaoLB_0f)
### Object list
All object that can be placed in the game are listed on this list. Select an object to edit its parameters.
You can modify **object ID** in the field below the list, add new objects using **Add** button, or remove selected object using **Remove** button.

### Name
Name of the selected object. Not used anywhere - objects are already named in GameData.cff.

### Mesh files
Each object has one or more meshes it consists of. They're listed on the mesh list. Each mesh name is the name of the mesh file in **mesh** directory. 
You can add, remove or change meshes on the list.

### Casts shadow?
True if the object casts shadow in game, False otherwise.

### Scale
Scale of the object in game in relation to base scaling of the meshes it consists of.

### Selection size
Radius of the object selection as displayed in the game and in the editor.

## Additional information
If you have GameData Editor open with GameData.cff loaded in, object names will be displayed on the object list in this editor.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzUwMDU4MzFdfQ==
-->