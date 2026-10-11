# TaskWave

A simple to-do list web app that lives entirely in your browser — add tasks, check them off or delete them, and see a fresh motivational quote every few seconds.

## What it does

- **Add tasks** through a popup form (fields for task name, timing, and date)
- **Mark done or delete** — each task card has a ✓ button and a ✕ button
- **Saves your tasks** in the browser's localStorage, so they survive page reloads
- **Motivational quote banner** — fetches a random quote from dummyjson.com with a typewriter animation, refreshes automatically, and falls back to a built-in quote if you're offline
- **Empty-state typing animation** — "Your Task's is Shown Here" types itself out when you have no tasks
- **Dark mode toggle** — the lightbulb icon in the nav switches the page background color
- **Floating "+" button** opens and closes the add-task panel; pressing Enter also adds a task
- **Mobile-friendly layout** — responsive styling kicks in on smaller screens

## Tech stack

- Plain HTML, CSS, and JavaScript — no frameworks, no build step, no package manager
- Font Awesome 6.4.0 icons (via CDN) and the Poppins font (via Google Fonts)
- `localStorage` for task persistence
- Quote source: `https://dummyjson.com/quotes/random` (fetch with a built-in fallback)

## Project structure

```
TaskWave/
├── index.html   # page structure: nav bar, add-task panel, task list, motivation banner
├── style.css    # all styling, including the dark-mode transition and mobile breakpoints
└── script.js    # task add/delete logic, localStorage save/load, quote fetch, typewriter animations
```

## Run it locally

No build step and no dependencies to install — just open `index.html` in a browser, or serve the folder with `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Notes

- The timing and date inputs in the Add Task form are not wired up yet — only the task name is saved and displayed.
- Tasks are stored per-browser in `localStorage` under the key `k`, so clearing site data clears your list.
