# Toronto research findings — T&K, Pro Doubles Men 45–49

Source: hyresult.com, harvested 2026-09-14. Events: HYROX Toronto 2024 (`s7-2024-toronto`, Enercare Centre, Oct 5–6 2024) and Toronto 2025 (`s8-2025-toronto`, same venue, Oct 3–5 2025). Toronto 2026 (`s9-2026-toronto`, Oct 1–4) is the target race — no results exist yet, same venue. Ottawa 2026 (`s8-2026-ottawa`) was harvested with the same method as a like-for-like control, including T&K's own result page.

Data: `hyrox_toronto_harvest.csv` — 189 teams, every station split, every run leg, and the roxzone in/out segment for every station.

| Set | n | What it is |
|---|---|---|
| Toronto 2025 Pro Doubles Men | 63 | every team 1:03–1:12, plus every 40+ team to 1:20 |
| Toronto 2024 Pro Doubles Men | 26 | same rule |
| Toronto 2024+2025 Doubles Men (open, lighter weights) | 42 | 40+ teams 1:03–1:12 only, labelled separately, never pooled with Pro |
| Ottawa 2026 Pro Doubles Men | 58 | every team 1:03–1:12 (includes T&K) |

Data-quality notes: 21 Toronto 2025 Pro teams carry no age group (shown as "75-79" or null on HYRESULT — a placeholder, treated as unknown, never counted as 45+). Ault/Bolger (2025, 40-44) have a 2:12 sled pull and 5:57 wall balls that look like a mis-placed split; excluded from the sled pull and wall ball medians. Every other team passed the checks (run legs sum to the official runs total, roxzone segments sum to the derived roxzone, no runs under 30:00, no roxzone over 7:00 in 2025). 2024 had five teams with 7:00+ roxzones — real, that layout was slow for everyone (see §3).

---

## The answer in one table

Runs held at 38:00. Toronto 2025 roxzone for a competent team is **4:45–5:00**, not the 3:50–4:20 in the handoff grid.

| Stations | rox 4:30 | rox 4:45 | rox 5:00 | rox 5:15 |
|---|---|---|---|---|
| 24:30 | 1:07:00 | 1:07:15 | 1:07:30 | 1:07:45 |
| **25:00** | 1:07:30 | **1:07:45** | **1:08:00** | 1:08:15 |
| 25:30 | 1:08:00 | 1:08:15 | 1:08:30 | 1:08:45 |
| 26:00 | 1:08:30 | 1:08:45 | 1:09:00 | 1:09:15 |

**Verdict: 25:00 is the right station number — but at Toronto it is the line, not a cushion.** 25:30 does not clear sub-1:08 on any realistic Toronto roxzone. 24:30 is what gives a 30–45 s margin, and it is what the 40+ teams who actually finish 1:05–1:07 post (their station blocks are 25:03–26:31, but they run 35–37 minutes to pay for it). With running fixed at ~38:00, T&K need the station block *and* a roxzone at the Toronto median.

---

## 1. Station-by-station: Ottawa actual → Toronto target → evidence

Evidence set = the nine Toronto Pro Doubles Men teams aged 40+ who finished 1:04–1:10 (eight from 2025, one from 2024). All-ages "25:00-block" = the 21 Pro teams (both years) whose station block was 24:30–25:30, median total 1:06:46.

