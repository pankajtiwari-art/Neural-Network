# 🧠 Quantum Neural Network 🌌

![Three.js](https://img.shields.io/badge/Three.js-Black?style=for-the-badge&logo=three.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![WebGL](https://img.shields.io/badge/WebGL-990000?style=for-the-badge&logo=webgl&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

A highly interactive, visually stunning 3D visualization of a complex neural network built entirely with **Three.js** and **Custom GLSL Shaders**. This project explores the intersection of quantum physics concepts, mathematics, and web development to render dynamic, glowing nodes and energy connections in a browser-based 3D environment.

🚀 **[Experience the Live Demo Here](https://pankajtiwari-art.github.io/Neural-Network/)**

---

## ✨ Key Features

* **Interactive Energy Pulses**: Click or tap anywhere on the network to send a ripple of energy (pulse) across the nodes and connections. Calculates distance in real-time to create a wave-like effect.
* **Dynamic Formations (Morphing)**: Seamlessly switch between three mathematically generated 3D structures:
  1. **Crystalline Sphere**: A mathematically rigorous spherical distribution using the Golden Ratio for even node spacing.
  2. **Helix Lattice**: A multi-strand DNA-like spiral structure.
  3. **Fractal Web**: A recursive, tree-like branching network.
* **Real-time Density Control**: A custom slider to dynamically increase or decrease the number of nodes (from 30% to 100%) without reloading the page, optimizing performance based on your device.
* **Thematic Color Palettes**: Three distinct visual themes (Purple Nebula, Sunset Fire, Ocean Aurora) that instantly update the node colors, connection lines, and glowing energy pulses.
* **Custom Shaders (GLSL)**: Utilizes complex Vertex and Fragment shaders paired with Simplex Noise to create a "breathing" effect, natural node jitter, and glowing auras that respond to the environment.
* **Premium UI**: Features a modern, responsive **Glassmorphism** interface with backdrop filters, hover effects, and animated buttons.

---

## 🛠️ Technologies & Tools Used

* **Three.js (v0.162.0)**: The core 3D library used to render the scene, camera, and geometries.
* **WebGL / GLSL**: Custom shaders for nodes (`THREE.Points`) and connections (`THREE.LineSegments`) to handle complex lighting, pulsing effects, and noise.
* **EffectComposer & Post-Processing**: Includes `UnrealBloomPass` to give the network its signature "neon/quantum" glow.
* **Vanilla JavaScript (ES6 Modules)**: Clean, modular logic using `importmap` for dependency management.
* **HTML5 & CSS3**: For the layout and premium Glassmorphism UI overlays.

---

## 📂 Project Structure

To maintain clean and readable code, the project is divided into three main files:

```text
📦 Quantum-Neural-Network
 ┣ 📜 index.html   # Main entry point, contains UI elements and Three.js import maps
 ┣ 📜 style.css    # Styling for the Glassmorphism UI, sliders, and buttons
 ┗ 📜 script.js    # Core Three.js logic, network generation, controls, and shaders
```

---

## 💻 Installation & Local Setup

Because this project uses JavaScript ES6 Modules (`<script type="module">`), modern browsers block these files from running directly via the `file://` protocol due to CORS (Cross-Origin Resource Sharing) security policies. 

To run this project locally, you **must** serve it through a local web server. Follow these simple steps:

### Step 1: Clone or Download the Repository
Clone the project to your local machine using Git:

```bash
git clone https://github.com/Pankajtiwari-art/Neural-Network.git
cd Neural-Network
```

### Step 2: Start a Local Development Server
Choose **one** of the following methods depending on the tools you have installed:

**Method A: Using VS Code (Recommended for Beginners)**
1. Open the project folder in **Visual Studio Code**.
2. Go to Extensions (`Ctrl+Shift+X`) and install the **Live Server** extension by Ritwick Dey.
3. Right-click on `index.html` in your file explorer and select **"Open with Live Server"**.
4. A new browser tab will automatically open with your project running.

**Method B: Using Python (If Python is installed)**
1. Open your terminal/command prompt inside the project folder.
2. Run the following command:

```bash
python -m http.server 8000
```

3. Open your browser and go to: `http://localhost:8000`

**Method C: Using Node.js (If Node/npm is installed)**
1. Open your terminal inside the project folder.
2. Run this command to serve the folder:

```bash
npx serve .
```

3. The terminal will provide a local link (usually `http://localhost:3000`). Open it in your browser.

---

## 🎮 How to Use (Controls)

* **Rotate**: `Left Click + Drag` to orbit around the 3D structure.
* **Zoom**: `Mouse Wheel` (Scroll up/down) to zoom in and out.
* **Send Pulse**: `Left Click` on the canvas to trigger an energy wave originating from your click point.
* **UI Controls**:
  * **Themes**: Click the colored circles to change the network's color palette.
  * **Density**: Drag the slider to adjust how complex/dense the network is.
  * **Morph**: Click to change the physical structure of the network.
  * **Freeze/Play**: Pause or resume the automatic rotation and breathing animations.
  * **Reset**: Returns the camera to its original starting position.

---

## 🧠 Under the Hood (Architecture)

### 1. The Math of the Network
The network is not a random scatter of points. The `generateNeuralNetwork` function uses algorithms to place nodes:
* The **Crystalline Sphere** uses spherical coordinates (`phi`, `theta`) and the **Golden Ratio** (`(1 + Math.sqrt(5)) / 2`) to ensure nodes are evenly distributed without overlapping.
* The **Fractal Web** uses recursive branching, calculating perpendicular vectors via cross products to ensure organic 3D growth.

### 2. Custom Shader Magic
Instead of standard Three.js materials, the project relies on `ShaderMaterial`. 
* **Vertex Shaders**: Inject *Simplex Noise* to make the nodes subtly vibrate and breathe over time. It calculates the exact distance of each node/line from a "Pulse Point" to scale them up during a wave.
* **Fragment Shaders**: Handle the alpha fading, dynamic colors, and smoothstep functions to create a glowing core that fades gracefully at the edges.

### 3. Connection Optimization
Instead of creating thousands of individual line objects, the project groups all connections into a single `THREE.LineSegments` mesh using a `BufferGeometry`. This drastically reduces draw calls and keeps the visualization running smoothly at 60 FPS even on mobile devices.

---

## 👨‍💻 About the Author

**Pankaj Tiwari** A developer, creator, and first-year electronics student with a deep passion for coding and exploring the fascinating worlds of quantum physics and higher mathematics. Beyond building numerous websites and game projects, I am the author of two books, including *Control Psychology: The Illusionary Game*, and I run the *Myth Over Mind* blog where I explore philosophy and human behavior.

* Let's connect, collaborate, and build the future!
