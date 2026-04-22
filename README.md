<div align="center">

<!-- ╔══════════════════════════════════════════════════════╗ -->
<!--            ANIMATED HERO — pure SVG, no JS             -->
<!-- ╚══════════════════════════════════════════════════════╝ -->

<svg width="900" height="400" viewBox="0 0 900 400" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#040408"/>
      <stop offset="50%" style="stop-color:#080810"/>
      <stop offset="100%" style="stop-color:#040408"/>
    </linearGradient>
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="softglow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="22" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="lineglow" x="-5%" y="-100%" width="110%" height="300%">
      <feGaussianBlur stdDeviation="2" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <radialGradient id="gm" cx="50%" cy="50%" r="55%">
      <stop offset="0%" style="stop-color:white;stop-opacity:0.18"/>
      <stop offset="100%" style="stop-color:white;stop-opacity:0"/>
    </radialGradient>
    <mask id="gfade"><rect width="900" height="400" fill="url(#gm)"/></mask>
    <linearGradient id="scan" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:rgba(255,255,255,0)"/>
      <stop offset="50%" style="stop-color:rgba(255,255,255,0.05)"/>
      <stop offset="100%" style="stop-color:rgba(255,255,255,0)"/>
    </linearGradient>
    <linearGradient id="shimmer" x1="0%" y1="0%" x2="100%" y2="0%" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#cccccc">
        <animate attributeName="offset" values="-0.6;1.4" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="15%" stop-color="#ffffff">
        <animate attributeName="offset" values="-0.4;1.6" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="35%" stop-color="#9999cc">
        <animate attributeName="offset" values="-0.1;1.9" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="55%" stop-color="#ffffff">
        <animate attributeName="offset" values="0.2;2.2" dur="4s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#bbbbbb">
        <animate attributeName="offset" values="0.5;2.5" dur="4s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
  </defs>

  <!-- BACKGROUND -->
  <rect width="900" height="400" fill="url(#bg)" rx="14"/>

  <!-- GRID -->
  <g mask="url(#gfade)">
    <g stroke="#ffffff" stroke-width="0.3" opacity="0.08">
      <line x1="0" y1="40" x2="900" y2="40"/><line x1="0" y1="80" x2="900" y2="80"/>
      <line x1="0" y1="120" x2="900" y2="120"/><line x1="0" y1="160" x2="900" y2="160"/>
      <line x1="0" y1="200" x2="900" y2="200"/><line x1="0" y1="240" x2="900" y2="240"/>
      <line x1="0" y1="280" x2="900" y2="280"/><line x1="0" y1="320" x2="900" y2="320"/>
      <line x1="0" y1="360" x2="900" y2="360"/>
      <line x1="75" y1="0" x2="75" y2="400"/><line x1="150" y1="0" x2="150" y2="400"/>
      <line x1="225" y1="0" x2="225" y2="400"/><line x1="300" y1="0" x2="300" y2="400"/>
      <line x1="375" y1="0" x2="375" y2="400"/><line x1="450" y1="0" x2="450" y2="400"/>
      <line x1="525" y1="0" x2="525" y2="400"/><line x1="600" y1="0" x2="600" y2="400"/>
      <line x1="675" y1="0" x2="675" y2="400"/><line x1="750" y1="0" x2="750" y2="400"/>
      <line x1="825" y1="0" x2="825" y2="400"/>
    </g>
  </g>

  <!-- DEEP GLOW CENTER -->
  <ellipse cx="450" cy="210" rx="320" ry="160" fill="none">
    <animate attributeName="rx" values="280;340;280" dur="6s" repeatCount="indefinite"/>
    <animate attributeName="ry" values="140;170;140" dur="6s" repeatCount="indefinite"/>
  </ellipse>
  <ellipse cx="450" cy="210" rx="200" ry="100" fill="#111122" opacity="0.4" filter="url(#softglow)">
    <animate attributeName="opacity" values="0.3;0.5;0.3" dur="5s" repeatCount="indefinite"/>
  </ellipse>

  <!-- ORBITING ORBS -->
  <g>
    <!-- Orb A: large slow clockwise -->
    <circle r="7" fill="#ffffff" opacity="0.14" filter="url(#softglow)">
      <animateMotion dur="16s" repeatCount="indefinite" calcMode="linear"
        path="M 650 200 A 200 80 0 1 1 649.99 200"/>
    </circle>
    <!-- Orb B: medium CCW -->
    <circle r="4.5" fill="#aaaadd" opacity="0.22" filter="url(#softglow)">
      <animateMotion dur="10s" repeatCount="indefinite" calcMode="linear"
        path="M 310 200 A 140 55 0 1 0 309.99 200"/>
    </circle>
    <!-- Orb C: small fast CW tilted -->
    <circle r="3" fill="#ffffff" opacity="0.35" filter="url(#softglow)">
      <animateMotion dur="6s" repeatCount="indefinite" calcMode="linear"
        path="M 550 200 A 100 38 20 1 1 549.99 200"/>
    </circle>
    <!-- Orb D: wide wandering ellipse -->
    <circle r="5" fill="#888899" opacity="0.16" filter="url(#softglow)">
      <animateMotion dur="22s" repeatCount="indefinite" calcMode="linear"
        path="M 800 100 Q 850 280 700 360 Q 500 400 200 340 Q 60 280 80 140 Q 120 50 400 60 Q 650 70 800 100"/>
    </circle>
    <!-- Orb E: tiny rapid -->
    <circle r="2" fill="#ffffff" opacity="0.45">
      <animateMotion dur="4s" repeatCount="indefinite" calcMode="linear"
        path="M 510 200 A 60 25 0 1 1 509.99 200"/>
    </circle>
  </g>

  <!-- SCAN LINE -->
  <rect x="0" y="-60" width="900" height="60" fill="url(#scan)">
    <animate attributeName="y" values="-60;440" dur="4.5s" repeatCount="indefinite" calcMode="linear"/>
  </rect>

  <!-- STATIC PARTICLES -->
  <g>
    <circle cx="48" cy="72" r="1.3" fill="#fff" opacity="0.35"><animate attributeName="opacity" values="0.35;0.9;0.35" dur="3.1s" repeatCount="indefinite"/></circle>
    <circle cx="831" cy="105" r="1.1" fill="#fff" opacity="0.3"><animate attributeName="opacity" values="0.3;0.8;0.3" dur="2.7s" repeatCount="indefinite"/></circle>
    <circle cx="120" cy="330" r="1.4" fill="#aaaaff" opacity="0.3"><animate attributeName="opacity" values="0.3;0.75;0.3" dur="3.8s" repeatCount="indefinite"/></circle>
    <circle cx="770" cy="290" r="1.2" fill="#fff" opacity="0.35"><animate attributeName="opacity" values="0.35;0.9;0.35" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="440" cy="30" r="1.0" fill="#fff" opacity="0.28"><animate attributeName="opacity" values="0.28;0.7;0.28" dur="4.3s" repeatCount="indefinite"/></circle>
    <circle cx="860" cy="340" r="1.3" fill="#aaaaff" opacity="0.22"><animate attributeName="opacity" values="0.22;0.65;0.22" dur="3.5s" repeatCount="indefinite"/></circle>
    <circle cx="38" cy="265" r="1.0" fill="#fff" opacity="0.28"><animate attributeName="opacity" values="0.28;0.72;0.28" dur="4.7s" repeatCount="indefinite"/></circle>
    <circle cx="710" cy="44" r="1.2" fill="#fff" opacity="0.3"><animate attributeName="opacity" values="0.3;0.82;0.3" dur="2.9s" repeatCount="indefinite"/></circle>
    <circle cx="310" cy="368" r="1.0" fill="#aaaaff" opacity="0.25"><animate attributeName="opacity" values="0.25;0.7;0.25" dur="5s" repeatCount="indefinite"/></circle>
    <circle cx="590" cy="372" r="1.1" fill="#fff" opacity="0.22"><animate attributeName="opacity" values="0.22;0.6;0.22" dur="3.3s" repeatCount="indefinite"/></circle>
    <circle cx="200" cy="55" r="0.9" fill="#fff" opacity="0.2"><animate attributeName="opacity" values="0.2;0.6;0.2" dur="4s" repeatCount="indefinite"/></circle>
    <circle cx="660" cy="360" r="1.0" fill="#aaaaff" opacity="0.25"><animate attributeName="opacity" values="0.25;0.7;0.25" dur="2.6s" repeatCount="indefinite"/></circle>
    <!-- Drifting streakers -->
    <circle r="1.5" fill="#fff" opacity="0">
      <animateMotion dur="18s" repeatCount="indefinite" path="M 50 180 Q 250 140 500 170 Q 700 200 870 160"/>
      <animate attributeName="opacity" values="0;0.4;0.4;0" dur="18s" repeatCount="indefinite"/>
    </circle>
    <circle r="1" fill="#aaaaff" opacity="0">
      <animateMotion dur="23s" repeatCount="indefinite" path="M 880 220 Q 650 300 400 230 Q 200 170 30 240"/>
      <animate attributeName="opacity" values="0;0.3;0.3;0" dur="23s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- CORNER BRACKETS -->
  <g stroke="#ffffff" stroke-width="1.8" fill="none" opacity="0.2">
    <path d="M18 46 L18 18 L52 18"/>
    <path d="M882 46 L882 18 L848 18"/>
    <path d="M18 354 L18 382 L52 382"/>
    <path d="M882 354 L882 382 L848 382"/>
  </g>

  <!-- TOP BORDER LINE animated extend -->
  <line x1="0" y1="1" x2="900" y2="1" stroke="#ffffff" stroke-width="1" opacity="0.12"/>
  <line x1="0" y1="399" x2="900" y2="399" stroke="#ffffff" stroke-width="1" opacity="0.12"/>

  <!-- SIDE ACCENT LINES sweeping in -->
  <line x1="0" y1="200" x2="0" y2="200" stroke="#ffffff" stroke-width="0.8" opacity="0.25" filter="url(#lineglow)">
    <animate attributeName="x2" values="0;300" dur="1.4s" fill="freeze" begin="0.1s" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </line>
  <line x1="900" y1="200" x2="900" y2="200" stroke="#ffffff" stroke-width="0.8" opacity="0.25" filter="url(#lineglow)">
    <animate attributeName="x2" values="900;600" dur="1.4s" fill="freeze" begin="0.1s" calcMode="spline" keySplines="0.4 0 0.2 1"/>
  </line>

  <!-- EYEBROW text fade+rise -->
  <text x="450" y="118" text-anchor="middle"
    font-family="'Courier New',monospace" font-size="11"
    fill="#666677" letter-spacing="5" opacity="0">
    FULL-STACK DEVELOPER  ·  AI/ML ENGINEER  ·  KIIT UNIVERSITY
    <animate attributeName="opacity" values="0;0;0.75" dur="1s" fill="freeze" begin="0.5s"/>
    <animateTransform attributeName="transform" type="translate" values="0 14;0 0" dur="0.85s" fill="freeze" begin="0.5s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </text>

  <!-- MAIN NAME — "SHIVAM" shimmer outline -->
  <text x="450" y="210" text-anchor="middle"
    font-family="Arial Black, Impact, sans-serif"
    font-size="96" font-weight="900" letter-spacing="-2"
    fill="none" stroke="url(#shimmer)" stroke-width="1.5"
    filter="url(#glow)" opacity="0">
    SHIVAM
    <animate attributeName="opacity" values="0;0;1" dur="1s" fill="freeze" begin="0.6s"/>
    <animateTransform attributeName="transform" type="translate" values="0 24;0 0" dur="1s" fill="freeze" begin="0.6s" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </text>

  <!-- "SHRIVASTAVA" solid delayed -->
  <text x="450" y="268" text-anchor="middle"
    font-family="Arial Black, Impact, sans-serif"
    font-size="54" font-weight="900" letter-spacing="10"
    fill="#e0e0e8" opacity="0">
    SHRIVASTAVA
    <animate attributeName="opacity" values="0;0;0;0.82" dur="1.4s" fill="freeze" begin="0.7s"/>
    <animateTransform attributeName="transform" type="translate" values="0 20;0 0" dur="0.95s" fill="freeze" begin="0.8s" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </text>

  <!-- ROLE PILLS — staggered appear -->
  <!-- Pill 1 -->
  <rect x="196" y="294" width="136" height="26" rx="4" fill="#141418" stroke="#2a2a2a" stroke-width="1" opacity="0">
    <animate attributeName="opacity" values="0;0;0;0;1" dur="1.9s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.5s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </rect>
  <text x="264" y="311" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#9999aa" letter-spacing="1" opacity="0">
    ⚡ MERN Stack
    <animate attributeName="opacity" values="0;0;0;0;1" dur="1.9s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.5s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </text>
  <!-- Pill 2 -->
  <rect x="344" y="294" width="162" height="26" rx="4" fill="#141418" stroke="#2a2a2a" stroke-width="1" opacity="0">
    <animate attributeName="opacity" values="0;0;0;0;0;1" dur="2.1s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.7s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </rect>
  <text x="425" y="311" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#9999aa" letter-spacing="1" opacity="0">
    👁 Computer Vision
    <animate attributeName="opacity" values="0;0;0;0;0;1" dur="2.1s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.7s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </text>
  <!-- Pill 3 -->
  <rect x="518" y="294" width="136" height="26" rx="4" fill="#141418" stroke="#2a2a2a" stroke-width="1" opacity="0">
    <animate attributeName="opacity" values="0;0;0;0;0;0;1" dur="2.3s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.9s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </rect>
  <text x="586" y="311" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#9999aa" letter-spacing="1" opacity="0">
    🧠 NLP / BERT
    <animate attributeName="opacity" values="0;0;0;0;0;0;1" dur="2.3s" fill="freeze" begin="0.4s"/>
    <animateTransform attributeName="transform" type="translate" values="0 10;0 0" dur="0.6s" fill="freeze" begin="1.9s" calcMode="spline" keySplines="0.22 1 0.36 1"/>
  </text>

  <!-- STATUS indicator -->
  <circle cx="366" cy="352" r="3.8" fill="#22c55e" opacity="0">
    <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;1" dur="3s" fill="freeze"/>
    <animate attributeName="r" values="3.8;5.5;3.8" dur="2.2s" repeatCount="indefinite" begin="3s"/>
    <animate attributeName="opacity" values="1;0.45;1" dur="2.2s" repeatCount="indefinite" begin="3s"/>
  </circle>
  <text x="378" y="357" font-family="'Courier New',monospace" font-size="11" fill="#555566" letter-spacing="1" opacity="0">
    Open to work  ·  Bhubaneswar, India
    <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;1" dur="3s" fill="freeze"/>
  </text>

  <!-- OUTER BORDER PULSE -->
  <rect x="1" y="1" width="898" height="398" rx="14" fill="none" stroke="#ffffff" stroke-width="1" opacity="0.07">
    <animate attributeName="opacity" values="0.07;0.15;0.07" dur="4s" repeatCount="indefinite"/>
    <animate attributeName="stroke-width" values="1;1.5;1" dur="4s" repeatCount="indefinite"/>
  </rect>
