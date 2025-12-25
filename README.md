# Repwise — Intelligent Workout Tracking (React Native + Expo) 💪🤖

Repwise is a cross-platform mobile app for intelligent, real-time workout tracking and personalized AI guidance. It combines clean mobile UX, fast local state (Zustand), a headless CMS for exercise content (Sanity), secure authentication (Clerk), and AI-powered coaching (OpenAI). Designed to scale from a polished solo project into a production-grade SaaS fitness platform.

---

## 🚀 Quick Overview

- Real-time workout timers, set/rep logging, and unit flexibility (kg / lbs)
- AI guidance during workouts (form tips, suggestions, micro-coaching)
- Headless CMS for rich exercise content, images, and videos
- Secure user accounts with Google OAuth and protected workout history
- Modern, accessible UI using NativeWind (Tailwind CSS for React Native)
- Cross-platform support for iOS and Android via Expo

---

## ✨ Features

- **Live workout sessions**: Stopwatch, rest timers, rounds, sets, and live progress tracking  
- **Smart logging**: Set/rep/weight history, 1RM estimation, progressive overload suggestions  
- **AI coaching**: Context-aware exercise tips and intelligent workout recommendations (OpenAI)  
- **Content-first architecture**: Sanity-powered exercise library with structured schemas  
- **Offline-friendly**: Local caching with background sync when online  
- **Type-safe codebase**: End-to-end TypeScript for maintainability and scale  
- **State management**: Lightweight and efficient stores with Zustand  
- **Authentication & security**: Clerk + Google OAuth with per-user data isolation  
- **Accessibility**: Screen reader support and touch-optimized components  
- **SaaS-ready**: Multitenancy support, analytics hooks, and Stripe-ready billing (planned)

---

## 🧭 Architecture (High-Level)

[Expo App (React Native + TypeScript)]
↕ (fetch / sync)
[API Layer / Serverless Functions] ←→ [OpenAI] (AI guidance)
↕
[Sanity CMS] (exercise content, media)
↕
[Database] (workout history, user metadata)
↕
[Auth: Clerk] (sessions, OAuth, user profiles)


---

## 🛠️ Tech Stack

- **Mobile**: React Native (Expo), TypeScript, NativeWind (Tailwind CSS)
- **State Management**: Zustand
- **CMS**: Sanity (Studio + Headless)
- **Authentication**: Clerk (Google OAuth)
- **AI**: OpenAI (GPT-based coaching)
- **Media**: Sanity asset pipeline (images & videos)
- **CI/CD**: GitHub Actions → Expo EAS (iOS & Android builds)
- **Backend (optional)**: Serverless functions (Vercel / Netlify)
- **Analytics & SaaS**: PostHog / Plausible, Stripe (billing)

---

## ⚙️ Getting Started

```bash
# Clone repository
git clone https://github.com/iamrautela/repwise.git
cd repwise

# Install dependencies
pnpm install
# or npm install / yarn install

# Start Expo dev server
expo start

# Run on emulator or device
expo run:android
expo run:ios

