# Milestone Visualiser — V20

## Files
- `index.html` — web visualiser
- `milestones.json` — milestones and deadlines imported from `261006_STRATEGY_V01(Deadlines)(1).xlsx`

## Publish on GitHub Pages
1. Upload `index.html` and `milestones.json` to the root of your GitHub repository, replacing the existing files.
2. Open **Settings → Pages**.
3. Choose **Deploy from a branch**, select your `main` branch and `/ (root)`, then save.
4. Open the GitHub Pages URL shown in Settings → Pages.

## Data mapping
- Excel `Type` column containing `M` or `D` maps to category `Milestones` or `Deadlines`.
- The second `Type` column maps to the discipline code, including `BUS`.
- Importance levels `0`, `1`, and `2` are retained for milestones.
- Deadline importance is blank because the visualiser applies importance levels to milestones only.
- Blank Excel dates remain blank.
- The visualiser stores edits in the current browser's localStorage. Edits are not automatically shared between browsers/devices.


## V20 filter/data loading fix
V20 uses a separate browser storage key (`milestoneDataV20`) so saved data from older versions cannot hide the newly imported Deadlines and importance levels. Use **Reset imported data** to reload the Excel import.
