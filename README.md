# 🎭 THE ACM HEIST — GHRCEM Pune

> **Target: Our Own Campus** · An immersive 3D Money Heist-themed treasure hunt experience organized by the **ACM Student Chapter**, G H Raisoni College of Engineering & Management, Pune.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-acm--th.vercel.app-red?style=for-the-badge&logo=vercel)](https://acm-th.vercel.app/)
[![Event Date](https://img.shields.io/badge/Event%20Date-23%20Sept%202026-black?style=for-the-badge&logo=eventbrite)](https://acm-th.vercel.app/)
[![ACM GHRCEM](https://img.shields.io/badge/ACM-GHRCEM%20Pune-blue?style=for-the-badge)](https://acm-th.vercel.app/)

---

## 🌐 Live Website

🔗 **[https://acm-th.vercel.app/](https://acm-th.vercel.app/)**

---

## 📸 Overview

**THE ACM HEIST** transforms the GHRCEM Wagholi campus into an interactive 3D heist arena. Participants form crews, register online through an interactive character-dossier registration wizard, and embark on a high-stakes campus treasure hunt.

```
                    ┌───────────────────────────────┐
                    │      THE ACM HEIST (GHRCEM)   │
                    │   18.5731° N · 73.9816° E     │
                    └──────────────┬────────────────┘
                                   │
       ┌───────────────────────────┼───────────────────────────┐
       ▼                           ▼                           ▼
 🏛️ 3D Campus Scene         📋 Crew Registration        💳 Dual-UPI Gateway
 (Three.js WebGL Engine)     (Multi-step Dossier Form)   (Auto ₹49 Pre-filled QR)
       │                           │                           │
       └───────────────────────────┼───────────────────────────┘
                                   ▼
                   ☁️ Google Apps Script & Drive Backend
```

---

## ✨ Features & Highlights

### 🏛️ Interactive 3D WebGL Campus Model
- **Architecturally Accurate Campus:** Real-world OSM data mapping GHRCEM academic blocks, central courtyard, arch gate, turf ground, parking, and pathways.
- **Cinematic Camera Flights:** Dynamic camera choreography between registration steps (`flyTo` camera choreography with smooth cubic-bezier easing).
- **Interactive 3D Explorer Mode:** Walk around the campus using keyboard (`W`, `A`, `S`, `D`, `R`, `F`) or on-screen directional touch pads.

### 🎭 Money Heist Atmosphere & Visuals
- **Cinematic Soundtrack:** Built-in HTML5 audio playing the iconic Money Heist theme (`heist.mp3`) with sound toggles and background lifecycle listeners.
- **Physical Particle Simulations:** 2D Canvas physics simulation for floating cash notes, gold bars, and balloon animations.
- **Salvador Dalí Aesthetic:** Character badges, planning board string-and-pin visualizations, and security dossiers.

### 📋 Multi-Step Recruitment Wizard
1. **Crew Identification:** Team name creation and college selection.
2. **Crew Leader:** Leader name, branch (11 departments), academic year, phone, and email.
3. **Crew Members:** Dynamic addition/removal of up to 3 teammates with live crew counter.
4. **Sealing the File:** Checklist verification and payment gateway.

### 💳 Dual-UPI QR Swapper System
- **Pre-filled Dynamic UPI QRs:** Scanning automatically fills in the exact registration fee (**₹49**).
- **Instant Swapper:** Allows participants to toggle between Primary (*Kumar Aditya Singh*) and Backup (*Sanika Sunil Bavaskar*) QR codes with single-click deep links (`PAY ₹49 VIA UPI APP ▸`).
- **Proof Verification:** 12-digit UTR validation and file upload with base64 encoding.

### ☁️ Cloud Backend Integration
- Integrated with a serverless **Google Apps Script Web App**.
- Automatically checks for duplicate crew names.
- Syncs team records directly to Google Sheets and stores payment screenshots in Google Drive.
- Provides WhatsApp Community connection links upon successful registration.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Three.js (WebGL)** | 3D Campus rendering, lighting, materials, and camera flight paths |
| **Vanilla JavaScript (ES6+)** | State management, audio playback, particle physics, and form wizard |
| **HTML5 & CSS3** | Custom typography (Oswald, Roboto Mono), glassmorphism, responsive UI |
| **Google Apps Script** | Serverless backend API endpoint for Sheets & Drive integration |
| **Vercel** | Edge deployment and continuous integration hosting |

---

## 🚀 Running Locally

Clone the repository and start a lightweight local development server:

```bash
# Clone the repository
git clone https://github.com/kumar-aditya79/ACM_TH.git

# Navigate to project directory
cd ACM_TH

# Start a local HTTP server (Python 3)
python -m http.server 5500
```

Open your browser and navigate to:
```
http://localhost:5500/intro.html
```

---

## 📂 Project Structure

```
ACM_TH/
├── audio/
│   └── heist.mp3          # Money Heist theme soundtrack
├── team/                  # Crew & Professor headshots / assets
├── campus.json            # Procedural building & ground coordinates
├── index.html             # Route redirect to intro.html
├── intro.html             # Main application (3D Engine, Form, UI)
├── osm_*.json             # OpenStreetMap boundary and road data
├── qr_kumar.png           # Primary UPI QR Code asset
├── qr_sanika.png          # Backup UPI QR Code asset
├── vercel.json            # Vercel routing and clean URL rules
└── README.md              # Project documentation
```

---

## 👥 Organized By

**ACM Student Chapter — GHRCEM, Pune**  
*G H Raisoni College of Engineering & Management, Domkhel Road, Wagholi, Pune - 412207*

---

<div align="center">
  <sub>Built with ❤️ by the ACM GHRCEM Tech Team. All rights reserved.</sub>
</div>
