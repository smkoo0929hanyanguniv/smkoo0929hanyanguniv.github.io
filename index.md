---
layout: home
permalink: /
permalink_name: /home
title: AI-BASED-SERVICE

---
<div style="background-color: #050505; padding: 30px; border-radius: 15px; text-align: center; margin-bottom: 30px; border: 1px solid #333;">
  <img src="/assets/images/ascii-art-group29.png" alt="Group 29 AI-BASED-SERVICE" style="width: 100%; max-width: 600px; filter: invert(1) drop-shadow(0 0 5px #00ffcc);">
</div>


# ai-based-service
<img src="/assets/images/Main Page of Game Website.png" width="100%">

**[🎮 Start the game 🎮](https://mellow-dragon-f0d9e2.netlify.app/)**

## 🌟 Featured Projects

**"Gamified Rehabilitation & Barrier-Free Leisure"**
A hands-free arcade game controlled entirely by <span style="color: #00ffcc; font-weight: bold;">head movements</span>. 
Designed for users with <span style="color: #ff9900;">upper limb disabilities</span> and for preventing <span style="color: #ff00de; font-weight: bold;">"Tech Neck" syndrome</span>.
This platform consists of two independent game modes designed to <span style="color: #ffcc00; font-weight: bold;">maximize neck exercise effects</span> by inducing <span style="color: #00ffcc; font-weight: bold;">vertical movement (Extension/Flexion)</span> and <span style="color: #00ffcc; font-weight: bold;">horizontal rotational movement (Rotation)</span> of the cervical spine, respectively.

* **Core Tech:**
    * **AI Vision:** Google MediaPipe Face Mesh (High-precision landmark detection)
    * **Game Engine:** p5.js (Physics & Rendering)
    * **Web:** HTML5/CSS3 (Neon UI, SPA structure)
* **How it works:** 
    * **Head Tracking:** Extracts Landmark #1 (Nose Tip) coordiantes to map user's head rotation to the paddle's X-position.
    * **Gesture Trigger:** Calculates the Euclidean distance between Landmark #13 (Upper Lip) and #14 (Lower Lip). If distance > threshold (0.03), game starts.
    * **Logic:** Self-written algorithm ensures robust real-time tracking.
* **Key Value:** Contactless interface, web accessibility, and neck exercise.

### Neon Breaker (Hands-Free Game)
👉 **[Get To Know About Neon Breaker (Hands-Free Game)](/head-breaker/)**

### Face Pong (Hands-Free Game)
👉 **[Get To Know About Face Pong (Hands-Free Game)](/face-pong/)**

---

## 🛠️ Technical Skills
* **AI/ML:** TensorFlow Lite, Google MediaPipe
* **Web/SW:** p5.js, Python, C++, HTML/CSS

<br>

## 📂 Weekly Activity Logs
Here are the latest updates on our development process.

<ul>
  {% for post in site.posts reversed %}
    <li>
      <a href="{{ post.url }}"><b>{{ post.title }}</b></a>
      <span style="font-size: 0.8em; color: #666;"> — {{ post.date | date: "%Y.%m.%d" }}</span>
    </li>
  {% endfor %}
</ul>

<br>
