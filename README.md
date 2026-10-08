# Which Monty Are You? · MONTY&Co.

7-question quiz → one of 6 Monty types → an Instagram-Story result card (1080×1920) to save and share.
Static site: no backend, no login, no API keys.

## Folder structure

```
monty-quiz/
├── index.html        ← the whole quiz
├── README.md
└── assets/
    └── monty.png     ← Monty (transparent PNG)
```

## Things to edit (top of the script in index.html)

- `CONFIG.photoBoothUrl` → link to the Photo with Monty site to show a "Foto bareng Monty" button.
- `CONFIG.quizLabel` → text in the card footer (empty = this website's address).
- `TYPES.<type>.menu` → drink recommendation per type ('' hides it). Only "Monty Kepanasan" has one now (Lemon Crush).
- `TYPES.<type>.img` → optional: a dedicated Monty expression PNG for that type (e.g. 'assets/monty-sleepy.png').
  When set, that PNG is used instead of the standard Monty + drawn mood props.
- `QUESTIONS` → questions and answers; each answer points to a type
  (hot, blush, angry, excited, sleepy, hungry).

## Deploy: GitHub → Vercel

1. github.com → New repository (e.g. `monty-quiz`) → upload `index.html`, `README.md` and the `assets` folder → Commit.
2. vercel.com → Add New… → Project → Import the repo → Framework Preset: **Other** → Deploy.
3. Share the `https://….vercel.app` link (bio link, QR at the outlet, Story link sticker).

## Notes

- iPhone: "Simpan ke galeri" opens the share sheet → choose "Save Image" (or press & hold the card).
- Android: the card downloads to the gallery/Downloads.
- "Tantang teman" opens the phone's share menu with the quiz link (copies the link if sharing isn't available).
