# RoundsAI — Day 5 Summary

**Capstone Project — Day 5 of 10**

## Objective

Build the live appointment queue for RoundsAI.

Day 5 focused on connecting the existing Visit data in MongoDB to a real dashboard queue where the doctor can see today's patients and move visits through their workflow.

---

# 1. Visit API Routes

Created:

`server/routes/visits.js`

Implemented two protected endpoints:

```text
GET   /api/visits/today
PATCH /api/visits/:id/status
