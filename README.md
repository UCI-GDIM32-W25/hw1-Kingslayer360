[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

Objects
UI-
-Seeds planted
		-Seeds remaining
			--seeds planted UI
			-Attributes   
				-text
				-White color
				-Actions
					-Count goes down when a player plants a seed
-Player
	Actions
		-Placeable plants with Space bar and plants one
		-Increases/decreases plant counts (in UI)
		-Plant seeds at location of player
	-movement with W,A,S,D
		-Can go off screen
	-No cursor
			
Input- Space / WASD keys
Output- Plant placed/ movement
	
Color
	-Solid background skybox
	-Player has outline
	-UI is white to stand out
No animation

Plant
	-Attributes (Quality or looks)
		-Plant Sprite 
		-Colored


## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


Write your Devlog here!

To relate to the initial breakdown, I started out with the player. Knowing the player is a gameobject, I went into the inspector, I decided to fill in the slot for a transform component(this is so the player script can relate to the players transform component specifically) and I slotted the canvas gameobject which conatined the PlantCountUI script and the 2 TMP_Text. I then go into the player script attached so I can work on the movement of the player. I went into the update function and started coding using an if statement with an Input.GetKey for each WASD key that is found in the breakdown. It then would output the movement in a direction based on a vector2 through _playerTransfom.Translate. There is also coding for the spacebar which is meant to plant one seed at a time, this was coded with an if statement containing Input.GetKeyDown and a condition that the numSeedsLeft > 0. This output corressponds with where and how the player plants the seed, as when the Space bar is pressed, the seed plants on the players location through calling the method PlantSeed(), in this method I instantiated the plant using the gameobject PlantPrefab (which has a an attribute of a new plant sprite), the players transform.position component and Quaternion.Identity. In this method I also increased seedsPlanted and decreased seedsLeft and then used FindAnyObjectByType<PlantCountUI> which means I am relating to the canvas gameobject, I then use the updateSeeds function which has code that accesses the text TMP_Text and it then sets the text to contain the new updated number for each category of seeds left or seeds planted.

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
