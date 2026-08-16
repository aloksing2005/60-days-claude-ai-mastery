# Day 51 — Product Discovery & Sprint Planning

## 🚀 Project: RoundsAI

**Challenge:** AB Talks 60-Day Claude AI Challenge  
**Day:** 51  
**Track:** Capstone Project — Day 1 of 10  
**Project Type:** AI-powered Doctor Healthcare Workflow Platform

---

## 📌 Project Overview

RoundsAI is a doctor-focused AI healthcare workflow platform designed to help doctors quickly understand patient history and manage essential clinical workflows from a single workspace.

The core differentiating feature is an AI-powered pre-visit patient summary. The system uses the Claude API to analyze available fictional patient records such as previous visits, diagnoses, medications, and allergies and produces a concise summary of important information that a doctor should know before a consultation.

The AI-generated information is clearly separated from verified patient records and is designed as decision-support rather than an autonomous diagnostic or treatment system.

---

## 🎯 Problem

Doctors may need to review multiple pieces of patient information before a consultation, including:

- Previous visits
- Diagnoses
- Medications
- Allergies
- Medical history
- Previous prescriptions

Manually reviewing all this information can take time and may make it difficult to quickly identify the most relevant information before a consultation.

RoundsAI aims to provide a focused doctor workspace where important patient information can be reviewed quickly.

---

## 💡 Solution

RoundsAI provides doctors with:

- A secure doctor login
- Patient management
- Patient medical history
- Appointment queue
- Real-time queue updates
- AI-generated pre-visit patient summaries
- Visit and diagnosis recording
- Digital prescriptions
- Downloadable/printable prescription PDFs

---

## 👨‍⚕️ Primary User

### Doctor

The entire v1.0 experience is designed around a single user role: the doctor.

Patient and hospital administrator interfaces are intentionally excluded from v1.0 to prevent scope creep and allow the doctor workflow to be developed deeply and professionally.

---

# ⭐ Core V1.0 Features

## 1. Doctor Authentication

A simple authentication system using pre-seeded demo doctor accounts.

### Included

- Doctor login
- Protected dashboard
- Logout
- Pre-seeded demo credentials

### Excluded

- Doctor registration
- Email verification
- Password reset
- Social login
- Multi-factor authentication

---

## 2. Doctor Dashboard

The dashboard provides a focused overview of the doctor's daily workflow.

It will include:

- Today's appointment queue
- Queue status
- Patient information
- Quick access to patient records
- AI summary access
- Consultation actions

---

## 3. Patient Management

Doctors can manage basic patient records.

### Patient information

- Name
- Age
- Gender
- Contact information
- Allergies
- Medical history

Doctors can also:

- Add patients
- View patients
- Update patient information
- View patient history

---

## 4. Live Appointment Queue

The doctor can view the current appointment queue.

Queue states:

```text
WAITING
   ↓
IN PROGRESS
   ↓
COMPLETED
