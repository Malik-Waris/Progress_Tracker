# 🎯 Goal Command — Personal Progress Tracker

A standalone, offline-friendly HTML app for tracking personal goals with priority levels, time management, task logging, and daily quotas. No installation required — just open the file in Chrome.

---

## 🚀 Getting Started

1. **Download** `goal-command.html`
2. **Double-click** the file — it opens directly in Chrome (or any modern browser)
3. That's it. No internet connection, no installs, no accounts needed.

> Your data is saved automatically in your browser's local storage, so your goals persist between sessions.

---

## 📋 Features

### Goal Cards
Each goal is displayed as a card containing:

| Field | Description |
|---|---|
| **Goal Name** | What you're working towards |
| **Priority** | High / Medium / Low — colour-coded |
| **Time Pitched** | Days already elapsed on this goal |
| **Time Given** | Total days allocated to complete it |
| **Days Remaining** | Automatically calculated (Time Given − Time Pitched) |
| **Tasks Done / Total** | How many tasks you've completed out of the total |
| **Today's Quota** | How many tasks you need to complete today |
| **Progress %** | Visual bar showing completion percentage |

### Status Badges
Each card automatically displays a status badge based on time elapsed vs. tasks completed:

| Badge | Meaning |
|---|---|
| 🟢 **ON TRACK** | Less than 60% of time used — you're fine |
| 🟡 **WATCH** | 60–85% of time used — start pushing harder |
| 🔴 **AT RISK** | Over 85% of time used — needs urgent attention |
| ✅ **COMPLETE** | All tasks logged — goal achieved |

### Progress Bar
The horizontal bar on each card has two layers:
- **Coloured fill** — your task completion progress
- **White marker line** — where you are in your time window, so you can visually see if your progress is ahead or behind your deadline

### Today's Quota Pips
Small square indicators show your daily target. Each pip fills in as you log tasks. A **QUOTA MET ✓** badge appears when you hit your daily goal.

---

## ✏️ Adding & Editing Goals

Click **+ ADD GOAL** in the top-right to open the form. Fill in:

- **Goal Name** — e.g. "Read 30 books"
- **Time Pitched** — how many days have already passed since you started
- **Time Given** — the total number of days you've set aside for this goal
- **Total Tasks** — the total number of units/tasks to complete (e.g. 30 books, 100 lessons)
- **Daily Quota** — how many tasks you aim to do each day
- **Priority** — High, Medium, or Low
- **Accent Colour** — pick a colour to visually distinguish your goals

To edit an existing goal, click the **EDIT** button on its card.

---

## 📊 Dashboard Overview

At the top of the page:

- **OVERALL %** — average completion across all your goals
- **QUOTA MET** — how many goals have had their daily quota met today
- **MASTER PROGRESS BAR** — a single gradient bar representing your combined progress

---

## 🔘 Buttons & Controls

| Button | What it does |
|---|---|
| **+ LOG TASK** | Adds one completed task to the goal (increments both total and today's count) |
| **UNDO** | Removes the last logged task |
| **EDIT** | Opens the goal form pre-filled with the goal's current data |
| **✕** | Deletes the goal (asks for confirmation first) |
| **↺ RESET DAY** | Resets today's quota count to 0 for all goals — use this each morning |

### Sorting
Use the **SORT BY** buttons to reorder your goal cards:
- **PRIORITY** — High priority goals appear first
- **PROGRESS** — Most-completed goals appear first
- **DEADLINE** — Goals with the least time given appear first

---

## 💾 Data & Storage

- All goal data is saved to your browser's **localStorage** automatically
- Data persists across page refreshes and browser restarts
- Data is stored **locally on your machine only** — nothing is sent anywhere
- To clear all data, open Chrome DevTools → Application → Local Storage → delete the `gc_goals` key

---

## 🖥️ Compatibility

| Browser | Support |
|---|---|
| Chrome | ✅ Fully supported |
| Edge | ✅ Fully supported |
| Firefox | ✅ Fully supported |
| Safari | ✅ Fully supported |

Works entirely offline after first load (fonts load from Google Fonts on first open).

---

## 📁 File Structure

This app is a **single HTML file** — everything is self-contained:

```
goal-command.html
├── Styles (CSS)
├── React 18 (loaded from CDN on first open)
├── Babel (for JSX transpilation)
└── App logic (JavaScript/JSX)
```

No build tools, no Node.js, no dependencies to install.

---

*Built with React 18 · Styled with custom CSS · Fonts: Bebas Neue + Courier Prime*
