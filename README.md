# Souup's Mineral Tracker

A browser-based mineral tracking tool for EVE Online players. Track your mineral stockpiles, monitor trends over time, and sync directly with your EVE character's assets via EVE SSO.

🔗 **Live app:** https://souup68.github.io/Edict-Supply-Network/

---

## Features

- **EVE SSO Login** — Connect your EVE character to auto-sync mineral quantities directly from your in-game assets
- **Minerals by Location** — See exactly which station or player structure each mineral is held in
- **Auto Snapshot** — A dated snapshot is saved automatically every time assets are refreshed
- **Jita Prices** — Fetch live Jita buy/split/sell prices with one click
- **Current Totals** — At-a-glance mineral quantities with ISK values on the Stock tab
- **Snapshot History** — Accumulating snapshots power the Trends charts
- **Trend Charts** — Visualise mineral quantities and portfolio ISK value across snapshots
- **Reprocessing Calculator** — Paste ore, auto-fetches live prices, and shows mineral output with buy / split / sell ISK totals
- **Corporation Requests** — Track outstanding mineral requests from corp members
- **Discord Export** — Copy current stock levels formatted for Discord
- **Backup & Restore** — Export/import all your data as JSON

---

## Getting Started

### Connect with EVE SSO
1. Click **Connect with EVE SSO** on the Stock tab
2. Log in with your EVE Online account and authorise access
3. Your mineral quantities will auto-populate from your character's assets, grouped by station and structure
4. A snapshot is saved automatically on each successful import
5. Hit **Refresh Assets** anytime to sync the latest quantities

> Your login persists across browser sessions — you only need to sign in once.

> **Note:** Player structure names (Athanors, Fortizars, etc.) require the `esi-universe.read_structures.v1` scope to be enabled on the registered EVE developer application and the app to be accessed from its registered callback URL (`https://souup68.github.io/Edict-Supply-Network/`).

---

## Reprocessing Calculator

1. Go to the **Reprocess** tab
2. Select your station type from the colour-coded preset dropdown, or type an efficiency value manually (e.g. `0.7231`)
3. Paste compressed ore or moon ore rows from your EVE assets window
4. Click **⚗️ Calculate Reprocess** — Jita prices are fetched automatically and the output shows mineral quantities with **Buy**, **Split**, and **Sell** ISK totals

**Preset colour key:**
| Colour | Structure |
|---|---|
| ⬜ White | NPC Station |
| 🟦 Blue | Athanor — T1 Rig |
| 🟪 Purple | Athanor — T2 Rig |
| 🟨 Yellow | Tatara — T1 Rig |
| 🟠 Orange | Tatara — T2 Rig |

**Efficiency presets (max skills + Beancounter RP-804 implant):**
| Station / Space | Ore Eff. |
|---|---|
| NPC Station (any space) | 0.7236 |
| Athanor T1 — Highsec | 0.7528 |
| Athanor T1 — Lowsec | 0.7980 |
| Athanor T1 — Nullsec / WH | 0.8432 |
| Athanor T2 — Highsec | 0.7823 |
| Athanor T2 — Lowsec | 0.8293 |
| Athanor T2 — Nullsec / WH | 0.8762 |
| Tatara T1 — Highsec | 0.7786 |
| Tatara T1 — Lowsec | 0.8254 |
| Tatara T1 — Nullsec / WH | 0.8721 |
| Tatara T2 — Highsec | 0.8092 |
| Tatara T2 — Lowsec | 0.8578 |
| Tatara T2 — Nullsec / WH | 0.9063 |

> Presets assume max skills + RP-804 implant. If your skills aren't maxed or you lack the implant, enter your value manually — e.g. 75% efficiency = `0.7500`. Works for ore and moon ore.

---

## Saving & Backup

- Snapshots are saved **automatically** every time assets are refreshed via EVE SSO
- A **💾 Save Snapshot** button is available on the Stock tab for manual saves if needed
- Snapshots accumulate and power the Trends charts
- Use **Export JSON** in the Data tab to back up all your data to a file
- When signing out, you'll be prompted to export first so you don't lose your history

---

## Privacy

- No data is sent to any external server (other than EVE's own ESI API for asset sync and Fuzzwork for Jita prices)
- All snapshot and request data is stored locally in your browser's `localStorage`
- EVE SSO uses PKCE OAuth2 — your credentials never touch this app
