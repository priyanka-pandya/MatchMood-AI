# MatchMood-AI

# 🎬 MatchMood AI — AI Video Gallery & Generator

![React](https://img.shields.io/badge/React-19-61DAFB?style=flat&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=flat&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-6.2-646CFF?style=flat&logo=vite&logoColor=white)
![Google GenAI](https://img.shields.io/badge/Google_GenAI-Veo_3.1-4285F4?style=flat&logo=google&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

An AI-powered video gallery that lets users browse, remix, and generate brand-new videos using **Google's Veo 3.1** generative video model. Built with React 19 + TypeScript + Vite, originally developed as a hackathon demo for the MI vs RR IPL match at Wankhede Stadium.

---

 
---

## ✨ Features

- 🎥 Browse a curated gallery of AI-generated videos
- ▶️ Full in-app video player with modal overlay
- ✏️ Edit any video's text prompt and regenerate it
- 🤖 Generates brand-new videos using **Google Veo 3.1 Fast** model
- ⏳ Async generation with real-time polling until video is ready
- 📥 Converts generated video to base64 for instant in-browser playback
- ❌ Graceful error handling with user-friendly error modals
- 💨 Built with Tailwind CSS v4 for a clean dark UI

---

## 🗂️ Project Structure

```
MatchMood-AI/
├── App.tsx                      # Main app — state, routing between views
├── index.tsx                    # React entry point
├── index.html                   # HTML shell
├── constants.ts                 # Mock video data & static file URLs
├── types.ts                     # TypeScript interfaces (Video)
├── index.css                    # Global styles
├── components/
│   ├── VideoGrid.tsx            # Gallery grid layout
│   ├── VideoCard.tsx            # Individual video card
│   ├── VideoPlayer.tsx          # Full modal video player
│   ├── EditVideoPage.tsx        # Prompt editing + generation trigger
│   ├── SavingProgressPage.tsx   # Loading screen during generation
│   ├── ErrorModal.tsx           # Error display modal
│   └── icons.tsx                # SVG icon components
├── vite.config.ts               # Vite configuration
├── tsconfig.json                # TypeScript config
└── package.json                 # Dependencies
```

---

## 🧠 How It Works

```
User selects a video → Opens VideoPlayer
       ↓
User clicks "Edit" → Opens EditVideoPage with current prompt
       ↓
User edits prompt → Clicks "Generate new video"
       ↓
App calls Google Veo 3.1 API (generateVideos)
       ↓
Polls every 10 seconds until generation is complete
       ↓
Fetches video blob → Converts to base64
       ↓
New video appears at top of gallery → Auto-plays
```

---

## 📦 Tech Stack

| Layer | Tool |
|-------|------|
| Framework | React 19 |
| Language | TypeScript 5.8 |
| Build Tool | Vite 6.2 |
| Styling | Tailwind CSS v4 |
| AI Model | Google Veo 3.1 Fast (via `@google/genai`) |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- A Google AI Studio API key with Veo 3 access (Paid Tier required)

### Setup

```bash
# 1. Clone the repo
git clone https://github.com/priyanka-pandya/MatchMood-AI.git
cd MatchMood-AI

# 2. Install dependencies
npm install

# 3. Add your API key
# Create a .env file in the root:
echo "API_KEY=your_google_api_key_here" > .env

# 4. Start the dev server
npm run dev
```

App runs at `http://localhost:5173`

> ⚠️ Veo 3 video generation requires the Google AI Paid Tier. Free tier will return an error.

---

## 🔑 Environment Variables

| Variable | Description |
|----------|-------------|
| `API_KEY` | Your Google AI Studio API key |

> Never commit your `.env` file. It is listed in `.gitignore`.

---

## 🔮 Future Scope

- Add mood-based video filtering (match the IPL hackathon theme)
- Support multiple video aspect ratios (9:16 for Reels/Shorts)
- User accounts to save and share generated videos
- Deploy to Vercel / Netlify with server-side API key handling

---

## 👩‍💻 Author

**Priyanka Pandya**
M.Sc. Data Science, Marwadi University
[LinkedIn](https://linkedin.com/in/priyanka--pandya )

---

*First-author researcher with a paper under review at Springer LNCS — CNN-Transformer hybrid models for industrial fault diagnosis.*
    
