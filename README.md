# EarthNest Eco Store

EarthNest is a Node.js eco-store application with a customer storefront, login/registration, and an admin portal.

## Deploy

This repository includes a Render Blueprint in `render.yaml`. In Render, create a new Blueprint and connect this repository:

https://dashboard.render.com/blueprints

The Blueprint configures the Node web service and a persistent disk for the store database. Set `ADMIN_EMAIL` to your own email during setup. Render generates `ADMIN_PASSWORD` securely; find it in the service's Environment settings and use it for the first admin login.

## Important

- Do not upload `db.json`, customer records, payment details, API keys, or passwords to GitHub.
- The live database is stored on Render's persistent disk, not in this public repository.
- Change/keep your admin password private. Never share it with customers.
- SMS OTP requires a private `FAST2SMS_API_KEY` environment variable; it is optional.
- The app uses Node.js 18 or newer.

## Main files

- `server.js` — application server and API
- `package.json` — Node start command
- `EarthNest-GitHub-Upload (1).zip` — application source bundle (contains the `public/` storefront, login and admin pages)
- `render.yaml` — hosting configuration
- `.gitignore` — excludes local database, secrets and dependencies
