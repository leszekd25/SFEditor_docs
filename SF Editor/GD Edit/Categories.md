# GameData categories
GameData.cff as a file is divided into 49 "categories" - each category contains data for different aspect of the game. Here's a description of each category found in the file.

Note that some categories are noted as "link category. This means the only purpose of the category is to bind data together - for an example, see category 9.

**1. Spell data**: All info about a particular spell/effect, including cost, cooldown/cast time and parameters unique to each spell type.

**2. Spell type data**: Contains data unique to each spell type, including spell description and UI icon used

**3. Unknown (1)**: Unknown category type, never used in game

**4. Unit/hero stats**: Unit stats can be SHARED between different units. This category contains data about unit combat stats, including unit attributes, unit level, and some miscellaneous info.

**5. Hero/worker skills**: Info about unit's skills. Unique per unit stats data, and only useful for workers and hero units.

**6. Hero spells**: Contains spell data per unit stats data. Only useful for hero units. Note that spell requirements do not apply here, so nothing stops you from giving Warrior Cord a Blizzard spell, maybe except mana cost.

**7. Item general info**: List of every item in the game. Every item in the game has an entry in this category. Contains item type data and item sell/buy price, among other info.

**8. Item armor data**: Contains item info about attributes the item provides to the wearer. Note that this is not exclusive to armor type items, so it's possible to give +30 Strength and +200 armor to your Windsteel Hammer.

**9. Inventory spell scroll link with installed spell scroll**: Link category, pairs inventory item ID with spell book item ID.

**10. Item weapon data**: Info about weapon type items. Includes weapon speed and weapon damage info.

**11. Item skill requirements**: Contains data about conditions required to use an item. Note that there can be multiple entries per item.

**12. Item weapon effects/inventory scroll link with spell**: Link category, pairs item ID with corresponding spell/effect ID. Note that there can be multiple entries per item - just as a weapon can have multiple effects attached.

**13. Item UI data**: Appearance of item in inventory. Note that there can be multiple entries per item- that's the case for scroll items.

**14. Item installed spell scroll link with spell**: Link category, pairs spell book item ID with corresponding spell ID.

**15. Text data**: The largest category, contains all text data in the game, in multiple languages.

**16. Race stats**: Contains info about races in the game. Some of the info is still missing as of 21.08.2018...

**17. Clan relations**: Info about relationships between clans.

**18. Unit general data/link with unit stats**: Every unit in the game is made using a template provided from this category. It contains info about experience and gold gained from killing this unit and base armor class, among other info.

**19. Unit equipment**: Info about items worn by a unit. Note that equipment's chest piece controls the unit's appearance, as evident in sql_items.lua.

**20. Unit spells**: Similarly to category 6., contains spells which can be cast by a unit.

**21. Army unit resource requirements**: Cost of summoning an army unit at the monument.

**22: Corpse loot**: Description of what items you can collect from the corpse of a given unit. Only 3 different items per slot, 6 slots per unit.

**23. Army unit building requirements**: Which buildings are required to summon a unit. Note that resource requirements imply basic building requirements (for example, cost of X iron adds a requirement of Forge).

**24. Building data**: Contains basic info about every building in game. Note that building ID can not exceed 213 due to hardcoded building limit.

**25. Building collision data**: Geometric description of building hitbox (convex polygon on a plane). Note that this hitbox is rasterized into game grid.

**26. Building resource requirements**: Similarly to 21, contains cost of constructing a building.

**27. Skills link with text data**: Link category, pairs avatar/hero skills with corresponding text ID.

**28. Skill point requirements**: Describes attribute points needed to raise a skill to a given level.

**29. Merchants link with unit general data**: Link category, pairs merchant ID with unit ID.

**30. Merchant inventory**: Contains info about items a given merchant sells.

**31. Merchant sell/buy rate**: Different merchants buy and sell items at a different price. You can find this info here.

**32. Resources link with data**: Link category, pairs resource ID with text ID.

**33. Player level scaling**: Info on how much do some stats scale with level. Note that this scaling applies to every unit in game.

**34. Environment object data**: Contains data about miscellaneous objects in the game: environment, quest related, decoration.

**35. Interactive object collision data**: Equivalent to category 25, but for miscellaneous objects.

**36. Environment object loot**: Equivalent to category 22, but for miscellaneous objects (chests, for example).

**37. NPC link with text data**: Link category, pairs NPC ID with text ID. Note that NPC IDs are assigned to units per game scripts, not in game data.

**38. Map data**: Each map belongs to a platform, denoted in PAKs as script\\p### folder. Scripts for a given platform are executed on that map. This category links maps in game directory with platforms and scripts. If a map doesn't have entry in this category, it's assigned platform ID 6666.

**39. Portal locations**: Data about portals, links with maps.

**40. Unknown (from sql_lua?)**: See category 3.

**41. Description link with txt data**: Link category, pairs displayed description ID with text ID.

**42. Extended description data**: Contains text data for advanced in-game descriptions.

**43. Quest hierarchy/description data**: Contains all quest data in the game. Note that it does not contain quest logic - it can be found in Lua scripts instead.

**44. Weapon types**: Info about available weapon types.

**45. Weapon materials**: Info about available weapon materials. Seems to be unused...

**46. Unknown (3)**: See category 3.

**47. Heads**: This is also an unknown category, doesn't seem to store anything.

**48. Unit upgrade data**: Describes which building has which upgrade, and how much it costs. Doesn't denote which unit is upgraded though...

**49. Item sets**: There are 9 available types of sets. This category describes all available sets and which type they belong to.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM2NjQxOTgwXX0=
-->