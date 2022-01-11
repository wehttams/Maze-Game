The program consists of 3 classes: mazeMaker, Player, and MazeGame. 


The Player class contains the fields used for changing the coordinates of the player rectangle, as well as the methods that do so by multiplying the x, y coordinates by a certain amount depending on user key input. 


The mazeMaker class provides the fields and methods used to create the walls of the mazes displayed on the screen. 


The MazeGame class is the “main” class used for implementing most of the gameplay and game state. Within it contains fields such as the timer, used to move the player and decrement the score, booleans such as gameWon and gameLost, and rectangle objects used for maze walls. The methods it contains implements the main gameplay functionality: the paintComponent method prints out the maze; the score method decrements the score starting from 5000; the collisionDetection method checks if the player hits a wall and, if true, forces the player to restart the maze; the menu method displays the main menu and precedes the maze screen; the winCheck method checks if the user has hit the “goal” at the end of the maze; the loseCheck method checks if the userScore has hit 0; and the winnerScreen and loserScreen replace the maze screen when win or lose conditions are met.

Known glitches: 
* The sound is known to be inconsistent with playing when transferring files across devices.
* Upon beginning the game, the first movement input will cause the drone to undesirably move in a different constant direction. Going up or down makes it move right, and going left or right seems to make it go down. Putting another movement input in the other axis direction solves the problem immediately.
* Upon beginning the game, the drone detects an unknown collision and the score decrements by 100 points, however it does not reset position at all.
* The loser screen has over spawned inconsistently across devices. Hopefully this is not the case for the grader. 
* The winner screen seems to print itself twice. The cause is unknown, but it is suspected to have to do with the lag of the timer.
* Hitboxes of the rectangles are sometimes inconsistent, but it seems to just be Java’s fault.
