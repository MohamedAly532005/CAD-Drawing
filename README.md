# WebGL CAD & Drawing Application

A lightweight, high-performance WebGL-based drawing application that allows users to interactively draw, color, fill, and manage custom 2D shapes directly in the browser.

---

## Features

- **Interactive Vertex Drawing**: Click on the canvas to place vertices and automatically connect them with line strips.
- **Continuous Path Drawing**: Click and drag your mouse to create smooth paths and complex shapes.
- **Custom Color Selection**: Choose from 7 built-in colors:
  - Black
  - Red
  - Yellow
  - Green
  - Blue
  - Magenta
  - Cyan
- **Shape Filling**: Close any custom polygon (minimum 3 vertices) and fill it using WebGL's `TRIANGLE_FAN` rendering.
- **Canvas Clearing**: Reset the canvas to start new drawings instantly.

---

## Project Structure

```text
CAD & Drawing/
├── common/
│   ├── MV.js             # Matrix/Vector library for graphics operations
│   ├── MV2.js            # Alternative Matrix/Vector library
│   ├── webgl-utils.js    # Google's WebGL context utilities
│   ├── initShaders.js    # Utility for inline HTML shader compilation
│   └── README.txt        # Description of common helpers
├── project/
│   ├── squarem.html      # Main HTML entry point
│   └── squarem.js        # Core WebGL graphics application logic
└── README.md             # Project documentation (this file)
```

---

## How to Run

> [!NOTE]
> No build steps or complex installations are required. Everything runs natively in modern web browsers using standard WebGL.

### Method 1: Local File System (Quickest)
1. Open the `project` folder.
2. Double-click **`squarem.html`** or drag it into any modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari).

### Method 2: Local Server (Recommended)
Using a local server is recommended for web graphics to ensure smooth permissions and prevent potential browser policy restrictions.

- **Using Python**:
  ```powershell
  cd "CAD & Drawing"
  python -m http.server 8000
  ```
  Then navigate to: `http://localhost:8000/project/squarem.html`

- **Using VS Code Live Server**:
  Open the project folder in VS Code, open `project/squarem.html`, and click the **Go Live** button in the status bar.

---

## How to Use

1. **Draw Paths**:
   - **Click** anywhere on the grey canvas to draw individual points/vertices connected by lines.
   - **Click and drag** the mouse to draw freeform paths.
2. **Change Colors**:
   - Use the dropdown menu below the canvas to select a new active color before clicking or dragging.
3. **Fill Shapes**:
   - Once you have clicked at least 3 points, click the **Fill Shape** button to close the path and fill the shape with the selected color.
4. **Reset**:
   - Click the **Clear Canvas** button to wipe all drawings and start fresh.
