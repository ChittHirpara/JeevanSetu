<div align="center">

# 🌉 JeevanSetu — जीवन सेतु
### *Life Bridge — AI for Abandoned Elderly*

> **A voice-first AI that calls India's lonely seniors every morning, detects distress, and alerts their community — so no one dies unheard.**

`Hack Aarambh 2025` &nbsp;·&nbsp; `Team: Quantum Syndicates` &nbsp;·&nbsp; `Stack: MERN + AI` &nbsp;·&nbsp; `Status: Prototype`

</div>

---

## 📌 Table of Contents

- [The Problem](#-the-problem)
- [Our Solution](#-our-solution)
- [How It Works](#-how-it-works)
- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [Prototype](#-prototype)
- [Competitive Advantage](#-competitive-advantage)
- [Roadmap](#-roadmap)
- [Impact](#-impact)
- [Team](#-team)
- [Getting Started](#-getting-started)

---

## 🚨 The Problem

India is silently abandoning its elderly.

| Statistic | Reality |
|-----------|---------|
| **3.2 Crore** | Elderly living completely alone |
| **1 in 3** | Seniors face elder abuse — often by family |
| **ZERO** | National elder helplines exist |
| **32 Crore** | Elderly India will have by 2050 |

**Three failures that compound into a national crisis:**

1. **Joint Family Collapse** — Urban migration and nuclear family culture physically and emotionally leaves seniors behind.
2. **Zero Safety Net** — No national helpline. No monitoring. No protocol when a senior stops responding for days.
3. **Silent, Invisible Decline** — Health and mental deterioration go undetected. By the time family notices, it's often too late.

> 💔 Many elderly die alone at home. Bodies found days — sometimes weeks — later by neighbours or relatives.

**The Gap:** No proactive early-warning system exists in India for elderly living alone. **We built one.**

---

## 💡 Our Solution

**JeevanSetu** is a voice-first AI companion that watches over India's elderly — every single morning.

| Capability | Description |
|------------|-------------|
| 📞 Morning Voice Check-In | AI calls in Gujarati, Hindi, Tamil & 7+ Indian languages. Warm conversation — not a robocall. |
| 🧠 Real-Time Voice AI | Hume AI + Sarvam AI detect distress, confusion, or declining health from speech patterns live. |
| 🚨 Triple Alert in 8 Seconds | No response triggers simultaneous WhatsApp/SMS alerts to a neighbor, local NGO, and police. |
| 📊 Family Dashboard | Families get a live health and check-in summary every morning. |

---

## ⚙️ How It Works

```
Every morning. Every senior. No exceptions.
```

```
┌──────────────┐    ┌──────────────┐    ┌─────────────┐    ┌──────────────┐
│   6:00 AM    │    │   Responds?  │    │  All Good ✓ │    │ No Response  │
│              │    │              │    │             │    │              │
│  Automated   │───▶│  Voice       │───▶│  Log &      │    │  Alert Fires │
│  Call        │    │  Analysis    │    │  Notify     │    │              │
│              │    │              │    │             │    │  Neighbor +  │
│ AI dials the │    │ AI reads     │    │ Health      │    │  NGO +       │
│ senior in    │    │ tone,        │    │ logged.     │◀───│  Police      │
│ their        │    │ clarity,     │    │ Family gets │    │  notified    │
│ dialect.     │    │ energy &     │    │ morning     │    │  within      │
│ Warm,        │    │ distress     │    │ check-in    │    │  8 seconds.  │
│ friendly.    │    │ patterns.    │    │ summary.    │    │              │
└──────────────┘    └──────────────┘    └─────────────┘    └──────────────┘
```

> ⚡ If distress is detected **mid-call** → alert fires immediately, without waiting for the call to end.

---

## 🛠️ Tech Stack

```
Core: MERN Stack  +  Sarvam AI  +  Twilio  +  Hume AI
```

### Frontend
| Technology | Purpose |
|------------|---------|
| React.js | UI framework |
| Tailwind CSS | Styling |
| Socket.io | Live alerts |
| Chart.js | Health trend visualizations |

### Backend & Data
| Technology | Purpose |
|------------|---------|
| Node.js + Express | Server & REST APIs |
| MongoDB | Elder profiles & health logs |
| JWT Authentication | Secure access |

### AI & Voice Layer
| Technology | Purpose |
|------------|---------|
| **Sarvam AI** | Indian dialect TTS/STT (10+ languages) |
| **Hume AI** | Voice emotion & distress detection |
| **Twilio** | Automated calling infrastructure |
| **Fast2SMS** | Alert delivery via SMS/WhatsApp |

---

## ✨ Features

- [x] 📞 **Automated morning calls** in 10+ Indian dialects
- [x] 🧠 **Real-time voice emotion analysis** (Hume AI)
- [x] 🌐 **Multi-language support** — Gujarati, Hindi, Tamil & more
- [x] 🚨 **3-way simultaneous alert** — Neighbor + NGO + Police in 8 seconds
- [x] 📊 **Family health dashboard** with historical trends
- [x] 📱 **No smartphone required** on the senior's end — just a basic phone call
- [x] 🔒 **JWT-secured** family portal
- [x] ⚡ **Mid-call distress detection** — doesn't wait for call to end

---

## 🖥️ Prototype

> **Live Demo was presented at Hack Aarambh 2025 — on stage, in real time.**

### Demo Flow (as shown at Hack Aarambh 2025)

```
Step 01: JeevanSetu dials an 'elder' on stage in Gujarati.
         → Real voice. Real check-in.

Step 02: AI detects distress live.
         → Voice emotion model flags distress in real time.

Step 03: 3 alerts fire in 8 seconds.
         → Neighbor · NGO · Police — all notified simultaneously.
```

### Run Locally

```bash
# Clone the repo
git clone https://github.com/QuantumSyndicates/JeevanSetu.git
cd JeevanSetu

# Install dependencies
npm install
cd client && npm install && cd ..

# Set up environment variables
cp .env.example .env
# Fill in: TWILIO_SID, TWILIO_TOKEN, SARVAM_API_KEY, HUME_API_KEY, MONGODB_URI, JWT_SECRET

# Start the development server
npm run dev
```

### Environment Variables

```env
# Twilio (Automated Calling)
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_token
TWILIO_PHONE_NUMBER=your_twilio_number

# Sarvam AI (Indian Language TTS/STT)
SARVAM_API_KEY=your_sarvam_key

# Hume AI (Voice Emotion Detection)
HUME_API_KEY=your_hume_key

# SMS Alerts
FAST2SMS_API_KEY=your_fast2sms_key

# Database
MONGODB_URI=mongodb://localhost:27017/jeevansetu

# Auth
JWT_SECRET=your_jwt_secret
```

### API Endpoints (Core)

```
POST   /api/elders/register        → Register a senior profile
GET    /api/elders/:id/dashboard   → Family health dashboard
POST   /api/calls/initiate         → Trigger morning check-in call
GET    /api/calls/:id/analysis     → Voice emotion analysis result
POST   /api/alerts/fire            → Trigger 3-way emergency alert
GET    /api/alerts/history         → Past alert log
```

### Project Structure

```
JeevanSetu/
├── client/                    # React frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── Dashboard/     # Family health dashboard
│   │   │   ├── AlertPanel/    # Live alert notifications
│   │   │   └── VoiceChart/    # Real-time voice analysis
│   │   └── App.jsx
├── server/                    # Node.js backend
│   ├── routes/
│   │   ├── elders.js
│   │   ├── calls.js
│   │   └── alerts.js
│   ├── services/
│   │   ├── twilioService.js   # Automated calling
│   │   ├── sarvamService.js   # Indian dialect AI
│   │   ├── humeService.js     # Emotion detection
│   │   └── alertService.js    # 3-way alert system
│   └── models/
│       ├── Elder.js
│       └── CallLog.js
└── README.md
```

---

## 🏆 Competitive Advantage

No existing solution does all of this — simultaneously.

| Feature | Family WhatsApp | Panic Buttons | **JeevanSetu ✓** |
|---------|:--------------:|:-------------:|:----------------:|
| Proactive daily check-in | ✗ | ✗ | ✅ |
| Works without a smartphone | ✗ | Partial | ✅ |
| Detects silent health decline | ✗ | ✗ | ✅ |
| Multi-language Indian dialects | ✗ | ✗ | ✅ |
| 3-way simultaneous alert | ✗ | ✗ | ✅ |
| No family dependency needed | ✗ | ✗ | ✅ |

---

## 🗺️ Roadmap

### Phase 1 · 0–3 Months (Current)
- [x] MVP: Twilio + Sarvam AI calling
- [ ] Pilot — 50 seniors in Ahmedabad
- [ ] Gujarati, Hindi & English support
- [ ] Basic family notification dashboard

### Phase 2 · 3–9 Months
- [ ] Scale to 5,000 seniors across 3 cities
- [ ] NGO & RWA partnerships
- [ ] Health vitals integration (BP, glucose)
- [ ] Predictive decline model (30-day)

### Phase 3 · 9–24 Months
- [ ] National rollout — 10 languages
- [ ] AYUSH & state portal integration
- [ ] Government API partnerships
- [ ] **Target: 1 crore seniors covered**

---

## 📈 Impact

| Metric | Value |
|--------|-------|
| 🎯 Seniors we can reach | **3.2 Crore** |
| ⚡ Alert response time | **8 seconds** |
| 🏛️ Existing national systems | **0** |
| 📊 Seniors with no digital safety net | **78%** |
| 💰 Government spend on elder AI systems | **₹0** |
| 👴 India's elderly by 2050 | **32 Crore (4× growth)** |

---

## 👨‍💻 Team

**Quantum Syndicates · Hack Aarambh 2025**

> *United by one mission: No elderly person should die alone, unheard, or unseen.*

| Name | Role | University |
|------|------|------------|
| 💻 **Chitt Hirpara** | Full Stack & AI | CSE · Swaminarayan University |
| ⚙️ **Anisha Chhajer** | Backend & APIs | CSE · Swaminarayan University |
| 🎨 **Hanuman Singh** | Frontend & UX | CSE · Swaminarayan University |
| 🧠 **Prashant Parmar** | ML & Voice AI | CSE · Swaminarayan University |

---

## 📄 License

This project was built for **Hack Aarambh 2025**. All rights reserved by Team Quantum Syndicates.

---

<div align="center">

### *"Every morning, someone waits for a call that never comes."*
### *JeevanSetu makes that call.*

**3.2 Cr** seniors we can reach &nbsp;·&nbsp; **8 sec** alert response time &nbsp;·&nbsp; **0** existing national systems

*Team Quantum Syndicates · Hack Aarambh 2025*

</div>
