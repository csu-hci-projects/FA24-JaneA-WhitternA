# FA24-JaneA-WhitternA

# VR FPS GAME
Made by Ashton Jane and Allison Whittern ***who did what is below***

**How to Run the game**
- Open our Github.
- Download it with the GitHub Desktop.
- Find where you saved it.
- Open the folder labled "CS310H_HW2".
- Open the uproject labled "CS310H_HW2.uproject".
- Once the game is running open the First Level.
- Then connect your VR headset and press play.
  
**Links**
- Our youtube Videos
  - Functionality Video:
  - Blueprints Video: 
- Our LLMs are a pdf in the GitHub.
  
**References**
- We used the lab videos provided.
- I referenced our HW1 for some of the logic.
**Meeting Times**
  - During allocated in class meetings
  - Discussion throughout the project through messages on teams to coordinate workload

**HW2 requirnments**
***Who did what is labeled by the names in [brackets] by the major categories***
- Create a new VR project. (20 PTS) **[Allison W]**
  - Use the VR Template and starter assets.
  - Configure and connect your assigned VR HMD.
- Create a new level with static mesh objects to decorate your world. (10 PTS) **[Allison W and Ashton J]**
  - Configure this level to use the VR gamemode and use the VR player pawn.
- Create a teleportation area (10 PTS) **[Allison W]**
  - Use a navigation volume and static mesh to enable teleportation in your VR level.
- Add at least 3 unique VR grab interactables (you are welcome to add more and add multiple instances on a unique interactable). (10 PTS) **[Ashton J]**
  - These should be static meshes with the grab component.
  - Ensure that “simulate physics” and “use gravity” are enabled.
- Modify the Pistol Blueprint to keep track of ammo (10 PTS) **[Ashton J]**
  - Add spatial UI to the pistol blueprint
  - Whenever the user shoots the ammo count should decrease
  - After shooting the UI should update to show the current ammo count
  - If the ammo count is 0 prevent the player from shooting
- Add a delayed reload function (15 PTS) **[Ashton J]**
  - Set up a button input as the reload button.
  - If the pistol is currently in the user’s hand and the button is pressed begin resetting the reload.
  - There must be a time delay before the ammo count is updated.
  - After the delay, update the spatial UI to display the new ammo count.
  - When reloaded play a notification sound to indicate that reloading has been completed.
- Add at least 5 targets to the level (10 PTS) **[Ashton J]**
  - These should keep track of how many times they’ve been hit by a projectile.
  - This should be an int variable that starts at 0.
  - After the first hit, change the color of the target material.
  - After the second hit, use an event to indicate that the target is being destroyed and then destroy it.
- Modify the level blueprint to keep track of the number of targets destroyed. (10 PTS) **[Ashton J]**
  - Add an event listener to the level blueprint that is connected to the target destroyed event delegate (see 5d).
  - Whenever a target is destroyed, increase an int variable that keeps track of the number of destroyed targets and print the number of destroyed targets to the screen.
- Create an unlockable “no-teleport” area. (10 PTS) **[Allison W]**
  - Due to a technical issue this section has been updated 11/21/24. Once a single target has been destroyed unlock the "no-teleport" area.
  - After increasing the level blueprint variable to keep track of destroyed targets check to see if at least 3 have been destroyed.
  - If at least 3 have been destroyed, unlock the “no-teleport” area.
- Add a “win” level (15 PTS) **[Allison W]**
  - Create a second level
  - Decorate this level with any static meshes, particle effects, etc. that you want.
  - Add in spatial text that reads “You Win!”
  - In your first level automatically load this second “win” level once all targets in the first level have been destroyed.


# HW1
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
