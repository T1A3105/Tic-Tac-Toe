## Tic-Tac-Toe-Game in Python

A simple and interactive Tic-Tac-Toe game implemented in Python.  
You can play **Player vs Player** or **Player vs Computer** with an optional GUI version.

## Features

- Playable in the console (terminal)
- Two-player mode (X vs O)
- Optional AI opponent
- Detects win, draw, and invalid moves
- Clean and modular code structure
- Optional GUI version with `tkinter`

## Screenshot
![WhatsApp Image 2026-01-22 at 4 19 57 PM](https://github.com/user-attachments/assets/dbb0a945-456f-4f06-8571-7c26a6adfc77)

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/T1A3105/Tic-Tac-Toe.git
cd Tic-Tac-Toe-Python

## Steps to Build Tic-Tac-Toe

Steps to Build Tic-Tac-Toe
Step 1: Plan Your Project
        Decide the game mode:
        Player vs Player (simplest)
        Player vs Computer (optional: AI)
        Decide the interface:
        Console/Terminal (simpler)
        GUI using tkinter or pygame (more impressive for GitHub)

Step 2 : Represent the Board
          Use a list of 9 elements for the 3x3 board:
          board = [" "] * 9
          0 | 1 | 2
          ---------
          3 | 4 | 5
          ---------
          6 | 7 | 8

Step 3: Display the Board
        Create a function to print the board in a readable format:
        def print_board(board):
            print(f"{board[0]} | {board[1]} | {board[2]}")
            print("--+---+--")
            print(f"{board[3]} | {board[4]} | {board[5]}")
            print("--+---+--")
            print(f"{board[6]} | {board[7]} | {board[8]}")

Step 4: Handle Player Moves
        Ask the current player to choose a position (0–8).
        Validate the move (check if the spot is empty).
        Place the player’s symbol (X or O) in that position.
Step 5: Check Win or Draw
        Define winning positions:
        winning_positions = [
            [0,1,2], [3,4,5], [6,7,8],  # rows
            [0,3,6], [1,4,7], [2,5,8],  # columns
            [0,4,8], [2,4,6]            # diagonals
          ]
       Check if a player has all three positions in any winning line.
       If the board is full and no winner → declare a draw.
Step 6: Switch Players
        After each move, switch the current player:
        current_player = "O" if current_player == "X" else "X"

Step 7: Loop Until Game Ends
        Keep asking for moves, updating the board, checking win/draw, and switching players.
        Stop the loop when either:
          A player wins → announce winner
          Draw → announce draw
