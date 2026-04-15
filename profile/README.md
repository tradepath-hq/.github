**FOR SCHOOL OWNERS**

# We Acquire and Operate **Vocational Trade Schools.**

TradePath is a Sun Belt platform built to buy, modernize, and grow independent trade schools. We bring capital, a custom-built AI operating system, and 24/7 enrollment infrastructure. So your school reaches its full potential.

[**Talk to Us About Your School**](mailto:owners@tradepath.com) &nbsp;&nbsp; [Learn How It Works](#how-it-works)

---

| **SUN BELT** | **4 LOCATIONS** | **DOD CERTIFIED** | **CAPITAL READY** |
|---|---|---|---|
| TX · NM · AZ · NV · FL · GA · LA · AL · SC · NC | El Paso · Alamogordo · San Antonio · Albuquerque | Active military & government contracts | We close fast, on your timeline |

---

## How It Works

Most vocational schools run on outdated websites, manual intake forms, and coordinators who spend their days answering the same questions by phone. We replace that with an AI-managed enrollment system that operates 24/7 and handles everything that doesn't require human judgment.

The system spans six stages:

```
1. Lead generation        → Inbound + outbound; AI responds in under 60 seconds
2. Funding approval       → AI orchestrates each funding track; staff executes onsite steps
3. Pre-start              → Automated checklist, welcome sequence, Day 1 logistics
4. Course delivery        → AI monitors attendance, flags at-risk students
5. Certification          → Exam scheduling, graduation, placement tracking, compliance reporting
6. Post-grad              → Referrals, reviews, re-enrollment, alumni nurture
```

A student who finds us at midnight on a Sunday can ask every question, find out which funding path they qualify for, and reserve a seat — without talking to anyone. A coordinator follows up the next morning with a warm lead who has already self-qualified.

Today, Stages 1–2 are functional. The rest is being built in sequence.

---

## The School Portfolio

Each school in the TradePath portfolio gets its own website cloned from the master template. The code never changes between schools — only the branding, programs, and content differ.

| School | Domain | Status |
|---|---|---|
| Mountain View Vocational Institute (MVVI) | mymvvi.com | Staging — pre-launch |

*Additional schools added as acquired.*

---

## Repositories

### In this organization

| Repo | What it does |
|---|---|
| [mvvi-website](https://github.com/tradepath-hq/mvvi-website) | MVVI public marketing site and master template for every future school. Built on Next.js, hosted on Railway. Includes the enrollment flyout that embeds the AI advisor. |
| [advisor](https://github.com/tradepath-hq/advisor) | The AI enrollment advisor — chat and voice. Students talk to Alex 24/7, get matched to programs, qualify for funding, and book cohorts. Powered by Claude (Anthropic) for chat and Vapi for phone calls. |

### Outside this organization

| Repo | What it does | Why it's separate |
|---|---|---|
| [porig212/Rally](https://github.com/porig212/Rally) | Multi-tenant CRM. Manages organizations, programs, cohorts, leads, and enrollments across all schools in the portfolio. Handles pre-start communications, coordinator tasks, and compliance data. | Rally predates TradePath and serves multiple clients. TradePath is one tenant. |

---

## How the Pieces Connect Today

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
  — Identifies funding path (VA, TWC, employer, Pell)
  — Collects name, email, phone
  — Books cohort seat
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

As stages 3–6 are built, the flow extends beyond class start — through certification, placement, and alumni re-engagement.

---

## Principles

**Own the pipeline.** School websites on Lovable or Wix can't be integrated, optimized, or scaled. We build and own every part of the stack.

**One codebase, many schools.** A bug fix or new feature in the master template deploys to every school. Adding a new school is a configuration change, not a rebuild.

**AI handles everything it can.** The advisor answers questions, identifies funding paths, schedules appointments, sends reminders, flags at-risk students, and drives post-grad engagement. Coordinators focus on decisions that require human judgment.

**Automate the obvious.** Reminder emails, cohort confirmations, financial aid follow-ups, 90-day placement checks — these don't need a human. They need a system.

**Build for compliance from day one.** TWC and DoD funding programs require outcome reporting. Placement rates, wages, and completion data are tracked on every enrollment record — not retrofitted later.
