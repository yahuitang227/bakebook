# Bakebook

A personal baking recipe notebook (PWA). Free to host, works offline, installs to your iPhone Home Screen. The interface is English; recipe content keeps each author's original language and wording.

## Deploy to GitHub Pages (one time, about 3 minutes)

1. Create a free GitHub account and a new **public** repository, e.g. `bakebook`.
2. Upload all files in this folder (on github.com: Add file, then Upload files. No command line needed).
3. In the repository: Settings, Pages, Source: Deploy from a branch, Branch: main, folder: root, Save.
4. After about a minute the app is live at `https://<your-username>.github.io/bakebook/`.

## Install on iPhone

Open the URL in Safari, tap Share, then Add to Home Screen. It launches full screen like an app and works offline.

## Where your data lives

- The two seed recipes live in `recipes-data.js` (public, inside the repo).
- Recipes you add and all bake log entries live only on your device (browser storage). They are private and never uploaded.
- Device storage can be cleared, so use Backup, Download backup regularly. Restoring the file on another device (for example your laptop) is also how you sync between devices for now.

## Photos

Recipe JSON can carry photo links from the source site (`photos.cover_url`, `steps[].photo_url`, `photos.doneness[]`). The app tries to load them, but many sites block images requested from another domain, and links break over time.

For photos that matter, especially doneness shots, open the recipe and tap **Add photo** on the header or any step to save an image from your device. Saved photos are compressed to 1200 px, stored on your device, take priority over the original link, and are included in the backup file. The Backup page shows how much photo storage you are using.

## Adding recipes

1. In the app: Add, then open the AI conversion prompt and copy it.
2. Paste the prompt plus the recipe page text (or MarkItDown or downsub output for PDFs and videos) to your choice of AI agent.
3. Paste the returned JSON into Add, then Import.

To make a recipe permanent across devices, you can also paste its JSON as a new entry inside `recipes-data.js` using GitHub's web editor (add a comma after the previous recipe's closing brace).

## Credits

Pan conversion uses the area ratio method from [Bakevert](https://www.bakevert.com/), a free tool by two Taiwanese creators. Temperature and time guidance follows their [adjustment guide](https://www.bakevert.com/blog/adjusting-baking-time-temperature-guide).
# bakebook
