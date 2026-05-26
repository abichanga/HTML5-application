# Fish Eats- Graphics Pipeline Demo

A simple HTML5 Canvas game built for my Multimedia Applications class. The player controls an orange fish using the mouse, eats smaller fish to grow bigger, and avoids larger fish that can eat you.

## How to Run

Just open `fish-eats.html` in any modern browser. No installs or dependencies needed.

## How to Play

- Move your mouse to steer the fish
- Eat fish that are smaller than you (coloured ones)
- Avoid red fish — they are bigger and will eat you
- Every fish you eat makes you grow a bit
- After eating 5 fish, bigger dangerous fish start appearing
- Use the Restart and Pause buttons below the canvas

## Graphics Pipeline Stages

The code is commented to show where each stage of the graphics pipeline occurs:

1. **Application Stage** — Game state, user input (mouse tracking, button clicks), collision detection, fish spawning logic, score tracking. This is all the game logic that decides *what* happens each frame.

2. **Geometry Stage** — The `computeFishGeometry()` function takes a fish's position and size and applies transformations (translation, scaling, rotation) to calculate where each body part (head, tail, fins, eyes) should be. No drawing happens here, just math.

3. **Rasterization Stage** — The `drawFish()` function and other draw functions take the computed geometry and actually render pixels on the canvas using `fillRect`, `ellipse`, `arc`, `lineTo`, etc.

## Technologies Used

- HTML5 Canvas API
- CSS
- Vanilla JavaScript
