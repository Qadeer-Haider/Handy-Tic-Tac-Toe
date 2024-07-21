# Handy-Tic-Tac-Toe
<!-- --
This project implements a Tic Tac Toe game where the user interacts with the game board using hand gestures captured by a webcam. The game uses MediaPipe for hand tracking and OpenCV for image processing. The game alternates turns between the player and a simple AI, which uses a basic strategy to determine its moves.

## Project Structure

1. **Video Capture and Frame Processing**
    - Opening the webcam
    - Processing video frames
    - Displaying messages on the frame

2. **Game Mechanics**
    - Initializing the game board
    - Drawing the Tic Tac Toe grid and marks
    - Checking win conditions and draws
    - Handling player and computer moves

3. **Hand Gesture Recognition**
    - Using MediaPipe for hand landmark detection
    - Mapping hand gestures to game actions

4. **User Interface**
    - Displaying player name input
    - Managing game state transitions

## Video Capture and Frame Processing

### Opening the Webcam

The webcam is opened using OpenCV to capture real-time video frames for the game.

### Processing Video Frames

Frames are processed to include the Tic Tac Toe grid and user gestures.

### Displaying Messages

Messages such as game results are displayed on the video frame using OpenCV.

## Game Mechanics

### Initializing the Game Board

The game board is initialized with empty cells, and the turn is set to the player.

### Drawing the Tic Tac Toe Grid and Marks

The grid is drawn on the frame, and marks (X or O) are placed based on player and computer moves.

### Checking Win Conditions and Draws

The game checks for win conditions and draws by evaluating the board state after each move.

### Handling Player and Computer Moves

Player moves are detected via hand gestures, and the computer makes moves using a basic strategy.

## Hand Gesture Recognition

### Using MediaPipe for Hand Landmark Detection

MediaPipe is used to detect hand landmarks and track the index finger to determine the cell being pointed at.

### Mapping Hand Gestures to Game Actions

The position of the index finger is mapped to the Tic Tac Toe grid to make moves in the game.

## User Interface

### Displaying Player Name Input

The user is prompted to enter their name before starting the game.

### Managing Game State Transitions

The game handles transitions between player and computer turns, as well as game resets after a win or draw.

## Functions Overview

### Open_Video_Frame()

Opens the webcam for video input.

### display_message(message, frame, position, font_scale, color, thickness)

Displays a message on the video frame.

### get_window_height_and_width()

Gets the dimensions of the screen and calculates window size.

### draw_grid(frame)

Draws the Tic Tac Toe grid on the frame.

### draw_marks(frame, board)

Draws the X and O marks on the Tic Tac Toe board.

### get_cell_number(frame, coordinate_of_index)

Gets the cell number based on the index finger coordinates.

### initialization()

Initializes the game board and turn.

### is_win(board, player_symbol)

Checks for a win condition.

### is_draw(board)

Checks if the game is a draw.

### is_valid_move(board, ri, ci)

Determines if a move is valid.

### computer_move(board, cs, ps)

Determines the computer's move using a basic strategy.

### update_text(key, typed_text)

Updates text based on key presses.

### main()

Main function to run the game.

## Game Flow

1. **Start Game**: Opens the webcam and initializes the game board.
2. **Player Name Input**: Prompts the user to enter their name.
3. **Hand Gesture Detection**: Tracks the index finger to select cells.
4. **Game Turn**: Alternates turns between the player and the computer.
5. **Win/Draw Check**: Checks for win or draw conditions after each move.
6. **Game Reset**: Resets the game after a win or draw.

## Screenshots

### Tic Tac Toe Grid and Marks

![Tic Tac Toe Grid](https://example.com/tic-tac-toe-grid.png)

### Hand Gesture Control

![Hand Gesture](https://example.com/hand-gesture.png)

## References

- [MediaPipe Documentation](https://google.github.io/mediapipe/)
- [OpenCV Documentation](https://docs.opencv.org/)
- [Hand Gesture Recognition with MediaPipe](https://github.com/google/mediapipe)
