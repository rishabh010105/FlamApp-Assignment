# Interactive Bézier Rope Simulation (Physics + Real-Time Input)

## 📌 Overview

This project implements an **interactive cubic Bézier curve** that behaves like a **springy rope** reacting to real-time user input.  
The entire system is built **from scratch**, without using any Bézier, animation, or physics libraries.

The curve dynamically responds to **mouse movement (Web)** and visualizes both:
- The **Bézier curve path**
- The **tangent vectors** along the curve

This project demonstrates applied knowledge of **mathematics, physics simulation, and real-time rendering**.

---

## 🎯 Features

- Manual implementation of **cubic Bézier curve math**
- Real-time **spring–damping physics** for smooth rope-like motion
- **Derivative-based tangent visualization**
- Interactive control via **mouse movement**
- Runs at **60 FPS** using `requestAnimationFrame`
- Clean separation of **Math, Physics, Input, and Rendering**

---

## 🧮 Bézier Curve Mathematics

A **cubic Bézier curve** is defined using four control points:

- `P0` – Fixed start point  
- `P1` – Dynamic control point  
- `P2` – Dynamic control point  
- `P3` – Fixed end point  

The curve equation is:


Each tangent vector is:
1. Computed at selected `t` values
2. Normalized
3. Drawn as a short line segment along the curve

This provides a clear visual representation of curve flow and direction.

---

## ⚙️ Spring–Damping Physics Model

To achieve smooth, natural motion, the dynamic control points (`P1` and `P2`) are driven by a **spring physics model**:

acceleration = -k * (position - target) - damping * velocity


Where:
- `k` is the spring stiffness
- `damping` reduces oscillations
- `target` is the mouse position

Each animation frame updates:
- Velocity
- Position

This creates realistic **elastic rope-like behavior** rather than abrupt movement.

---

## 🖱️ Interaction

- Mouse movement controls the target position
- Control points smoothly follow the target with physical lag
- Endpoints remain fixed, simulating an anchored rope

---

## 🎨 Rendering Details

The visualization includes:
- Bézier curve path (cyan)
- Control points (red for dynamic, white for fixed)
- Tangent vectors (yellow)
- Smooth animation at ~60 FPS

Rendering is performed using **HTML Canvas** and manual draw calls.

---

## 🧱 Code Architecture

The code is organized into clear logical sections:

- **Vector Math** – 2D vector operations
- **Bézier Math** – Curve and derivative calculations
- **Physics Engine** – Spring and damping simulation
- **Input Handling** – Mouse interaction
- **Rendering Loop** – Real-time drawing

No external libraries or helper APIs are used.

---

## 🚫 Constraints Followed

- ❌ No `bezierCurveTo`, `UIBezierPath`, or graphics helpers
- ❌ No physics or animation libraries
- ❌ No third-party math utilities

All logic is manually implemented.

---

## ▶️ How to Run

1. Clone or download the repository
2. Open the `.html` file in any modern browser
3. Move the mouse to interact with the rope

No build steps or dependencies required.

---

## 📈 Possible Improvements

Future enhancements could include:
- Rope tension constraints
- Gravity effects
- Multiple connected Bézier segments
- iOS gyroscope input using CoreMotion
- Touch-based interaction for mobile devices

---

## 🧠 What This Project Demonstrates

- Strong understanding of **mathematical modeling**
- Practical use of **physics simulation**
- Real-time **graphics programming**
- Clean, readable, and maintainable code design

---

## 🎥 Demo

A short screen recording (≤30s) is included in the submission to demonstrate real-time interaction and smooth motion.

---

