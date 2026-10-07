# Milestone Timeline — GitHub Pages

## What this version contains

- 28 milestones imported from the supplied Excel workbook.
- Six existing milestone types: LEG, ADM, STRAT, TECH, BD, OPS.
- Three importance levels: High, Medium, Low, plus Unassigned for imported rows.
- Add, edit and delete milestones.
- Click timeline milestones for details.
- Filter by multiple types and importance levels.
- Undated milestones remain in the list but are not plotted on the date timeline.
- Export the current data as JSON.
- Reset to the original imported dataset.

## GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and `milestones.json` to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Select **Deploy from a branch**, choose the main branch and `/ (root)`.
5. Save. GitHub will provide the public Pages URL.

## Important: persistence

This first GitHub-ready version uses browser `localStorage` for edits. That means:
- edits persist on the same browser/device;
- different users/devices do not share edits;
- the original 28 milestones are loaded from `milestones.json`;
- `Export JSON` can be used to save the current state.

This is intentional because GitHub Pages is a static hosting service and cannot itself act as a shared writable database.

## Next database step

The UI is separated from the initial data file so the next version can connect to a shared backend such as Supabase/Firebase/a small API. The add/edit/delete functions can then be changed from local storage to database calls without redesigning the visualiser.
