# **Conceptual Overview \- Programmer**

## Stars Align Video Game

# **Introduction**

This conceptual overview explains the general concept of the game, ‘Stars Align’, that a game developer would need to know in order to create it. A programmer should read this if they are new to the project and need help setting up to begin working. After reading this document a programmer should understand the game engine they will be using, the programming language they will be writing in, the basic game concept and breakdown, as well as where they can find more precise information about the different parts of the game that they will need to build. For more information on each specific topic the programmer should read the topic’s specific document.

- Note that they don’t need to worry about story, give additional context maybe?

# **Parts and Tools**

## *Game Infrastructure*

This section goes over the basic tools and setup that the programmer will need to begin developing the game. 

* Language: python   
  * Ren'Py[^1] specific functions should be known  
* Game engine: Ren'Py  
* Programming editor: Visual Studio Code  
* Genre: visual novel[^2] and puzzle game  
* Installation: for installation please see reference page

## *Game UI*

This section goes over the basic set up of the game’s UI. This should be read to gain an understanding of the way the UI will operate and interact between the different screens in broad strokes.

* Main menu WILL HAVE:  
  * Start game  
  * Load (a previous save file)  
  * Preferences  
  * Fates  
  * Achievements  
  * About  
  * Help  
  * Quit  
* In game menu WILL HAVE:  
  * Save  
  * Load   
  * Preferences  
* In game menu SHOULD NOT HAVE:  
  * Look back through dialogue history while they are playing  
  * Skip dialogue  
  * Go back in dialogue  
  * Auto the dialogue (when dialogue plays on its own)  
* Fates screen WILL HAVE:  
  * The menu necessary to change a character’s character traits[^3]  
* Achievements screen WILL HAVE:  
  * The menu necessary to change a character’s character traits  
* All screens besides main menu SHOULD NOT HAVE access to all the other screens, unless otherwise specified like with in game menu  
  * All sub screens (ie save, load, preferences, achievements, etc), should have a back button to return to the main menu

## *Gameplay*

This section will explain the general game loop that the programmer will be expected to develop. A programmer should be familiar with this general structure before looking into details on each specific game mechanic.

* Game loop:  
  * Introduction (or the tutorial):  
  * Player opens main menu  
    * Player can enter any of the permitted screens (as listed in game ui)  
  * Optional: Player enters the game and assists in conducting a survey  
    * Player receives results of survey  
  * Player is greeted by the astrologer and is told that they should help the main character complete their day to day tasks while he does his work  
  * Player enters the basic game loop of cleaning the room  
    * The player at this point cannot actually do anything besides clean the room and after doing so completes the first game loop.  
    * The astrologer gives the player the ability to change the main character’s ‘characteristics’ allowing the player to now replay and gain access to certain puzzles and receive new dialogue options.  
    * The astrologer asks the main character to help the main character see the truth/help her get out.  
  * A day’s game loop:   
    * Player changes main character’s ‘character traits’  
    * Player enters the game  
    * Player in the game can now access new information, puzzles and new tasks.  
    * Player completes tasks/puzzles  
    * The day/loop ends when the player completes all the originally assigned tasks (clean the room)  
    * Repeat  
  * Ending\!

* Endings:  
  * Vary depending on what ‘character traits’ the player gives the main character, although they are not truly endings but more like thoughts/monologues the main character shares based off the puzzles/information the player uncovers and how the player behaves  
    * If the player is nice \-\> the main character will respond kindly  
    * If the player is unking/rude \-\> the main character will become sad (this carries over between days)  
  * The actual ending:the main character with the help of the player finds the box under the floorboards, solves it and leaves the room (revealed the main character is talking to themselves in the mirror, not the player)  
    * This can only happen with the proper collection of character traits unlocked  
  * If there will be proper alternative endings is still in development and undecided


:  


[^1]:  Ren’Py: Ren’Py Visual Novel Engine, or Ren’Py for short is a free and open-source game engine which was specifically designed for the creation of visual novel games.

[^2]:  Visual novel: a form of digital interactive fiction characterized by static or minimally moving sprites. The game focuses on story and player choices. (example: Ace Attorney)

[^3]:  Character traits/characteristics: within the game the player can define the main character’s personality by giving them specific stars in a constellation. For example, they could give them a star segment that states they are curious, giving the player the chance to explore. Alternatively, the player can define the character to be melancholic, making them more sad and introspective in their dialogues.
