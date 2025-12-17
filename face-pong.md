---
layout: page
title: AI Face Pong
permalink: /face-pong/
---

# 🎮 AI Face Pong
> **"Play with your head, not your hands."**
> A hands-free arcade game designed for <span style="color: #ff00de;">accessibility</span> and <span style="color: #00ffcc;">digital healthcare</span>.

<br>

## 📺 Demo & Play
> **[👉 Play Game Now (Click Here)](https://mellow-dragon-f0d9e2.netlify.app/)**
> 
<img src="/assets/images/Face Pong_Loading.png" width="100%">
*This is the Ready Window*
<br>
<img src="/assets/images/Face Pong_Playing.png" width="100%">
*This is the Playing Window*
<br>
<img src="/assets/images/Neon Breaker_Game Over.png" width="100%">
*This is the Game Over Window*

<br>

## 💡 Project Overview
**AI Face Pong** is a <span style="color: #00ffcc; font-weight: bold;">web-based "ping pong" game</span> that eliminates the need for a mouse or keyboard. By utilizing a standard webcam and AI vision technology, users can control the game entirely through facial movements.

This project was developed with two main goals:
1.  **<span style="color: #ff00de; font-weight: bold;">Inclusive Leisure (Barrier-Free):</span>** To provide a gaming experience for individuals with upper limb disabilities who cannot use standard controllers.
2.  **<span style="color: #39ff14; font-weight: bold;">Gamified Rehabilitation:</span>** To help prevent **"Tech Neck"** syndrome by encouraging <span style="color: #ffcc00; font-weight: bold;">neck stretching exercises</span> through gameplay.

<br>

## 🕹️ How to Play (Hands-Free Interface)
The game operates <span style="color: #ffcc00; font-weight: bold;">100% contactless</span> using **Face Landmark Detection**.

* **Move Paddle:** Tilt or turn your head **<span style="color: #00ffcc;">Up / Down</span>**.
    * *Logic:* The system tracks the y-coordinate of your <span style="color: #ff00de;">nose tip (Landmark #1)</span>.
* **Start / Resume:** **<span style="color: #00ffcc;">Open your mouth</span>**.
    * *Logic:* The system calculates the vertical distance between your upper and lower lips. If it exceeds a specific threshold (0.05), it triggers a "Click" event.

<br>

<br>

## 🧠 Technical Deep Dive: Vertical Nodding Interface
We developed a specialized algorithm for **"Face Pong: Survival Mode"**, where the player controls the paddle by nodding up and down.

### 1. Game Mechanics
* **Concept:** A survival reinterpretation of Pong. The user must block a ball falling from top to bottom.
* **Controls (Hands-Free):**
    * **Movement:** **<span style="color: #00ffcc;">Lifting head (Up)</span>** moves the paddle up; **<span style="color: #00ffcc;">Bowing (Down)</span>** moves it down.
    * **Locking:** **Opening the mouth** locks the paddle in place. This allows users to rest in a comfortable posture while waiting for the ball.
    * **Calibration:** Pressing `[Space]` sets the current head angle as <span style="color: #ffcc00;">'Neutral'</span>, compensating for individual physical differences.

### 2. Core Algorithms
To ensure stability and smooth control, we applied two key mathematical logic:

#### A. Ratio-Based Pitch Calculation (Depth Robustness)
Using raw Y-coordinates causes errors when the user leans closer/further from the camera. We solved this using **facial structural proportions**.

> **Formula:** <span style="color: #ff00de; font-weight: bold;">Pitch Ratio = (Nose.y - MidEye.y) / FaceHeight</span>

* By dividing the distance between the *eyes and nose* by the *total face height*, we extract a <span style="color: #39ff14;">normalized value</span> that remains consistent regardless of the user's distance (Z-axis) from the camera.

#### B. Velocity Control System
Instead of 1:1 position mapping, we used **Velocity Control** for a smoother feel.

> **Logic:** <span style="color: #ff00de; font-weight: bold;">PaddleSpeed = (CurrentPitch - NeutralPitch) * Sensitivity</span>

* **Dynamic Speed:** Small head movements move the paddle slowly; large nods move it quickly.
* **Deadzone:** A threshold (0.01) filters out minute tremors to <span style="color: #ffcc00;">prevent jitter</span>.

### 3. Dynamic Difficulty
The game gets harder geometrically.
* **Acceleration:** Every time the ball is returned, its velocity vector `(dx, dy)` is multiplied by **<span style="color: #ff00de;">1.03</span>**, gradually increasing the speed.

<br>

## 🛠️ Tech Stack & Implementation
* **Frontend:** HTML5, CSS3 (Neon Cyberpunk Aesthetic)
* **Game Engine:** **p5.js** (Physics calculation, Rendering, Collision detection)
* **AI / Computer Vision:** **<span style="color: #00ffcc; font-weight: bold;">Google MediaPipe Face Mesh</span>**
    * *Why MediaPipe?* We initially tested *Teachable Machine*, but it had significant latency. We switched to MediaPipe to process video frames locally on the device, achieving **<span style="color: #39ff14; font-weight: bold;">real-time performance (<15ms latency)</span>**.

<br>

## 🏥 Social Value & Impact
### 1. Zero-Barrier Accessibility
Unlike traditional games requiring fine motor skills, this service allows anyone to enjoy the thrill of arcade games using **only head movements**. It requires no expensive hardware (like eye-trackers)—just a laptop webcam.

### 2. Digital Healthcare Solution
Modern people suffer from neck pain due to smartphone use. This game naturally induces **<span style="color: #ff00de;">Neck Rotation</span>** (looking left/right) and **<span style="color: #ff00de;">Extension</span>**, transforming tedious rehab exercises into an enjoyable activity.

<br>

## 🚀 Future Roadmap
* **Auto-Calibration:** Automatically adjusting sensitivity based on the user's distance from the camera.
* **Full Hands-Free UI:** Navigating menus and "Game Over" screens using only facial gestures.
* **Auditory Feedback:** Adding dynamic sound effects to enhance immersion for visually impaired users.

---
[🏠 Back to Home](/)