</svg>

<br/>

<!-- TYPING ANIMATION -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=15&duration=2800&pause=700&color=888899&center=true&vCenter=true&multiline=true&width=700&height=70&lines=Building+at+the+edge+of+web+engineering+%26+AI+%F0%9F%9A%80;Shipped+real-time+CV+to+enterprise+%E2%80%94+before+sophomore+year+%F0%9F%8E%AF;MERN+%E2%80%A2+OpenCV+%E2%80%A2+BERT+%E2%80%A2+Node.js+%E2%80%A2+MongoDB)](https://git.io/typing-svg)

<br/>

<!-- CONNECT BADGES -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230a0a0a.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shivam-shrivastava-90a6282a7)
[![LeetCode](https://img.shields.io/badge/LeetCode-%230a0a0a.svg?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/shivam10-bit)
[![Gmail](https://img.shields.io/badge/Gmail-%230a0a0a.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shivamshrivatava004@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-%230a0a0a.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shivam10-bit)

<br/><br/>

</div>

---

## `whoami`

```typescript
const shivam: Developer = {
  name       : "Shivam Shrivastava",
  location   : "Bhubaneswar, Odisha, India 🇮🇳",
  education  : "B.Tech IT · KIIT University · 2023–Present · CGPA: 7.57",
  roles      : ["Full-Stack Developer", "AI/ML Engineer", "Computer Vision Enthusiast"],
  building   : "Lie Detector — YouTube Comment Forensics (BERT + NLP)",
  seeking    : "Internships & Full-time SWE / AI roles",
  contact    : "shivamshrivatava004@gmail.com",
  funFact    : "Shipped a real-time CV system to enterprise before my 2nd year ended 🎯",
};
```

<br/>

---

## ⚡ Tech Stack

<div align="center">

**Languages**

![Java](https://img.shields.io/badge/Java-%23000000.svg?style=flat-square&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-%23000000.svg?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-%23000000.svg?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23000000.svg?style=flat-square&logo=javascript&logoColor=F7DF1E)
![SQL](https://img.shields.io/badge/SQL-%23000000.svg?style=flat-square&logo=mysql&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React.js-%23000000.svg?style=flat-square&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux_Toolkit-%23000000.svg?style=flat-square&logo=redux&logoColor=764ABC)
![TailwindCSS](https://img.shields.io/badge/Tailwind-%23000000.svg?style=flat-square&logo=tailwind-css&logoColor=38BDF8)
![HTML5](https://img.shields.io/badge/HTML5-%23000000.svg?style=flat-square&logo=html5&logoColor=E34F26)
![CSS3](https://img.shields.io/badge/CSS3-%23000000.svg?style=flat-square&logo=css3&logoColor=1572B6)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-%23000000.svg?style=flat-square&logo=node.js&logoColor=339933)
![Express](https://img.shields.io/badge/Express.js-%23000000.svg?style=flat-square&logo=express&logoColor=white)
![JWT](https://img.shields.io/badge/JWT_Auth-%23000000.svg?style=flat-square&logo=jsonwebtokens&logoColor=white)
![REST](https://img.shields.io/badge/REST_APIs-%23000000.svg?style=flat-square&logo=postman&logoColor=FF6C37)

**AI / ML**

![OpenCV](https://img.shields.io/badge/OpenCV-%23000000.svg?style=flat-square&logo=opencv&logoColor=5C3EE8)
![BERT](https://img.shields.io/badge/BERT_NLP-%23000000.svg?style=flat-square&logo=huggingface&logoColor=FFD21E)
![NumPy](https://img.shields.io/badge/NumPy-%23000000.svg?style=flat-square&logo=numpy&logoColor=013243)
![Pandas](https://img.shields.io/badge/Pandas-%23000000.svg?style=flat-square&logo=pandas&logoColor=150458)

**Databases & Infra**

![MongoDB](https://img.shields.io/badge/MongoDB-%23000000.svg?style=flat-square&logo=mongodb&logoColor=47A248)
![Cloudinary](https://img.shields.io/badge/Cloudinary-%23000000.svg?style=flat-square&logo=cloudinary&logoColor=3448C5)
![Razorpay](https://img.shields.io/badge/Razorpay-%23000000.svg?style=flat-square&logo=razorpay&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-%23000000.svg?style=flat-square&logo=git&logoColor=F05032)
![GitHub](https://img.shields.io/badge/GitHub-%23000000.svg?style=flat-square&logo=github&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-%23000000.svg?style=flat-square&logo=postman&logoColor=FF6C37)
![VS Code](https://img.shields.io/badge/VS_Code-%23000000.svg?style=flat-square&logo=visualstudiocode&logoColor=007ACC)
![Flutter](https://img.shields.io/badge/Flutter-%23000000.svg?style=flat-square&logo=flutter&logoColor=02569B)

</div>

<br/>

---

## 🏗️ Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🔍 Lie Detector
**YouTube Comment Forensics Tool**

Detects inauthentic comments on YouTube videos using NLP and ML. Fetches & preprocesses comments via YouTube Data API, classifies them with a pre-trained BERT model for sentiment & authenticity scoring. Extending toward bot, promoter, and spam detection.

`Python` `BERT` `NLP` `Flutter` `React.js` `YouTube Data API` `ML`

*Dec 2025 – Mar 2026*

</td>
<td width="50%" valign="top">

### 📚 StudyNotion
**Full-Stack EdTech Platform**

Comprehensive MERN platform with Student / Instructor / Admin roles. Razorpay webhooks for payment consistency, JWT + bcrypt auth, OTP via Nodemailer, Redux Toolkit state, Cloudinary media delivery for video lectures.

`React.js` `Node.js` `Express.js` `MongoDB` `Redux` `Razorpay` `Cloudinary` `JWT`

*Oct 2025 – Jan 2026*

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 👁️ Automated Attendance System
**Enterprise Computer Vision**

Real-time face recognition tracker deployed at **Aditya Birla Group / UltraTech Cement**. Secure DB management, automated exportable compliance reports, HR analytics at enterprise scale.

`Python` `OpenCV` `NumPy` `Pandas` `Face Recognition`

*May – Jun 2025*

</td>
<td width="50%" valign="top">

### 🚧 Next Project
**Always Building**

Exploring the intersection of AI and the web. New projects in progress — watch this space.

`React.js` `Node.js` `Python` `AI/ML`

*2026 →*

</td>
</tr>
</table>

<br/>

---

## 💼 Experience

```
┌──────────────────────────────────────────────────────────────────────┐
│  IT Intern — Computer Vision & AI                           2024     │
│  Aditya Cement Works (ACW) · UltraTech Cement                       │
│  Aditya Birla Group                                                  │
├──────────────────────────────────────────────────────────────────────┤
│  ▸ Designed & deployed real-time automated attendance system         │
│  ▸ Built face recognition model for contactless employee tracking    │
│  ▸ Integrated automated record management & exportable reports       │
│  ▸ Delivered enterprise-grade UI adopted across all end-users        │
│                                                                      │
│  Stack: Python · OpenCV · NumPy · Pandas · Face Recognition         │
└──────────────────────────────────────────────────────────────────────┘
```

<br/>

---

## 📊 GitHub Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=shivam10-bit&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d0d0d&title_color=ffffff&text_color=777788&icon_color=aaaaaa&include_all_commits=true&count_private=true"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=shivam10-bit&layout=compact&theme=github_dark&hide_border=true&bg_color=0d0d0d&title_color=ffffff&text_color=777788&langs_count=8"/>

<br/><br/>

<img width="68%" src="https://github-readme-streak-stats.herokuapp.com/?user=shivam10-bit&theme=github-dark-blue&hide_border=true&background=0d0d0d&ring=ddddee&fire=ddddee&currStreakLabel=ffffff&sideLabels=666677&currStreakNum=ffffff&sideNums=bbbbcc&dates=444455"/>

<br/><br/>

<img width="88%" src="https://github-readme-activity-graph.vercel.app/graph?username=shivam10-bit&theme=github-compact&bg_color=0d0d0d&color=666677&line=aaaaaa&point=ffffff&area=true&area_color=222233&hide_border=true"/>

</div>

<br/>

---

## 🎓 Education & Certifications

| | |
|---|---|
| 🏛️ **KIIT University** | B.Tech — Information Technology · Aug 2023 – Present · Bhubaneswar, Odisha |
| 📊 **CGPA** | 7.57 |
| 🏆 **MERN Stack Bootcamp** | CodeHelp · Full-stack Web Development |
| ⚡ **LeetCode** | Active problem solver — Data Structures & Algorithms |

<br/>

---

## 📬 Let's Connect

<div align="center">

I'm actively seeking **internships** and **full-time roles** in software engineering and AI/ML.
If you're building something impactful — let's talk.

<br/>

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-%23000000.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shivam-shrivastava-90a6282a7)
[![Gmail](https://img.shields.io/badge/Send_an_Email-%23000000.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shivamshrivatava004@gmail.com)
[![GitHub](https://img.shields.io/badge/Follow_on_GitHub-%23000000.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shivam10-bit)

<br/>

📞 **+91 90578 18622**

</div>

<br/>

---

<div align="center">

<svg width="900" height="80" viewBox="0 0 900 80" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="footbg" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#040408"/>
      <stop offset="50%" style="stop-color:#0c0c14"/>
      <stop offset="100%" style="stop-color:#040408"/>
    </linearGradient>
  </defs>
  <rect width="900" height="80" fill="url(#footbg)" rx="8"/>
  <line x1="0" y1="1" x2="900" y2="1" stroke="#ffffff" stroke-width="0.8" opacity="0.1"/>
  <!-- Animated line sweep -->
  <line x1="0" y1="40" x2="0" y2="40" stroke="#ffffff" stroke-width="0.6" opacity="0.15">
    <animate attributeName="x2" values="0;900;0" dur="6s" repeatCount="indefinite" calcMode="linear"/>
  </line>
  <text x="450" y="34" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#444455" letter-spacing="3">
    "The best code ships and solves real problems."
  </text>
  <text x="450" y="56" text-anchor="middle" font-family="'Courier New',monospace" font-size="10" fill="#333344" letter-spacing="4">
    © 2025 SHIVAM SHRIVASTAVA · KIIT UNIVERSITY · BHUBANESWAR
  </text>
</svg>

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=shivam10-bit&color=000000&style=flat-square&label=Profile+Views)

</div>
