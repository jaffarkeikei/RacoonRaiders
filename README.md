In this project, there is a game that is somewhat similar to [Rodent’s Revenge](https://en.wikipedia.org/wiki/Rodent%27s_Revenge).

During the game, raccoons try to climb into one of the available garbage cans. The main player aims to prevent the raccoons from reaching the garbage cans by trapping them using recycling bins.

Here is a little demo of how the game will look like:



![animation](https://user-images.githubusercontent.com/94993837/187968590-4eec1d38-8d87-419e-8f9a-ad66e3566129.gif)



The game takes place on a grid whose width and height are both measured in tiles (also called squares). In the example above, the grid has width 8 and height 6.

The origin is at the top-left corner. The values on the x-axis increase from left to right. The values on the y-axis increase from top to bottom. Below is an example of the tile locations for a game board whose width and height are both 6.

https://q.utoronto.ca/courses/249810/files/19434654/preview

Each character takes up exactly one tile, except that a raccoon can crawl inside an open garbage can, in which case there will be two characters (a raccoon and a garbage can) on the same tile.

Some characters are movable (the main player, raccoons, and recycling bins) while others are static (garbage cans). Some of the movable characters can take turns (the main player and raccoons). Each turn-taking character can move exactly one tile on its turn, in one of the following directions: up, down, left or right. Raccoons are given turns less frequently than the main player, as can be seen in the example gameplay above.

When the game starts, the player is placed on the top-left corner. Raccoons, garbage cans and recycling bins are placed randomly on the board. Two types of raccoons exist in the game: regular raccoons and smart raccoons (with glasses), that move randomly or smartly respectively, aiming to crawl inside the garbage cans.

When a raccoon reaches an unoccupied, unlocked garbage can, it crawls inside and stays there. If the garbage can is locked, the raccoon will use up its turn to unlock it.

The player’s objective is to prevent the raccoons from getting into the garbage cans by trapping them with recycling bins, while trying to keep as many recycling bins clumped together as possible. We want to trap the raccoons, but we do not want to leave recycling bins all over the neighbourhood in doing so!

The player moves using the four arrow keys and pushes around the recycling bins in an attempt to trap the raccoons.

Recycling bins can’t move autonomously but can be pushed by the main player in the hope of trapping the raccoons. When pushed by the main player, a recycling bin moves in the same direction as the player. If the new tile happens to be occupied with another recycling bin, this recycling bin is also moved in the same direction as well. If there is a row or column of recycling bins being pushed, they all move. Here is a little example.

bin_move.gif

A raccoon is considered trapped if it is surrounded in all four directions (diagonals don’t matter) by recycling bins, other raccoons (including ones in garbage cans), the player, or the border of the game board.

The game ends once all raccoons are either trapped or inside garbage cans.

When the game ends, your score is displayed. The score is determined based on the number of trapped raccoons, as well as the maximum number of adjacent recycling bins.

Note that sometimes you may get into a game state where it will become impossible for the game to end (i.e. you can’t possibly trap the remaining raccoons). You will just need to close the game window. In this case, you never see a score.

The program
The program for this assignment consists of the following classes in a1.py:

Character: An abstract class that represents any character in the game. All characters must define move and get_char methods.

TurnTaker: An abstract class that inherits from Character that represents any character in the game that can take a turn. All turn-takers must define a take_turn method in addition to the Character abstract methods.

Raccoon: A class representing a raccoon that moves around randomly.

SmartRaccoon: A class representing a raccoon that moves in a less random way. This is drawn as a raccoon with glasses.

GarbageCan: A class representing a garbage can that a raccoon can climb into. A garbage can cannot be moved around. It is either locked or unlocked; a player can lock it, but a raccoon can open it.

RecyclingBin: A class representing a recycling bin that a raccoon cannot climb into, but a player can move around to trap the raccoons.

Player: The player that the user can move around via the arrow keys on their keyboard.

GameBoard: The game board that keeps track of the game objects. In this board, there is at most one item on each tile, with this exception: A raccoon can climb into an unlocked garbage can.

The required public interfaces to every class, method, and function have been designed, but we have left some private implementation decisions up to you.

The file a1_game.py is client code for the code you complete in a1.py and handles the actual playing of the game. You do NOT need to write any code in a1_game.py, but you can run it as you complete the assignment to see your progress towards the working game!

