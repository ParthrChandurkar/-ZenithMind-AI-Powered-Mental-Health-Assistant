# 🧠 ZenithMind — AI-Powered Mental Health Assistant

> A full-stack digital mental wellness ecosystem combining **Cognitive Behavioral Therapy (CBT)**, **AI-driven mood analytics**, and **gamified self-care** — built for students and young professionals.

---

## 📌 Project Overview

Mental health challenges like stress, anxiety, and disrupted sleep have become increasingly prevalent among college students and early-career professionals. Existing wellness apps address these in isolation — some focus only on meditation (Headspace, Calm), others only on chatbot conversations (Woebot, Wysa). None bring it all together.

**ZenithMind bridges that gap.** It is a modular, AI-informed mental health platform that combines structured CBT techniques, real-time mood tracking, physical health data (via Google Fit), and gamified engagement — all under one cohesive interface. Built on the MERN stack with a CBT-powered AI chatbot at its core, ZenithMind aims to democratize mental wellness support in an accessible, private, and always-available format.

---

## ✨ Key Features

- 🤖 **AI-Powered CBT Chatbot** — 24/7 NLP-enabled chatbot applying cognitive restructuring, thought reframing, and coping strategies in real conversation
- 📊 **Mood & Stress Analytics Dashboard** — daily mood logs visualized as line graphs, pie charts, and weekly trends for long-term self-awareness
- 🏃 **Google Fit Integration** — correlates physical metrics (steps, heart rate, sleep cycles) with mental states for data-driven wellness recommendations
- 🎮 **Gamified Habit Engine** — streaks, badges, and achievement milestones to reinforce positive mental health habits
- 🩺 **Therapist & Admin Panel** — role-based dashboards for counselors and institutions to monitor anonymized group well-being trends
- 🔐 **Secure Authentication** — JWT-based login with role assignment (User / Admin / Therapist)
- 📈 **Progress Reflection** — analytics-driven growth charts help users track emotional improvement over time

---

## 🧪 Research Validation

ZenithMind was piloted with **18 participants** (undergraduate students and early-career professionals):

| Metric | Result |
|---|---|
| Users who found the system easy to use | **83%** |
| Users who found the interface visually clear | **72%** |
| Task completion without assistance (first-time users) | **13 / 18** |
| CBT chatbot responses rated contextually relevant | **~66%** |
| Users who found mood visualizations helpful | **72%** |
| Users who reported increased daily engagement via gamification | **~70%** |
| Average chatbot response time | **< 2–3 seconds** |
| Dashboard visualization accuracy | **> 95%** |

---

## 🏗️ System Architecture

ZenithMind follows a modular **MERN stack** architecture:

```
┌─────────────────────────────────────────────────┐
│                  React Frontend                  │
│     Dashboards · Chatbot UI · Mood Logger        │
└───────────────────┬─────────────────────────────┘
                    │ REST API
┌───────────────────▼─────────────────────────────┐
│              Node.js + Express Backend           │
│     JWT Auth · NLP Processing · API Routing      │
└──────┬────────────────────────┬─────────────────┘
       │                        │
┌──────▼──────┐       ┌─────────▼────────┐
│  MongoDB    │       │  Google Fit API  │
│  Atlas      │       │  (OAuth 2.0)     │
│  (User Data │       │  Steps · Sleep · │
│  Mood Logs) │       │  Heart Rate      │
└─────────────┘       └──────────────────┘
```

---

## 🧠 CBT Techniques Implemented

ZenithMind operationalizes evidence-based CBT techniques digitally:

**Cognitive Restructuring** — the chatbot guides users through identifying negative automatic thoughts and gradually reframing them toward rational viewpoints through structured questioning.

**Structured Journaling** — mood logging follows a semi-automated CBT thought-record format, capturing triggers, thoughts, and emotional reactions to build pattern awareness over time.

**Behavioral Activation** — when mood trends and activity indicators signal avoidance behaviors, the system suggests small, achievable actions (e.g. a 15-minute walk, a breathing session) to reinforce positive routines.

