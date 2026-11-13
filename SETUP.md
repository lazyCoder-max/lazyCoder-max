# Profile README — setup

1. Create a **public** repo named exactly `lazyCoder-max` (same as your username) and push these files to `main`.
2. GitHub renders `README.md` on your profile automatically. The SVGs in `assets/stage/` are already generated, so it works immediately.
3. (Optional, recommended) Add a repo secret `STATS_TOKEN` — a classic PAT with `repo` + `read:user` — so the daily
   **Refresh profile** Action can count commits (incl. private) and refresh stars/repos. Without it the Action still
   runs with `GITHUB_TOKEN` and updates public stats. Run it once from the Actions tab → "Refresh profile" → Run workflow.

## Editing
- Everything you see comes from `profile.config.json`. Edit it, then `python3 scripts/gen_profile.py` (no deps).
- `accent`: add `"accent": "#512bd4"` to change the colour (default is .NET purple).
- `targets`: repos to feature; `label`/`tag`/`wip`/`url` are optional overrides.
- `posts.items`: manual entries (your video, studio). If you ever start a blog with RSS, set `posts.feed` and the Action pulls the latest posts.
- `contacts`: the buttons at the bottom.

`assets/profile.json` holds live stats; the Action rewrites it. The seeded numbers (20 stars, 39 repos, 15 followers) are
from your public profile today; commits show up after the first Action run.
