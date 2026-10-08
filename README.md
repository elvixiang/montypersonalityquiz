# Which Monty Are You? · MONTY&Co.

7-question quiz → one of 6 Monty types → an Instagram-Story result card (1080×1920) to save and share.
Static site: no backend, no login, no API keys.

## Folder structure

```
monty-quiz/
├── index.html        ← the whole quiz
├── README.md
└── assets/
    ├── monty.png     ← Monty (transparent PNG), used on the "question" screen
    └── moods/        ← one Monty expression per quiz type
        ├── hot.png  blush.png  angry.png
        └── excited.png  sleepy.png  overthink.png
```

## Things to edit (top of the script in index.html)

- `CONFIG.photoBoothUrl` → Photo with Monty link (set to https://montyphotobooth.vercel.app/).
- `CONFIG.quizLabel` → text in the card footer (empty = this website's address).
- `TYPES.<type>.menu` / `why` → drink recommendation + one-line reason per type ('' hides it).
- `TYPES.<type>.img` → the expression PNG for that type. To swap one, replace the file in `assets/moods/`
  with the same name (transparent PNG, ~400 px is enough).
- `QUESTIONS` → questions and answers; each answer points to a type
  (hot, blush, angry, excited, sleepy, overthink).

## Deploy: GitHub → Vercel

1. github.com → New repository (e.g. `monty-quiz`) → upload `index.html`, `README.md` and the `assets` folder → Commit.
2. vercel.com → Add New… → Project → Import the repo → Framework Preset: **Other** → Deploy.
3. Share the `https://….vercel.app` link (bio link, QR at the outlet, Story link sticker).

## Notes

- iPhone: "Simpan ke galeri" opens the share sheet → choose "Save Image" (or press & hold the card).
- Android: the card downloads to the gallery/Downloads.
- "Tantang teman" opens the phone's share menu with the quiz link (copies the link if sharing isn't available).
