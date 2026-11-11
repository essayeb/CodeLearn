# CodeLearn — Interactive Programming Learning Platform

**Author:** Rayen Essayeb  
**Year:** 2026  
**Project type:** Front-end educational web application

##  Concept

CodeLearn is a responsive learning interface designed to help beginners explore programming fundamentals through structured learning paths, concise lessons, coding practice, and a browser-based playground. It is a portfolio project demonstrating front-end development, UI design, state management, and interactive JavaScript.

##  Features

- Personalized dashboard with lesson, exercise, and progress statistics.
- Five learning paths: HTML & CSS, JavaScript, Python, SQL, and Algorithms & Problem Solving.
- Structured lessons with explanations, code examples, course outline, and completion tracking.
- Course search, category filters, and favorites.
- Practice challenges with difficulty levels, hints, example solutions, and local completion tracking.
- HTML/CSS/JavaScript playground with editable tabs, Run, Reset, and sandboxed iframe preview.
- Progress profile and JSON export.
- Local progress persistence through `localStorage`.
- Responsive dark interface with mobile navigation.
- Clear “under development” modal for account/backend-dependent features.

##  Technologies

- HTML5 for semantic structure.
- CSS3 for responsive layout, design system, and transitions.
- Vanilla JavaScript (ES6+) for navigation, rendering, events, exercises, and state.
- Browser `localStorage` for persistence.
- Sandboxed `iframe` with `srcdoc` for the coding preview.
- Google Fonts (Manrope and DM Mono) loaded from Google Fonts; system fonts remain as fallbacks.

No framework, package manager, backend, or database is required.

##  Project architecture

```text
CodeLearn/
├── index.html    # Application structure and page containers
├── style.css     # Theme, components, responsive rules
├── script.js     # Course data, navigation, interactions, local state
└── README.md     # Documentation
```

### State model

The application stores a compact object under the `codelearn_rayen_v1` localStorage key:

- `completed`: completed lesson identifiers.
- `exercises`: completed exercise identifiers.
- `favorites`: favorite course identifiers.
- `quizBest`: reserved best-score field for future quiz expansion.
- `activity`: recent local activity entries.

The data is browser/device-specific. Clearing browser site data or using another browser/device will not transfer this progress. The current release does not implement accounts, authentication, cloud synchronization, or a global leaderboard.

##  Run and validate the playground

Open **Playground**, edit the HTML, CSS, or JavaScript tab, then select **Run code**. The output is rendered in a sandboxed iframe. Reset restores the initial sample. The preview is intended for learning snippets, not for hosting untrusted production code.

##  Limitations and future improvements

Potential next iterations:

- Add dedicated multiple-choice quizzes with per-topic feedback and saved scores.
- Replace example-solution review with in-page code submission and automated test cases.
- Add more lessons, projects, and guided tracks.
- Add accessibility audits, richer keyboard navigation, and localization (French/English).
- Add a backend API, secure authentication, database-backed progress, and cross-device sync.
- Add instructor/admin tools and a global leaderboard only after server-side validation is implemented.
- Add automated unit and browser tests.

##  Academic and portfolio note

CodeLearn is a front-end prototype created to demonstrate web development skills and product thinking. Backend-dependent controls intentionally show an under-development notice. No real user accounts or online services are represented as operational.
