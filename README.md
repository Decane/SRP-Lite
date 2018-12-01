Changes:
-------
- Fixed several crashes caused by the game attempting to alter the attitude of a non-existing squad, including a crash in the Red Forest if the player followed one of Strelok's helpers into the ambush at the Witch Circle when the ambush squad had already been killed: ! [LUA][ERROR] ERROR: There is no squad [red_pursuit_bounty_hunters_squad_3] in sim_board. - Decane
- Fixed an occasional crash upon the game evaluating whether to assign the player a 'help' task: sim_combat.script:614: attempt to index local 'attack_squad_obj' (a nil value). - Decane
- Fixed a rare crash upon a smart terrain being captured: sim_squad_generic.script:456: attempt to index field 'current_action' (a nil value). - Decane