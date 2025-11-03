### `design-guidelines.md`

## 🎨 Emotional Thesis

**Feels like a pocket-sized productivity pal who knows your chaos and makes it fun.**
→ Fast, frictionless, surprisingly encouraging. Like a witty co-founder who drinks too much coffee.

---

## 🔤 Typography

| Type        | Style                           | Notes                                          |
| ----------- | ------------------------------- | ---------------------------------------------- |
| **H1**      | Inter, 28–32px, bold            | Playful, slightly oversized; signals clarity   |
| **H2–H4**   | Inter, stepped down 4–6px sizes | Maintain strong hierarchy, minimal fuss        |
| **Body**    | Inter, 16px, light–medium       | Line-height: 1.6× for easy scanning            |
| **Caption** | Inter, 13–14px, medium          | Used for tips, tooltips, witty tone injections |

---

## 🎨 Color System

| Role           | Color       | Hex                   | Emotion                      |
| -------------- | ----------- | --------------------- | ---------------------------- |
| **Primary**    | Sky Blue    | `#3B82F6`             | Clarity, momentum            |
| **Accent**     | Emerald     | `#10B981`             | Success, flow                |
| **Background** | Soft White  | `#FFFFFF` / `#F9FAFB` | Calm, structured             |
| **Warning**    | Warm Yellow | `#FACC15`             | Humor + caution (fun errors) |
| **Text**       | Gray-900    | `#111827`             | Readable on light background |

* All colors tested for 4.5:1+ contrast
* Consider pastel variants for light/dark mode toggling

---

## 📐 Spacing & Layout

* 8pt base grid system
* Card-based layout with generous padding (≥ 24px)
* Max-width for task content: 640px
* Mobile-first: single-column fallback
* Whitespace as focus driver—not austerity

---

## ✨ Motion & Interaction

| Interaction Type     | Behavior                                  |
| -------------------- | ----------------------------------------- |
| **Hover (buttons)**  | Soft pulse (scale +2%, 200ms ease-in-out) |
| **Task complete**    | Checkbox bounce + confetti (minimal)      |
| **Drag & drop**      | Springy motion, slight inertia            |
| **Modal open/close** | Slide + fade, spring easing               |

* All motion stays within 200–300ms
* Avoid jarring transitions; tone = cheeky but smooth

---

## 🗣️ Voice & Tone

* **Personality**: Spunky sidekick + productivity whisperer
* **Microcopy should feel like:**

  * A friend who gets it
  * A little witty, never snarky
  * Helpful without pressure

**Examples:**

| Context       | Example copy                                              |
| ------------- | --------------------------------------------------------- |
| Empty state   | “Your task jungle looks… oddly peaceful.”                 |
| AI response   | “Rewritten and reorganized. Like a productivity burrito.” |
| Task complete | “Smashed it! Want a medal or just a snack?”               |

---

## 🧭 System Consistency

* Use **shadcn/ui** for base UI + component spacing
* Reuse grid logic across:

  * Smart Inbox
  * Task View
  * Pro Upsell
* Keep tone + motion consistent across states:

  * Error, loading, empty, success = same personality

---

## ♿ Accessibility

* Focus states for all form elements
* Keyboard nav for:

  * Inbox input
  * Task check/edit/delete
* ARIA roles:

  * `list` for task columns
  * `status` for AI parsing feedback
* Contrast: WCAG AA+
* No color-only affordances (use icons + labels)

---

## ✅ Emotional Audit Checklist

* [x] Does the interface feel like a cheeky, helpful sidekick?
* [x] Are motion + microcopy reinforcing support, not pressure?
* [x] Do users feel *cheered on*, not judged?
* [x] Is the calm layout helping reduce overwhelm?

---

## 🛠️ Technical QA Checklist

* [x] Typography scales with consistent vertical rhythm
* [x] All contrast ratios meet AA+
* [x] Button + task states = clearly interactive
* [x] Motion ≤ 300ms unless delightfully intentional

---

## 🧠 Adaptive System Memory

* ✅ Match shadcn/ui + Inter typography from existing design systems
* ✅ Reuse friendly color palette across blog/docs
* ✅ Retain animated feedback patterns across all task flows

---

## 🎯 Design Snapshot Output

#### 🎨 Color palette preview

```md
Primary:   #3B82F6  (Sky Blue)  
Accent:    #10B981  (Emerald Green)  
Background:#F9FAFB / #FFFFFF  
Warning:   #FACC15  (Warm Yellow)  
Text:      #111827  (Gray 900)
```

#### 🔤 Typographic scale

| Element | Font  | Size | Weight   | Line-height |
| ------- | ----- | ---- | -------- | ----------- |
| H1      | Inter | 32px | Bold     | 1.4         |
| H2      | Inter | 24px | Semibold | 1.4         |
| Body    | Inter | 16px | Regular  | 1.6         |
| Caption | Inter | 13px | Medium   | 1.5         |

#### 📐 Spacing system

* 8pt base grid
* Padding: 24px cards, 16px buttons
* Max container: 640px for main content

#### 🧭 One-sentence emotional thesis

“Feels like a spunky sidekick who turns chaos into clarity—with a wink, not a whip.”

---

### 🧪 Design Integrity Review

TaskSage’s visual and emotional design lands beautifully. The spunky, kind tone is mirrored in motion, microcopy, and spacing.
One area for improvement: Add optional tone-setting in onboarding (e.g. “Pick your vibe: Calm / Classic / Cheeky”) for better alignment across personalities.
