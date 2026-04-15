# Tradepath

Tradepath acquires and operates vocational schools across America. We build the technology that runs the enrollment pipeline — from the moment a prospective student lands on a school's website to the day they start class.

---

## What we're building

Most vocational schools run on outdated websites, manual intake forms, and enrollment coordinators who spend their days answering the same questions by phone. We're replacing that with a modern, automated pipeline that works 24/7.

The pipeline has four stages:

```
1. School website          → Student discovers programs, reads pricing, decides to inquire
2. AI enrollment advisor   → Student asks questions, gets matched to a program, books a seat
3. CRM (Rally)             → School team manages leads, cohorts, and pre-start communications
4. Pre-start comms         → Automated emails and reminders keep students engaged until day one
```

The goal: a student who finds us at midnight on a Sunday can ask every question, find out if they qualify for financial aid, and reserve a seat — without talking to anyone. A coordinator follows up the next morning with a warm lead who has already self-qualified.

---

## The school portfolio

Each school in the Tradepath portfolio gets its own website cloned from the master template. The code never changes between schools — only the branding, programs, and content differ.

| School | Domain | Status |
|---|---|---|
| Mountain View Vocational Institute (MVVI) | mymvvi.com | Staging — pre-launch |

*Additional schools added as acquired.*

---

## Repositories

### In this organization

| Repo | What it does |
|---|---|
| [mvvi-website](https://github.com/tradepath-hq/mvvi-website) | MVVI public marketing site. Also the master template for every future school. Built on Next.js, hosted on Railway. Includes the enrollment flyout that embeds the AI advisor. |
| [advisor](https://github.com/tradepath-hq/advisor) | The AI enrollment advisor — chat and voice. Students talk to Alex 24/7, get matched to programs, qualify for funding, and book cohorts. Powered by Claude (Anthropic) for chat and Vapi for phone calls. |

### Outside this organization

| Repo | What it does | Why it's separate |
|---|---|---|
| [porig212/Rally](https://github.com/porig212/Rally) | Multi-tenant CRM. Manages organizations, programs, cohorts, leads, and enrollments across all schools in the portfolio. Handles pre-start communications. | Rally predates Tradepath and serves multiple clients. Tradepath is one tenant. |

---

## How the pieces connect

```
Student visits mymvvi.com
        │
        ▼
Clicks "Enroll Now" → AI advisor flyout opens (embedded iframe)
        │
        ▼
advisor app (tradepath-hq/advisor)
  — Claude answers questions
  — Vapi handles phone calls
  — Collects name, email, phone
        │
        ▼
Rally CRM (porig212/Rally)
  — Lead created via Advisor API
  — Cohort booking recorded
  — Pre-start email sequence triggered
        │
        ▼
Coordinator follow-up → Student starts class
```

---

## Principles

**Own the pipeline.** School websites on Lovable or Wix can't be integrated, can't be optimized, and can't be scaled. We build and own every part of the stack.

**One codebase, many schools.** A bug fix or new feature in the master template can be deployed to every school. Adding a new school is a configuration change, not a rebuild.

**AI-first enrollment.** The advisor handles 80% of prospective student questions. Coordinators spend their time on students who are ready to enroll, not answering "how long is the CDL program?"

**Automate the obvious.** Reminder emails before the first day of class, cohort confirmations, financial aid follow-ups — these don't need a human. They just need a system.
