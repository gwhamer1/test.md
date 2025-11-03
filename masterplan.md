### `masterplan.md`

## 🚀 30-second elevator pitch

**TaskSage** is your smart, cheerful productivity sidekick.
Dump your messy to-dos, and it auto-sorts, rewrites, and cheers you on.
Fast, minimal, and a little bit witty—finally, a task app that feels like a teammate.

---

## 🎯 Problem & mission

**Problem:** Most to-do apps help you *log* chaos, not tame it. They’re rigid, joyless, and ignore emotional friction.
**Mission:** Make task management feel light, kind, and energizing—using AI to convert mental clutter into clear action.

---

## 🎯 Target audience

* Productivity power-users (Reddit threads, Notion nerds)
* University students juggling classes + life
* Indie hackers and startup founders with 99 things to do and 0 systems

---

## 🧩 Core features

* **Smart Inbox**:
  One input for brain dumps → AI sorts & rewrites into Today, Week, Later
* **Organized Task View**:
  3-column layout with drag & drop + cheerful complete interactions
* **AI Nudges**:
  Friendly suggestions like “Might wanna prep snacks for this one”
* **Pro Upgrade ($4.99)**:
  Calendar sync, recurring tasks, and “priority coaching”
* **Auth & Onboarding**:
  Fast sign-up, enter 3 tasks, see AI magic instantly
* **Playful Microcopy**:
  Delightful tone everywhere from errors to empty states

---

## ⚙️ High-level tech stack

| Layer        | Tech                              | Why it fits                                                             |
| ------------ | --------------------------------- | ----------------------------------------------------------------------- |
| **Frontend** | Next.js 14 + Tailwind + shadcn/ui | Fast, flexible, highly customizable—great for sharp UI with personality |
| **Backend**  | Supabase                          | Instant auth + DB + edge functions = fast iteration                     |
| **Auth**     | Email + Google OAuth              | Low-friction and familiar                                               |
| **AI**       | OpenAI GPT (e.g. GPT-4o)          | Handles parsing, rewriting, nudges—your sidekick brain                  |
| **CMS**      | Notion (optional)                 | Easy blog/docs management, fits productivity-nerd persona               |

---

## 🧠 Conceptual data model (ERD in words)

* **User**

  * id, name, email, auth method
* **Task**

  * id, user_id, text_original, text_rewritten, category (Today / Week / Later), status, priority, created_at
* **Nudge**

  * id, task_id, message, type (reminder, suggestion), delivered_at
* **Subscription**

  * user_id, plan (free/pro), start_date, renewal_date

---

## 🎨 UI design principles (Krug + Kindness)

* **Don’t make me think**: One inbox. Everything flows from there.
* **Delight over duty**: Every checkmark feels rewarding.
* **Whitespace = calm**: Minimal layout with breathing room.
* **Microcopy = empathy**: Voice that supports, never scolds.
* **Motion = kindness**: Smooth transitions, never jarring.

---

## 🔐 Security & compliance notes

* Secure auth via Supabase
* All task data scoped to user ID
* AI prompts anonymized; no long-term storage
* Compliant with GDPR best practices (opt-out + delete user data)
* Stripe or Paddle for safe payments

---

## 🛣️ Phased roadmap

**MVP**

* Smart inbox + task view
* Basic AI parsing + rewrite
* Email auth
* Delightful task complete interactions

**V1**

* Pro plan: calendar sync, recurring tasks, priority coaching
* Google login
* Nudge engine + reminders
* Mobile web polish

**V2**

* Notion sync
* iOS/Android native wrapper
* Team shared tasks
* Time-block planning

---

## ⚠️ Risks & mitigations

| Risk                                  | Mitigation                                           |
| ------------------------------------- | ---------------------------------------------------- |
| AI misfires on parsing                | Let user preview/edit rewrites before sorting        |
| Tone mismatch (humor can fall flat)   | A/B test microcopy with opt-in “voice level” setting |
| Feature creep from productivity nerds | Stick to MVP scope; roadmap = user votes             |
| Supabase rate limits for free users   | Monitor + scale with paid tier if needed             |

---

## 🔮 Future expansion ideas

* Personal productivity insights: “You complete most tasks at night”
* Mood-based task themes (focus mode, playful mode)
* Shared lists + collaborative nudges
* Wearable integrations (“You’re near the store—buy snacks?”)
* AI-generated weekly review emails
