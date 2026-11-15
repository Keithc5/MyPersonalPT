# MyPersonalPT

A mobile-friendly personal training tracker, built as a lightweight static web app.

**Website:** https://keithc5.github.io/MyPersonalPT/  
**Repository:** https://github.com/Keithc5/MyPersonalPT

## Features

- Paste full free-form workout notes and convert them into a reviewed, editable workout draft before saving
- Log exercises with workout date, session name, sets, reps, weight (kg), RPE and notes
- Group exercises by date and session name
- Dashboard showing workout count, sets and estimated training volume
- Six-week activity chart
- Workout history with exercise filtering and deletion
- 60-, 90- and 120-second rest timer
- Sample weekly strength, cycling and recovery schedule
- JSON backup/restore and CSV export
- Mobile-friendly layout and no account required

The exercise library includes **cross-body kettlebell toe rows**. For this custom movement, one repetition means one full left-and-right-hand sequence.

## Getting started

Open the [live site](https://keithc5.github.io/MyPersonalPT/) or open `index.html` in a modern browser. No build tools, dependencies, API keys or server are required.

To import notes, choose **Log workout**, paste your full notes into **Paste workout notes**, select **Convert notes to workout**, review the parsed exercises and save. Unclear weights are not guessed. You can also log manually: choose **Log workout**, enter the session and exercise details, and save. Add another exercise with the same date and session name to build a full session. Review past entries under **History**.

## Data and privacy

Workout records are saved in the browser's `localStorage` under `mypersonalpt-v1`. **They do not sync across devices or browsers** and are not sent to GitHub. Clearing site data, using private browsing or changing devices can remove access to records. Use **Settings → Export JSON backup** regularly and restore it on another device if needed. CSV export is intended for analysis, not restore.

The dashboard's training volume is an estimate: sets × reps × entered weight. Bodyweight and unilateral exercise volume may require interpretation.

## Deployment

The GitHub Actions workflow at `.github/workflows/pages.yml` publishes the repository root to GitHub Pages when changes land on `main`, and can also be run manually.

In repository **Settings → Pages**, set **Build and deployment → Source** to **GitHub Actions**. Check the **Actions** tab for deployment results. The site should be served at https://keithc5.github.io/MyPersonalPT/.

## Project structure

```text
index.html                   Standalone HTML, CSS and JavaScript application
README.md                    Project documentation
.github/workflows/pages.yml  GitHub Pages deployment workflow
.gitignore                   Common local/editor artifacts
```

## Limitations and next steps

This is an early functional prototype, not a medical or professional training prescription. Planned improvements include editing logged entries, per-set logging, exercise-specific personal records, progression suggestions, richer training plans, accessibility improvements and automated tests. Avoid recording sensitive personal information in notes on shared devices.

## Contributing

Issues and pull requests are welcome. Test changes on mobile and desktop, keep the app usable without external services, and preserve existing locally stored workout data.
