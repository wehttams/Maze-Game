The program consists of 3 classes: mazeMaker, Player, and MazeGame. 


The Player class contains the fields used for changing the coordinates of the player rectangle, as well as the methods that do so by multiplying the x, y coordinates by a certain amount depending on user key input. 


The mazeMaker class provides the fields and methods used to create the walls of the mazes displayed on the screen. 


The MazeGame class is the “main” class used for implementing most of the gameplay and game state. Within it contains fields such as the timer, used to move the player and decrement the score, booleans such as gameWon and gameLost, and rectangle objects used for maze walls. The methods it contains implements the main gameplay functionality: the paintComponent method prints out the maze; the score method decrements the score starting from 5000; the collisionDetection method checks if the player hits a wall and, if true, forces the player to restart the maze; the menu method displays the main menu and precedes the maze screen; the winCheck method checks if the user has hit the “goal” at the end of the maze; the loseCheck method checks if the userScore has hit 0; and the winnerScreen and loserScreen replace the maze screen when win or lose conditions are met.

Flourish: Our game implements a playSound method utilizing the javax.sound.sampled imports which searches for a file containing the specific .wav file to play a sound. Our project game plays the Family Feud ‘Ding!’ sound on start up (and has a fun little button to just keep playing it). It also has a hit marker sound when colliding with something, plus a victory and loser theme when either happens. The sound files seem to inconsistently work across different devices, but it does for sure work on the main computer the sound methods were built on, so if needed, we can record a video showing that it works on our end. The user will have to download the wav files and store them in the project folder in another folder specifically named “SoundFiles” otherwise the sound doesn't work. In the situation where the audio cannot be played, it will enter a catch throw and display an error message to the user.


The game is a simple maze game. Upon start up, the user is prompted with a menu containing two buttons, one to begin the game and the other is for fun times to make a dinging noise. The user controls a red square and guides themselves throughout a maze. The score clocks down from 5000 points and decreases by 100 points per second. If the user collides with a wall before reaching the goal, they will lose an additional 100 points. Upon reaching the end, they are greeted with a victory screen. If the user does not reach the end before the score reaches 0 and below, they will be prompted a loser screen.


Known glitches: 
* The sound is known to be inconsistent with playing when transferring files across devices.
* Upon beginning the game, the first movement input will cause the drone to undesirably move in a different constant direction. Going up or down makes it move right, and going left or right seems to make it go down. Putting another movement input in the other axis direction solves the problem immediately.
* Upon beginning the game, the drone detects an unknown collision and the score decrements by 100 points, however it does not reset position at all.
* The loser screen has over spawned inconsistently across devices. Hopefully this is not the case for the grader. 
* The winner screen seems to print itself twice. The cause is unknown, but it is suspected to have to do with the lag of the timer.
* Hitboxes of the rectangles are sometimes inconsistent, but it seems to just be Java’s fault.
