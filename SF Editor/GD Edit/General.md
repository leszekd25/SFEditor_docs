# GameData Editor general information
GameData Editor is a tool to use when you want to make modifications to SpellForce gameplay - whether it's Fireball damage, Shadowblade weapon effects, Ogre level or anything number- or text-related.
Game directory doesn't have to be specified in order to use this tool.

## User Interface
Here's a short description of the GameData Editor interface.

![enter image description here](https://lh3.googleusercontent.com/a0HAwkbCDcYcxT-K-VRf-JmHL_MLFnxUd0XoI5v0hA4Df9M520M4_X_zk1mtMRtDJf4_CSIVSRs4)
1 - Opened GameData file
2 - Menu bar
3 - Selected **category**
4 - Modification panel
5 - **Elements** contained within selected category
6 - Search utility
7 - Editor Status
8 - **Backtracking** panel (unused here)
9 - Selected element inspector
10 - Selected element description and additional information

## Menu bar
Menu bar contains the following menus: File, Edit and Special.

### File
#### Open GameData.cff (Ctrl-O)
Select and open GameData file to edit. If there's another GameData file already opened and it was modified, you will be prompted to save the file before it's closed.
Loaded game data is stored in-memory, so there's no risk of _accidentally_ overwriting the GameData.cff file.
#### Save as (Ctrl-S)
Saves opened GameData file to the location provided by the user.
#### Close GameData.cff
Closes currently opened GameData file. You will be prompted to save the currently opened GameData file if you modified it prior.
#### Exit (Alt-F4)
Closes GameData Editor. You will be prompted to save the currently opened map before this happens.

### Edit
#### Undo (Ctrl-Z)
Undoes a change you made to the currently selected category. Undo history persists even if you change between categories. 
#### Redo (Ctrl-Y)
Redoes a change you've previously undone. Note that you can't redo a change you've undone if you make another change after that.

### Special
#### Find all references (F3)
This special tool allows you to find all places where selected gamedata element is **referenced**.
![enter image description here](https://lh3.googleusercontent.com/f129Chu3uAj067ylBlBCmf9CDA-p48SrIRwS8I6QTB5Y5s5ZNQwA7DaPbLaeg150eV5D7a7RGhXc)
You can select any of the references to instantly edit the referencing element.
#### Calculators
This tool allows you to calculate some of the more complicated properties from the game - for example, hit chance of unit 1 against unit 2. More calculators to come.

## Selected category
GameData.cff contains data which is divided into 49 categories. Selecting a category loads in all elements which belong to that category.

## Modification panel
Operations described below must be used with special care - it might be that element you remove is used somewhere else, upon which there's a high chance that the game will crash when you try to run it.
### Insert
Inserts a new element under the selected element. It will be an empty (all data set to 0 or empty text) element, or it will be cloned from a previously copied element (see below). If no element is selected, no element will be inserted.
### Remove
Removes selected element from the category.
### Copy
Copies selected element and stores it internally. While an element is stored, the Insert button has a **yellow** color. Switching between categories clears stored element.
### Clear
Clears stored element (if it exists).

## Elements contained within selected category
Each category contains a number of elements. Select an element to inspect its content.

## Search Utility
Search Panel makes finding specific elements much easier. It has following options:
### Value
Enter what you search for here, and specify type of searched data:
 - **Number** - Value must be an integer, otherwise it will be set to 0 before search occurs.
 - **String** - any text you search for (lowercase or uppercase, it doesn't matter). Note that if "Search by column" is not selected, element names will also be searched through, which makes finding elements by name easy.
 - **Bitfield** - some of the values contained within elements are tagged as "flags". This means that the value is a sequence of bits, where each bit has different meaning. For example, if element X contains flag value 5, its bitfield is 00000101 - its first and third bit is set to 1 (counting from right to left). Therefore, if you search for 4, which is 00000100 (third bit set), the element X will meet the search criteria.
### Search by column
Every element of a category has the same data layout - it's divided into columns. If you check "Search by column", you will be able to only look through one column at a time. To choose which column to look through, simply select it below the "Search by column" checkbox.
### New search
Clears previous search results, conducts a new search with parameters provided previously, and displays the results in the elements list.
### Continue search
Does not clear previous search results - instead, it only searches through the results, using new parameters provided by the user, and displays the matching results.
### Clear search
Clears search results and returns to default category elements display, listing all elements cantained in the category as if it was just selected.

## Editor status
Editor status simply displays whether there's an operation currently running.

## Backtracking panel
You may have noticed that some of the element data are displayed in a field with **orange** background. Such fields are **gamedata link fields**. Whenever you see a gamedata link field, you can right-click it, and the editor will display content of the element the field links to.
![enter image description here](https://lh3.googleusercontent.com/631_yzeFva-_cXYYz9Dzw5iw8DSTYZ1AbzPKkOlYq-MvjOc0h7827u1bHD8koCKst7NxGlukZSIs)
On the left side of the backtrack panel you see the name of the element the gamedata field linked to. On the right side the "Back" button appears. Clicking the button will return to editing the element the gamedata link field linked from.

## Selected element inspector
The main part of the GameData Editor is this inspector. It allows you to view and edit data contained in the selected element. The data types range from numerical, to text, to bitfields.
Some text fields are limited in length, so keep that in mind.

## Selected element description and additional information
Some of the information contained in the game data isn't provided explicitly - for example, how much XP you can gain from killing same unit over and over (yes, there is a limit). This panel infers such information from available data and is generally a useful thing to have.

## Additional information
When you open a map with Map Editor while GameData Editor is open, they will attempt to synchronize. Successful attempt will load in GameData.cff currently in data folder of your SpellForce directory, disable ability to load or close another GameData.cff and temporarily disable Redo/Undo functions. Closing the map will desynchronize Map Editor from GameData Editor, enabling the features above.
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI2ODIyNDE1Ml19
-->