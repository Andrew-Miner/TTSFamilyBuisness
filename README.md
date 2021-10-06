# TTSFamilyBuisness
These scripts go along side my [Family Bussiness Steam Workshop mod](https://steamcommunity.com/sharedfiles/filedetails/?id=360152489) for the game Tabletop Simulator. This mod is based on the real-life Mayfair Games' card game of the same name. 

An explanation of the game's rules can be found at [this link](https://www.ultraboardgames.com/family-business/game-rules.php). 

These scripts include the systems needed for handling Family Business’s dynamic turn order, each players’ hand of cards, each players’ mobster cards, the game’s concept of a “hit list”, custom XML-based UIs, and implements the unique effects of each of the 24 offensive, defensive, and passive cards in the game.
 

The file [`Global.-1.ttslua`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Global.-1.ttslua) serves as the entry point. The core logic of the game can be found in the [`GameManager.ttslua`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/GameManager.ttslua) class.

The 24 different cards and their effects are implemented using Polymorphism and can be found in the [`Cards` folder](https://github.com/Andrew-Miner/TTSFamilyBuisness/tree/master/Cards).

The code for the different UIs can be found in the [`UI` folder](https://github.com/Andrew-Miner/TTSFamilyBuisness/tree/master/UI) and the file [`Global.-1.xml`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Global.-1.xml). Because of the way Tabletop Simulator works, all of the different UI Xml data has to be in the same Global file.

Both the [`HitList`](https://github.com/Andrew-Miner/TTSFamilyBuisness/tree/master/HitList) and [`Player`](https://github.com/Andrew-Miner/TTSFamilyBuisness/tree/master/Player) code can be found in their corresponding folders.

### Other Utility Classes:
* [`Scheduler`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Scheduler.ttslua): A class that schedules task to be run in the future
* [`Shuffler`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Shuffler.ttslua): Handles the main deck of cards and shuffles them when needed
* [`HandTracker`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/HandTracker.ttslua): Tracks each Player's set of cards, what card they are currently holding and whether it belongs to them, etc
* [`Logger`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Logger.ttslua): Keeps a log of each player's actions and makes it visible to the players

### Constants:
* [`ColorData`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/ColorData.ttslua): Contains data about each of the seats/colors at the table, including mobster card locations and neighboring colors
* [`MobsterConstants`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/MobsterConstants.ttslua): Contains data about each of the six teams of mobsters
* [`Zones`](https://github.com/Andrew-Miner/TTSFamilyBuisness/blob/master/Zones.ttslua): Contains the GUIDs of each of the card zones on the table
