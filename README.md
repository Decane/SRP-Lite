Changes:
-------
### Stability improvements:
- Fixed several crashes caused by the game attempting to alter the attitude of a non-existing squad, including a crash in the Red Forest if the player follows one of Strelok's helpers into the ambush at the Witch Circle when the ambush squad has already been killed: ! [LUA][ERROR] ERROR: There is no squad [red_pursuit_bounty_hunters_squad_3] in sim_board. - Decane
- Fixed a crash in the Garbage if the player receives a task with Wild Napr as its target while a squad registered to the Flea Market is in a combat/defense state: ! [LUA][ERROR] ERROR: wrong target for storyline quest: logic@work5,gar_smart_terrain_6_3. - Decane
- Fixed a crash upon entering the Garbage if the player took Yoga's task to kill Stringov, accepted Stringov's bribe, left Stringov alive, finished the task while Yoga was offline, and did not loot Stringov's stash: ! [LUA][ERROR] ERROR: Unable to give treasure [gar_treasure_quest_smuggler_weapons] because inventory box is already in use by treasure [gar_treasure_quest_smuggler_weapons]. - Decane
- Fixed an occasional crash upon the game evaluating whether to assign the player a 'help' task: sim_combat.script:614: attempt to index local 'attack_squad_obj' (a nil value). - Decane
- Fixed a rare crash upon a smart terrain being captured: sim_squad_generic.script:456: attempt to index field 'current_action' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:968: attempt to index field 'actor' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:419: attempt to index field 'actor' (a nil value). - Decane
- Fixed a crash upon attempting to load a deleted savegame: ui_load_dialog.script:297: attempt to index local 'item' (a nil value). - Decane
- Fixed a crash upon attempting to delete an already deleted savegame in the load menu: ui_load_dialog.script:249: attempt to index local 'item' (a nil value). - Decane
- Fixed a crash upon attempting to delete an already deleted savegame in the save menu: ui_save_dialog.script:172: attempt to index local 'item' (a nil value). - Decane
- Fixed two task entity identifier leaks which could eventually destabilize the game. - Decane

### General fixes:
- Fixed the issue where loading a savegame would make the game copy offered but unassigned combat tasks to a Lua table intended only for assigned combat tasks, causing various bugs ranging from stuck faction wars to the robbery scheme ceasing to activate. - Decane
- Fixed eight stash coordinates being unattainable from the following characters due to programming mistakes: Drifter (1), General Krylov (2), Hermit (1), Hound (1), Kolobok (1), Mitay (1), Semyon Lambee (1). Notably, Drifter now offers coordinates to a stash containing the third Cordon flash drive if the player saves him from dogs. - Decane
- Fixed Clear Sky's "Find a way to Chernobyl NPP" task not completing. - Decane
- Fixed Freedom's "Eliminate the potential threat at the gas station" task being cancelled when the player completes the objective. - Decane
- Fixed the "Life support system" upgrade for the Freedom Exoskeleton making the player bleed out faster rather than slower as intended. - Talrivian
- Fixed the "Relief backpack" upgrade for various armors wrongly incrementing the carry weight tooltip value by only 5kg instead of the 15kg actually unlocked by the upgrade. - vlad54rus
- Fixed mutants not behaving aggressively on patrol paths linking them to attack-targets unless aggravated by an external force (e.g. the player). - Decane
- Fixed the audio of an NPC's instrument-playing animation continuing to play even when the animation is interrupted by the NPC getting up intermittently. - Decane
- Fixed faction reward tooltips failing to update to reflect new rewards after resuming progress from a savegame in which the player already has an outstanding reward from the relevant faction. - Decane
- Fixed the HUD bleeding icon being misaligned with its background in widescreen mode. - Armada