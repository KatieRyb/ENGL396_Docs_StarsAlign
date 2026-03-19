# **Setup**

Make sure you have downloaded the Ren’Py application from their [official website](https://www.renpy.org/latest.html), as in this document you will be taught how to build two of the puzzles in the Stars Align game.

# **The Game Engine Review**

To begin, create your project by **pressing the ‘Create New Project’ button**. **Name the project ‘Stars Align’** when prompted, and then **click on ‘Stars Align’ to select the project** on the left hand side as shown below.

![](task1.png)

You will be using a few specific buttons in the Ren’py game engine:

- **Navigate script**: this opens up a navigation window to all of the scripts your selected project has associated with it. Ren’Py automatically generates the following scripts: gui.rpy, options.rpy, screens.rpy, script.rpy.  
- **Images**: this will open up your images folder in your game’s folder in your file explorer. This is where you will be putting all your 2D game assets into.  
  - The path to this will look something like: Stars Align (or whatever name the project is) -> game -> images

![](task2.png)

This is what clicking on Navigate script will show you currently.  

![][image4]  

If you **double click on script.rpy** it will open up the file in Visual Studio Code. Currently your code will look like this; 
```
label start:  
    scene bg room

    # This shows a character sprite. A placeholder is used, but you can  
    # replace it by adding a file named "eileen happy.png" to the images  
    # directory.  
    show eileen happy

    # These display lines of dialogue.  
    e "You've created a new Ren'Py game."

    e "Once you add a story, pictures, and music, you can release it to the world\!"

    # This ends the game.  
    return
```

The **label start indicates where the program begins to run from**. We will not be writing all of our puzzle code here, instead we will **create new labels and screens** that we will **call from the start label**.  
**Return as shown ends the game.**

If we **want to test the labels or screens** that we will be writing for the Stars Align project, we will be **using the start label as the place to debug our code by calling those methods**.

Now that you have created your first Ren’Py project, let’s add some puzzles to it! The first puzzle you will be making is a grid puzzle.

# **Puzzles**

Puzzles are screens within the game into which the player can enter and attempt to solve them. Within this documentation there are two puzzles that I will explain how to construct, [grid puzzle](GridPuzzle.md) and [book puzzle](Book.md). The grid puzzle while more complex is a good place to start to learn more about Ren'Py and to understand how to work with data in Python. There are and will be other screens within the game that are not puzzle, like menus, but the majority of them will be puzzles.

