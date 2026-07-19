# arise
ARISE Life OS tracker app
# ARISE: Life Operating System Documentation

**ARISE** is a comprehensive, self-hosted Progressive Web Application (PWA) designed to act as a complete Life Operating System. Built entirely on client-side technologies, it ensures 100% data privacy by storing all user data locally on the device while offering the fluid experience of a native application.

The core philosophy of ARISE is based on balancing and optimizing the **7 Pillars of Life**: Health, Knowledge, Career, Wealth, Relationship, Spirituality, and Lifestyle.

---

## 🛠 System Architecture & Tech Stack

ARISE is designed to be lightweight, lightning-fast, and entirely offline-capable.

* **Frontend Interface:** HTML5, Tailwind CSS (for responsive, modern styling), and Lucide Icons.
* **Application Logic:** Vanilla JavaScript (ES6+) structured as a dynamic Single Page Application (SPA).
* **Data Persistence:** Browser `localStorage` for high-speed retrieval of tasks, goals, achievements, and settings.
* **Privacy-First:** No external databases, telemetry, or server-side processing. The user retains absolute control over their data matrix.

---

## 🧭 Core Navigation & Modules

The application is divided into four primary workspaces, accessible via the bottom navigation bar.

### 1. Today (Daily Execution Hub)

The Today tab is the active dashboard for daily execution and mindfulness. It dynamically aggregates data based on the currently selected date in the global header.

* **Morning Check-in:** A mood-tracking module where users select an emoji representing their current state and log a brief morning note.
* **Dynamic Agenda:** Automatically calculates and displays tasks scheduled for the day based on their recurrence rules (e.g., Daily, Custom Days, Weekly).
* **Task Actions:** One-tap completion of tasks, which instantly updates global streak and completion statistics. Tasks linked to long-term goals display their parent goal as context.

### 2. Growth (System Configuration)

The Growth tab is the structural engine of ARISE. It displays the 7 Pillars as interactive blocks showing active task counts. Tapping a pillar opens a sliding bottom-sheet modal to configure three distinct layers:

* **Goals:** Long-term objectives serving as the north star for the pillar.
* **Tasks & Routines:** Actionable items with an advanced recurrence engine. Frequencies include *Once, Daily, Weekly, Bi-weekly, Monthly,* and *Custom* (specific days of the week). Tasks can be optionally tethered to a Goal.
* **Achievements:** Gamified milestones. Can be set as **Manual Unlock** (checked off when a one-time feat is accomplished) or **Streak/Milestone** (automatically unlocks when a specific task is completed a set number of times).

### 3. Progress (Analytics & Alignment)

The Progress tab provides a high-level analytical view of system-wide balance.

* **Alignment Matrix (Septagon Radar Chart):** A dynamic, 7-axis radar chart powered by the HTML5 Canvas API. It calculates an alignment score based on task consistency, goal completion, and unlocked achievements. The chart features a radial shaded gradient and solid vertex nodes that adapt to the user's current theme.
* **Completion Ratios:** Linear progress bars breaking down the specific completion percentage of each individual pillar.

### 4. Journal (Digital Diary)

A distraction-free, full-screen digital diary designed for long-form reflection, brainstorming, and daily journaling.

* **Date-Specific Entries:** Entries are tied to the globally selected date. Users can navigate back in time via the header to read or edit past entries.
* **Auto-Saving:** Text is safely stored in local memory, persisting across sessions.
* **Clean Interface:** Focuses purely on typography and whitespace to encourage uninterrupted writing.

---

## ⚙️ Global Controls & Data Management

The persistent top header serves as the control center for the application.

* **Global Date Picker:** A centralized calendar input that acts as a time machine. Changing the date instantly updates the Today agenda, Header Stats, and Journal to reflect that specific day in history.
* **Streak & Stat Tracking:** Real-time counters showing the user's active day streak (consecutive days with at least one task completed) and the ratio of tasks completed today.
* **Theme Engine:** A seamless toggle to switch the entire application interface between Light Mode and Dark Mode.
* **Profile & Data Management:**
* **Export:** Downloads the entire ARISE data matrix as a `.json` backup file.
* **Import:** Restores the application state from a previously exported `.json` file.
* **Factory Reset:** A safeguard option to completely wipe the browser's local storage and start fresh.
