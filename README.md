SpiroPlotter Studio

SpiroPlotter Studio is a high-performance, browser-based generative art tool designed to simulate multi-arm kinematic drawing machines. Inspired by classic spirographs and complex harmonographs, this studio allows users to create intricate geometric patterns through a sophisticated simulation of mechanical joints, motors, and rotating canvases.

🚀 Overview

Unlike traditional spirograph toys limited to two gears, SpiroPlotter Studio utilizes a modular kinematic engine. It simulates a series of connected "arms" (linkages), each governed by its own orbital parameters, culminating in a drawing point that traces unique mathematical curves onto a dynamic, rotating surface.

✨ Key Technical Features

1. Multi-Arm Kinematic Engine

Variable Linkages: Support for multiple interconnected arms where each joint serves as the anchor for the next.

Independent Motor Control: Each arm features adjustable parameters for:

Length: The radius of the orbital path.

Speed: Precise angular velocity (RPM-style control).

Phase: Initial starting angle for complex synchronization.

Real-time Computation: High-frequency coordinate calculation using trigonometric summation.

2. Dynamic Canvas Simulation

Rotating Paper: Beyond arm movement, the drawing surface itself can rotate at an independent speed, enabling "cycloid" and "epicycloid" patterns that evolve over time.

High-DPI Rendering: Optimized HTML5 Canvas implementation for crisp lines on Retina and 4K displays.

Interactive Viewport: Zoom and pan capabilities to inspect fine details of high-density paths.

3. Advanced Visualization & Stylization

Dynamic Coloring: Support for gradient paths, time-based color shifting, and opacity controls.

Path Persistence: Toggle between "Live Trail" (showing the current movement) and "Long Exposure" (rendering the full geometric history).

Variable Resolution: Adjust the sampling rate (step size) to balance between simulation speed and line smoothness.

4. Export & Compatibility

Multi-Color SVG Export: If a drawing contains multiple colors, the system automatically generates a separate SVG file for each color.

Pen Plotter Optimization: * Each exported SVG maintains the exact same canvas dimensions.

This facilitates precise alignment and registration during multi-pass plotting on machines like the AxiDraw or PolarDraw.

Paths are exported as continuous polylines for optimal machine efficiency.

🛠️ Tech Stack

Framework: React 18+ (Functional Components & Hooks)

Rendering: HTML5 Canvas API / SVG DOM

Styling: Tailwind CSS (for a sleek, responsive dark-mode interface)

State Management: Optimized local state for real-time parameter scrubbing without lag.

📥 Getting Started

Clone the repository

git clone [https://github.com/salvmecai-cpu/SpiralPlotterStudio.git](https://github.com/salvmecai-cpu/SpiralPlotterStudio.git)


Install dependencies

npm install


Run the development server

npm run dev


📐 Mathematical Foundation

The position of the drawing tip is calculated as the vector sum of all arm segments and the counter-rotation of the canvas:

$$X(t) = \sum_{i=1}^{n} L_i \cos(\omega_i t + \phi_i)$$

$$Y(t) = \sum_{i=1}^{n} L_i \sin(\omega_i t + \phi_i)$$

Where $L$ is length, $\omega$ is angular velocity, and $\phi$ is the phase shift.

📄 License

This project is licensed under GNU General Public License v3.0
