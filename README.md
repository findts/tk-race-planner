# T&K Race Planner

A lightweight HYROX Pro Doubles planner with Ottawa results, Toronto targets, reasons for savings, and handoff strategies.

## Use the planner

Open `tk-hyrox-race-planner.html` in a desktop browser, or use the GitHub Pages link on an iPhone. An iPhone attachment preview displays the default plan as read-only.

The planner is one standalone HTML file with embedded CSS and JavaScript. No installation, backend, framework, or build step is required. `index.html` directs visitors to that file.

Edits and scenarios save in the current browser's localStorage. They do not sync between athletes or devices. Use Export Plan and Import to exchange plans or keep a backup.

## Add a team

One file serves every team. Each team is an entry in the `TEAMS` block at the top of the planner's script, and a team's page is the same URL with `?team=<key>`:

```
https://findts.github.io/tk-race-planner/tk-hyrox-race-planner.html?team=tk
```

No `?team=` gives `DEFAULT_TEAM`, and an unrecognised key falls back to it rather than showing an empty page.

To add a team, copy an existing block, give it a new key, and set:

| Field | What it is |
| --- | --- |
| `brand` | Page title and masthead |
| `badge` | Division label beside the masthead |
| `prevRace` / `nextRace` | Race names; these fill the hero, column headers and mobile labels |
| `officialPrev` | Official finish at the first race, `h:mm:ss` or `mm:ss` |
| `planName` | Name of the starting scenario |
| `storageKey` | **Must be unique** |
| `footnote` | Optional timing caveats; a generic note is used if omitted |
| `rows` | The 17 segments: `[type, name, first-race time, target, reason]` where type is `run`, `station` or `roxzone` |

Each team also gets a small entry page named after its key (`ce-4hq7.html`). Share that, not the `?team=` URL: link previews in Messages, Slack and the like are built by crawlers that do not run JavaScript, so they never see the team chosen at runtime and would show the default team's name. The entry page carries its own `<title>` and Open Graph tags and redirects with a script — a meta refresh would be followed by the crawler, which defeats the point.

Team keys are deliberately not guessable (`ce-4hq7`, not `ce`), so nobody wanders into another team's page by editing the URL. This is obscurity, not privacy: the repository is public, so anyone who opens the source can read every team's data. Optional `prevShort` / `nextShort` give the mobile column labels a shorter name when the race name is long.

`storageKey` matters more than it looks: every team on `findts.github.io` shares one localStorage, so two teams with the same key overwrite each other's saved plans. Keep `tk` on `hyrox-doubles-planner-v1` or existing saved plans are orphaned.

Because the teams share one file, a fix or design change reaches every team on the next push. The read-only attachment preview is the one exception — it shows the default team's numbers, since it renders without JavaScript.

## Publish with GitHub Pages

In the repository's Settings → Pages, select **Deploy from a branch**, then **main** and **/ (root)**. GitHub provides a website link when deployment completes. GitHub Pages availability depends on the repository visibility and account plan.

## Update

Edit `tk-hyrox-race-planner.html`, bump the version in **both** `version.json` and the `APP_VERSION` constant in the planner's last script block, then commit and push to `main`. When Pages is configured, GitHub publishes the changes at the same address. Preserve the localStorage key and compatibility with saved plans to retain existing browser edits.

Correcting a team's recorded race times is safe: saved targets, notes and handoffs are kept, the new times replace the old ones, and the viewer is told their plan was carried across. Exports carry the team key, so one team's plan cannot be imported into another team's page; an export made before a times correction still imports, using the current times.

The two version strings must match. The planner fetches `version.json` with `cache: 'no-store'` on load and whenever the page regains focus; when the fetched version differs from `APP_VERSION`, it reloads itself with a fresh `?v=` query string so a phone cannot serve the stale copy. This matters most for a Home Screen icon, which caches aggressively. If the versions are left unbumped, the page simply never reloads; if only `version.json` is bumped, every visit reloads once and then settles. Local file and attachment previews have no `version.json` to fetch, so the check fails silently and the page works as before.

## Timing notes

- The individual Ottawa run splits total 38:39; the official running aggregate was 38:35.
- The Toronto targets total 1:07:38, 22 seconds inside 1:08:00 and 54 clear of the 1:08:32 that took second in 45-49 at Ottawa. They are weighted by the age-group field rather than the global one.
- Overall improvement uses the official Ottawa finish of 1:11:30. Roxzone carries HYRESULT's 4:42, so the baseline rows sum to 1:11:34; the 4 seconds is the run-split discrepancy.
- Roxzone is an aggregate added last; earlier projected clocks exclude transitions.
