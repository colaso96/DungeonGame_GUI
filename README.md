## Overview:
In this version of our adventure game, you will add an option to play the game using an interactive graphical user interface (GUI).

## Features:
The user starts by specifying the rows, columns, interconnectivity, whether the grid wraps or not, the number of monsters in the dungeon and the percentage of treasures that are in the caves.
The dungeon game has a sequence of features that will create a 2D grid.  Using Kruskals algorithm and corresponding helper methods this program
creates a minimum spanning tree connecting all points on the grid.  For each point on the grid if there are two directions in or out then the point is
classified as a tunnel.  Otherwise, the point is labeled a cave. After the grid is created we can start to play the game.
Features of the game include:
- Placing treasure & arrows in a certain pct of caves in the grid, from the user specified percentage
- The player starting at the set location on the grid and an output when the player reaches the end, which is at least 5 spaces away from the start
- Output of possible directions to move for the player within the grid
- Output of the players location, name, treasures they have collected, the amount of arrows they have and if they are at the end
- Displaying the players movements varying on how the grid is created i.e.:
  - wrapping or non wrapping grid
  - Degree of interconnectivity
  - rows & columns of the grid
- The player can move with a given direction
- The dungeon has monsters in the cave specified by user input, but always includes one monster at the end location
- The player can shoot a monster given a direction and distance
  - arrows are cooked so they will follow a different direction if they enter a  tunnel that turns
  - if the arrows final distance is in a cave with a monster then the monster is hit
  and loses 50 health
  - a monster dies when their health reaches 0
- a player can win the game when they reach the end location and the monster is dead, or if the monster has 50 health then the player has a 50% chance of surviving

GUI:
- The GUI shows the players description on the bottom label, the game state as well as results of user inputs on the right and a menu bar with instructions, game settings & buttons to restart with the same grid, reset the game and exit the game.

## How To Run:
The user starts by specifying the rows, columns, interconnectivity, whether the grid wraps or not, the number of monsters in the dungeon and the percentage of treasures that are in the caves.

The main output will display the players location, which directions they can move, what treasures the room has an asks to input move, pickup or shoot.

If the user enters "P" then the player will pickup the treasures that are in the room.
If the user enters "M" then it will ask the player for a valid direction, given by the arrow keys or keyboard input then execute the move, displaying the output to the screen and asking for the next move.

The player can also click on a valid cell to execute a move.

If the user enters "S" then it will ask the user to specify a valid direction and a distance between 1-5. It will then output if the monster has been hit and for the next move.

## Description of Examples:
In addition, the GUI shows the players description on the bottom label, the game state as well as results of user inputs on the right and a menu bar with instructions, game settings & buttons to restart with the same grid, reset the game and exit the game.

The image shown in the game start file is a blank dungeon since the player has not explored yet.  It starts with multiple blank tiles and the start cell explored, the player shown & the thief shown.

The next image is the dungeon after the game is over and shows the player at the end state with no monster.  This GUI shows the current step plus where the open pathways are shown.

Finally, we have an image shown with paths that the player has explored as well as the end state of the player encountering the monster at the end and dying.

## Assumptions:
I assume that the player will always collect the treasure & arrows if there are any items in the cave.  In addition, I assumed that the player can only shoot an arrow a max distance of 5.  I also assumed that the thief would steal every treasure and every arrow from the player.

