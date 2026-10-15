# SkillBridge AI — Personalized Career Roadmap Generator

**VORTEX 2K26 | Theme: Future of Education & Employability**

SkillBridge AI helps students turn a career goal into small, practical learning tasks. A student chooses a target role, current skill level, weekly study hours, and roadmap duration. The app generates a paced plan with skill milestones, task checklists, a portfolio project, and a downloadable text version.

## Problem statement
Students often have access to learning material but struggle to decide what to learn first, how to break goals into manageable actions, and how to turn learning into portfolio evidence. Generic roadmaps rarely account for a student's current level or limited weekly time.

## Proposed solution
SkillBridge AI personalizes a roadmap around a chosen role and the student's time budget. The built-in explainable recommendation engine works without a server, login, or paid service. An optional Gemini API mode can generate more tailored content when the user supplies their own API key in the browser. The API key is not stored in localStorage or included in the project files. Task completion is saved locally in the browser; users can export their plan.

## Features
- Five starter tracks: Frontend Developer, Data Analyst, AI/ML Engineer, Cybersecurity Analyst, and UI/UX Designer.
- Beginner/intermediate options and 2–20 available study hours per week.
- Two-, four-, six-, or eight-week roadmap.
- Week-by-week tasks, estimated time, portfolio project, progress percentage, and checklist.
- Downloadable plain-text roadmap with resource links.
- Optional Gemini API integration; fallback mode works if the API is unavailable.
- Responsive layout for desktop and mobile; local browser storage for progress.

## Technology
- HTML5
- CSS3 (responsive layout)
- Vanilla JavaScript
- `localStorage` for local progress persistence
- Optional Google Gemini API (`gemini-2.5-flash`) for generative plan enhancement
- GitHub Pages-compatible static deployment

## Run locally
1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Generate a plan, switch weeks, complete tasks, and download your plan.

No package installation or backend is required for the built-in mode.

## Deploy with GitHub Pages
1. Create a **public** repository on GitHub, e.g. `skillbridge-ai`.
2. Upload `index.html`, `README.md`, and `SUBMISSION.md` to the repository root (do not upload only the ZIP).
3. Open **Settings → Pages**.
4. Under the build/deployment settings, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Wait for GitHub Pages to publish. Use the generated `https://YOUR-USERNAME.github.io/skillbridge-ai/` URL as the demo link and test it in a private/incognito window.

GitHub Pages publication can take several minutes. If the URL is not live immediately, keep the source repository link ready and check the Pages deployment status.

## Optional Gemini mode
1. Create a Gemini API key from Google AI Studio.
2. Run the website and expand **Optional: enhance with Gemini AI**.
3. Paste the key and generate a roadmap.

The key is kept only in the input field during the current page session and is not written to localStorage. Do not use the feature on a shared computer. The core demo does not require this key; API availability, quotas, network access, and model responses are outside the local app's control.

## Limitations and future work
- Built-in recommendations are curated rules/templates rather than a trained model; Gemini mode is optional.
- The roadmap is a planning aid and cannot guarantee employment or replace mentorship.
- Future versions could add validated learning-resource metadata, user accounts, evidence-based skill assessments, multilingual guidance, accessibility testing, and mentor feedback.

## Evaluation demo flow
1. Select **Data Analyst**, beginner, 5 hours/week, 4 weeks.
2. Generate the plan and browse week tabs.
3. Mark a task complete and show the progress indicator.
4. Download the plan.
5. Optionally demonstrate AI enhancement if an API key is available.
