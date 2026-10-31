<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 280" width="1000" height="280" role="img" aria-label="RAVS DEV header">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#0d1117"/>
      <stop offset="0.55" stop-color="#0b1730"/>
      <stop offset="1" stop-color="#0a2a5e"/>
    </linearGradient>
    <linearGradient id="accent" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#1f6feb"/>
      <stop offset="0.5" stop-color="#58a6ff"/>
      <stop offset="1" stop-color="#00d4ff"/>
    </linearGradient>
    <linearGradient id="scan" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#58a6ff" stop-opacity="0"/>
      <stop offset="0.5" stop-color="#58a6ff" stop-opacity="0.35"/>
      <stop offset="1" stop-color="#58a6ff" stop-opacity="0"/>
    </linearGradient>
    <pattern id="grid" width="32" height="32" patternUnits="userSpaceOnUse">
      <path d="M32 0H0V32" fill="none" stroke="#58a6ff" stroke-opacity="0.07" stroke-width="1"/>
    </pattern>
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <clipPath id="typeClip">
      <rect x="188" y="170" width="0" height="40">
        <animate attributeName="width" from="0" to="624" dur="3s" begin="1s" fill="freeze"/>
      </rect>
    </clipPath>
    <clipPath id="round"><rect width="1000" height="280" rx="18"/></clipPath>
  </defs>

  <g clip-path="url(#round)">
    <!-- background -->
    <rect width="1000" height="280" fill="url(#bg)"/>
    <rect width="1000" height="280" fill="url(#grid)"/>

    <!-- soft glowing orbs -->
    <circle cx="140" cy="60" r="90" fill="#1f6feb" opacity="0.12">
      <animate attributeName="cx" values="140;220;140" dur="9s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.08;0.18;0.08" dur="6s" repeatCount="indefinite"/>
    </circle>
    <circle cx="860" cy="230" r="110" fill="#00d4ff" opacity="0.10">
      <animate attributeName="cx" values="860;780;860" dur="11s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.06;0.15;0.06" dur="7s" repeatCount="indefinite"/>
    </circle>

    <!-- scanning beam -->
    <rect x="-120" y="0" width="120" height="280" fill="url(#scan)">
      <animate attributeName="x" from="-120" to="1000" dur="5s" repeatCount="indefinite"/>
    </rect>

    <!-- rotating HUD rings (right side) -->
    <g transform="translate(870 140)" opacity="0.9">
      <circle r="78" fill="none" stroke="#1f6feb" stroke-opacity="0.35" stroke-width="1.5" stroke-dasharray="4 10">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="24s" repeatCount="indefinite"/>
      </circle>
      <circle r="58" fill="none" stroke="#58a6ff" stroke-opacity="0.6" stroke-width="2" stroke-dasharray="60 30 10 30">
        <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="14s" repeatCount="indefinite"/>
      </circle>
      <circle r="38" fill="none" stroke="#00d4ff" stroke-opacity="0.5" stroke-width="1.5" stroke-dasharray="2 8">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="8s" repeatCount="indefinite"/>
      </circle>
      <text text-anchor="middle" y="8" font-family="'JetBrains Mono','Courier New',monospace" font-size="22" font-weight="700" fill="#58a6ff" filter="url(#glow)">&lt;/&gt;</text>
    </g>

    <!-- mirrored rings (left side) -->
    <g transform="translate(130 140)" opacity="0.7">
      <circle r="62" fill="none" stroke="#58a6ff" stroke-opacity="0.35" stroke-width="1.5" stroke-dasharray="3 9">
        <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="20s" repeatCount="indefinite"/>
      </circle>
      <circle r="42" fill="none" stroke="#1f6feb" stroke-opacity="0.55" stroke-width="2" stroke-dasharray="40 24">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="12s" repeatCount="indefinite"/>
      </circle>
      <text text-anchor="middle" y="8" font-family="'JetBrains Mono','Courier New',monospace" font-size="22" font-weight="700" fill="#00d4ff" filter="url(#glow)">{ }</text>
    </g>

    <!-- window title bar -->
    <rect x="0" y="0" width="1000" height="34" fill="#0d1117" fill-opacity="0.85"/>
    <circle cx="24" cy="17" r="5" fill="#ff5f56"/>
    <circle cx="44" cy="17" r="5" fill="#ffbd2e"/>
    <circle cx="64" cy="17" r="5" fill="#27c93f"/>
    <text x="500" y="21" text-anchor="middle" font-family="'JetBrains Mono','Courier New',monospace" font-size="12" fill="#8b949e">ravs@github:~/profile — bash</text>
    <line x1="0" y1="34" x2="1000" y2="34" stroke="#58a6ff" stroke-opacity="0.25"/>

    <!-- prompt line -->
    <text x="500" y="76" text-anchor="middle" font-family="'JetBrains Mono','Courier New',monospace" font-size="14" fill="#58a6ff" fill-opacity="0">
      <tspan>$ ./init --profile</tspan>
      <animate attributeName="fill-opacity" from="0" to="0.9" dur="0.6s" begin="0.2s" fill="freeze"/>
    </text>

    <!-- title -->
    <text x="500" y="150" text-anchor="middle" font-family="'JetBrains Mono','Courier New',monospace" font-size="84" font-weight="800" letter-spacing="6" fill="url(#accent)" filter="url(#glow)" opacity="0">
      MUHAMMAD FAKRURAZI
      <animate attributeName="opacity" from="0" to="1" dur="1s" begin="0.4s" fill="freeze"/>
    </text>

    <!-- accent line under title -->
    <rect x="500" y="162" width="0" height="3" rx="1.5" fill="url(#accent)">
      <animate attributeName="width" from="0" to="520" dur="1s" begin="0.8s" fill="freeze"/>
      <animate attributeName="x" from="500" to="240" dur="1s" begin="0.8s" fill="freeze"/>
    </rect>

    <!-- typed subtitle -->
    <g clip-path="url(#typeClip)">
      <text x="188" y="196" font-family="'JetBrains Mono','Courier New',monospace" font-size="20" fill="#e6edf3">Backend Developer | Game Developer | Web Developer</text>
    </g>
    <rect x="188" y="180" width="10" height="20" fill="#58a6ff">
      <animate attributeName="x" from="188" to="812" dur="3s" begin="1s" fill="freeze"/>
      <animate attributeName="opacity" values="1;0;1" dur="1s" begin="4s" repeatCount="indefinite"/>
    </rect>

    <!-- status bar -->
    <rect x="0" y="240" width="1000" height="40" fill="#0d1117" fill-opacity="0.85"/>
    <line x1="0" y1="240" x2="1000" y2="240" stroke="#58a6ff" stroke-opacity="0.25"/>
    <circle cx="30" cy="260" r="5" fill="#27c93f">
      <animate attributeName="opacity" values="1;0.25;1" dur="1.6s" repeatCount="indefinite"/>
    </circle>
    <text x="46" y="265" font-family="'JetBrains Mono','Courier New',monospace" font-size="13" fill="#27c93f">ONLINE</text>
    <text x="500" y="265" text-anchor="middle" font-family="'JetBrains Mono','Courier New',monospace" font-size="13" fill="#8b949e">SA-MP  •  open.mp  •  FiveM  •  Backend  •  Web  •  Android</text>
    <text x="970" y="265" text-anchor="end" font-family="'JetBrains Mono','Courier New',monospace" font-size="13" fill="#58a6ff">v2026.10</text>

    <!-- HUD corner brackets -->
    <g fill="none" stroke="#58a6ff" stroke-width="2" stroke-opacity="0.8">
      <path d="M14 52 V44 H22"/>
      <path d="M986 52 V44 H978"/>
      <path d="M14 228 V236 H22"/>
      <path d="M986 228 V236 H978"/>
    </g>
  </g>

  <!-- outer border -->
  <rect x="1" y="1" width="998" height="278" rx="17" fill="none" stroke="#1f6feb" stroke-opacity="0.6" stroke-width="2"/>
