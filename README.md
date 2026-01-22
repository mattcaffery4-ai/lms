
# Last Man Standing (Swimlanes Edition)

Static web app to run a monthly LMS with **swimlanes per round** showing Alive / Pending / Out players. No server required. Data is stored in the browser (localStorage). Host it free on GitHub Pages.

## Files
- `index.html` – landing page with links
- `lms_picks.html` – main app (swimlanes + admin tools)
- `.nojekyll` – disables Jekyll on GitHub Pages

## Publish on GitHub Pages
1. Create a **public** repository (e.g., `lms`)
2. Upload these files to the **repo root**
3. Go to **Settings → Pages** → **Deploy from branch** → `main` / `(root)` → Save
4. Wait ~1 minute, then open `https://<username>.github.io/<repo>/`

## Using swimlanes
- Each **lane** is a **round** (e.g., GW1, GW2). Columns show:
  - **Alive** – players who won (or drew when Draw = Replay)
  - **Pending** – alive players whose result or pick isn’t set yet
  - **Out** – eliminated this round
- **Advance Round** moves the competition forward; if one survivor remains, the month closes and winner is recorded.
- You can run **January and February concurrently** by switching months.
- New entrants are **Round 1** only; subsequent rounds only accept **alive** players.

## Admin notes
- Admin password is client-only and just gates editing (not security). Use Export/Import to share state between devices.
- You can set per-round **labels** (e.g., `GW1 (Jan 3–5)`) and **deadlines**.
- Entry fee is per-month; pot = entrants × fee.

## Back up / move data
- **Export JSON** from the header to backup; import on another device to continue.
- **Export CSV** for the current month to analyse or archive.
