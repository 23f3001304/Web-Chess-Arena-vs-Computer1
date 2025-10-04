# Chess Arena

## Summary

Chess Arena is a production-ready web application that allows users to play chess against a powerful, client-side AI opponent. The goal of this project is to provide a polished, smooth, and accessible chess experience that runs entirely in the browser, without the need for remote engines or cloud calls.

## Setup

To get started with Chess Arena, you'll need to have Node.js and npm installed on your machine.

1.  **Clone the repository:**

    
```bash
    git clone https://github.com/your-username/chess-arena.git
    ```


2.  **Navigate to the project directory:**

    
```bash
    cd chess-arena
    ```


3.  **Install the dependencies:**

    
```bash
    npm install
    ```


4.  **Start the development server:**

    
```bash
    npm start
    ```


    The application will be available at `http://localhost:3000`.

## Usage

Once the application is running, you can start a new game by clicking the "New Game" button. You can choose your desired difficulty level and time control.

To make a move, simply drag and drop the pieces on the board. The board is fully responsive and supports touch and keyboard controls. Legal moves will be highlighted when you select a piece.

The application also includes a number of other features, such as:

*   **Move history:** A list of all moves made in the game, with the ability to undo and redo moves.
*   **Timers:** Both increment and countdown timers are available.
*   **Score tracking:** The score is displayed based on the material advantage.
*   **PGN/FEN import-export:** You can import and export games in PGN or FEN format.
*   **Opening book hints:** The application will provide hints from a built-in opening book.
*   **Configurable themes:** You can choose from a variety of board and piece themes.

## Code Explanation

The application is built using modern web technologies, including HTML, CSS, and JavaScript. It uses the following libraries:

*   **chess.js:** A JavaScript library for chess move generation, validation, and game state management.
*   **chessboard.js:** A JavaScript library for rendering the chessboard and handling user interaction.

The project is structured as follows:

*   `index.html`: The main HTML file for the application.
*   `style.css`: The CSS file for styling the application.
*   `script.js`: The main JavaScript file for the application logic.
*   `ai.js`: The JavaScript file for the chess AI.

The AI is implemented in `ai.js` and uses a web worker to run in the background without blocking the UI thread.

## AI Architecture

The chess AI is based on a depth-limited minimax search algorithm with alpha-beta pruning. This algorithm explores the game tree to a certain depth and chooses the move that leads to the best possible outcome for the AI.

The AI's evaluation function is based on a number of heuristics, including:

*   **Material:** The value of the pieces on the board.
*   **Piece-square tables:** The value of each piece on each square of the board.
*   **Mobility:** The number of legal moves available to each player.
*   **King safety:** The safety of the king from attack.
*   **Pawn structure:** The structure of the pawns on the board.

The AI also uses a transposition table to store the results of previous searches, which can significantly improve performance.

## How to Tweak Evaluation Weights

You can tweak the AI's evaluation weights by modifying the `evaluation.js` file. This file contains the weights for each of the heuristics used by the AI.

For example, to make the AI more aggressive, you could increase the weight for the `mobility` heuristic. To make the AI more defensive, you could increase the weight for the `kingSafety` heuristic.

After modifying the weights, you will need to restart the development server for the changes to take effect.

## Running Tests

To run the tests, use the following command:


```bash
npm test
```


## Extending Features

There are a number of ways you could extend the features of Chess Arena, such as:

*   **Adding more opening books:** You could add more opening books to the application to provide a wider variety of opening hints.
*   **Implementing different AI algorithms:** You could implement different AI algorithms, such as Monte Carlo Tree Search, to provide a different playing experience.
*   **Improving the user interface:** You could improve the user interface by adding new features, such as a chat box or a friends list.

## License

This project is licensed under the MIT License.