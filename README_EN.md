# 🧬 Conway's Game of Life - Infinite Canvas

A modern, interactive, and high-performance implementation of **John Conway's famous Game of Life**, written entirely in **pure JavaScript (Vanilla JS)** with no external dependencies.

This project uses HTML5 Canvas to render a large virtual grid, offering smooth navigation controls similar to those of an interactive map (Pan & Zoom).

![https://via.placeholder.com/800x400?text=Screenshot+Game+of+Life+Preview](https://github.com/prinzimaker/game_of_life/blob/main/screenshot.png)


## ✨ Key Features

* **Zero Dependencies:** Works on any modern browser by simply opening the HTML file.
* **High-Performance Rendering:** Uses `requestAnimationFrame` and HTML5 Canvas API.
* **Advanced Navigation:**
    * **Smart Zoom:** Zoom in/out centered on the mouse cursor position.
    * **Dynamic Limits:** Zoom adapts to always show the entire game area or a minimum detail of 50 cells.
    * **Pan:** Smooth viewport movement with the right mouse button.
* **Free Drawing:** Click and drag to manually "bring cells to life".
* **Memory Function:**
    * 💾 **Save:** Stores the current grid state in a temporary variable.
    * 📂 **Load:** Instantly restores the last saved state.
* **Minimalist UI:** Floating control bar (Dock) with intuitive icons and integrated visual help.

## 🚀 How to Use

No installation, build system, or local server required.

1.  Download or clone this repository.
2.  Open the `index.html` file in your preferred browser (Chrome, Firefox, Edge, Safari).
3.  Start playing!

## 🎮 Controls

### Mouse
| Action | Input |
| :--- | :--- |
| **Draw / Erase** | Click and drag **Left Button** |
| **Move View** | Click and drag **Right Button** (or Middle) |
| **Zoom In / Out** | **Mouse Wheel** |

### Interface (Dock)
The control bar is located at the bottom center of the screen:

* ▶ **Play:** Start the simulation.
* ■ **Stop:** Pause the simulation to modify the grid.
* 🔀 **Random:** Generate a random distribution of living cells.
* 🗑️ **Clear:** Clear the entire grid (kill all cells).
* 💾 **Save:** Save the current configuration to memory.
* 📂 **Load:** Load the saved configuration from memory.

## 🛠️ Technical Details

### Virtual Grid & Camera
The game simulates a fixed-size virtual grid (e.g., 300x300 cells) that is much larger than the browser viewport.
The "camera" manages visualization through 2D matrix transformations:
```javascript
ctx.translate(camera.x, camera.y);
ctx.scale(camera.zoom, camera.zoom);
```
