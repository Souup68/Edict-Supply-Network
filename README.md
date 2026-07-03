# Souup's Mineral Tracker

A browser-based mineral tracking tool for EVE Online players. Track your mineral stockpiles, monitor trends over time, and sync directly with your EVE character's assets via EVE SSO.

🔗 **Live app:** https://souup68.github.io/Edict-Supply-Network/

---

## Features

- **EVE SSO Login** — Connect your EVE character to auto-sync mineral quantities directly from your in-game assets
- **Manual Entry** — Paste ore/mineral rows from the EVE assets window or type quantities manually
- **Jita Prices** — Fetch live best-buy prices from Jita (The Forge) with one click
- **Snapshot History** — Save dated snapshots to track your stockpile over time
- **Trend Charts** — Visualise mineral quantities and ISK value across snapshots
- **Reprocessing Calculator** — Paste ore and calculate mineral yields at your efficiency %
- **Corporation Requests** — Track outstanding mineral requests from corp members
- **Discord Export** — Copy current stock levels formatted for Discord
- **Backup & Restore** — Export/import all your data as JSON

---

## Getting Started

### Connect with EVE SSO (Recommended)
1. Click **Connect with EVE SSO** on the Stock tab
2. Log in with your EVE Online account and authorise access
3. Your mineral quantities will auto-populate from your character's assets
4. Hit **Refresh Assets** anytime to sync the latest quantities

> Your login persists across browser sessions — you only need to sign in once.

### Manual Entry
1. Open EVE → Assets window
2. Filter by mineral type, select all, copy
3. Paste into the **Paste from EVE Assets** box and click **Import Quantities**

---

## Reprocessing Calculator

1. Go to the **Reprocess** tab
2. Click the **▾** arrow next to *Ore eff.* to select your station type, or type a value manually (decimal format, e.g. `0.7231`)
3. Paste compressed ore or moon ore rows from your EVE assets window
4. Click **Calculate Reprocess** to see the mineral output

**Efficiency presets (max skills + Beancounter RP-804 implant):**
| Station / Space | Ore Eff. |
|---|---|
| NPC Station (any space) | 0.7231 |
| Player Refinery — Highsec (T2 rig) | 0.8249 |
| Player Refinery — Lowsec (T2 rig) | 0.8744 |
| Player Refinery — Nullsec / WH (T2 rig) | 0.9239 |

> Presets assume max skills + RP-804 implant. If your skills aren't maxed or you lack the implant, enter your value manually — e.g. 75% efficiency = `0.7500`. Works for ore and moon ore.

---

## Saving & Backup

- Click **Save Snapshot** to record the current quantities with a timestamp
- Snapshots accumulate and power the Trends chart
- Use **Export JSON** in the Data tab to back up all your data to a file
- When signing out, you'll be prompted to export first so you don't lose your history

---

## Privacy

- No data is sent to any external server (other than EVE's own ESI API for asset sync and Jita prices)
- All snapshot and request data is stored locally in your browser's `localStorage`
- EVE SSO uses PKCE OAuth2 — your credentials never touch this app
