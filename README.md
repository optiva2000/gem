# Gem Travel Agencies

Single-page travel site (sightseeing, car rental with driver, airport transfer).
Destinations, places and photos are read from a Google Drive folder.

## Setup
1. In `index.html`, set `DRIVE_API_KEY` (Google Drive API key).
2. Restrict the key to the Drive API and to the site's domain (HTTP referrer, e.g. `https://USERNAME.github.io/*`).
3. Make sure the Drive folder is shared as "Anyone with the link" (Viewer).

## Deploy (GitHub Pages)
Settings > Pages > Deploy from a branch > `main` / `(root)`.
