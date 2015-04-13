---
published: false
---

For my next learning session of Unity I decided to go with the [2D Roguelike](http://unity3d.com/learn/tutorials/projects/2d-roguelike). The main reason of why I choose this one over the others it's the fact that this tutorial was already made in Unity 5, having no risk of encountering something that changed over the transition between Unity 4 and 5.

As I'm starting to blog I haven't actually decided the way I feel more comfortable with for my analysis and review so I'm still experimenting. Don't think you misspelled the address, I'm just trying something different than the other format.

## About the tutorial

'Learn how to make a 2D Roguelike game with this project. Over the course of the project will create procedural tile based levels, implement turn based movement, add a hunger system, audio and mobile touch controls. This video series was filmed in Unity 5, but is compatible with Unity 4.6 as well.'

Basically another project with most part of the assets ready for use and most part is focused aiming to create a basic 2D Roguelike.

## Part by part analysis

 As I said, I'm experimenting a different way to review and analyze the tutorial, so I'm going to share some thoughts and basic overview for each part of the project tutorial.

### Chapter 1

#### [Part 01 - Project Introduction](http://unity3d.com/learn/tutorials/projects/2d-roguelike/introduction)

 Not much to be said about this part, like most unity learning modules the first part is used to give a brief explanation of what we want to do and how to set the project up

#### [Part 02 - Player and enemy animations](http://unity3d.com/learn/tutorials/projects/2d-roguelike/animations)

 This part is basically composed of grouping sprites of the player and the enemy in a way that they create an animation. It's easy to understand but still
 very important and useful for most people who want to learn how to group their sprites in a easy way. It's easy to notice how Unity have been making the life of 2d game developers.
 
 #### [Part 03 - Creating the tile prefabs](http://unity3d.com/learn/tutorials/projects/2d-roguelike/tileprefabs)
 
 Just like the 2nd part, this one is focused on creating all the assets using the sprites available in the spritesheet. Like the title says, we create the tiles that the game will use. Pretty basic stuff, not much to learn here.
 
 #### [Part 04 - Writing the board manager](http://unity3d.com/learn/tutorials/projects/2d-roguelike/boardmanager)
 
 This is one of the most important and useful parts of the tutorial. It goes through the whole creation of the board, creating a class inside the board manager class and turning it serializable for showing it on the inspector (really useful). The whole generation of the board is pretty interesting because it's made in a way that have bits of randomness and at the same time so much consistency.
 
 #### [Part 05 - Writing the game manager](http://unity3d.com/learn/tutorials/projects/2d-roguelike/gamemanager)
 
 Like the board manager, the game manager represents a valuable part of the game itself, since it's the good guy game manager who's gonna boss around the board manager and the sound manager. Despise it being so necessary for the game, the chunk of code for the game manager is pretty simple, being in the end just a singleton with one or two special functions.
 
 #### [Part 06 - Moving object script](http://unity3d.com/learn/tutorials/projects/2d-roguelike/movingobject)
 
 The moving object script is the base for the player and the enemy. The code for this part is more advanced, making use of abstract classes and generic type functions. I could say that this is one of the most important parts of the game, since you have to use this script for managing enemy and player behaviour.
 
 #### [Part 07 - Creating destructible walls](http://unity3d.com/learn/tutorials/projects/2d-roguelike/wall-script)
 
 Since the walls are going to represent an obstacle in the player game they must present a way to the player overcome such them, so why not make the walls breakable? This part involves pretty much just a wall script and the chunks of code are pretty simple, where we create ways for the wall to be breaked.
 
 #### [Part 08 - Player animator controller](http://unity3d.com/learn/tutorials/projects/2d-roguelike/player-animator)
 
 Using the animator in Unity it's really easy if you don't have many states for your sprite so likewise this video covers some pretty basic stuff for setting up the player animations. It's good to see that we must adjust some settings when we're dealing with 2D sprites like removing the transition.
 
 #### [Part 09 - Writing the player script](http://unity3d.com/learn/tutorials/projects/2d-roguelike/player-script)
 
 The player script makes use of the moving object class so many parts are way more simple thanks to that. It's nice to note that the major functions in this script are the OnCantMove, that deals with the player obstacles, and the OnTriggerEnter2D, that deals with the player interaction with other game objects like soda and the exit.