</svg>

---

## ⟨ SYSTEM PROFILE :: IDENTITY CORE ⟩

```text
┌──────────────────────────────────────────┐
│                                          │
│  USER     : Muhammad Fakrurazi           │
│  STATUS   : [ ONLINE ]                   │
│  VERSION  : 2026                         │
│                                          │
├──────────────────────────────────────────┤
│  ROLES                                   │
│  ├─ [01] Backend Developer               │
│  ├─ [02] Game Developer                  │
│  ├─ [03] Apk Developer                   │
│  ├─ [04] Fivem Developer                 │
│  ├─ [05] Web Developer                   │
│  └─ [06] Android Developer               │
│                                          │
├──────────────────────────────────────────┤
│  CURRENT FOCUS                           │
│  ├─ Backend & Database Systems           │
│  ├─ Apk Applications                     │
│  └─ Web Applications                     │
│                                          │
├──────────────────────────────────────────┤
│  MISSION                                 │
│  > Build. Learn. Improve. Repeat.        │
└──────────────────────────────────────────┘
```

---

## ◈ PROGRAMMING LANGUAGES

<div align="center">

<img src="https://skillicons.dev/icons?i=c,cpp,py,java,js,php" />

<br><br>

![C](https://img.shields.io/badge/C-PROGRAMMING-3949ab?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-PROGRAMMING-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/PYTHON-PROGRAMMING-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/JAVA-PROGRAMMING-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JAVASCRIPT-PROGRAMMING-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-BACKEND-777BB4?style=flat-square&logo=php&logoColor=white)
![Pawn](https://img.shields.io/badge/PAWN-SA--MP%20/%20OPEN.MP-5b2cff?style=flat-square)

</div>

---

## ◈ GAME DEVELOPMENT

<div align="center">

![open.mp](https://img.shields.io/badge/OPEN.MP-MULTIPLAYER%20SERVER-6C3CFF?style=flat-square)
![Pawn](https://img.shields.io/badge/PAWN-GAMEMODE%20DEVELOPMENT-0d1117?style=flat-square)

</div>

---

## ◈ WEB & BACKEND DEVELOPMENT

<div align="center">

<img src="https://skillicons.dev/icons?i=html,css,js,php,nodejs,py,java" />

<br><br>

![HTML5](https://img.shields.io/badge/HTML5-FRONTEND-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-STYLING-1572B6?style=flat-square&logo=css3&logoColor=white)
![Node.js](https://img.shields.io/badge/NODE.JS-BACKEND-00a82d?style=flat-square&logo=nodedotjs&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-BACKEND-777BB4?style=flat-square&logo=php&logoColor=white)

</div>

---

## ◈ DATABASE

<div align="center">

<img src="https://skillicons.dev/icons?i=mysql" />

<br><br>

![MySQL](https://img.shields.io/badge/MYSQL-DATABASE-4479A1?style=flat-square&logo=mysql&logoColor=white)

</div>

---

## ◈ MOBILE DEVELOPMENT

<div align="center">

<img src="https://skillicons.dev/icons?i=androidstudio,java" />

<br><br>

![Android Studio](https://img.shields.io/badge/ANDROID%20STUDIO-MOBILE%20DEVELOPMENT-00e676?style=flat-square&logo=androidstudio&logoColor=white)
![Java](https://img.shields.io/badge/JAVA-ANDROID-ED8B00?style=flat-square&logo=openjdk&logoColor=white)

</div>

---

## ◈ SYSTEM & SERVER

<div align="center">

<img src="https://skillicons.dev/icons?i=linux,bash" />

<br><br>

![Linux](https://img.shields.io/badge/LINUX-SERVER-f5c400?style=flat-square&logo=linux&logoColor=black)
![VPS](https://img.shields.io/badge/VPS-SERVER-0d1117?style=flat-square&logo=linux&logoColor=white)
![Bash](https://img.shields.io/badge/BASH-TERMINAL-1fb800?style=flat-square&logo=gnubash&logoColor=white)

</div>

---

## ◈ DEVELOPMENT TOOLS

<div align="center">

<img src="https://skillicons.dev/icons?i=vscode,visualstudio,git,github" />

<br><br>

![VS Code](https://img.shields.io/badge/VS%20CODE-EDITOR-3f6fdc?style=flat-square&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/GIT-VERSION%20CONTROL-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GITHUB-REPOSITORY-0d1117?style=flat-square&logo=github&logoColor=white)

</div>

---

## ⟨ SYSTEM TERMINAL :: COMMAND LINE ⟩

```bash
user@github:~$ whoami

> Backend Developer
> Game Developer
> Apk Developer
> Web Developer
> Android Developer

user@github:~$ cat languages.conf

> C
> C++
> PAWN
> Python
> Java
> JavaScript
> PHP

user@github:~$ cat mission.conf

> Building scalable systems and immersive game experiences.

user@github:~$ ls projects/

> Gamemode-OpenMp/
> Web-Projects/
> Backend-Projects/

user@github:~$ system-status

> DEVELOPMENT ................ ONLINE
> DATABASE ................... ONLINE
> GAME SYSTEM ................ ONLINE
> BACKEND .................... ONLINE
> WEB SYSTEM ................. ONLINE
> APK SYSTEM ................. ONLINE

> SYSTEM READY.
```

---

## ⟨ CURRENT OBJECTIVES :: DEVELOPMENT ROADMAP ⟩

```text
[ ACTIVE ]

[✓] MySQL Database Integration
[✓] Backend Development
[✓] Web Development

[ IN PROGRESS ]

[>] Account & Character Systems
[>] UCP Development
[>] API Integration
[>] Performance Optimization

[ NEXT ]

[ ] Advanced Backend Architecture
[ ] More C / C++ Projects
[ ] More Python Projects
[ ] Web Dashboard Systems
```

---

## ⟨ ACTIVE DEVELOPMENT :: CURRENT SYSTEMS ⟩

```text
user@github:~$ systemctl status development

● gamemode-openmp.service
   ├─ Status  : ACTIVE
   └─ Building multiplayer roleplay systems

● web-development.service
   ├─ Status  : ACTIVE
   └─ Building modern web applications

● backend.service
   ├─ Status  : ACTIVE
   └─ Database • API • Server Logic

● database.service
   ├─ Status  : ACTIVE
   └─ MySQL • Account • Player Data

STATUS: ALL DEVELOPMENT SYSTEMS OPERATIONAL
```

---

## ⟨ DEVELOPMENT NETWORK :: SPECIALIZATION ⟩

```text
DEVELOPMENT NETWORK
│
├── PROGRAMMING
│   ├─ C
│   ├─ C++
│   ├─ PAWN
│   ├─ Python
│   ├─ Java
│   ├─ JavaScript
│   └─ PHP
│
├── GAME SYSTEMS
│   ├─ SA-MP
│   ├─ open.mp
│   ├─ Gamemode
│   ├─ Account Systems
│   ├─ Vehicle Systems
│   ├─ Inventory Systems
│   └─ Database Integration
│
├── BACKEND
│   ├─ Node.js
│   ├─ PHP
│   ├─ MySQL
│   ├─ REST API
│   └─ Authentication
│
├── WEB
│   ├─ HTML
│   ├─ CSS
│   ├─ JavaScript
│   └─ Dashboard
│
├── MOBILE
│   ├─ Android Studio
│   ├─ Java
│   └─ Android Client
│
└── SERVER
    ├─ Linux
    ├─ VPS
    ├─ Bash
    ├─ Git
    └─ Deployment
```

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:0d1117&height=100&section=footer" width="100%"/>

</div>
