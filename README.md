## Snake Game
This project is a JavaScript-based **Snake Game**, which is built to run on a web browser. Here’s a detailed breakdown:

### Project Description
The Snake Game is an interactive game where the player controls a snake to eat food, causing it to grow in length. The goal is to continue eating food to increase the score, while avoiding collisions with the snake's own body or the walls. The game maintains the player's high score across sessions using browser local storage.

### Key Concepts Used

1. **HTML Structure**:
   - The `index.html` file provides the base structure of the game. It includes sections for displaying the score, high score, and directional controls (arrows).
   - A `play-board` div acts as the main area where the snake moves and food appears.

2. **CSS Styling** :
   - The game would use CSS to style elements, position the grid, and visually represent the snake and food.

3. **JavaScript Game Logic**:
   - **DOM Manipulation**: JavaScript is used to select and modify elements (`play-board`, `score`, `high score`, and controls).
   - **Game Loop**: The game runs on a loop (`setInterval`), calling `initGame` to update the game state regularly.
   - **Event Handling**: Uses `keydown` events and control buttons for directional inputs. Listeners adjust the snake’s direction based on arrow key presses.
   - **Local Storage**: The game’s high score is stored and retrieved from local storage, allowing the player to maintain their highest score across sessions.

4. **Game Mechanics**:
   - **Food Generation**: The food position is randomly generated within the grid, ensuring it appears in new locations each time.
   - **Snake Movement**: The snake moves in a grid-based environment, with each segment following the previous segment’s position to simulate a slithering motion.
   - **Collision Detection**: Checks for collisions between the snake’s head and walls or its own body. If a collision is detected, the game ends.

5. **Score Calculation**:
   - Every time the snake eats food, the score increases, and the high score is updated if the current score exceeds it.

### Resources and Tools Used

1. **HTML & CSS** for game layout and styling.
2. **JavaScript**:
   - Core functionality, game loop, and logic implementation.
   - **LocalStorage** API to save and retrieve high scores.
   - Event listeners for capturing key inputs and button clicks.
3. **Development Tools**:
   - **Browser Developer Tools** (for debugging JavaScript and styling).
   - **Code Editors**: VS Code or similar for writing and managing the code files.

### Functions

Here are the main functions within `script.js`:

1. **`updateFoodPosition()`**: Generates a new position for the food on the grid.

2. **`handleGameOver()`**: Handles game termination by clearing the interval and reloading the page.

3. **`changeDirection(e)`**: Updates the snake’s direction based on keyboard input (arrow keys) or button clicks.

4. **`initGame()`**: The primary game loop function that:
   - Moves the snake based on current velocity.
   - Checks for food collision, wall collision, and self-collision.
   - Updates the display of the snake and food on the play board.

The project combines HTML, CSS, and JavaScript to create an engaging, browser-based game with interactive elements and dynamic scorekeeping.
