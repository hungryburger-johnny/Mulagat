# Mulagat 🌤️

A voice AI assistant that teaches everyday skincare routines with a focus on **skin cancer prevention**. Built with Agora's Conversational AI Engine for the AWS Student Community Day Mega Manila 2026 Workshop.

## What Mulagat Does

Mulagat is a friendly voice coach that helps users:
- Build a proper daily skincare routine (cleansing, SPF, moisturizing)
- Understand sun safety habits that reduce skin cancer risk
- Learn the ABCDE rule for spotting suspicious moles (Asymmetry, Border, Color, Diameter, Evolving)
- Get personalized advice based on their skin type, lifestyle, and climate

Mulagat is educational, not diagnostic — it always encourages seeing a dermatologist for any concerning skin changes.

## Tech Stack

- **Framework:** Next.js (TypeScript)
- **Voice AI:** Agora Conversational AI Engine (Agents SDK)
- **Speech-to-Text:** Deepgram (nova-3)
- **LLM:** OpenAI (gpt-4o-mini)
- **Text-to-Speech:** MiniMax

## How It Works

The app runs a real-time voice pipeline: your speech is transcribed (STT), sent to an LLM guided by Mulagat's custom persona, and spoken back to you (TTS) — all orchestrated through Agora's real-time network with sub-500ms latency.

The persona and behavior are defined in [`app/api/invite-agent/route.ts`](./app/api/invite-agent/route.ts).

## Getting Started

### Prerequisites
- Node.js and npm
- An [Agora account](https://console.agora.io) (free tier available)
- Agora CLI installed

### Setup

```bash
git clone https://github.com/hungryburger-johnny/Mulagat.git
cd Mulagat
npm install
agora project env write server/.env.local
npm install agora-agents
npm run dev
```

Open [http://localhost:3000](http://localhost:3000), start a session, and talk to Mulagat.

## Demo

*(Add your demo video/screenshots here)*

## Built For

AWS Student Community Day Mega Manila 2026 Workshop — Agora Agents SDK

## Disclaimer

Mulagat provides general skincare education only and is not a substitute for professional medical advice. Always consult a dermatologist for concerns about your skin.