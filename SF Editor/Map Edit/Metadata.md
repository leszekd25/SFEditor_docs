# Metadata editor mode
In this editor mode, you can set coop map parameters, manage player spawn points and set up team compositions on multiplayer maps.

## User interface
![enter image description here](https://lh3.googleusercontent.com/-LyAO03Ijdw2u13NAqT0BO44AwRKOSi7ju-FLmy_ydyJTnigluG_LtwE-fKu2jDHbnFN8_H8E1yK)

### Map type
Map Editor recognizes map type automatically from data found in map file. There are 3 map types:
- **Campaign** type disables editing coop spawn parameters and multiplayer team compositions altogether.
- **Multiplayer** type disables editing coop spawn parameters.
- **Coop** type does not disable anything.

### Coop spawn parameters
Every coop spawn has parameters, as seen in **GdRtsCoopCampSpawns.lua** in SQL Modifier. These are global multipliers to some of the parameters:
- **Max clan size factor**, multiplies the maximum amount of monsters from a single camp
- **Init spawn factor**, mutiplies the amount of monsters spawning at the camp on game start
- **Begin wave factor**, multiplies time of first monster spawn on a particular wave
- **Spawn delay factor**, multiplies time of subsequent monster spawns on a particular wave

Every parameter takes a floating point value, with 1.0 being 100% of base value.

### Player spawn points
In Campaign map type, player spawn points are simply bindstone definitions.
In Coop and Multiplayer map types, these define points where players first spawn on the map. When you are in game lobby and select side to be on, in reality you choose a spawn point.
Spawn points have a 1 to 1 correspondence with bindstones on the map. You create spawn points by placing bindstones.
#### Spawn point list
Select a spawn point on the list to edit its parameters.
#### Bindstone
Changing value in this field will swap spawn point positions between the selected spawn point and the one chosen with this field.
#### Text ID
ID of an entry in category **41. Description link with txt data** in GameData Editor. It is the name of the bindstone.
This is a gamedata link field.

### Multiplayer teams panel
This panel is divided into 4 quadrants.
#### Multiplayer team compositions
You can define several team compositions per map - for example, you can have a 2 team version and a 4 team version of the map. Both can be implemented on the same map as different team compositions.
**Add** button adds a composition with the least number of teams possible that doesn't already exist on the map. There is a limit of 4 teams in a single composition, so you can have at most 4 team compositions. Additionally, you can't have 1 team in a team composition if the map is of Multiplayer type.
**Remove** button removes a team composition from the map.
Select a team composition from the **Team composition list** to edit its parameters.

All official coop maps have 1 team composition with 1 team, which has 3 players, equal to numbers of spawns.
#### Teams
There is a predetermined amount of teams in a given team composition. They will all be listed in the **Team list** when you select a team composition. Select a team to edit which players it contains.
#### Team members
Each team consists of arbitrary number of members, as long as the sum of all players in all teams in any team composition is equal to number of spawn points on the map.
Select a player from **Team member list** to edit its parameters.
#### Selected player name, Selected player level range
These are used on Coop maps as a map description. Apparently unique to each player on team. Not very useful...
#### Text ID
ID of an entry in category **15. Text data** in GameData Editor. It is the name of the selected player as seen in side selection in game lobby.
This is a gamedata link field.
#### Available players
All players unassigned to any team are listed in **Available player list**.
#### Kick from team
Removes a player from currently selected team and moves it to **Available player list**.
#### Move to team
Moves currently selected available player to **Team member list**.


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ4Mzk1NjQ2Nl19
-->