---
layout: page
title: AI Face Pong
permalink: /face-pong/
---

# 🎮 AI Face Pong
> **"Play with your head, not your hands."**
> A hands-free arcade game designed for accessibility and digital healthcare.

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
*This is the Playing Window*

<br>

## 💡 Project Overview
**AI Face Pong** is a web-based "ping pong" game that eliminates the need for a mouse or keyboard. By utilizing a standard webcam and AI vision technology, users can control the game entirely through facial movements.

This project was developed with two main goals:
1.  **Inclusive Leisure (Barrier-Free):** To provide a gaming experience for individuals with upper limb disabilities who cannot use standard controllers.
2.  **Gamified Rehabilitation:** To help prevent **"Tech Neck"** syndrome by encouraging neck stretching exercises through gameplay.

<br>

## 🕹️ How to Play (Hands-Free Interface)
The game operates 100% contactless using **Face Landmark Detection**.

* **Move Paddle:** Tilt or turn your head **Up/Down**.
    * *Logic:* The system tracks the y-coordinate of your nose tip (Landmark #1).
* **Start / Resume:** **Open your mouth**.
    * *Logic:* The system calculates the vertical distance between your upper and lower lips. If it exceeds a specific threshold (0.05), it triggers a "Click" event.

<br>

<br>

## 🧠 Technical Deep Dive: Vertical Nodding Interface
We developed a specialized algorithm for **"Face Pong: Survival Mode"**, where the player controls the paddle by nodding up and down.

### 1. Game Mechanics
* **Concept:** A survival reinterpretation of Pong. The user must block a ball falling from top to bottom.
* **Controls (Hands-Free):**
    * **Movement:** **Lifting head (Up)** moves the paddle up; **Bowing (Down)** moves it down.
    * **Locking:** **Opening the mouth** locks the paddle in place. This allows users to rest in a comfortable posture while waiting for the ball.
    * **Calibration:** Pressing `[Space]` sets the current head angle as 'Neutral', compensating for individual physical differences.

### 2. Core Algorithms
To ensure stability and smooth control, we applied two key mathematical logic:

#### A. Ratio-Based Pitch Calculation (Depth Robustness)
Using raw Y-coordinates causes errors when the user leans closer/further from the camera. We solved this using **facial structural proportions**.

> **Formula:** `Pitch Ratio = (Nose.y - MidEye.y) / FaceHeight`

* By dividing the distance between the *eyes and nose* by the *total face height*, we extract a normalized value that remains consistent regardless of the user's distance (Z-axis) from the camera.

#### B. Velocity Control System
Instead of 1:1 position mapping, we used **Velocity Control** for a smoother feel.

> **Logic:** `PaddleSpeed = (CurrentPitch - NeutralPitch) * Sensitivity`

* **Dynamic Speed:** Small head movements move the paddle slowly; large nods move it quickly.
* **Deadzone:** A threshold (0.01) filters out minute tremors to prevent jitter.

### 3. Dynamic Difficulty
The game gets harder geometrically.
* **Acceleration:** Every time the ball is returned, its velocity vector `(dx, dy)` is multiplied by **1.03**, gradually increasing the speed.

<br>

## 🛠️ Tech Stack & Implementation
* **Frontend:** HTML5, CSS3 (Neon Cyberpunk Aesthetic)
* **Game Engine:** **p5.js** (Physics calculation, Rendering, Collision detection)
* **AI / Computer Vision:** **Google MediaPipe Face Mesh**
    * *Why MediaPipe?* We initially tested *Teachable Machine*, but it had significant latency. We switched to MediaPipe to process video frames locally on the device, achieving **real-time performance (<15ms latency)**.

<br>

## 🏥 Social Value & Impact
### 1. Zero-Barrier Accessibility
Unlike traditional games requiring fine motor skills, this service allows anyone to enjoy the thrill of arcade games using only head movements. It requires no expensive hardware (like eye-trackers)—just a laptop webcam.

### 2. Digital Healthcare Solution
Modern people suffer from neck pain due to smartphone use. This game naturally induces **Neck Rotation** (looking left/right) and **Extension**, transforming tedious rehab exercises into an enjoyable activity.

<br>

## 🚀 Future Roadmap
* **Auto-Calibration:** Automatically adjusting sensitivity based on the user's distance from the camera.
* **Full Hands-Free UI:** Navigating menus and "Game Over" screens using only facial gestures.
* **Auditory Feedback:** Adding dynamic sound effects to enhance immersion for visually impaired users.

---
[🏠 Back to Home](/)