| Station | Ottawa actual | **Toronto plan** | Floor (bankable) | Δ plan | 40+ evidence median (n=9) | Evidence: what the 40+ Toronto teams posted | Basis for the target |
|---|---|---|---|---|---|---|---|
| SkiErg | 3:43 | **3:45** | 3:45 | +2 | 3:56 | Ault/Bolger 3:42, Wyles/Barg 3:48, Chaimbrone/Hasyj 3:56, Dalfonso/Frain 3:56, Hinchey/Sylvestre 3:56, Higson/Houston 3:59, Kaup/Snee 4:00, Gobeille/Martel 4:02, Matthews/Cebulski 4:09 | Already faster than 8 of 9 evidence teams. Hold; do not buy seconds here with the run. |
| Sled Push | 2:23 | **2:15** | 2:15 | −8 | 2:06 | Ault/Bolger 1:49, Dalfonso/Frain 2:00, Higson/Houston 2:02, Hinchey/Sylvestre 2:05, Kaup/Snee 2:06, Wyles/Barg 2:08, Chaimbrone/Hasyj 2:16, Matthews/Cebulski 2:24, Gobeille/Martel 2:25 | Position cues only, no sled to train on. 2:15 is still slower than 7 of 9; median would be 2:06. |
| Sled Pull | 4:11 | **3:40** | 3:45 | −31 | 4:06 (n=8) | Higson/Houston 3:24, Hinchey/Sylvestre 3:33, Kaup/Snee 3:45, Matthews/Cebulski 3:58, Chaimbrone/Hasyj 4:13, Gobeille/Martel 4:16, Wyles/Barg 4:32, Dalfonso/Frain 4:44 (Ault/Bolger 2:12 excluded) | The ~29 s of process waste at Ottawa (walking off after 3 lengths, slack-rope starts) alone gives 3:42. 3:40 asks for nothing physical. |
| Burpee Broad Jump | 3:10 | **2:25** | 2:40 | −45 | 2:16 | Wyles/Barg 2:04, Gobeille/Martel 2:08, Ault/Bolger 2:09, Dalfonso/Frain 2:14, Hinchey/Sylvestre 2:16, Matthews/Cebulski 2:19, Chaimbrone/Hasyj 2:33, Kaup/Snee 2:42, Higson/Houston 3:14 | **Biggest gap to the field** — 3:10 is slower than 8 of 9 evidence teams, and the 45–49 pair Gobeille/Martel did 2:08. Not currently in training and needs no equipment. 2:25 is still outside the evidence median. |
| Row | 3:58 | **4:00** | 4:00 | +2 | 4:18 | Chaimbrone/Hasyj 4:12, Matthews/Cebulski 4:13, Wyles/Barg 4:15, Gobeille/Martel 4:16, Dalfonso/Frain 4:18, Higson/Houston 4:19, Kaup/Snee 4:20, Hinchey/Sylvestre 4:23, Ault/Bolger 4:27 | Faster than every evidence team. Hold; the row is not where 45–49 teams win. |
| Farmers Carry | 1:56 | **1:45** | 1:45 | −11 | 1:36 | Matthews/Cebulski 1:25, Ault/Bolger 1:32, Chaimbrone/Hasyj 1:32, Wyles/Barg 1:34, Kaup/Snee 1:36, Higson/Houston 1:37, Hinchey/Sylvestre 1:38, Dalfonso/Frain 1:42, Gobeille/Martel 1:44 | Capped per the handoff. 1:45 is the slowest of the evidence set; ceiling is real but small. |
| Sandbag Lunges | 4:00 | **3:10** | 3:25 | −50 | 3:18 | Gobeille/Martel 2:36, Matthews/Cebulski 3:00, Ault/Bolger 3:05, Wyles/Barg 3:05, Higson/Houston 3:18, Kaup/Snee 3:25, Chaimbrone/Hasyj 3:29, Dalfonso/Frain 3:29, Hinchey/Sylvestre 3:56 | In training. 3:10 sits between the 40+ median (3:18) and the all-ages 25:00-block median (3:04). Four 40+ teams did 3:05 or better. |
| Wall Balls | 4:52 | **4:00** | 4:15 | −52 | 3:55 (n=8) | Higson/Houston 3:16, Matthews/Cebulski 3:35, Wyles/Barg 3:46, Hinchey/Sylvestre 3:48, Dalfonso/Frain 4:01, Kaup/Snee 4:11, Chaimbrone/Hasyj 4:20, Gobeille/Martel 4:41 (Ault/Bolger 5:57 excluded) | In training. 4:00 is a few seconds over the 40+ median (3:55). All-ages 25:00-block median is 3:45, so 4:00 is not aggressive for the division, only for T&K's history. |
| **Total** | **28:13** | **25:00** | **25:50** | **−3:13** | 25:35 (40+, 1:06–1:09) | | |

How to read the two target columns:

- **Plan (25:00)** is what sub-1:08 requires. Three stations carry it: BBJ (−45), lunges (−50), wall balls (−52) — 2:27 of the 3:13. Sled pull's −31 is process, not fitness.
- **Floor (25:50)** is what I'd call bankable — the sled pull process fix, farmers, push cues, and the wall ball/lunge work already under way at conservative numbers. On its own the floor gives **1:08:35–1:08:50**. It misses.
- The difference between the two columns is almost entirely BBJ, lunges and wall balls — the three stations that need no sled. That is where the race is.

---

## 2. Roxzone: Toronto is a slow layout

Same method (total − runs − stations), same finish band (Pro Doubles Men, 1:03–1:12):

