# Mod Manager general information
While installing mods for Spellforce isn't particularly difficult, managing multiple mods manually - removing files from one mod and adding files from another - becomes a chore quickly. Mod Manager's purpose is to alleviate the issue. It provides an interface to install, manage and remove mods with ease. This page explains how to do that.
Mod Manager requires the game directory to be specified.

## What is a mod
Mod Manager allows you to manage mods, which are defined as packages made using the Mod Creator tool. A package is a single file, which contains gamedata changes, all required assets and some metadata. Such packages have a .sfmd file extension and only those are recognized by Mod Manager as mods. On how to create a package, see **Creating mods**.

## What happens when you run Mod Manager for the first time
After you run Mod Manager for the first time, it does several things:
- It creates **mods** and **backup** directory. **mods** directory is where you put your mods to manage, and **backup** contains original **GameData.cff**, **SpellForce.exe** and the entirety of original **map** directory.
- It also generates **modtemplates** directory, currently only for storing which mods were used last time.

## User interface![enter image description here](https://lh3.googleusercontent.com/YcGWQl0QdSfKYIB2u6cja4VHpbSeTyKcEzeYaLjWdhM-MDoPjXkN0hknUQtM1wgp9ySXd-3NJpDT)
1. Menu bar
2. Mod description
3. Mod panel

## Menu bar

### Mods
#### Restore game to original
Use this option to delete all files which are modified or created by any of the installed mods, and to restore GameData.cff, SpellForce.exe and all maps to the original state.

The button visible under **Mod description** does the same thing.
#### Reload mod list
You should use this option after you manually moved some mods to the mods directory while Mod Manager was running.
#### Make your own mod
You run Mod Creator tool using this option. More on this on **Creating mods** page.

### Settings
#### SpellForce.exe run arguments
You can specify SpellForce command line arguments to run the game with when you use the **Apply and run** button. For the record, here are listed all available command line arguments (though for most of those the purpose is not known):
- nomessagebox: with this, the game will not display error boxes and si
- window: makes the game run in window
- odb
- nologfile
- logfile filename
- cursorclip
- minimized
- showcursor
- windowsize AxB: sets the window resolution when running in window mode

For example, to run in windowed mode, set command line arguments to **-window -windowsize 1280x720**.

## Mod description
Each mod provides a description, which contains the following info:
- Full mod name
- Author name
- Revision number
- A short note on what the mod does

## Mod panel
### Mod list
Here are visible all mods currently in **mods** directory. You can select mods you want to install here.
### Apply changes
The essential part of the Mod Manager, this button installs all mods you want to play SpellForce with. The process as follows:
- First, the game is restored to original state, removing all currently installed mods.
- Then, it sequentially installs all mods selected on the **Mod list**. If there are game data discrepancies, the mods lower on the list supercede changes made by mods installed prior. If there are asset discrepancies, mods lower on the list will replace files made by mods installed prior.
### Apply changes and run
It applies the changes as seen above, after which it runs the game with arguments specified in **Settings->SpellForce.exe run arguments**.

## Additional information
Mod Manager can remove and create files in the game directory without explicit permission. However, if your game directory requires Administrator level permission to write files to, you need to run the entire SpellForce Editor in administrator mode.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEyODIzMDUzMl19
-->