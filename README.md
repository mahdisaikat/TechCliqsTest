# Langton's Ant JavaScript Implementation

This project demonstrates Langton's Ant simulation using HTML and JavaScript. Langton's Ant is a cellular automaton that follows simple rules but exhibits complex and unpredictable behavior.

## Usage

Open the `index.html` file in a web browser to run the Langton's Ant simulation.

## Code Overview

- **`index.html`**: HTML file containing the canvas element and JavaScript code.
- **`script.js`**: JavaScript file with the Langton's Ant implementation.

## Implementation Details

### Langton's Ant Logic

- The ant moves forward, turning clockwise or counterclockwise based on the color of the current cell.
- The grid cells are represented by a 2D array (`grid`), where `0` represents white and `1` represents black.

### Canvas Rendering

- The canvas is used to visualize the grid and the ant's movement.
- The ant is drawn as a blue triangle with legs.

### Ant Movement

- The ant's direction (`up`, `right`, `down`, `left`) is updated based on the current direction and cell color.
- The ant's position is updated, and the cell color is flipped.

## Corner Cases

1. **Grid Edge Case**
   - Test with smaller `gridSize` values (e.g., 5) to ensure the ant behaves correctly near the edges of the canvas.

   ```javascript
   const gridSize = 5;

2. **Initial Ant Position**
   - Confirm that the ant starts at the center of the grid.

   ```javascript
   const ant = { x: Math.floor(cols / 2), y: Math.floor(rows / 2), direction: 'up' };

## Test Cases

1. **Multiple Ants**
   - Create multiple ants with different starting positions and directions.

   ```javascript
   const ants = [
      { x: 5, y: 5, direction: 'right' },
      { x: 15, y: 10, direction: 'down' },
      // Add more ant configurations
   ];

2. **Random Initial Grid Colors**
   - Initialize the grid with random cell colors and observe the ant's reaction.

   ```javascript
   let grid = Array.from({ length: rows }, () => Array(cols).fill(Math.round(Math.random())));

3. **Speed Variation**
   - Test the animation with different speeds.

   ```javascript
   const animationSpeed = 500; // Faster animation
   // OR
   const animationSpeed = 2000; // Slower animation

4. **Custom Rules**
   - Modify the turning and moving forward rules and observe how the ant behaves.

   ```javascript
   function moveForwardCustomRules() {
     // Custom rules for turning and moving forward
     // ...
   }

5. **Grid Color Visualization**
   - Visualize the grid with different colors for 0 and 1.

   ```javascript
   function drawGrid() {
     for (let y = 0; y < rows; y++) {
        for (let x = 0; x < cols; x++) {
            ctx.fillStyle = grid[y][x] === 1 ? '#000' : '#fff'; // Custom colors
            ctx.fillRect(x * gridSize, y * gridSize, gridSize, gridSize);
        }
     }
   }



This README file provides an overview of the project, details on how to run the simulation, explanations of the code logic, and specific test cases and corner cases for further exploration.










