---
name: emil-ui
description: >-
  All-in-one orchestrator for Emil Kowalski's full UI design engineering and
  animation skill suite. Triggered by /emil-ui or when the user wants to apply
  Emil's complete craft bar (UI polish, library selection, animation,
  choreography, gestures, performance, mobile-native feel, and strict review)
  automatically to a task or session.
---

# Emil UI — Full Suite Orchestrator (`/emil-ui`)

You are operating with **Emil Kowalski's complete UI & Design Engineering skill suite**. Instead of guessing which single skill applies, you orchestrate the right combination of sibling skills in this plugin (`../<skill>/SKILL.md`) end-to-end so the final UI meets the Vercel / Linear craft bar.

## Initial Response

When `/emil-ui` is invoked **without** a specific task, respond concisely:

> Modo `/emil-ui` activado. Aplicaré la suite completa de diseño UI y animaciones de Emil Kowalski en esta sesión. ¿Qué componente, pantalla o mejora vamos a trabajar?

And keep this orchestrator active for the rest of the session until the user asks to disable it.

## Step 1: Detect Scope & Platform

Before writing code, classify the request along two axes:

1. **Platform**
   - **Web (React / Next.js / HTML / CSS)** → default path.
   - **React Native / Expo** → load `../animate-expo/SKILL.md` instead of web animation skills.
   - **Native iOS / Swift** → load `../write-swift/SKILL.md`.
2. **Intent / Mode**
   - **Build or redesign UI** (`/emil-ui <task>`) → run the **Full Build Flow** below.
   - **Polish existing UI** (`/emil-ui polish`) → run craft + motion + mobile + performance pass.
   - **Review changes** (`/emil-ui review`) → read and execute `../review-animations/SKILL.md` (and `../review-animations/STANDARDS.md`) + `../emil-design-eng/SKILL.md` craft checks.
   - **Audit codebase** (`/emil-ui audit`) → read and execute `../improve-animations/SKILL.md` (consulting `../find-animation-opportunities/SKILL.md` and `../remove-animations/SKILL.md`).
   - **Explore variants** (`/emil-ui prototype <idea>`) → read and execute `../prototype/SKILL.md`.
   - **Stress-test UI** (`/emil-ui break`) → read and execute `../break-ui/SKILL.md`.
   - **Save corrections** (`/emil-ui learn`) → read and execute `../learn-taste/SKILL.md`.
   - **Unsure which skill** → read `../ask-emil/SKILL.md`.

## Step 2: Load Only the Relevant Sibling Skills (Progressive Disclosure)

Do **not** read all 20 skills blindly. Read `../emil-design-eng/SKILL.md` as the baseline, then read every sibling skill that matches the task:

| Condition in the task | Read and apply |
| :--- | :--- |
| Always (web UI craft, polish, shadows, borders, hover/press, popovers) | `../emil-design-eng/SKILL.md` |
| Needs a UI primitive or dependency (dialog, dropdown, drawer, toast, command menu, OTP, charts, DnD, virtualization) | `../pick-ui-library/SKILL.md` |
| Uses Sonner toasts | `../ask-sonner/SKILL.md` |
| Adds or edits any web animation or transition | `../animate/SKILL.md` |
| Coordinates 2+ elements moving together (stagger, hero entrance, view swap, layout shift) | `../choreograph/SKILL.md` |
| Involves drag, swipe, fling, bottom sheet, snap points, pull-to-refresh, hold-to-confirm | `../gestures/SKILL.md` |
| Apple-style fluid motion, springs, translucent depth, optical typography, spatial continuity | `../apple-design/SKILL.md` |
| Runs on mobile browsers / PWA / touch devices (100vh, safe areas, tap highlight, sticky hover, input zoom) | `../mobile-native/SKILL.md` |
| Performance concerns, jank, dropped frames, `will-change`, GPU layers, layout thrashing | `../animation-performance/SKILL.md` |
| React Native / Expo animations, gestures, sheets, haptics | `../animate-expo/SKILL.md` |
| Native Swift / SwiftUI / Swift 6 concurrency | `../write-swift/SKILL.md` |
| User asks what a motion effect is called | `../animation-vocabulary/SKILL.md` |

## Step 3: Full Build Flow (Default Execution Order)

When building or polishing a UI feature, execute in this order:

1. **Dependencies first**: Never hand-roll complex primitives (toasts, drawers, popovers, command menus). Check `../pick-ui-library/SKILL.md` first.
2. **Craft & Visual Polish**: Apply `../emil-design-eng/SKILL.md` (semi-transparent borders/shadows over harsh solid borders, tactile press feedback, popover transform-origin, tooltip grouping/timing, restraint).
3. **Motion Decisions**: Apply `../animate/SKILL.md` (and `../choreograph/SKILL.md` / `../gestures/SKILL.md` when applicable):
   - Decide *whether* to animate at all — **no motion** on keyboard shortcuts or high-frequency repeated actions (`../remove-animations/SKILL.md`).
   - Use the right easing (`ease-out` for enter/UI responses, `ease-in-out` for on-screen movement, springs for physical/interruptible gestures) and short durations (150–300ms for UI).
   - Keep dynamic transitions interruptible and respect `prefers-reduced-motion`.
4. **Mobile & Performance Check**:
   - Animate compositor-only properties (`transform`, `opacity`, `clip-path`) per `../animation-performance/SKILL.md`.
   - Apply `../mobile-native/SKILL.md` fixes if the interface is used on phones.
5. **Self-Review Gate**: Before finalizing, mentally verify your diff against `../review-animations/STANDARDS.md`. Fix any HIGH-severity feel-breaking issue before replying.

## Step 4: Handoff & Next Steps

When presenting your work:
- Briefly list which skills from the suite were applied (1 line, e.g. *Aplicado: `emil-design-eng`, `animate`, `mobile-native`*).
- Summarize the key craft/motion decisions made (easings, durations, interruptibility, accessibility).
- If the user built a new screen or made design corrections during the session, optionally offer `/emil-ui break` (worst-case data test) or `/emil-ui learn` (save rules to `DESIGN.md`).
