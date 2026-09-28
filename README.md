# Atreya Bag | Portfolio

An immersive, single-page portfolio: a scroll-driven 3D journey through a data pipeline,
with a playable validation-gate game and sound synthesised live in the browser.

No build step and no backend. It's one static file: `index.html`.

## Deploy (GitHub + Vercel)

1. Create a new **public** repository on GitHub, e.g. `portfolio`.
2. Upload `index.html` and `README.md` (GitHub: **Add file → Upload files → Commit changes**).
3. Go to vercel.com, sign in with GitHub, click **Add New → Project**, and import the repo.
4. Framework preset: **Other**. Leave build command and output directory empty. Click **Deploy**.
5. Your site is live at `https://<project-name>.vercel.app`.
   Optional: rename the project in Vercel settings to get `atreyabag.vercel.app`,
   or connect a custom domain under **Settings → Domains**.

Every time you push a change to GitHub, Vercel redeploys automatically.

## Editing content

All text lives in the `CONTENT` object near the top of the main `<script>` in `index.html`:
chapters, certifications, tech stack and links. Nothing else needs changing.

## Adding side projects later

In `CONTENT`:

```js
showSideProjects: true,
sideProjects: [
  { title: "Project name", summary: "One or two lines on what it does.",
    stack: ["Next.js", "NestJS"], link: "https://github.com/AtreyaBag/..." }
]
```

They appear in the final section under "Beyond the pipeline".

## Notes

- Visitors choose "Enter with sound" or "Enter quietly"; press **M** or use the button to toggle sound.
- "Summary view" shows everything as a normal page (also the automatic fallback without WebGL).
- Phones get a lighter scene and compact cards with a "Show details" toggle.
- Respects the "reduce motion" accessibility setting.
