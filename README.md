# Sokoban in Jack

## Overview

This project is an implementation of the classic Sokoban puzzle game using the Jack programming language as part of the Nand2Tetris course.

The objective of the game is to push boxes onto their target locations while navigating around obstacles. 
Since boxes can only be pushed and never pulled, players must think carefully before every move to avoid deadlock situations. 

The game includes multiple levels with increasing difficulty, requiring more planning and strategy as level progresses.

---

## Gameplay Rules

* Push all boxes onto target locations to complete a level.
* Boxes can only be pushed, never pulled.
* Boxes cannot be pushed against walls or other boxes.
* The player cannot move through walls.
* Some moves can create unwinnable situations, requiring the player to restart the level.

---

## Controls

### During Gameplay

Arrow Keys or WASD - Move player
R / r - Restart current level
Q / q - Quit to menu

### Main Menu

H / h - Help section
L / l - Level selection menu (Unlocked levels can be selected)
ENTER (Return/Enter key) - Start game
ESC (Escape key) - Exit game

### Quit Confirmation

This prompt appears after pressing Q / q during gameplay.

Y / y - Confirm quit  
N / n - Cancel quit

---

## Game Elements

* Player - Rendered as a filled circle
* Wall - Rendered as a brick-pattern block
* Box - Rendered as a filled square
* Target - Rendered as a hollow square
* Box on Target - Rendered as a filled square inside a hollow square

---

## Features

* Multiple Sokoban levels with progressive difficulty
* Optimized rendering to eliminate screen flicker
* Main Menu options to start new game, select an unlocked level, read help section, and exit game
* Best score tracking for each level
* Box pushing mechanics
* Collision detection
* Target location tracking
* Level completion detection
* Move counter
* Restart current level
* Quit level confirmation screen
* Level completion screen
* Victory screen
* Close program confirmation screen
* Ability to enter Main Menu anytime

---

## Project Structure

### Main.jack

Program entry point.

### Game.jack

Main game loop, input handling, movement logic, level progression, efficient rendering coordination 
to avoid flickering, restart functionality, and win detection.

### Level.jack

Stores and manages level layouts and game board state including best scores, lock status, etc.

### Player.jack

Stores and updates the player's position.

### Renderer.jack

Handles all graphics rendering, including walls, boxes, targets, and the player.

### UI.jack

Displays Main Menu, level selection menu, help section, HUD information, and all game messages.

---

## Technical Highlights

* Object-oriented design using multiple Jack classes.
* Clear separation between game logic, rendering, UI, input and level management.
* Tile-based game engine implemented entirely in Jack.
* Custom rendering system built using the Hack graphics API.
* Incremental redraw approach that updates only changed objects and HUD values, avoiding screen flicker during gameplay.
* Support for multiple levels and game state transitions.
* Clear UI messages, main menu, level selection menu, help section, and HUD.
* Ability to start from unlocked levels anytime.
* Program terminates only when user confirms exit option from the Main Menu.

---

## Acknowledgements

Sokoban was originally designed by Hiroyuki Imabayashi in 1981.

This project is an original implementation of the Sokoban game for the Nand2Tetris platform. One of the puzzle layouts is inspired by a classic Sokoban level design.
