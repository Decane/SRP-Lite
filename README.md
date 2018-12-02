Changes:
-------
### Stability improvements:
- Fixed several crashes caused by the game attempting to alter the attitude of a non-existing squad, including a crash in the Red Forest if the player follows one of Strelok's helpers into the ambush at the Witch Circle when the ambush squad has already been killed: ! [LUA][ERROR] ERROR: There is no squad [red_pursuit_bounty_hunters_squad_3] in sim_board. - Decane
- Fixed a crash in the Garbage if the player receives a task with Wild Napr as its target while a squad registered to the Flea Market is in a combat/defense state: ! [LUA][ERROR] ERROR: wrong target for storyline quest: logic@work5,gar_smart_terrain_6_3. - Decane
- Fixed an occasional crash upon the game evaluating whether to assign the player a 'help' task: sim_combat.script:614: attempt to index local 'attack_squad_obj' (a nil value). - Decane
- Fixed a rare crash upon a smart terrain being captured: sim_squad_generic.script:456: attempt to index field 'current_action' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:968: attempt to index field 'actor' (a nil value). - Decane
- Fixed a rare crash upon reloading a savegame: sim_combat.script:419: attempt to index field 'actor' (a nil value). - Decane
- Fixed two task entity identifier leaks which could eventually destabilize the game. - Decane

### General fixes:
- Fixed the issue where loading a savegame would make the game copy offered but unassigned combat tasks to a Lua table intended only for assigned combat tasks, causing various bugs ranging from stuck faction wars to the robbery scheme ceasing to activate. - Decane