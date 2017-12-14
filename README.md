# COMP210_2_interace_task

# Proposal

The game I will be making for the VR project will be a top down bullet hell dungeon crawler. This will be achieved by using the VR controllers in the style of a twin stick shooter. 

This project will only have three key requirements:

* Top down camera
*	Movement
* Shooting

One controller will be pointed where the player wants their character to move and the other will be used to point at where they want to shoot. 

This is taking the traditional twin stick approach but using motion controllers instead of joysticks. 

Due to the nature of the game the camera may have to be fixed meaning not much functionality can be gained from the headset itself but depending on the art assets this might change and give the player some freedom in their view.

![TopDown1](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Topdown1.png)
![TopDown2](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Topdown2.png)

I originally wanted to work with AR using the HoloLens but because the game project is being developed on the unreal engine and HoloLens not having the best unreal support currently this is not practical. 

I also looked at changing the camera to first person and have the player be in the dungeon. Some VR titles that have achieved this:

## A Legend of Luca (£14.99)
![A legend of Luca](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Luca.png)

(http://store.steampowered.com/app/433600/A_Legend_of_Luca/)  

VR rouge like dungeon crawler in the first-person perspective, rated very positively.

## VR Dungeon Knight (£14.99)
![DungeonKnight](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Dungeon%20Knight.png)

(http://store.steampowered.com/app/566860/VR_Dungeon_Knight/)


First person randomly generated dungeon crawler also having very positive reviews

## The Crypts of Anak Shaba – VR (£0.79)
![AnakShaba](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Crypts.png)

(http://store.steampowered.com/app/566060/The_Crypts_of_Anak_Shaba__VR/)

This one is also exploring “crypts” in a dungeon crawler style but rated very badly because of the number of game breaking bugs and bad controls.

After looking at these three games it’s clear that this style of VR game has been explored and can be successful. For my project I want to try something different though so going for the top down approach. Having a look on steam and online I found some games that have tried to achieve this.

## AirMech® Command (£14.99)
![AirMech](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/AirMech.png)

(http://store.steampowered.com/app/364630/AirMech_Command/)

This game is a top down strategy that uses VR to command the troops, shows how VR can be used for top down games and is rated highly.

## Volume: Coda (Yet to be released)
![Volume](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Volume%20Coda.png)

(https://blog.eu.playstation.com/2016/06/08/watch-the-first-volume-coda-gameplay-trailer-coming-soon-to-playstation-vr/)

Volume: Coda is a PlayStation VR exclusive stealth inspired puzzle game using a VR top down view.

## Salvaged (£9.99)
![Salvaged](https://raw.githubusercontent.com/Phil-Sparkes/COMP210_2_interace_task/master/Pictures/Salvaged.png)

(http://store.steampowered.com/app/504470/Salvaged/)

Salvaged is very interesting in its approach to VR, the VR experience is a first-person dungeon crawler, but one player (using mouse and keyboard) has control over all the other players movements using a top down view. The concept is liked but the game currently has massive performance and UI problems so is rated negatively on steam.

These games show that top down can be used to a level of success with VR, but a dungeon crawler style game has not been attempted yet. 

# Design of the solution

The player will have a virtual reality headset, two motion controllers (one in each hand) and a tracking device attached to a belt around their waist.

The headset is used for the players view. It has a top down perspective although the player looks directly forward rather than down. The player can look around in full 360 degrees but too much of this can cause motion sickness.

The controllers are used for character movement, shooting, pickups and switching between weapons. They also give haptic feedback when the player gets hit by a projectile.

The tracker is attached to the players belt and used for the ‘special attack’, when the player does a fast movement of the hips then it will trigger the special attack.


# User Stories

### As a player I would like the game to feel like a traditional twin stick shooter.
A traditional twin stick shooter has two joysticks, one for player movement and one for aiming. To achieve this in VR I decided to use the two VR motion controllers in the same way. One for movement and one for aiming.

### As a player I would like to be able to move my character in an intuitive way.
In the game both controllers have laser pointers that are aimed at the Gameworld. For intuitive movement the player would aim at a location in the world and the character would move there using “simple move to location” this proved to be very buggy through playtesting so was later changed to walk directly towards the pointer when trigger was held down. This new method worked well and was considered intuitive after playtesting again.

### As a player I want to be able to aim with a good amount of accuracy.
The player can aim at a location in the world and pull the trigger. The projectile will travel towards directly towards the location so this has been achieved.

### As a player I want the gameplay to be fast paced.
Through good control of the character and being able to move and shoot at the same time this has been achieved.

### As a player I want gameplay to be somewhat challenging.
Dodging the enemy projectiles and being able to shoot them does take some time to get good at and could be considered challenging.

### As a player I want physical feedback when I get hit by a projectile.
When the player gets hit by a projectile both controllers vibrate.

### As a player I want a special move that works with a physical movement.
A special move was added when the player provides a fast hip movement. Projectiles would spawn in all directions from the player.

### As a user I want the camera to be in the top down perspective.
Top down camera has been implemented but also the player has freedom to look around to not induce motion sickness.

### As a user I do not want a sense of motion sickness playing the game.
With the unusual camera angle some player did induce motion sickness but giving the player freedom to look around did help with this.

### As a player I want to be able to pick up and use weapons.
The game has weapon loot boxes which drop weapons, the player can pick up these weapons and switch between them.

### As a player I want randomly generated levels.
The game has five generated levels.
