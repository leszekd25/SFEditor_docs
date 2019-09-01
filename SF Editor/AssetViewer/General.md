# Asset Viewer general information
Asset Viewer allows you to see all 3D models and animations used in the game, as well as listen to game music, sounds and voiceover. It also has options to extract currently viewed assets and to synchronize with GameData Editor.
Game directory has to be specified before using this tool, since it uses game PAKs to load resources in.

## User Interface
Here's a short description of Asset Viewer interface.
![enter image description here](https://lh3.googleusercontent.com/cwjjmJeh5WerFVV44-kKsYqVFWqT8OOFHGmR9VULphz6zyciVAWm6fawg1Ztc4pOHe-zr2ylduYP)
1. Viewer mode
2. Primary item panel
3. Animation/sound player
4. Secondary item panel
5. Viewer Status
6. **3D display**

## Viewer mode
There are 6 available modes, listed below.
### Mesh
When you select Mesh viewer mode, primary item list fills up with all meshes found in game PAKs. Select an item from the list to show the mesh on the 3D display.
### Animation
Selecting Animation viewer mode activates animation player. Primary item list fills up with all animated meshes found in game PAKs. Selecting an item from the list fills up secondary item list with all animations _potentially_ fitting for the selected items, and shows the animated mesh on the 3D display. When you select an item from the secondary list, the selected animation will play (if it fits the animated mesh).

Note: Sometimes Asset Viewer can't find any animation suitable for the selected animated mesh, or it finds animations which do not fit the mesh. This is a limit of the application: it uses file names to find animations for the mesh, and some file names don't follow the expected pattern.
### Synchronize with GameData Editor
This is a special viewer mode. Selecting it clears everything from Asset Viewer. Instead, it will display models and animations, depending on what is currently selected in GameData Editor.
![enter image description here](https://lh3.googleusercontent.com/mfDh68_Bv5BU04UNCaSLN96WTDKCVOHV-R7xQXm39FIpDWMJ5b89KREQeILjd5Wfel4z6C4nFNVS)
When you select any element in GameData Editor while Asset Viever is in synchronization mode, the viewer will display the selected element (whenever possible). If the selected element is an animated object (a military unit, for example), animation player is activated, and the secondary list fills up with any suitable animations found for the object.
### Music
Selecting Music viewer mode activates sound player. 
Upon selecting Music viewer mode, primary item list fills up with all music pieces found in game PAKs. Selecting an item from the primary list loads the music piece. Click "Play" on sound player to listen to music.
### Sounds
Selecting Sounds viewer mode activates sound player.
Similarly to Music viewer mods, primary item list fills up with all general type sounds (not voiceover) found in game PAKs.
### Messages
Selecting Messages viewer mode activates sound player.
In addition to selecting this mode, you must also specify message type to load in items. Available message types:
- Male
- Female
- RTS Workers
- RTS Battle
- NPC

After you select message type, primary list fills up with all sounds belonging to the type found in game PAKs.

## Primary and secondary item panels
In addition to displaying list of items depending on viewer mode, the panels contain an "Extract" button. Using it will extract all assets displayed/played currently in the viewer to the SpellForce Editor directory, respecting SpellForce directory tree. 

For example, if you extract a building from game PAKs, two folders will be created in GameData Editor directory: "mesh" and "texture". 3D building model will land in "mesh" folder, while its textures will end up in "texture" folder.

## Animation/sound player
After you open an animation or sound in Asset Viewer, you can use this player to control the played resource. It's pretty straightforward: "Play" plays/resumes the animation/sound, "Stop" stops the animation/sound. Dragging the scroll bar will set the animation/sound time to a given value.

## 3D display
When you select a mesh or an animated mesh, or use synchronized viewer mode, this is where the 3D resource will be displayed.

While you hold Left Mouse Button over the display, you can move around the camera. Controls:

 - W: move camera forward
 - A: strafe left
 - S: move camera backward
 - D: strafe right
 - Move mouse around: change camera angle

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExODg0MDg2NzddfQ==
-->