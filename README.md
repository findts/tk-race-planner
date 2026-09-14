# T&K Race Planner

A lightweight HYROX Pro Doubles planner with Ottawa results, Toronto targets, reasons for savings, and handoff strategies.

## Use the planner

Open `tk-hyrox-race-planner.html` in a desktop browser, or use the GitHub Pages link on an iPhone. An iPhone attachment preview displays the default plan as read-only.

The planner is one standalone HTML file with embedded CSS and JavaScript. No installation, backend, framework, or build step is required. `index.html` directs visitors to that file.

Edits and scenarios save in the current browser's localStorage. They do not sync between athletes or devices. Use Export Plan and Import to exchange plans or keep a backup.

## Publish with GitHub Pages

In the repository's Settings → Pages, select **Deploy from a branch**, then **main** and **/ (root)**. GitHub provides a website link when deployment completes. GitHub Pages availability depends on the repository visibility and account plan.

## Update

Edit `tk-hyrox-race-planner.html`, bump the version in **both** `version.json` and the `APP_VERSION` constant in the planner's last script block, then commit and push to `main`. When Pages is configured, GitHub publishes the changes at the same address. Preserve the localStorage key and compatibility with saved plans to retain existing browser edits.

The two version strings must match. The planner fetches `version.json` with `cache: 'no-store'` on load and whenever the page regains focus; when the fetched version differs from `APP_VERSION`, it reloads itself with a fresh `?v=` query string so a phone cannot serve the stale copy. This matters most for a Home Screen icon, which caches aggressively. If the versions are left unbumped, the page simply never reloads; if only `version.json` is bumped, every visit reloads once and then settles. Local file and attachment previews have no `version.json` to fetch, so the check fails silently and the page works as before.

## Timing notes

- The individual Ottawa run splits total 38:39; the official running aggregate was 38:32.
- The supplied Toronto targets total 1:07:27, four seconds below the stated 1:07:31.
- Overall improvement uses the official Ottawa finish of 1:11:32.
- Roxzone is an aggregate added last; earlier projected clocks exclude transitions.
