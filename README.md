# BoardGames
# BoardGames


# CS611-Assignment 1

---------------------------------------------------------------------------
Name: Beaudlaire Jeancharles
Email: bmalik@bu.edu
Student ID: U70445938

## Files
---------------------------------------------------------------------------

This section should be all of the source code files that have a .java extension. You should also include a brief description of what the class does.

Board.java: The board class represents a board consist up of a two dimensional array of Tile objects. 
BoardGame.java: The BoardGame class is an abstract class that contains most of the default things that a board game would need, such as the board, teams, and methods needed. 
Main.java: The main class is just where we give the user the option to start either puzzle.
Piece.java: The piece class is what makes up the tiles. It is able to hold both a integer
value and a string value.
Player.java: The player class represents a player in our board game. Right now we only have the name attribute for the player but it is easily extendable in the future in case we need other attributes.
SlidingPuzzle.java: This is our main class for the sliding puzzle. It inherits from the BoardGame.java class and does most of the work for the game to function.
Teams.java: Teams.java holds the information of each team and player on those teams.
It also keeps track of team number and team colors for our dots and boxes game.
UserInput.java: The UserInput class handels most of the user input and error checking to make sure that we are getting an input that makes sense from the user. This ensures that we would not need to check it repeatly.
Tile.java: Tile class represents a tile on our board. Our tile consists of 5 pieces that 
is used for dots and boxes to represent the side walls. Althrough sliding puzzle only 
uses one.
Color.java: This color class has a list of colors that we are able to use to make the terminal print which ever colors we desire.
boardDB.java: This class inherites from our original board class. Since we need a different toString method for our dots and boxes game.
QuoridorGame.java: This class contains all the functions and members that keeps our quoridor game working.
ChooseGame.java: This class acts as our starter place to choose which games we want to play and prints the game statics at the end. 

## Notes
---------------------------------------------------------------------------
Please explain the cool features of your program. Anything that you feel like you did a good job at or were creative about, explain it in bullets here. Additionally, any design decisions should be made here.

1. The toString for our board actually was the same exact one as dots and boxes.
2. I decided to limit the lower bound of board size to 3x3 since any lower is unplayable.
3. I decided to give the user the choice of how many walls they would like for both teams
4. I decided that team numbers would only range from 2-4 since any other one does not make sense as there would be no starting points.
5. I used static members to keep track of total number of games played.
6. I could not figure out how to print the statistics if we type quit since I am handeling it in a different class and using System quit right now. I think if I had more  time
I would definitily think of a way to reorganize the userinput handeling.

## Citaions
---------------------------------------------------------------------------
I used this to brush up on DFS
https://www.geeksforgeeks.org/depth-first-search-or-dfs-for-a-graph/

## How to compile and run
---------------------------------------------------------------------------
Your directions on how to run the code. Ideally should resemble the lines below

1. Navigate to the directory after unzipping the files
2. Run the following instructions:
javac *.java
java Main

## Input/Output Example
---------------------------------------------------------------------------
Please give us a full execution of what we should see on the screen. Label each text with input and output. For example:
Output:
[+] Enter 1 for sliding puzzle, enter 2 for dots and boxes, enter 3 for Quoridor game
[+] TYpe quit at any time to exit
Input: 
3
Output:
[+] Welcome to Quoridor Game
[+] Enter board height:
Input:
3
Output:
[+] Enter board width:
Input:
3
Output:
[+] How many teams would be playing?
Input:
2
Output:
[+] How many players per team?
Input:
1
Output:
[+] How many walls are allowed per team?
Input: 
10
Output:
[+] Team 0, enter your team name:
Input: 
First
Output:
[+] Team First, enter your team color:
Input:
Red
Output:
[+] Enter your name Player 0 of team Number 1 :
Input: 
Peter
Output:
[+] Team 1, enter your team name:
Input:
Winners
Output:
[+] Team Winners, enter your team color:
Input:
Blue
Output:
[+] Enter your name Player 0 of team Winners :
Josua
Output:
[+] Current Board: // 1 should be colored red and 7 should be colored blue since those are the players' starting points.
+---+---+---+
| 0 | 1 | 2 |
+---+---+---+
| 3 | 4 | 5 |
+---+---+---+
| 6 | 7 | 8 |
+---+---+---+
[+] Peter, would you like to move your piece or place a wall. Enter m for move and w for wall
Input: 
m
Output:
[+] Peter, which direction would you like to move? (North, South, East, West)
Input:
South
Output:
[+] Current Board:  // 4 should be red now, 7 is still blue
+---+---+---+
| 0 | 1 | 2 |
+---+---+---+
| 3 | 4 | 5 |
+---+---+---+
| 6 | 7 | 8 |
+---+---+---+
[+] Josua, would you like to move your piece or place a wall. Enter m for move and w for wall
Input:
w
Output: 
[+] Josua, which box would you like to choose to place the wall on?
Input:
7
Output: 
[+] Josua, which wall would you like to choose? (North, South, East, West). Vertical walls will place one more below and horizontal walls will place one more to the right.
Input:
North
Output: 
[+] Current Board: // 4 is red, 7 is blue, and the horizontal wall above 7 is blue
+---+---+---+
| 0 | 1 | 2 |
+---+---+---+
| 3 | 4 | 5 |
+---+---+---+
| 6 | 7 | 8 |
+---+---+---+

[+] Peter, would you like to move your piece or place a wall. Enter m for move and w for wall
Repeat until end of the game....
[+] Congradulations!
[+] Would you like to play Quoridor Game again?
Input:
N
Output:
[+] Would you like to choose another game?
Input:
N
Output:
[+] Total number of games finished: 1
[+] Number of sliding puzzle games finished: 0
[+] Number of dots and boxes games finished: 0
[+] Number of quoridor games finished: 1


