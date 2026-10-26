# Vidya Saathi

**Vidya Saathi** is a beginner-friendly prototype of a Socratic study tutor for students in Classes 6–8, paired with a simple teacher dashboard showing example concept gaps.

> **Current status:** This repository contains a standalone HTML/CSS/JavaScript demonstration. It uses predefined questions, hint sequences, answer-matching rules, and in-memory dashboard counts. It is not yet connected to a live AI model, WhatsApp, a backend, or a persistent database.

## Features in the current prototype

- Student-style chat interface with Math, Science, and Social Studies questions.
- Predefined hints and explanations for each subject.
- Basic recognition of a few anticipated misconceptions.
- Teacher dashboard with sample concept-gap counts.
- In-session dashboard count updates for recognized misconceptions.
- Responsive layout and light/dark styling based on the browser preference.

## Requirements

- A modern browser such as Chrome, Firefox, Edge, or Safari.
- No package manager, API key, server, or paid service is required for the current demo.

## Setup and run locally

1. Download or clone this repository.
2. Open `index.html` in your browser.

That is enough to run the current standalone prototype. If your browser restricts local files, use any simple local static-file server; no server-side code is included.

## Environment variables

**None are required.** The current prototype has no external API integrations and does not read environment variables. Do not add API keys to `index.html`. If a backend or AI provider is added later, keep secrets in server-side environment variables and document them separately.

## Repository layout

```text
vidya-saathi/
├── index.html
├── README.md
├── LICENSE
├── .gitignore
├── docs/
│   └── TECHNICAL_DESIGN.md
├── data/
│   └── sample_student_learning_data.csv
└── tests/
    └── TEST_CASES.md
```

## Sample data

`data/sample_student_learning_data.csv` contains fictional, non-identifiable example records for documentation and test planning. The current HTML demo does not load this CSV; its dashboard counts are hard-coded in the JavaScript `gaps` object and are adjusted only in browser memory during a session.

## Tests

See [`tests/TEST_CASES.md`](tests/TEST_CASES.md) for manual test cases and expected results. They are documented test cases, **not a claim that an automated test suite has been run**.

## Limitations

- The tutoring logic is rule-based, not generative AI.
- Only three predefined questions are included.
- Answer checking uses simple string/regular-expression matching and may not understand equivalent wording.
- Recognized concept gaps are a small set of hard-coded patterns.
- Dashboard counts are demonstration values and are not real class analytics.
- State is not saved after reloading the page.
- There is no actual WhatsApp integration, student account system, teacher login, backend, or database.
- The UI labels the idea as a WhatsApp tutor, but this HTML file itself does not send or receive WhatsApp messages.

## Roadmap ideas

- Add a backend API and persistent database with appropriate privacy protections.
- Add teacher authentication and access controls.
- Connect a real messaging channel only after implementing and testing its integration.
- Improve answer evaluation and misconception mapping with a clearly documented approach.
- Add accessibility checks and automated browser tests.
- Use consent, data minimization, and safeguarding practices appropriate for school-age learners.

## License

This project is released under the MIT License. See [`LICENSE`](LICENSE). Replace the copyright placeholder with the appropriate owner before publishing.
