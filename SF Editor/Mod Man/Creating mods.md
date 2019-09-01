# Creating mods using Mod Creator
Mod Manager allows you to install and uninstall packages made in Mod Creator, to be used in your SpellForce game.

## User interface
![enter image description here](https://lh3.googleusercontent.com/2ZjaRYyyJlY30NDw1Ktr8WIRx9toyzurOXGQ3XFY39w0Kzij5UWoNO7N4T8M_GZYpfuwsNxA6acD)
## Mod file name
Required. Specify short mod name that will be seen on Mod Creator's mod list.

## Choose asset directory
Select folder with all assets you want your mod to contain. Asset folder structure should be the same as the SpellForce game directory structure - textures should go to **texture** folder, models to **mesh** directory, and so on.
If your asset directory contains **data\\GameData.cff** file, it will not be put as an asset. Instead, Mod Creator will generate a diff data, which is all changes between **backup\\GameData.cff** and **{assets}\\data\\GameData.cff**. This is to reduce mod file size.

## Add mod information
It's good to let users know what the mod does before installing it. To that end, you're allowed to specify additional information to embed into mod file.
![enter image description here](https://lh3.googleusercontent.com/Qcb4-RkwcVBoMrcqSn-6QKFrqjfUr1Juxs2ZbTfK536-yg3-0BbSdDeqw8SLc1E3ooHD8LQLxMb4)
### Mod name
Long, proper name of your mod
### Author
That's you : )
### Revision number
When you first create a mod, you should set this to 1.
### Description
Provide information about what your mod does. Should be short, but concise.

## Create mod
When you're done with your changes, click this button to generate a mod. It might take a while if your mod is large or has a lot of files. The mod will be placed in **mods** directory, and the Mod Manager will find it automatically when you close the Mod Creator.
If the game finds a mod with the same file name as the one you provided, you'll be asked if you want to simply increase revision number by 1 compared to the found mod's revision number, or leave it as you specified.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjcxNjMwNjczXX0=
-->