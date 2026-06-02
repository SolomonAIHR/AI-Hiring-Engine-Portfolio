# Tangoe AI Hiring Engine
### AI-Powered Interview & Screening Platform

> Built independently by a Talent Acquisition leader to demonstrate what the future of structured, bias-aware, high-volume screening looks like in practice.

🔗 **Live Demo:** [tangoe-screening.vercel.app](https://tangoe-screening.vercel.app)

---

## What It Does

The Tangoe AI Hiring Engine is a fully functional, end-to-end hiring platform that replaces the manual, inconsistent screening process with an intelligent, JD-matched experience for both candidates and recruiters.

A candidate receives a link. They complete a structured video interview — on their own time, from any device. The system does the rest.

---

## Key Features

### 🎯 JD-Matched Video Interviews
- Questions are dynamically generated from the Job Description
- Each interview is tailored to the role — no generic screening
- Configurable question count, time limits, and focus areas

### 📄 Automated Resume Parsing
- Resumes parsed and scored against the JD automatically
- Structured candidate data available to recruiters instantly

### 🔒 Live Proctoring & Integrity Monitoring
- Tab-switch detection with real-time alerts and audit trail
- External device heuristic to flag suspicious behaviour
- Adaptive camera threshold for fair, environment-aware monitoring
- Focus score (0–100) surfaced per candidate

### 📊 Recruiter Scoring Dashboard
- Real-time dashboard showing all candidates by requisition (TEREQ)
- Search by name, email, or TEREQ number
- TEREQ filter dropdown for bulk requisition management
- Candidate profile card with full interview summary in modal view
- 30-second auto-refresh — live pipeline visibility without page reload

### 📈 Analytics
- TEREQ-level analytics badges showing pipeline health
- Hiring funnel metrics: completion rate, score distribution, proctoring flags

### ⚙️ Admin Controls
- JD library for reusable job configurations
- Multi-recruiter access with role-based permissions
- Bulk CSV export for ATS integration

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Static HTML / Vanilla JavaScript |
| Hosting | Vercel (serverless, zero infra cost) |
| AI Engine | Claude AI (Anthropic) — interview generation, resume parsing, scoring |
| Database | Upstash Redis — candidate results, JD configs, session state |
| Media Storage | Cloudinary — video storage and delivery |
| API Layer | Vercel Serverless Functions |

---

## Architecture

```
Candidate Link
      ↓
interview.html — JD-matched questions served via Claude AI
      ↓
Proctoring layer — tab-switch detection, camera monitoring, focus scoring
      ↓
api/save-result.js — stores response + proctoring data to Upstash Redis
      ↓
dashboard.html — recruiter view, live scoring, TEREQ filters
      ↓
analytics.html — pipeline health, funnel metrics, TEREQ badges
```

---

## Why This Was Built

Standard screening is broken — inconsistent questions, interviewer bias, scheduling bottlenecks, and no data trail. At scale (300–500 hires/year across multiple geographies), these problems compound into missed deadlines and poor hire quality.

This tool was built to solve that — not as a concept, but as a working, deployed platform that runs real interviews and gives recruiters real data to make decisions faster.

---

## What This Demonstrates

- **AI fluency in practice** — not claiming AI knowledge, but applying it to build a production tool
- **TA systems thinking** — understands the full hiring lifecycle from JD intake to recruiter decision
- **Zero-cost deployment mindset** — serverless architecture delivering enterprise-grade functionality at zero infrastructure cost
- **Product thinking from a TA leader** — built by someone who has hired 300–500 people per year and knows exactly what recruiters actually need

---

## Status

✅ Live and deployed  
✅ Active development — next priorities: email notifications, SMS link delivery, interview scheduling, mobile-responsive dashboard

---

## Contact

**Rufus Solomon** — India TA Lead, Tangoe  
solomon.mr@gmail.com  
[linkedin.com/in/rufus-Solomon-ta](https://linkedin.com/in/rufus-Solomon-ta)

> *Source code is maintained in a private repository. This portfolio repo exists to document the project publicly.*
