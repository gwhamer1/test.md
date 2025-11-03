### `implementation-plan.md`

## 🧱 Step-by-step build sequence

### 🔹 Phase 1 — MVP (core + delight)

1. **Set up project infrastructure**

   * Scaffold Next.js 14 app
   * Install Tailwind CSS + shadcn/ui
   * Connect Supabase project (auth + DB)

2. **Build auth + onboarding**

   * Email/password login
   * Simple onboarding: user enters 3 tasks → auto sorted
   * Save user session in Supabase

3. **Smart Inbox**

   * Single input for task dump
   * GPT prompt: split into subtasks → rewrite → auto-tag as Today / Week / Later
   * Return structured JSON → store in DB

4. **Organized Task View**

   * 3-column layout with drag & drop
   * Mark complete → soft bounce + confetti burst
   * Edit/delete inline
   * Live updates from DB (Supabase Realtime)

5. **Task complete interaction**

   * Animate: springy checkbox, confetti, snappy feedback ("Boom. Nailed it.")

6. **Playful microcopy system**

   * Microcopy tags (e.g., taskComplete, emptyState, nudge)
   * Store copy variations for testing tone

---

### 🔸 Phase 2 — Pro Plan + AI Coach

7. **Pro feature gating**

   * Add Stripe (or Paddle) for monthly billing
   * Add feature flags for Pro users

8. **Calendar sync**

   * Integrate Google Calendar API
   * Sync task deadlines to/from calendar

9. **Recurring tasks**

   * Extend data model: recurrence pattern, next_due_date
   * Auto-generate next instance after completion

10. **Priority coaching (AI)**

    * GPT prompt: suggest top 3 tasks for the day
    * Add “What should I do next?” button

---

### 🔸 Phase 3 — Polish + Optional Extras

11. **Add Google OAuth login**

12. **Notion integration**

    * Sync blog/docs with public Notion pages

13. **Mobile UX tweaks**

    * Simplify gestures, single-column fallback
    * Sticky input bar for Inbox

14. **Dark mode + accessibility audit**

    * WCAG AA+ contrast
    * Keyboard nav for task actions
    * ARIA roles on all interactive elements

15. **Final polish**

    * Add loading skeletons
    * Add gentle empty states
    * Test error states with humor + kindness

---

## 🗓️ Timeline with checkpoints

| Week | Milestone                                |
| ---- | ---------------------------------------- |
| 1    | Project scaffolding + Supabase auth      |
| 2    | Smart Inbox working w/ AI parsing        |
| 3    | Organized Task View (drag & drop)        |
| 4    | Microcopy system + task complete delight |
| 5    | Pro plan billing + feature gating        |
| 6    | Calendar sync + priority coaching        |
| 7    | Recurring tasks + dark mode              |
| 8    | Mobile tweaks + Notion sync              |
| 9    | Final polish + bug fixes                 |
| 10   | Soft launch + feedback loop              |

---

## 👥 Team roles & rituals

### Roles

* **Founder/PM**: Vision, tone, roadmap
* **Frontend Dev**: UI + interactions (Next.js + Tailwind)
* **Backend Dev**: Supabase, API, auth, billing
* **AI/Prompt Engineer**: GPT task parsing + nudges
* **UX Writer**: Microcopy, onboarding, upsells

### Rituals

* **Mon weekly check-in**: Demos + roadmap review
* **Fri async share**: “One delight we added”
* **Bi-weekly user tests**: 3 testers x 30 mins → log top 3 moments of confusion/delight

---

## 🎯 Optional integrations & stretch goals

* iOS/Android wrapper (Expo or Capacitor)
* Task export (Markdown / Notion / PDF)
* Daily summary email with mood-based tone
* Browser extension: save tabs as tasks
* “Focus mode” with ambient sounds & timer

