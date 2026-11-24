# Mikael OS

**A Local-First Personal Organization System**

Mikael OS is a personal organization web application designed to centralize different aspects of everyday life in a single, integrated environment. Built from scratch using **HTML5, CSS3, and Vanilla JavaScript (ES6+)**, it combines productivity, financial management, study tracking, personal goals, and note-taking without relying on external frameworks or dependencies.

The application follows a **local-first architecture**, prioritizing data ownership, privacy, and independence from external servers.

---

## Features

### 📊 Dashboard
A centralized overview of daily and monthly activity, providing quick access to essential information.

- Daily and monthly productivity summaries.
- Routine completion metrics.
- Financial balance overview.
- Total study time tracking.
- Weekly activity chart.
- Quick actions for frequently used features.

### 🔄 Routines & Habits
A flexible system for organizing recurring activities and monitoring personal consistency.

- Activity tracking by category.
- Multiple recurrence options: Once, Daily, Weekdays, Weekly, Biweekly, Monthly, and Annual.
- Progress bars based on selected periods.
- Retroactive activity editing.
- Monthly reports exported to Excel (.xlsx).

### 💰 Finance
A personal financial management module for tracking income, expenses, and monthly financial performance.

- Income and expense registration.
- Custom and predefined categories.
- Reference-month organization.
- Automatic balance calculation.
- Archived monthly financial closings.
- Excel (.xlsx) exports with multiple worksheets:
  - Summary
  - Transactions
  - Expenses by Category

### 📚 Studies
A study management system designed to track learning activities, academic progress, and time invested in each subject.

- Subject creation and management.
- Configurable study frequency and target minutes.
- Manual study session registration.
- Automatic session logging through Pomodoro integration.
- Permanent study session history.
- Study time breakdown by subject.
- Monthly statistics exported to Excel (.xlsx).

### 📝 Notes
A structured writing environment for organizing information, ideas, and personal knowledge.

- Notebooks and individual pages.
- Instant search functionality.
- Automatic saving.
- Trash system with page restoration.
- JSON backup and restore.
- Consolidated Markdown (.md) export for use with AI assistants.

### 🎯 Goals
A goal management module designed to organize objectives across different time horizons.

- Short-term goals.
- Medium-term goals.
- Long-term goals.
- Mandatory deadlines.
- Status management: Active, Completed, and Missed.
- Filtering by goal status.

### ⏱️ Pomodoro
A customizable focus timer integrated with the study management system.

- Pomodoro, Short Break, and Long Break modes.
- Configurable focus and break durations.
- Customizable study cycles.
- Pop-out timer window.
- Subject linking.
- XP and level progression based on focused minutes.
- 12-month activity heatmap.
- CSV activity export.

---

## Tech Stack & Architecture

Mikael OS was developed using native web technologies, without frameworks, libraries, or external dependencies.

| Technology | Purpose |
|---|---|
| HTML5 | Semantic structure and application layout |
| CSS3 | Responsive interface, Grid, Flexbox, and CSS variables |
| Vanilla JavaScript (ES6+) | Application logic, state management, and interactions |
| localStorage | Local data persistence |
| OOXML | Native Excel file generation |
| Blob API | Client-side file exports |

### Architecture Highlights

**Single-File Architecture**

The application runs independently from a single `index.html` file, containing the necessary HTML, CSS, and JavaScript.

**Local-First Persistence**

All application data is stored locally in the browser using `localStorage`, without requiring a backend or external database.

**Data Integrity & Migrations**

The persistence layer includes state normalization and versioned data migrations to maintain compatibility and preserve historical records as the application evolves.

**Native File Generation**

File exports are implemented directly in JavaScript, without third-party libraries.

Supported formats:
- `.xlsx` — Excel spreadsheets generated through OOXML, `Uint8Array`, and CRC32 calculation.
- `.csv` — Structured data exports.
- `.json` — Complete application backup and restoration.
- `.md` — Consolidated notes and context exports.

---

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Edge, Firefox, or Safari).
- No installation, backend, or additional dependencies required.

### Installation

Clone the repository:

```bash
git clone https://github.com/MicaelMoras/MicaelOs.git
```

Navigate to the project directory:

```bash
cd MikaelOs
```

Open `index.html` directly in your browser.

Alternatively, you can download the repository and open the HTML file manually.

### GitHub Pages Deployment

Mikael OS can also be hosted for free using GitHub Pages.

1. Open the repository on GitHub.
2. Navigate to **Settings → Pages**.
3. Under **Build and deployment**, select the `main` branch.
4. Choose the root directory (`/`).
5. Save your configuration.

GitHub Pages will publish the application.

---

## Backup & Privacy

Mikael OS was designed with local data ownership in mind.

- All information remains stored in the browser's `localStorage`.
- No external database or backend server is required.
- Users can export a complete `.json` backup.
- Previously exported backups can be imported to restore application data.

**Important:** Since data is stored locally in the browser, clearing browser storage or changing devices may result in data loss. Regular backups are recommended.

---

## Project Philosophy

Mikael OS was created with the idea of bringing multiple personal management tools together into one cohesive system.

Instead of relying on several disconnected applications, the project provides a unified environment for managing finances, routines, studies, notes, goals, and productivity.

The development also explores how far native web technologies can go when building a complete application without external frameworks or dependencies.

---

## Author

**Micael Morás**

- GitHub: [@MicaelMoras](https://github.com/MicaelMoras)
- Repository: [Mikael OS](https://github.com/MicaelMoras/MicaelOs)

---

<p align="center">
  Built with HTML, CSS, and Vanilla JavaScript.
</p>
