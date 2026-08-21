# Day 56 — Complete the MVP & AI Pre-Visit Summary

## Project

**RoundsAI — AI co-pilot for your clinic day**

Day 6 focused on completing the AI pre-visit summary feature while keeping the implementation within the approved Day 6 scope.

---

## Day 6 Objective

Build and verify the AI-powered pre-visit summary feature using the Claude API, with a deterministic fallback when the AI service is unavailable.

The application should remain functional even when the Claude API cannot be accessed.

---

## What Was Completed

### 1. Claude AI Summary Backend

Implemented a dedicated AI summary service:

- `server/services/aiSummary.js`
- `server/routes/summary.js`

The backend:

- Builds a structured clinical summarization prompt.
- Sends patient information to Claude when the API is available.
- Restricts the model to summarization rather than diagnosis or treatment recommendations.
- Limits the summary to a concise doctor-readable format.
- Stores the generated summary against the patient's visit.

### 2. Deterministic Fallback

A fallback summary generator was implemented for situations where the Claude API is unavailable.

The fallback uses existing patient and visit data, including:

- Patient demographics
- Reason for visit
- Reported symptoms
- Chronic conditions
- Current medications
- Allergies
- Recent past visits

The fallback was actually tested against a real Anthropic API failure.

The API returned:

> `Your credit balance is too low to access the Anthropic API.`

The application handled the failure gracefully and returned:

```text
source: fallback