**Emotional Labeling** — users categorize their emotional states, building literacy in connecting mental health patterns to lifestyle factors like sleep and activity.

---

## 🗂️ Project Structure

```
zenithmind/
│
├── src/
│   ├── components/         # React UI components (dashboards, chatbot, mood logger)
│   ├── pages/              # Route-level views
│   ├── hooks/              # Custom React hooks
│   └── utils/              # Helper functions, constants
│
├── public/                 # Static assets
├── package.json            # Frontend dependencies
└── README.md
```

> Backend (Node.js/Express + MongoDB) is maintained in a separate repository or `/server` directory.

---

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- npm or yarn
- MongoDB Atlas account
- Google Cloud project with Fit API enabled

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/zenithmind.git
cd zenithmind

# Install frontend dependencies
npm install

# Start the development server
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Available Scripts

| Command | Description |
|---|---|
| `npm start` | Run in development mode with hot reload |
| `npm test` | Launch test runner in interactive watch mode |
| `npm run build` | Build optimized production bundle to `/build` |
| `npm run eject` | Eject from Create React App (irreversible) |

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory:

```env
REACT_APP_API_BASE_URL=http://localhost:5000
REACT_APP_GOOGLE_FIT_CLIENT_ID=your_google_client_id
REACT_APP_JWT_SECRET=your_jwt_secret
MONGODB_URI=your_mongodb_atlas_connection_string
```

---

## 📦 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js (Create React App) |
| Backend | Node.js + Express.js |
| Database | MongoDB Atlas (NoSQL) |
| Authentication | JWT (JSON Web Tokens) |
| Health Data | Google Fit REST API (OAuth 2.0) |
| NLP / Chatbot | NLP libraries + CBT-structured prompt logic |
| Visualization | Plotly / Recharts (mood & stress dashboards) |

---

## 🔬 Comparative Analysis

ZenithMind was benchmarked against leading mental health apps across 10 core feature dimensions:

| Feature | ZenithMind | Headspace | Woebot | Wysa | Calm | Replika |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| CBT Chatbot | ✅ | ❌ | ✅ | ✅ | ❌ | ❌ |
| Mood Analytics Dashboard | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Google Fit / Wearable Integration | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Gamified Engagement | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ |
| Therapist Panel Access | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Structured Journaling | ✅ | ❌ | ✅ | ✅ | ❌ | ❌ |
| Psychoeducation | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |

ZenithMind is the only platform in this comparison to combine all seven features in a single cohesive system.

---

## ⚠️ Limitations

- Google Fit integration depends on third-party API reliability — delays can affect real-time insights
- Mood entries are self-reported, introducing subjectivity in data accuracy
- The CBT chatbot is a guided support tool, **not a replacement** for clinical diagnosis or treatment in severe cases
- Recommendations deepen as more behavioral data accumulates — early-use suggestions may be less personalized
- Continuous operation requires stable internet access and device permissions for Google Fit data sync

---

## 🔭 Future Work

- 🎙️ **Voice therapy module** — spoken CBT sessions using speech-to-text
- 📡 **Passive stress prediction** — ML models on wearable signals without active user input
- 🌍 **Multilingual & cultural localization** — adapting to Indian academic and corporate contexts
- 🏥 **Certified therapist dashboards** — expanding clinical integration and validation
- 📏 **Longitudinal clinical trials** — statistically rigorous validation with larger, diverse populations

---

## 📄 Research Paper

This project is documented in a peer-reviewed research paper:

> **"ZenithMind: Mental Health Assistant with CBT Integration"**
> Aditya Badgujar, Prathamesh Walishetty, Parth Chandurkar, Anurag Gupta *(VIIT Pune)* · Riddhi Mirajkar *(VIT Pune)* · Rishikaysh Kaakandikar *(SBIMS Pune)*

---

## 📜 License

This project is developed for academic research purposes. See `LICENSE` for details.
