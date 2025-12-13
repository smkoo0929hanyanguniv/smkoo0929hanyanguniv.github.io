---
layout: home
permalink: /
permalink_name: /home
title: AI-BASED-SERVICE

detail_image: assets/theme_logo.svg

---
   _____                         ___   ___             _____      ____           _____ ______ _____         _____ ______ _______      _______ _____ ______ 
  / ____|                       |__ \ / _ \      /\   |_   _|    |  _ \   /\    / ____|  ____|  __ \       / ____|  ____|  __ \ \    / /_   _/ ____|  ____|
 | |  __ _ __ ___  _   _ _ __      ) | (_) |    /  \    | |______| |_) | /  \  | (___ | |__  | |  | |_____| (___ | |__  | |__) \ \  / /  | || |    | |__   
 | | |_ | '__/ _ \| | | | '_ \    / / \__, |   / /\ \   | |______|  _ < / /\ \  \___ \|  __| | |  | |______\___ \|  __| |  _  / \ \/ /   | || |    |  __|  
 | |__| | | | (_) | |_| | |_) |  / /_   / /   / ____ \ _| |_     | |_) / ____ \ ____) | |____| |__| |      ____) | |____| | \ \  \  /   _| || |____| |____ 
  \_____|_|  \___/ \__,_| .__/  |____| /_/   /_/    \_\_____|    |____/_/    \_\_____/|______|_____/      |_____/|______|_|  \_\  \/   |_____\_____|______|
                        | |                                                                                                                                
                        |_|                                                                                                                                


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
