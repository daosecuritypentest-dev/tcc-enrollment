# TCCI Junior High School Portal System

Static, single-page school portal (enrollment form, student portal, teacher advisory records, principal master list). Everything runs client-side; data is stored in each browser's `localStorage`.

## Run locally

Open `index.html` in a browser — that's it.

## Demo accounts

- Student: `juandelacruz@gmail.com` or `anareyes@gmail.com` — password `password123`
- Teacher: any full name + grade level (password is set on first login)
- Principal: any full name (password is set on first login)

## Deploy on Render

This repo includes a `render.yaml` Blueprint:

1. Push this repo to GitHub/GitLab/Bitbucket.
2. In the Render Dashboard: **New → Blueprint**, pick the repo (or **New → Static Site** and set Publish Directory to `.`).
3. Done — live at `https://<service-name>.onrender.com` with free HTTPS.

## Notes

- No build step is required; Render serves the files as-is from the repo root.
- Because data lives in `localStorage`, records are per-browser/device: a teacher on one device won't see a student who enrolled from another device. Adding a shared backend (e.g., Render web service + Postgres) is a separate step if needed.
