# Day 52 — System Design

## 🚀 Project: RoundsAI

RoundsAI is a doctor-only AI healthcare workflow platform designed to help physicians manage their daily workflow through patient management, appointment queue management, AI-powered pre-visit summaries, and structured digital prescriptions.

---

## 🎯 Day 52 Objective

Today I transformed the approved Day 1 product plan into a complete technical blueprint that can directly guide implementation from Day 3 onward.

The main focus was:

- Finalizing the technology stack
- Designing the system architecture
- Designing the database schema
- Defining the complete API contract
- Designing the UI/user flow
- Defining the project folder structure
- Checking Day 3 implementation readiness

---

## 🛠️ Finalized Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React + Vite + Tailwind CSS |
| Backend | Node.js + Express |
| Database | MongoDB Atlas + Mongoose |
| Authentication | JWT + HTTP-only Cookie |
| AI | Anthropic Claude API |
| PDF Generation | pdf-lib |
| Frontend Hosting | Vercel |
| Backend Hosting | Render |
| Database Hosting | MongoDB Atlas |

### Why these technologies?

The stack was selected because it fits the approved 10-day scope, supports free-tier deployment, and matches technologies I already have experience with.

---

## 🏗️ System Architecture

The application follows a simple client-server architecture:

```text
Doctor
   ↓
React + Vite Frontend
   ↓
Node.js + Express API
   ↓
MongoDB Atlas
   ↓
External Services
   ├── Anthropic Claude API
   └── pdf-lib
