---
layout: page
title: AI Neon Breaker
permalink: /head-breaker/
---

# 🎮 AI Neon Breaker
> **"Play with your head, not your hands."**
> A hands-free arcade game designed for accessibility and digital healthcare.

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
**AI Head Breaker** is a web-based "brick breaker" game that eliminates the need for a mouse or keyboard. By utilizing a standard webcam and AI vision technology, users can control the game entirely through facial movements.

This project was developed with two main goals:
1.  **Inclusive Leisure (Barrier-Free):** To provide a gaming experience for individuals with upper limb disabilities who cannot use standard controllers.
2.  **Gamified Rehabilitation:** To help prevent **"Tech Neck"** syndrome by encouraging neck stretching exercises through gameplay.

<br>

## 🕹️ How to Play (Hands-Free Interface)
The game operates 100% contactless using **Face Landmark Detection**.

* **Move Paddle:** Tilt or turn your head **Left/Right**.
    * *Logic:* The system tracks the x-coordinate of your nose tip (Landmark #1).
* **Start / Resume:** **Open your mouth**.
    * *Logic:* The system calculates the vertical distance between your upper and lower lips. If it exceeds a specific threshold (0.05), it triggers a "Click" event.
 
<br>

## 🧠 Technical Deep Dive: Horizontal Rotation (Neon Breaker)
While "Face Pong" uses vertical nodding, **"Neon Breaker"** utilizes horizontal head rotation (yaw) to control a brick-breaking game.

### 1. Game Mechanics
* **Concept:** A classic brick-breaking arcade game. The goal is to destroy all procedural bricks generated at the top.
* **Controls:**
    * **Paddle:** Turning the head **Left/Right** moves the paddle in that direction.
    * **Items:** Catching falling items triggers effects like 'Multi-ball' or 'Fireball' (penetration).
* **Progression:** Levels are generated infinitely using procedural algorithms.

### 2. Core Algorithms
We implemented distinct logic to handle lateral movement and ball physics.

#### A. Threshold-based State Machine
Unlike the analog control of Face Pong, this mode requires clear directional states.

> **Logic:** `If |Nose.x - 0.5| > Threshold (0.03) → Move State (LEFT or RIGHT)`

* **Constant Speed:** The paddle moves at a fixed speed when the head is turned beyond the threshold.
* **Fatigue Reduction:** Users only need to maintain a slight turn to move the paddle to the edge, minimizing neck strain compared to continuous turning.



#### B. Vector-Based Reflection Calculation
To add depth to the gameplay, we calculated the reflection angle based on the impact point.

> **Formula:** `ReflectionAngle = HitPoint * MaxBounceAngle (75°)`

* **Tactile Control:** The ball curves significantly when it hits the edges of the paddle, allowing users to "spin" or aim the ball precisely using only head movements.



#### C. Procedural Level Generation
New map patterns are created every round by iterating through a 2D array with random probability logic, ensuring infinite replay value without manual level design.

<br>

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