| Event | n | p10 | p25 | median | p75 | p90 |
|---|---|---|---|---|---|---|
| Ottawa 2026 | 58 | — | 4:12 | **4:25** | 4:45 | — |
| **Toronto 2025** | 51 | 4:19 | 4:32 | **4:45** | 4:55 | 5:10 |
| Toronto 2024 | 22 | 5:18 | 5:35 | **5:56** | 6:17 | 6:23 |
| Toronto 2025, open Doubles Men 40+ | 29 | — | 4:59 | 5:07 | 5:16 | — |

- Toronto 2025 is ~20 s slower than Ottawa for the same team, floor-to-floor. The fastest roxzone in the whole 2025 Pro Doubles Men field was 3:58.
- T&K's Ottawa 4:42 was 17 s over the Ottawa median. Transposed to Toronto that is **~5:00**; matching the Toronto median means **4:45**. 4:20 is not on the table at Toronto unless the 2026 floor plan changes.
- Toronto 2024 was a different floor plan at the same venue: median 5:56, and a completely different run-leg shape (§3). So the venue has hosted a slow layout before. Plan on the 2025 numbers (most recent, same venue), but treat 4:45–5:00 as a floor, not a ceiling, until the 2026 layout is seen.

Where Toronto's roxzone time actually goes (medians, 2025 Pro DM 1:03–1:12), against Ottawa and T&K's own Ottawa segments:

| Segment | Toronto 2025 | Ottawa 2026 | T&K at Ottawa |
|---|---|---|---|
| Run 1 → SkiErg in | 0:02 | 0:10 | 0:10 |
| SkiErg out → run | **0:36** | 0:13 | 0:14 |
| → Sled push in | 0:08 | 0:02 | 0:02 |
| Sled push out | 0:31 | 0:29 | 0:34 |
| → Sled pull in | 0:15 | 0:08 | 0:09 |
| Sled pull out | 0:31 | 0:28 | 0:30 |
| → BBJ in | 0:21 | 0:18 | 0:19 |
| BBJ out | 0:10 | 0:20 | 0:22 |
| → Row in | 0:02 | 0:20 | 0:20 |
| Row out | **0:44** | 0:12 | 0:12 |
| → Farmers in | 0:37 | 0:34 | 0:38 |
| Farmers out | 0:07 | 0:12 | 0:13 |
| → Lunges in | 0:31 | 0:41 | 0:41 |
| Lunges out (to wall balls) | 0:10 | 0:16 | 0:21 |
| **Total** | **4:45** | 4:23 | 4:42 |

Practical read: the two long Toronto segments are the walks *out* of the SkiErg and the rower (0:36 and 0:44). Those are geometry — you cannot fix them, but you can decide in advance who carries what and not stand at the erg. The walk into farmers (0:37) and into lunges (0:31) is where the equipment pick-up happens; T&K lost their Ottawa time in the sled-out and lunges-out segments (+5, +5 s over median), which is the controllable part. Getting to the Toronto median (4:45) is realistic; beating it materially is not.

---

## 3. First and last runs: short at Toronto 2025, long at Toronto 2024

Median run legs, Pro Doubles Men 1:03–1:12:

| | Run 1 | Run 2 | Run 3 | Run 4 | Run 5 | Run 6 | Run 7 | Run 8 | Runs total |
|---|---|---|---|---|---|---|---|---|---|
| **Toronto 2025** (n=51) | **3:44** | 4:27 | 4:51 | 4:49 | 4:55 | 4:51 | 4:57 | **4:07** | 36:57 |
| Toronto 2024 (n=22) | 4:54 | 4:19 | 4:41 | 4:32 | 4:36 | 4:32 | 4:38 | 5:09 | 37:04 |
| Ottawa 2026 (n=58) | 4:22 | 4:24 | 4:46 | 4:42 | 4:47 | 4:44 | 4:50 | 5:04 | 37:54 |
| T&K at Ottawa | 4:38 | 4:37 | 4:50 | 4:50 | 4:59 | 4:53 | 4:44 | 5:05 | 38:35 |

- At Toronto 2025, Run 1 is ~1:05 shorter and Run 8 ~1:20 shorter than the mid-race legs; Run 2 is also ~25 s short. The 8 km is made up on Runs 3–7, which come out ~5–10 s longer than Ottawa's.
- Whether the *total* course is shorter is not provable from this data: at 1:06–1:09 the Toronto field ran ~1:00 less than Ottawa's, but at 1:10–1:12 it ran ~1:05 *more*. Field composition swamps any course-length signal. **Keep 38:00 as the run total.** Do not bank a "short course" minute.
- What it does change is the clock T&K will see. Scaled to a 38:00 total, the 2025 layout looks like roughly **3:50 · 4:35 · 5:00 · 5:00 · 5:05 · 5:00 · 5:05 · 4:15**. A 5:05 on Run 5 at Toronto is on plan, not a fade. Pace Runs 3–7 by effort, not by the Ottawa numbers.
- Correction to the handoff's "splits drift after halfway": T&K's Ottawa Run 8 (5:05) matched the Ottawa field median (5:04) — that leg is long for everyone. The real fade was Runs 5–6 (+12 s and +9 s over the field median) and, more surprisingly, Runs 1–2 (+16 and +13 s over the field median; the field goes out harder on the short opening legs). The late-run drift is smaller than it looked.
- 2024 was the mirror image (long first/last legs), so the 2026 layout is not certain. If the 2026 course map shows the start and finish where they were in 2025, use the 2025 shape.

