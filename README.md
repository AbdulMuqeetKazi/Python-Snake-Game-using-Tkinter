# Python-Snake-Game-using-Tkinter

In this Python tutorial, we'll delve into the exciting world of game development by creating a simple yet addictive Snake game using the Tkinter library. Whether you're a novice programmer or just someone looking for a fun coding project, this tutorial is perfect for you. We'll guide you through the entire process, from setting up your development environment to adding the finishing touches to your game.

Before we start coding the game, let's ensure you have everything set up correctly. 
Follow these steps:

    1)Install Python: If you haven't already, download and install Python from the official website
     (https://www.python. org/downloads/).
    2)Tkinter Installation: Tkinter usually comes pre-installed with Python, so you don't need to worry about this step. 3)To check if Tkinter is available, open your Python IDLE and run the following command:
        import tkinter as tk
    If no errors occur, you're good to go.
    4)Code Editor: Choose a code editor of your preference and install it.



Here's an explanation of the code:

Importing necessary libraries:
    *from tkinter import *: Imports the entire tkinter library for creating GUI elements.
    *import random: Imports the random module for generating random numbers.

Constants and Global Variables:
    *Several constants and global variables are defined at the beginning of the code, specifying attributes of the game *such as dimensions, speed, colors, and more.

Snake Class:
    *The Snake class is defined to represent the snake in the game.
    *It initializes with the snake's size, coordinates, and squares (the individual segments of the snake).
    *The snake's initial coordinates are set to (0, 0) for each segment.
    *The create_rectangle method from the tkinter canvas is used to create each square of the snake, and these squares are stored in the self.squares list.

Food Class:
    *The Food class is defined to represent the food that the snake must eat.
    *It initializes with random x and y coordinates within the game boundaries, and these coordinates are stored in the self.coordinates.
    *An oval shape is created using create_oval from tkinter to represent the food on the canvas.

next_turn Function:
    *This function is called to update the game state after each turn.
    *It calculates the new head position of the snake based on the current direction.
    *If the snake eats the food, the score is incremented, and new food is generated.
    *The function also removes the tail of the snake to maintain its size.
    *It checks for collisions with boundaries or itself using the check_collisions function.
    *If a collision is detected, it triggers the game_over function.
    *Otherwise, it schedules the next turn after a delay defined by SPEED.

change_direction Function:
    *This function is called when the player presses arrow keys to change the snake's direction.
    *It updates the direction global variable but prevents the snake from reversing its direction.

check_collisions Function:
    *This function checks for collisions between the snake and the boundaries of the game window or itself.
    *It returns True if there's a collision and False otherwise.

game_over Function:
    *This function is called when the game is over (i.e., when the snake collides with a boundary or itself).
    *It displays a "GAME OVER" message in the center of the canvas and a "Restart" button to start a new game.

reset Function:
    *This function resets the game when the "Restart" button is clicked.
    *It resets the score, clears the canvas, creates a new snake and food, and starts a new game.

Main Code:
    *The main code initializes the tkinter window, sets up event bindings for arrow keys to change the snake's direction, and creates the initial snake and food.
    *The game loop is started with window.mainloop(), which keeps the game running until the window is closed.