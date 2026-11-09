# JAS — AI Workspace

A responsive, installable web app/PWA starter with a Capacitor Android wrapper and a GitHub Actions workflow for a debug APK.

## Run locally
- Install Node.js 20+
- `npm install`
- `npm run dev`
- `npm run build`

## Connect a model
Open **Settings & providers** and enter an OpenAI-compatible Chat Completions endpoint, API key, and model name. The browser stores the key in local storage. This is suitable only for a personal prototype; do not deploy a public multi-user app with client-side secrets. Use a server-side proxy and authentication for production. API calls may incur provider charges.

## Deploy as a website
Build with `npm run build` and deploy the `dist/` directory to any static host. Configure the host for SPA fallback if needed. For GitHub Pages, configure a Pages workflow/hosting path appropriate to the repository subpath.

## Android
The GitHub Actions workflow builds a debug APK on push or manual dispatch. After uploading these files to the repository's `main` branch, open **Actions**, run/inspect **Build Android APK**, and download the `JAS-Android-debug-apk` artifact when successful.

## Current scope
Chat is functional when a compatible endpoint/key/model is configured. Image, voice, and video tools are represented as navigation/workspace entry points and require separate provider/API integrations; this starter does not unlock paid AI services or include those providers automatically.