---

## 4. Do older teams at ~1:07 get there differently?

Toronto Pro Doubles Men, 1:04–1:10, medians:

| | 40+ (n=9) | Under 40 (n=37) | Difference |
|---|---|---|---|
| Total | 1:06:20 | 1:07:38 | |
| Runs | **36:22** | 37:03 | older faster by 41 s |
| Stations | 25:35 | **24:46** | older slower by 49 s |
| Roxzone | **4:52** | 5:08 | older faster by 16 s |
| SkiErg | 3:56 | 3:51 | +5 |
| Sled push | 2:06 | 1:58 | +8 |
| Sled pull | 3:58 | 3:53 | +5 |
| Burpee broad jump | **2:16** | 2:29 | **−13** |
| Row | 4:18 | 4:08 | +10 |
| Farmers | 1:36 | 1:33 | +3 |
| Lunges | 3:18 | 3:08 | +10 |
| Wall balls | 4:01 | 3:44 | +17 |

(Ault/Bolger's suspect 2:12 pull and 5:57 wall balls are in the 40+ column here; without them the 40+ pull median is 4:06 and wall balls 3:55 — the direction of every row is unchanged.)

The hypothesis in the handoff (older teams slower on strength, faster on ergs) does not hold at Toronto. The 40+ teams at this level are slightly slower on *every* station including both ergs, give back most of it on wall balls, row and lunges — and get to 1:06–1:07 by running 40 s faster and transitioning 16 s faster. The one station where they beat the younger teams is BBJ. n=9 is small; treat this as direction, not a rule. The implication for T&K is uncomfortable but clear: their ergs are already ahead of the 40+ field, so the remaining gap is BBJ, lunges and wall balls, exactly the three stations in §1.

---

## 5. Toronto 40+ Pro teams at 1:06–1:09 (question 1, as asked)

| | n | Median | Range |
|---|---|---|---|
| Total | 5 | 1:06:49 | 1:06:02 – 1:08:36 |
| Runs | | 36:36 | 35:20 – 37:17 |
| Stations | | 25:35 | 25:03 – 26:24 |
| Roxzone | | 4:52 | 4:37 – 6:03 (6:03 is the 2024 team; 2025 only: 4:37–4:55) |

Widened to 40+ at 1:04–1:11 (n=9): runs 36:22 (34:29–39:32), stations 25:35 (24:53–26:31), roxzone 4:52 (4:11–6:03). The two 45–49 teams in the window: Gobeille/Martel 1:04:48 (34:29 / 26:08 / 4:11) and Chaimbrone/Hasyj 1:05:55 (34:58 / 26:31 / 4:26). Both ran under 35:00 and neither had a station block under 26:00. Nobody 40+ in either Toronto edition has finished 1:06–1:09 with a 38:00 run and a 25:00 block — T&K would be doing it a different way from everyone in the evidence set, which is why the plan has no slack in it.

For reference only (different weights): open Doubles Men 40+ at 1:06–1:09 (n=12) — runs 37:08, stations 24:20, roxzone 5:34. Not comparable on sleds (1:32 push / 2:50 pull) and not used for any target above.

---

## What to do with it

1. Re-run the app's arithmetic with roxzone 4:45–5:00, not 3:50–4:20. The sub-1:08 line at Toronto is stations 25:00 with roxzone 4:45.
2. BBJ is the cheapest 45 s on the board and is not in the programme. It is the station where 45–49 teams match or beat younger ones.
3. Sled pull process (finish all four lengths, tension before the first pull) is worth 30 s at zero training cost. Rehearse it dry.
4. Expect the mid-race runs to read ~5:00–5:05 at Toronto and plan the pacing conversation before the race, not during Run 4.
5. Check the 2026 course map when it is published: if start/finish and wall balls sit where they did in 2025, everything above applies; if the layout looks like 2024, add a minute to the roxzone and re-plan.
