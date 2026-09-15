# Handoff: Toronto data harvest for T&K (Pro Doubles Men, 45–49)

Paste this whole file as the opening message of the new chat.

## Who and what

Tobias Scott and Kevin Lyman, HYROX **Pro Doubles Men, age group 45–49**.
Next race: **Toronto**. Goal: **sub 1:08:00**.

Baseline — HYROX Ottawa 2026, official finish **1:11:30** (#80 of 144 overall, #4 of 6 in 45–49):

| | Ottawa 2026 |
|---|---|
| Runs (official aggregate) | 38:35 — splits sum to 38:39, a known 4s discrepancy |
| Stations | 28:13 |
| Roxzone (derived) | 4:42 |

Run splits: 4:38, 4:37, 4:51, 4:50, 4:59, 4:53, 4:45, 5:06
Stations: SkiErg 3:43 · Sled Push 2:23 · Sled Pull 4:11 · Burpee Broad Jump 3:10 · Row 3:58 · Farmers Carry 1:56 · Sandbag Lunges 4:00 · Wall Balls 4:52

## Planning assumptions for Toronto

- **Running ≈ 38:00.** Maybe slightly better, not much. Do not build a plan that needs a running breakthrough.
- **Stations ≈ 25:00** is the working target. This is the question to pressure-test.
- Roxzone is venue-dependent (see below), so it is an unknown for Toronto until the data says otherwise.

Arithmetic, with runs held at 38:00:

| Stations | rox 3:50 | rox 4:05 | rox 4:20 | rox 4:40 |
|---|---|---|---|---|
| 24:30 | 1:06:20 | 1:06:35 | 1:06:50 | 1:07:10 |
| **25:00** | 1:06:50 | **1:07:05** | 1:07:20 | 1:07:40 |
| 25:30 | 1:07:20 | 1:07:35 | 1:07:50 | 1:08:10 |
| 26:00 | 1:07:50 | 1:08:05 | 1:08:20 | 1:08:40 |

So a 25:00 station block clears the goal on any plausible roxzone. A 26:00 block needs a fast roxzone to survive.

## What to harvest

Source: **hyresult.com**.

**Events:** HYROX Toronto **2024, 2025 and 2026**. Find the slugs via the month listings at `https://www.hyresult.com/events/<year>/<month>` — each event links to `/event/<slug>` (Ottawa 2026 was `s8-2026-ottawa`, so expect `s7-2025-toronto`, `s6-2024-toronto` style ids, but confirm rather than guess).

**Division:** `https://www.hyresult.com/ranking/<slug>-hyrox-pro-doubles-men`.
If Pro Doubles Men is thin in the older years, also pull `-hyrox-doubles-men` and label it clearly as a different division — the weights differ (Pro men: sled push 202 kg, sled pull 153 kg, carry 2×32 kg, sandbag 30 kg, wall ball 9 kg).

**Teams of interest:** finish between **1:04:00 and 1:11:00**, prioritising **age groups 40–44, 45–49, 50+**. Older teams are the useful comparison; a 30-year-old at 1:07 says little about what is available to a 47-year-old.

**Per team, collect:** total, runs total, stations total, roxzone (derived: total − runs − stations), age group, and every individual station split.

## Method that worked (use it, it avoids a lot of pain)

- Ranking pages are server-rendered. Rows parse out of the HTML with a regex pairing `<span class="font-semibold">TIME</span>` with the following `href="/result/ID"`. Each row appears twice (mobile + desktop markup) — dedupe by result id.
- **Pagination is `?p=2`**, 100 teams per page. Page 1 alone will stop well short of 1:07 in a big field.
- **The age group is NOT in the ranking page.** It is only on the result page, in the meta description: `...in division HYROX PRO DOUBLES MEN 45-49`. So age-group filtering requires fetching each result page. The on-page age filter is client-side and not URL-addressable — `?ag=`, `?ageGroup=` etc. all 404.
- Result pages carry Runs / Stations / Roxzone / Total as `<h3>` labels with the time in the surrounding card, and the eight station splits likewise.
- **Rate limiting is real.** Roughly 200 rapid requests triggers a 403 that took several minutes to clear, and it escalates if you keep probing. Pace at ~1.5s between requests, back off 90s on any 403, and do not retry in a tight loop.
- Browser tool calls may cap around 45s. Run the harvest as a background async job writing to a global, and poll it with short calls.

## Pitfalls found the hard way

1. **Sanity-check every parse.** A Berlin harvest returned teams "running" 28:09 with 11-minute roxzones. The numbers summed to the finish time, so they looked plausible until read. Discard anything where runs are implausibly fast or roxzone exceeds ~7 minutes, and say so rather than pooling it.
2. **Roxzone is as much the venue as the team.** Age-group means across events: Cardiff 2:57, New York 4:04, Ottawa 4:16, Barcelona 4:43, Cologne 4:48, Rotterdam 4:53. Never compare roxzone across cities. **Establishing what Toronto's roxzone looks like is one of the most valuable outputs of this harvest.**
3. **Run splits are not all 1 km.** First and last runs vary with the layout of the start, the roxzone and the wall ball station. One team's Run 1 came back as 3:32 while their other runs were ~6:00 — real, not an error, because that leg was short and the 8 km made up elsewhere. So compare **run totals**, not run splits, across venues, and check whether Toronto's first/last runs are short before reading anything into them.
4. HYRESULT's finish time can differ from the official result by a second or two.

## Questions to answer

1. For Toronto specifically, what do 45–49 (and 40+) Pro Doubles Men teams finishing **1:06–1:09** actually run for stations, runs and roxzone? Give the range and median for each.
2. **What does a 25:00 station block look like station by station** at this age and division? Give a target for each of the eight stations, drawn from what teams at that level actually post, not from even percentage cuts.
3. What is a realistic **Toronto roxzone** for a competent-but-not-elite team? Is Toronto a fast or slow layout?
4. Are Toronto's **first and last runs** full kilometres, or short/long? If short, what does that do to a 38:00 run total?
5. Do older teams (45+) at ~1:07 get there with a different station profile than younger ones — specifically, are they slower on the strength stations and faster on the ergs?

## Constraints to respect in any recommendation

- Running ≈ 38:00, improvable only slightly, and mostly in the **later runs** — the splits drift after halfway (Run 5 4:59, Run 8 5:06) while Runs 1 and 2 are 4:38 and 4:37.
- **No sled access to train on.** Sled push gets position cues only. Sled pull has ~29 seconds available from process alone: they walked off after three of the `4 × 12.5 m` lengths, were reminded, came back, and they also started pulls on a slack rope.
- **Wall balls and sandbag lunges are already in training**, so those can carry real targets.
- **Farmers carry is capped** — worst rank of the race (#112 of 144) but the station is only 1:56 long, so the ceiling is ~10–15 seconds.

## Output wanted

A station-by-station table: Ottawa actual → recommended Toronto target → the evidence behind it (which Toronto teams, what they posted). Plus the roxzone read for Toronto and whether 25:00 is the right station number or whether it should be 25:30 or 24:30.
