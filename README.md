# Tokens

Drop-in DnD 5e Tokens for maptool.

These a specifically aimed at:
* face to face play
* online play, with minimum automated management. Some players love to roll dice and track their HP

These tokens won't add anything to your campaign settings, they are drop-in macros. They can be dragged into any exisiting campaign session.
Updating them is as trivial as dragging tokens into your maptool map.

If you are searching for fully automated frameworks, they are more heavy frameworks to be found on the maptool forum.

## Installation

### Campaign file version
Download https://1drv.ms/u/s!Amfr5xYDSzo2mC-J6QDBBNGZCvdL and open the file with MapTool.

### Drop-in version

Download and extract https://1drv.ms/u/s!Amfr5xYDSzo2mCrAqHL6sLMJNLga

Copy `Lib_Addon5e.rptok` into your library map (any non player visible map), create one if you don't have any. **Rename the token "Lib:Addon5e"**,
(depending on your Maptool options, the application may have renamed it when you dragged it). Finally, execute the Lib:Addon5e **onCampaignLoad** by clicking
on its macro button (not required when loading the campaign from a file).

Drag any token file in your maps to start using it.

Optionaly, you can add the tokens directory to your maptool library window.

## Usage

### Tokens

Best used with the "Selected" windows where all the macro are visible, giving you a idea of what the token is capable of.


### POI (map markers)

A special token, POI stands for Point Of Interest (feel free to suggest a better name). Put on the hidden layer, it's not visible from any player.
While on the token layer, the GM can still click on that token, and a splash window will pop with info.

* It's a token for the GM, to mark stuff on the map. You can change the token image instantaneously using the macros.
* The "fromHandout" macro (I need a better name !=) will send the token to the hidden layer and use the handout image as splash stat block
* the 2 macros "bigger" and "smaller" increase or decrease the token size.
* Don't use the GM notes! it will be erased by the fromHandout macro
* Use the Notes (players still wont see the token) to customize the text

Trick: The look an feel of text in the Maptool splash screen sucks. I found out that using external program to write your info, and then screenshoting that part into the token handhouts is a good and quick way of getting fancy map markers. Using pre written pdf campaigns also works very well.


## Known limitations
* some monsters have their SRD version stats instead of the Monster Manual ones
* as a general rule, for important NPCs, double check with the monster manual
* tokens are editable only using a token manager (http://forums.rptools.net/viewtopic.php?t=14458)
* further edition of the token are not reflected on the token sheet (but all other macros will be udpated)

## Credits

* I borrowed a lot from existing frameworks (Paulstrait's, Wolf42)
* I stole all SRD monsters data from dnd5Api.com
* This was made possible by the active community on the Maptool forum and the discord server. Thanks for their valuable help.
* POI token images stolen from Phergus number tokens
* Tome Of the Beast public data, buy their book to support their work


## Changelogs

### v0.7
* fix monsters showing the 'NPC' instead of the monster type (aberration, fey, etc...)
* tokens are now organized into their own monster tytpe subdir, this should improve user experience when MT is building thumbnails

### v0.6
* fix skill bonuses: tokens were always using the ability modifier instead of the stat block bonus (thanks to Smash The Cookies for finding this one)
* the skill entry in the monster sheet is now fixed
* improvements on the POI (Point Of Interest) magic token for GMs

### v0.5
* fix some bad monster sheet utf-8 characters
* remove large thumbnail from token, lowering the token size on disk by a great deal
* a demo campaign file is now available showcasing all the tokens in one map
* fix a bug for some spellcasters missing their spellslots. The spell description should now be displayed.

### v0.4
* Descriptions/rolls/text is now sent to "self", this is configurable through the token property "oTargets". You can change it to "all" to broadcast macro output to everyone.
* added onCampaignLoad to register UDFs, be sure to reload the campaign or manually click on the macro onCampaignLoad

### v0.3
* restore compatibility with 1.4.0.0 versions (tested with 1.4.0.5)

### v0.2
* dependency to the DnD5e framework is now gone, these are now complete drop-in tokens
* added 40+ tokens from volo's
* fix a bug where the to-hit bonus was used instead of the damage bonus :-/
* add rolls for ability checks
* add rolls for saving throws
* add an init button to auto add and set a NPC token to the init windows
* fix a lot of issues with non ascii characters messing with the monsters sheet
