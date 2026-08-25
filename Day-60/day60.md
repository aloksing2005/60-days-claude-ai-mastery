# Day 60 — RoundsAI Capstone Graduation

## Challenge
AB Talks 60-Day Claude AI Challenge

## Final Project
RoundsAI — AI-powered doctor workflow platform

## Live Application
https://roundsai-tau.vercel.app

## GitHub Repository
https://github.com/aloksing2005/roundsai

## Release
v1.0.0

## What I Built

RoundsAI is a doctor-focused workflow platform built end-to-end from requirements to production deployment.

Core capabilities:

- JWT-based doctor authentication
- Patient management
- Manual appointment queue
- Claude-powered pre-visit summaries
- Deterministic AI fallback for reliability
- Digital prescriptions
- Branded PDF prescription export
- Responsive dark/glassmorphism UI
- Production security hardening

## Technology

- React
- Vite
- Tailwind CSS
- Node.js
- Express
- MongoDB Atlas
- Claude API
- pdf-lib
- Vercel
- Render

## Engineering Highlights

### AI Reliability
The Claude integration includes a deterministic fallback. During testing, the Anthropic API returned an actual insufficient-credit error, and the fallback successfully produced a usable summary instead of allowing the application to fail.

### Security
The application was hardened against:

- NoSQL injection
- Excessive login attempts
- Missing security headers
- Oversized requests
- Unhandled server errors

During final release review, a JWT stored in localStorage was identified and removed so the production frontend returned to the intended HTTP-only cookie authentication model.

### Production Verification
The final application was tested directly against the live production deployment with a 23-point end-to-end walkthrough.

## Final Result

RoundsAI reached a production-ready v1.0.0 release after a focused 10-day build sprint inside the broader AB Talks 60-Day Claude AI Challenge.

This project demonstrates not only AI integration and full-stack development, but also scope management, debugging, security review, reliability engineering, and production deployment.

## Final Milestone

**60 days of learning → 10 days of focused building → 1 production application.**

**RoundsAI v1.0.0 — Complete.**
