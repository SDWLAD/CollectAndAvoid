# CollectAndAvoid

Engine: Unreal Engine 5\
Version: 5.8.0


## Controlls:
### Movement:
> WASD + Arrows - Move\
> Mouse - Look around\
> Shift - Sprint\
> Ctrl - Dash
### UI
> Esc - Pause

## How to run:
Download ColectandAvoid.zip Unarchive that and open CollectAndAvoid.exe.

## Blueprints descriptions:

> BP_Coint - Collectable, that adds score, play sound and spawn niagara system, when you touch it.\
> BP_Hero - PLayer blueprint. Responsible for movement, model animation, camera, death etc.\
> BP_PlayerController - Processes keyboard input.\
> BP_GameMode - Has realisation of AddScore and variables: Score, TargetScore, E_GameState, IsPaused.\
> BP_GameInstance - Contains cross-level variables(for example - MasterVolume).\
> BP_MenuHero, BP_MenuGameMode - BP_Hero & BP_PlayerController copies without movement and changed camera location.\
> BP_Enemy - Enemy blueprint whith AI movement. Has 2 modes - patrol and BP_Hero persecution.\
> BP_EnemyAIController - Has persecution realisation.\
> BTT_GoToPoint - Behaviour tree task, that Move BP_Enemy to point.\
> BTT_NextPoint - Changes next point for BP_Enemy.\
> ABP_Unarmed - Blueprint, that has animations for BP_Hero.\
> ABP_Enemy - ABP_Unarmed clone for enemy.\
> WBP_HUD, WBP_Lose, WBP_Menu, WBP_Pause, WBP_Settings, WBP_Win - UI Widgets.

## Questions
For .uasset and .uamap files was used GIT LFS.
Changed three movement parameters: Walk Speed, Air Control, Max Acceleration.
Cast check with BP_Hero needed, becouse if in future its will be more players, score will not add  to correct player.
In UI I update the score through an event, not through per-frame bindings, becouse that more optimised. All assets was fabric or made by me.