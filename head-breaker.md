---
layout: page
title: AI Neon Breaker
permalink: /head-breaker/
---

# 🎮 AI Neon Breaker
> **"Play with your head, not your hands."**
> A hands-free arcade game designed for <span style="color: #ff00de;">accessibility</span> and <span style="color: #00ffcc;">digital healthcare</span>.

<br>

## 📺 Demo & Play
> **[👉 Play Game Now (Click Here)](https://mellow-dragon-f0d9e2.netlify.app/)**
> 
<img src="/assets/images/Neon Breaker_Loading.png" width="100%">
*This is the Ready Window*
<br>
<img src="/assets/images/Neon Breaker_Playing.png" width="100%">
*This is the Playing Window*
<br>
<img src="/assets/images/Neon Breaker_Game Over.png" width="100%">
*This is the Game Over Window*

<br>

## 💡 Project Overview
**AI Head Breaker** is a <span style="color: #00ffcc; font-weight: bold;">web-based "brick breaker" game</span> that eliminates the need for a mouse or keyboard. By utilizing a standard webcam and AI vision technology, users can control the game entirely through facial movements.

This project was developed with two main goals:
1.  **<span style="color: #ff00de; font-weight: bold;">Inclusive Leisure (Barrier-Free):</span>** To provide a gaming experience for individuals with upper limb disabilities who cannot use standard controllers.
2.  **<span style="color: #39ff14; font-weight: bold;">Gamified Rehabilitation:</span>** To help prevent **"Tech Neck"** syndrome by encouraging <span style="color: #ffcc00; font-weight: bold;">neck stretching exercises</span> through gameplay.

<br>

## 🕹️ How to Play (Hands-Free Interface)
The game operates <span style="color: #ffcc00; font-weight: bold;">100% contactless</span> using **Face Landmark Detection**.

* **Move Paddle:** Tilt or turn your head **<span style="color: #00ffcc;">Left / Right</span>**.
    * *Logic:* The system tracks the x-coordinate of your <span style="color: #ff00de;">nose tip (Landmark #1)</span>.
* **Start / Resume:** **<span style="color: #00ffcc;">Open your mouth</span>**.
    * *Logic:* The system calculates the vertical distance between your upper and lower lips. If it exceeds a specific threshold (0.05), it triggers a "Click" event.
 
<br>

## 🧠 Technical Deep Dive: Horizontal Rotation (Neon Breaker)
While "Face Pong" uses vertical nodding, **"Neon Breaker"** utilizes <span style="color: #ff00de;">horizontal head rotation (yaw)</span> to control a brick-breaking game.

### 1. Game Mechanics
* **Concept:** A classic brick-breaking arcade game. The goal is to destroy all procedural bricks generated at the top.
* **Controls:**
    * **Paddle:** Turning the head **<span style="color: #00ffcc;">Left / Right</span>** moves the paddle in that direction.
    * **Items:** Catching falling items triggers effects like 'Multi-ball' or 'Fireball' (penetration).
* **Progression:** Levels are generated infinitely using procedural algorithms.

### 2. Core Algorithms
We implemented distinct logic to handle lateral movement and ball physics.

#### A. Threshold-based State Machine
Unlike the analog control of Face Pong, this mode requires clear **directional states**.

> **Logic:** <span style="color: #ff00de; font-weight: bold;">If |Nose.x - 0.5| > Threshold (0.03) → Move State (LEFT or RIGHT)</span>

* **Constant Speed:** The paddle moves at a fixed speed when the head is turned beyond the threshold.
* **Fatigue Reduction:** Users only need to maintain a <span style="color: #ffcc00;">slight turn</span> to move the paddle to the edge, minimizing neck strain compared to continuous turning.

#### B. Vector-Based Reflection Calculation
To add depth to the gameplay, we calculated the reflection angle based on the impact point.

> **Formula:** <span style="color: #ff00de; font-weight: bold;">ReflectionAngle = HitPoint * MaxBounceAngle (75°)</span>

* **Tactile Control:** The ball curves significantly when it hits the edges of the paddle, allowing users to <span style="color: #39ff14;">"spin" or aim the ball precisely</span> using only head movements.

#### C. Procedural Level Generation
New map patterns are created every round by iterating through a 2D array with random probability logic, ensuring <span style="color: #00ffcc;">infinite replay value</span> without manual level design.

<br>

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
