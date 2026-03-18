# **Reference Documentation \- Programmer**

# **Introduction**

Here is a database of all the variables and functions used in the grid puzzle and the book puzzle. It contains all of the variables with their respective value, with more complex ones like lists having a miniature explanation provided as well. Functions are explained only by their purpose, the whole code for them is not included. Use this to check you have all the necessary pieces to run the code at the end or as a guide for what variables and functions should look like when you are creating your own screens.

# **Grid Puzzle:**

## *Variables*

**cell\_width** \= 195

**cell\_height** \= 138

**rows** \= 6

**cols** \= 6

**start\_x** \= 100

**start\_y** \= 100

**board** \= \[ \[None for x in range(cols) \] for y in range(rows) \]

**sidebar\_x** \= 1200

**sidebar\_y** \= 100

**spacing** \= 20

**available\_pieces** \= set(pieces.keys()): a list of all the names for pieces that are not in the grid yet.

**piece\_home** \= {}: a list to which the program can add all of the pieces that are available to the player to drag and drop.

**i**\=0: a variable assisting in traversing the ‘for name in pieces.keys():’

**pieces** \= { “L”: { “shape”: \[ (0,-1), (0,0), (0,1), (-1,1) \], “image”: “Lpuzzlepiece.png” },   
                “Square”: { “shape”: \[ (-1,-1), (0,-1), (-1,0), (0,0) \] “image”: “Squarepuzzlepiece.png” },   
                “Horizontal”: { “shape”: \[ (0,0), (-1,-1), (0,-1), (1,-1) \], “image”: “Horizontal.png”} }:  the dictionary for all the pieces that can be dropped onto the grid.

## *Functions*

**can\_place(board, shape, x, y)**: returns True/False depending on if a piece can or cannot be placed onto the grid. 

**place\_piece(board, shape, x, y, piece\_name)**: places a piece onto the grid.  
remove\_piece(board, piece\_name): removes a piece from the grid and adds it back as an available piece.

**make\_drop\_callback(x,y)**: this function is called by the screen when a player attempts to drag and drop the piece onto the grid. It then calls the nested function inside of it.

- **callback(drop\_target, drags)**: nested inside make\_drop\_callback, it calls on can\_place(), pleace\_piece() and remove\_piece() to actually add pieces to the grid if they can be placed. It also notifies the developer on what coordinates the piece is being dropped.

# **Book Puzzle:**

## *Variables*

**first\_choice** \= none

**current\_books** \= \[“C”, “B”, “A”\]: the ordered list of the way the books will appear on the screen when the game is loaded in.

**correct\_books** \= \[“A”, “B”, “C”\]: the ordered list of the way the books should be lined up on the screen for the player to solve the puzzle.

**book\_images** \= { “A”: “bookA.png”, “B”: “bookB.png”, “C”: “bookC.png”,}: the list of all the book images when the book is not selected.

**book\_selected\_images** \= { “A”: “bookA\_selected.png”, “B”: “bookB\_selected.png”, “C”: “bookC\_selected.png”,}: the list of all the book images when the book is selected.

## *Functions*

**swap\_books(index)**: swaps two books. When the swap takes place the passed-in index variable is the index of the second book that is being moved to the index of the first book that has been selected. The index of the first selected book was saved to first\_choice.