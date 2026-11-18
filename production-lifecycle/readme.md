# 📁 `/production-lifecycle` — README

## What this folder is

This folder is your **permanent reference system** for building, shipping, and running any application you create — from a side project to a real product with paying users.

It answers one question: **"What do I need to think about and do before, during, and after I build an app so it survives in production?"**

It is not a tutorial. It is a **working document**. You update it as you learn. Every new app you build starts by copying this folder, then filling in the placeholders for that specific app.

## The seven phases

Every app you build will move through these phases. They are not a straight line — after Phase 6 you go back to Phase 0 for the next iteration. But for planning purposes, you treat each phase as a gate: **you do not enter Phase 1 until Phase 0 is done for that app.**

| Phase | Name | Core Question | Primary Output |
|---|---|---|---|
| **0** | **Foundation & Design** | *What are we building, for whom, and how will it run?* | Foundation Document (this is the most important phase) |
| **1** | **Development & Instrumentation** | *Can we build it while measuring everything?* | Working app with events, logs, metrics, traces |
| **2** | **Build & Test** | *Is the artifact safe and verified?* | Immutable, tested artifact in staging |
| **3** | **Release & Deploy** | *Can we ship without breaking users?* | Safe production release with rollback |
| **4** | **Operate** | *Is it running, and do we know when it's not?* | Monitoring, alerts, runbooks, backups |
| **5** | **Observe & Analyze** | *What are users actually doing?* | Dashboards, funnels, retention reports |
| **6** | **Maintain & Improve** | *How do we make it better and cheaper?* | Postmortems, upgrades, A/B tests, cost reviews |
| **7** | **Retire / Decommission** | *How do we shut it down safely?* | Migration plan, data archive, infrastructure removal |

## How to use this folder

**For each new app:**

1. Create a new folder: `/apps/<app-name>/`
2. Copy the **template files** from `/templates/` into that folder.
3. Fill in **Phase 0** completely before writing any production code.
4. Move to Phase 1 only when Phase 0 has no unanswered placeholders.
5. After launch, revisit Phase 0 monthly. Foundations drift.

**Folder structure:**

```
/production-lifecycle/
├── README.md                    ← you are here
├── /templates/
│   ├── phase-0-foundation.md    ← the master template
│   ├── phase-1-development.md
│   ├── phase-2-build-test.md
│   ├── phase-3-release-deploy.md
│   ├── phase-4-operate.md
│   ├── phase-5-observe-analyze.md
│   ├── phase-6-maintain-improve.md
│   └── phase-7-retire.md
├── /apps/
│   └── /habitloop/              ← example app
│       ├── phase-0-foundation.md
│       ├── phase-1-development.md
│       └── ...
└── /reference/
    ├── checklists/              ← extracted checklists
    ├── tools/                   ← tool comparisons
    └── glossary.md              ← terms you keep forgetting
```


---
