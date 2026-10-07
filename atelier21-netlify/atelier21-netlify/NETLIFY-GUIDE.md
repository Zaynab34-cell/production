# Publish ATELIER 21 on Netlify

This is the ready-to-publish version of the V2 app. No backend, API key, npm installation or build command is required.

## From your computer — easiest method

1. Download `atelier21-netlify.zip` and unzip it.
2. Find the `atelier21-netlify` folder. `index.html` must be directly inside that folder, alongside `blocs/` and this guide.
3. Sign into your Netlify account, then open https://app.netlify.com/drop.
4. Drag the **atelier21-netlify folder** into the Drop zone. Upload the folder that directly contains `index.html`, not its parent folder.
5. Once publishing finishes, Netlify shows a URL ending in `.netlify.app`. Open that URL on your phone.

Netlify's official folder-upload and live-URL workflow: [3](https://docs.netlify.com/start/choose-your-path/).

If you already have a manually deployed Netlify project, open its **Deploys** page and drop the updated folder into its deploy dropzone. Keep using the same project URL when updating: [1](https://docs.netlify.com/deploy/create-deploys/).

## What is included

- `index.html`: the complete dashboard, with all 21 blocks, 252 questions and tools embedded.
- `blocs/`: 21 optional standalone learning sheets.
- `netlify.toml`: optional configuration if you later connect a Git repository; publish directory is the root `.`. No build command is needed for these finished files.

Do not upload the development/source project by accident. This deployment folder contains only the finished pages and these deployment instructions.

## On your phone

Open your published URL in a modern browser. You can bookmark it, or use **Add to Home Screen** if your browser offers that option. This creates a convenient shortcut; this package does not include a service worker or promise offline reloads as a PWA. Internet is needed to reliably open/reload the hosted site.

Your laptop does not serve this app after upload: the ready-made HTML pages are hosted on Netlify. You do not need to run a local development server.

## Progress and privacy

- The learning site itself is public to anyone with its URL; the app does not add a login/password system.
- Progress, notes and sessions stay in each browser's local storage. This app does not send them to a server.
- Progress is **not automatically synced** between your computer and phone.
- To transfer it, use **Progression → Exporter** on the first device, send the JSON backup privately to the other device, then use **Progression → Importer** there.
- Import replaces that device's current app state after confirmation. Export it first if needed.
- **Never put private JSON backups into this deploy folder**, since uploaded files may become publicly accessible.
- Clearing browser storage or using a different browser/domain can show a fresh profile. Keep a private export backup.

## If Netlify shows a 404 at the homepage

Confirm you dropped the folder whose first level contains `index.html`. Do not drop an outer folder that contains another nested application folder. No SPA redirect file is needed for the dashboard: its internal navigation uses URL hashes such as `/#bloc/b03`.
