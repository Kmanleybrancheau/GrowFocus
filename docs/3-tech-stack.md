# Tech Stack & Hosting Strategy

## Defined Tech Stack

| Tool | Purpose |
| :--- | :--- |
| `React` (with Vite) | Builds the interactive front-end: session setup screen, timer, and study material view. |
| `JavaScript Browser APIs` | The **Page Visibility API**, `window` focus/blur events, and the **Fullscreen API** detect when the student leaves the app (Tab Checking). |
| `Tailwind CSS` | Styles the layout quickly and keeps the interface clean and distraction-free. |
| `localStorage` | Stores the student's pasted study material and session settings in their own browser. No account or server is needed for the MVP. |
| `GitHub` | Version control and project documentation. |

**Planned for later versions (not in the MVP):** MediaPipe or TensorFlow.js for in-browser camera detection, and a small backend or Firebase for saving quiz statistics.

## Hosting & Deployment Strategy

GrowFocus will be hosted as a static site on **Vercel** (or **GitHub Pages**), deployed automatically from the `main` branch of the GitHub repository. Every merge to `main` updates the live site, so students can open it from any modern browser with nothing to install. Since the MVP stores data in the browser and has no backend, hosting is free.
