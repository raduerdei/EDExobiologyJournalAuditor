# Elite Dangerous // Exobiology Journal Auditor

A lightweight, zero-dependency, single-file HTML/JavaScript utility that parses local *Elite Dangerous* player journal logs (`Journal.*.log`) to audit completed exobiology scans, verify First Footfall eligibility, and calculate exact Vista Genomics payouts—including the 5x First Footfall multiplier.

Built for deep-space explorers who want an instant, verifiable accounting of what is currently sitting in their genetic sampler without bloated background apps, database rescans, or inaccurate running wallet estimates.

---

## Key Features

* **100% Local & Zero-Dependency:** Runs entirely in your browser from a single `.html` file. No Node.js, Python, backend servers, or external API calls—your journal logs never leave your machine.
* **Multi-Session Chronological Parsing:** Automatically sorts multiple selected `Journal.YYYY-MM-DDTHHMMSS.XX.log` session files in chronological order and maintains system/body state across game launches.
* **Accurate First Footfall (5x) Detection:** Evaluates `Touchdown` and `Disembark` events (`"FirstFootfall": true` vs. `false`) alongside `Scan` discovery flags (`"WasDiscovered": false`) to distinguish untouched worlds (Base + 4x Bonus) from previously claimed planets (1x Base Value), complete with an audit trail label per scan and a manual override toggle.
* **Automatic Vista Genomics Turn-In Resets:** Detects `SellOrganicData` and `Resurrect` events to separate already-cashed-in samples (`SOLD`) from your active, uncashed hold (`IN HOLD`).
* **Complete Species & Variant Breakdown:** Maps all Odyssey biological species and color variants against current Vista Genomics base payouts, breaking down **Base Value**, **First Footfall Bonus (4x)**, and **Total Estimated Payout**.
* **Date & Status Filtering:** Filter results by local date/time cutoff and toggle between uncashed samples only or full expedition history.

---

## Quick Start

1. **Download:** Save `exobio-audit.html` anywhere on your computer.
2. **Open:** Launch the file in any modern web browser (Chrome, Edge, Brave, Firefox).
3. **Select Logs:** Click **1. Browse Journal Log(s)**, navigate to your *Elite Dangerous* journal directory (use the built-in **Copy Path** button for quick access):
   ```text
   %USERPROFILE%\Saved Games\Frontier Developments\Elite Dangerous
