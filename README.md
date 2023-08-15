# Racoon Raiders

Welcome to the repository for **Racoon Raiders** - a game reminiscent of [Rodent’s Revenge](https://en.wikipedia.org/wiki/Rodent%27s_Revenge).

In this game, raccoons endeavor to infiltrate available garbage cans, while the main player strives to thwart their efforts by ensnaring them with recycling bins.

![Game Animation](https://user-images.githubusercontent.com/94993837/187968590-4eec1d38-8d87-419e-8f9a-ad66e3566129.gif)

## Table of Contents

- [Game Overview](#game-overview)
- [Gameplay Mechanics](#gameplay-mechanics)
- [Program Structure](#program-structure)
- [Demo](#demo)
- [Getting Started](#getting-started)
- [Content Structure](#content-structure)

## Game Overview

The game unfolds on a grid with width and height measured in tiles. Raccoons and the main player move on the grid, and their objective is to interact with garbage cans and recycling bins. The key elements include:

- **Character Movement**: Characters like raccoons, the main player, and recycling bins can move one tile per turn.
- **Raccoon Varieties**: Regular raccoons and smart raccoons (with glasses) follow distinct movement patterns.
- **Garbage Cans**: These can be locked or unlocked, and raccoons may crawl inside them.
- **Trapping Raccoons**: The main player traps raccoons by pushing recycling bins to enclose them.
- **Game Objective**: The main player aims to trap raccoons while maximizing the number of adjacent recycling bins.

## Gameplay Mechanics

- **Player Movement**: Use arrow keys to move the main player.
- **Recycling Bins**: Push them to block raccoons' path.
- **Raccoon Types**: Regular raccoons move randomly, smart raccoons move more intelligently.
- **Garbage Cans**: Racoon can crawl inside unlocked cans.
- **Victory**: Trap raccoons with recycling bins.
- **End Game**: Game concludes when all raccoons are trapped or inside garbage cans.
- **Score**: At the game's end, the score reflects trapped raccoons and adjacent recycling bins.

## Program Structure

The game is built using several classes:

- **Character**: An abstract class representing game characters, defining move and get_char methods.
- **TurnTaker**: Inherits from Character, depicting characters that can take turns, defining a take_turn method.
- **Raccoon**: Class for random raccoon movement.
- **SmartRaccoon**: Class for intelligent raccoon movement (with glasses).
- **GarbageCan**: Represents garbage cans, locked or unlocked.
- **RecyclingBin**: Represents movable recycling bins.
- **Player**: Main player, controlled via arrow keys.
- **GameBoard**: Manages game objects on the board.

## Demo

For a visual representation of how the game works, check out the following GIF:

![Gameplay](https://user-images.githubusercontent.com/94993837/187969771-6a69f1a5-2f68-4eb5-b6e6-08a6583d506c.jpeg)

## Getting Started

To start playing Racoon Raiders, follow these steps:

1. Clone the repository.
2. Execute the game using the appropriate command.
3. Use arrow keys to control the main player and interact with the game elements.

## Content Structure

- **Game Overview**: A brief introduction to the game's concept.
- **Gameplay Mechanics**: Explanation of gameplay elements and rules.
- **Program Structure**: Overview of classes and components in the program.
- **Demo**: A visual GIF showcasing the game in action.
- **Getting Started**: Steps to set up and play the game.

For any questions or feedback, feel free to reach out. Enjoy playing Racoon Raiders!

Thank you for exploring the world of raccoons, recycling bins, and strategic gameplay!

