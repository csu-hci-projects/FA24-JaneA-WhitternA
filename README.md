# FA24-JaneA-WhitternA

# FPS GAME
Made by Ashton Jane and Allison Whittern

Our game is a FPS game where each level you will go around finding targets and shooting them. As you go around you'll have to avoid hazards! But don't worry if you do get hurt you are able to find health packs to heal yourself. Your goal is to hit all the targets and get through all the levels! Have fun!

Controls (Computer):
- WASD are for movement.
- Moving your mouse allows you to look around.
 -Right click on the mouse allows you to zoom in for better aim.
- Left click on the mouse allows you to shoot. 
- Shift allows you to sprint.
- Space bar allows you to jump.

To run our game you need to open the main branch with github desktop and then find where you have the files saved. Once you do open up the CS310H_HW1 then either double click the .uproject file or right click the file and open with Unreal. Once its open make sure to start by opening the start level and pressing play.

**Communication Methods:**
Constantly communicating with each other over teams as early as Sept 25th.
Set clear communication and working standards with each other.

**Tasks and who completed them:**
- Create a new project (10 PTS) [Ashton]
    - Use the FPS template and load the starter assets. [Ashton]
- Create 3 unique levels 
    - One level must be a “menu” scene with a start button that loads the first level and a quit button that exits the game. (10 PTS) [Ashton J]
    - The level that is loaded from the menu must have hazards and targets (required functionality for these described below). Once all targets have been destroyed the third level must automatically load. (10 PTS) [Allison W]
    - The third (last) level must also have hazards and targets, but a different layout. Once all targets have been destroyed the menu scene must automatically load. (10 PTS) [Ashton J]
    - Both of the non-menu levels must have static meshes with materials applied for the user to navigate. (10 PTS) [Allison W] [Ashton J]
- Each non-menu level must have at least 3 targets and at least 3 hazards 
    - Targets can be any mesh, but must have a “health” variable. Their starting health should be 100. (20 PTS) [Allison W]
      - The health variable is an integer that is reduced when shot (the exact amount of health lost is up to you). After a target’s health reaches 0 or less the target should be destroyed. [Allison W]
      - Once all targets in a level are destroyed the next level should automatically be loaded (see 2b and 2c for details). [Ashton J]
    - Hazards need to damage the player. (20 PTS) [Allison W]
      - The player needs to have a health variable as well. The starting health should be 100. [Allison W]
      - When a player collides with a hazard (i.e. lava pit, spike trap, etc.) they will lose health (the exact amount they lose is up to you). [Allison W]
      - Once a player’s health reaches 0 or less the level should automatically restart (hint load the level currently being played!). [Allison W]
- Ammo
    - The player should have limited ammo. (10 PTS) [Ashton J]
      - Whenever the player fires if they have ammo the ammo integer is reduced by 1. [Ashton J]
      - If the player is currently at 0 or less ammo the gun does not fire. [Ashton J]
      - The ammo count should be displayed at all times as: “AMMO: ##” [Ashton J]
- Pickups
    - Ammo pickups (10 PTS) 
      - If the player runs over an ammo pickup their ammo count increases and the pickup is destroyed. [Allison W]
      - This pickup should have a unique mesh visual to identify the pickup. [Allison W]
    - Health pickups (10 PTS) 
      - If the player runs over a health pickup their health increases. However, the player’s health cannot exceed 100. The pick up should then be destroyed. [Allison W]
      - This pickup should have a unique mesh visual to identify the pickup. [Allison W]

**Meetings:**
- Friday Oct 11th in person meeting for approx 1.5 hours. Went over working expectationis, how we were splitting up the workload equally, and what we wanted the game to look like.
- Monday Oct 21st in person during class. Went over splitting up the videos and final steps.
