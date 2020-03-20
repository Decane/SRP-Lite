Changes:
-------
### Stability improvements:
- Fixed the game sometimes becoming corrupted during the Flea Market basement mugging scene in the Garbage (new game recommended). - Decane
- Fixed a crash in Agroprom if Orest is displaced from his designated space restrictor: [error]Description : any vertex in patrol path [agr_stalker_leader_walk] is inaccessible for object [agr_stalker_base_leader]. - Decane
- Fixed several crashes caused by the game attempting to alter the attitude of a non-existing squad, including a crash in the Red Forest if the player follows one of Strelok's helpers into the ambush at the Witch Circle when the ambush squad has already been killed: ! [LUA][ERROR] ERROR: There is no squad [red_pursuit_bounty_hunters_squad_3] in sim_board. - Decane
- Fixed a crash in the Garbage if the player receives a task with Wild Napr as its target while a squad registered to the Flea Market is in a combat/defense state: ! [LUA][ERROR] ERROR: wrong target for storyline quest: logic@work5,gar_smart_terrain_6_3. - Decane
- Fixed a crash upon entering the Garbage if the player took Yoga's task to kill Stringov, accepted Stringov's bribe, left Stringov alive, finished the task while Yoga was offline, and did not loot Stringov's stash: ! [LUA][ERROR] ERROR: Unable to give treasure [gar_treasure_quest_smuggler_weapons] because inventory box is already in use by treasure [gar_treasure_quest_smuggler_weapons]. - Decane
- Fixed a potential waypoint crash when mutants spawn at the Military Warehouses military base: ! [LUA][ERROR] ERROR: Path between [mil_smart_terrain_7_11] and [mil_smart_terrain_7_10] doesnt exist for [mil_dogs_lair_6] (new game required for effect). - Decane, smoq2
- Fixed a potential waypoint crash when an NPC patrols the 'Bonfire in forest' at the Cordon: [error]Description : patrol path[esc_smart_terrain_3_7_walker_1_walk], point on path [name05],object [sim_default_stalker_228836]. - Decane
- Fixed two potential crashes in Limansk during the Monolith ambush at the square. - Decane, InnerGround
- Fixed an occasional crash upon the game evaluating whether to assign the player a 'help' task: sim_combat.script:614: attempt to index local 'attack_squad_obj' (a nil value). - Decane
- Fixed a rare crash upon a smart terrain being captured: sim_squad_generic.script:456: attempt to index field 'current_action' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:968: attempt to index field 'actor' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:419: attempt to index field 'actor' (a nil value). - Decane
- Fixed a crash upon attempting to load a deleted savegame: ui_load_dialog.script:297: attempt to index local 'item' (a nil value). - Decane
- Fixed a crash upon attempting to delete an already deleted savegame in the load menu: ui_load_dialog.script:249: attempt to index local 'item' (a nil value). - Decane
- Fixed a crash upon attempting to delete an already deleted savegame in the save menu: ui_save_dialog.script:172: attempt to index local 'item' (a nil value). - Decane
- Fixed two task entity identifier leaks which could eventually destabilize the game. - Decane

