---
layout: page
title: AI Head Breaker
permalink: /head-breaker/
---

# 🎮 AI Head Breaker
> **"Play with your head, not your hands."**
> A hands-free arcade game designed for accessibility and digital healthcare.

<br>

## 📺 Demo & Play
> **[👉 Play Game Now (Click Here)](https://YOUR_ID.github.io/GAME_URL)**
> *(Replace this link with your actual game URL)*

![Game Play Screenshot](/assets/images/head-breaker-play.jpg)
*(Please upload a screenshot of your game to the assets/images folder)*

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
