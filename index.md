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

## 🌟 Featured Projects

### AI Head Breaker (Hands-Free Game)
👉 **[Go To AI Head Breaker (Hands-Free Game)](/head-breaker/)**
<br>
**"Gamified Rehabilitation & Barrier-Free Leisure"**
A hands-free arcade game controlled entirely by head movements. Designed for users with upper limb disabilities and for preventing "Tech Neck" syndrome.

* **Core Tech:** p5.js, Google MediaPipe (Face Mesh), HTML5/CSS3
* **How it works:**
    * **Head Tracking:** Moving the head left/right controls the paddle.
    * **Mouth Trigger:** Opening the mouth starts/resumes the game.
* **Key Value:** Contactless interface, web accessibility, and neck exercise.

<br>
---

## 🛠️ Technical Skills
* **AI/ML:** TensorFlow Lite, Google MediaPipe
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