### General fixes:
- Fixed the storyline breaking if the player does not respond to the SOS signal in the Red Forest before speaking with Forester. - Decane
- Fixed the issue where the Freedom base gate would open upon completion of the "Deliver ammo to the outpost" task instead of only after the player has found the active PDA on the dead blockpost commander's corpse, enabling the player to speak to Chekhov prematurely and break the storyline. - Decane
- Fixed the storyline temporarily breaking if the player suppresses the Limansk military machine gun nest during the interval between receiving and completing the task to speak to the Clear Sky squad commander. - Decane
- Fixed the level changers to the Cordon not becoming unlocked when the player first travels there from the Great Swamps if Clear Sky loses their victory over the renegades during the player's pre-travel conversation with the guide, resulting in the player getting locked into the Swamps upon first returning there if Clear Sky has not by then regained victory over the renegades. - Decane
- Fixed the issue where loading a savegame would make the game copy offered but unassigned combat tasks to a Lua table intended only for assigned combat tasks, causing various bugs ranging from stuck faction wars to the robbery scheme ceasing to activate. - Decane
- Fixed eight stash coordinates being unattainable from the following characters due to programming mistakes: Drifter (1), General Krylov (2), Hermit (1), Hound (1), Kolobok (1), Mitay (1), Semyon Lambee (1). Notably, Drifter now offers coordinates to a stash containing the third Cordon flash drive if the player saves him from dogs. - Decane
- Fixed the issue where new faction equipment chest supplies would spawn on smart terrains occupied by an online squad every time the game is loaded. (Supplies are supposed to spawn only when an online squad first enters a smart terrain.) - Decane
- Fixed the issue where non-scripted squads loaded from a savegame (as opposed to spawning into the Zone in the current game session) would not spawn inventory box items. - Decane
- Fixed the wrong location-based multiplier being used to spawn faction equipment chest supplies for scripted squads loaded from a savegame (as opposed to spawning into the Zone in the current game session). - Decane
- Fixed the script bugs responsible for Drifter and Hound dying upon switching online from an offline state following completion of the tasks to escort them to safety. - Decane
- Fixed the issue where the dogs spawned for Wolf's "Help the stalker" task might never attack Drifter if the player picks up Sidorovich's loot before taking the task. - Decane
- Fixed the issue where the stalker squad overlooking the Cordon vehicle station would not budge when they are supposed to raid it alongside the player in exchange for payment if Valerian has not yet tasked the player with assaulting it as part of the main storyline (new game required for effect). - Decane
- Fixed the issue where the player could bypass the space restrictor that completes Clear Sky's "Find the generator" task by entering the institute building through its eastern entrance (new game required for effect). - Decane
- Fixed Clear Sky's "Find a way to Chernobyl NPP" task not completing. - Decane
- Fixed Clear Sky's "Find generator" task not completing when the player deactivates the generator in Limansk if the task is still active then. - Decane
- Fixed Clear Sky's "Return to the group commander" task not cancelling when the player deactivates the generator in Limansk if the task is still active then. - Decane
- Fixed Clear Sky's "Return to the group commander" task being completed immediately after being assigned each time the player receives it after initially completing it. - Decane
- Fixed Freedom's "Eliminate the potential threat at the gas station" task being cancelled when the player completes its objective. - Decane
- Fixed the issue where submitting the item requested in a 'return item' task would not complete the task if the player possesses multiple units of the item when submitting it. - Decane
- Fixed the Red Forest bridge lowering sequence becoming prematurely unlocked as soon as the player completes the "Go to the army base" task rather than only after the player has transmitted the coordinates to free Leshiy's squad from the space bubble. - Decane
- Fixed the exploit where the player could repeatedly break the Compass artifact submission dialog and re-enter it to receive the reward (a Vintar BC) again and again an endless amount of times. - Decane
- Fixed the greeting audio of some NPCs � most notably Professor Beanpolev � occasionally playing over their first spoken dialogue when the player opens a dialogue window with them. - Decane
- Fixed the issue where the dialog concerning the military presence at the Cordon vehicle station could be repeated endlessly with the stalker squad on the hill overlooking it, potentially leading to the player paying the stalker squad multiple times for their assistance in dealing with the military. - Decane
- Fixed the issue where the player could pay the stalker squad on the hill overlooking the Cordon vehicle station for their assistance in dealing with the vehicle station military squad even after the military squad has already been liquidated. - Decane
- Fixed the "Life support system" upgrade for the Freedom Exoskeleton making the player bleed out faster rather than slower as intended. - Talrivian
- Fixed the "Relief backpack" upgrade for various armors wrongly incrementing the carry weight tooltip value by only 5kg instead of the 15kg actually unlocked by the upgrade. - vlad54rus
- Fixed the upgrades unlocked by the "Flash drive with data on a psy-protection system" and the "Flash drive with data on reinforced army body armor" being swapped for the SEVA suit at the Garbage bandit mechanic. - Decane
- Fixed the "Barrel modification" and "Gas system modification" upgrades for the RP-74 at the Agroprom Duty mechanic incorrectly being unlocked by the "Flash drive with data on balancing the automated parts of a machine gun" instead of by the "Flash drive with data on a machine gun muzzle break" and the "Flash drive with data on modifying the gas exhaust of a machine gun", respectively. - Decane
- Added the missing 'doesn't use shot' attribute text to the "Barrel modification" upgrade tooltip for the Chaser 13. - Decane
- Added the missing '+15%' handling attribute quantifier text to the "Barrel modification" upgrade tooltip for the Akm 74/2U. - SetaKat
- Stopped PSI emission hit intensity doubling on save/reload (new game required). - Decane
- Stopped PSI emission audio and visual effector intensity doubling on save/reload (new game required). - NatVac
- Fixed mutants not behaving aggressively on patrol paths linking them to attack-targets unless aggravated by an external force (e.g. the player). - Decane
- Fixed a script typo preventing the Lost Party's PDA from being transferred to Sakharov upon talking to him following completion of the task to retrieve it. - Decane
- Fixed the audio of an NPC's instrument-playing animation continuing to play even when the animation is interrupted by the NPC getting up intermittently. - Decane
- Fixed faction reward tooltips failing to update to reflect new rewards after resuming progress from a savegame in which the player already has an outstanding reward from the relevant faction. - Decane
- Fixed the mechanic specialization tooltip displaying 'none' for Aydar, Yar, and Thunderov, despite all of them having a specialization. - Decane
- Fixed the Abandoned Hospital not having a magnifiable map in the PDA. - Decane
- Fixed the HUD bleeding icon being misaligned with its background in widescreen mode. - Armada
- Fixed the invalid compound vector comparison in shader mark_msaa_edges.ps. - GSC Game World
- Improved the accuracy of the error message printed by _G.abort(). - Decane
- Fixed the Sunrise Suit using the Leather Jacket HUD model instead of its own. - Kill_the_Strelok
- Fixed the Bandit Jacket using the Sunrise Suit HUD model. The Bandit Jacket now has its own unique HUD model, imported from S.T.A.L.K.E.R. - Call of Pripyat. - Decane, GSC Game World
- Fixed the SEVA Suit using the Bulat Armored Suit HUD model. The SEVA Suit now has its own unique HUD model, imported from S.T.A.L.K.E.R. - Call of Pripyat. - Decane, GSC Game World
- Replaced the generic masked face of the player's unarmored character model with Scar's face, as in the leather jacket armored character model (new game required for effect). - Decane
- Fixed the alignment of the off-center 'Game over' text and accompanying flashing prompt in widescreen mode. - Decane
- Fixed some strings in the credits being rendered incorrectly with the Russian localization. - SurDno
- Fixed the German voice acting credits being misattributed to English voice actors. - SurDno
- Removed the Akm 74/2 introduced into Scar's starting inventory by patch v1.5.09 (new game required for effect). - Decane