---
layout: home
permalink: /
permalink_name: /home
title: AI-BASED-SERVICE

<div style="background-color: #050505; padding: 30px; border-radius: 15px; text-align: center; margin-bottom: 30px; border: 1px solid #333;">
  <img src="/assets/images/group29_ascii.png" alt="Group 29" style="width: 100%; max-width: 600px; filter: invert(1) drop-shadow(0 0 5px #00ffcc);">
</div>

---



# ai-based-service

## 🌟 Featured Projects

### 1. AI Head Breaker (Hands-Free Game)
**"Gamified Rehabilitation & Barrier-Free Leisure"**
A hands-free arcade game controlled entirely by head movements. Designed for users with upper limb disabilities and for preventing "Tech Neck" syndrome.

* **Core Tech:** p5.js, Google MediaPipe (Face Mesh), HTML5/CSS3
* **How it works:**
    * **Head Tracking:** Moving the head left/right controls the paddle.
    * **Mouth Trigger:** Opening the mouth starts/resumes the game.
* **Key Value:** Contactless interface, web accessibility, and neck exercise.

<br>

### 2. AI Smart Trash Can
**"Solving Recycling Confusion with Computer Vision"**
An automated waste sorting bin that uses AI to recognize recyclables and physically sorts them into the correct compartments.

* **Core Tech:** Raspberry Pi 4, Arduino Uno, TensorFlow Lite
* **How it works:**
    * **Recognition:** AI camera identifies the type of waste (plastic, can, etc.).
    * **Sorting:** Servo motors automatically open the correct lid.
* **Key Value:** Improving recycling accuracy and user convenience.

<br>

---

## 🛠️ Technical Skills
* **AI/ML:** TensorFlow Lite, Google MediaPipe
* **Hardware:** Raspberry Pi, Arduino, Sensors & Actuators
* **Web/SW:** p5.js, Python, C++, HTML/CSS

<br>

## 📂 Weekly Activity Logs
Here are the latest updates on our development process.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}"><b>{{ post.title }}</b></a>
      <span style="font-size: 0.8em; color: #666;"> — {{ post.date | date: "%Y.%m.%d" }}</span>
    </li>
  {% endfor %}
</ul>

<br>
