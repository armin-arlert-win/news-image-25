# NEWS-IMAGE-20261125 — BUILD REPORT

**Built:** 25 Nov 2026, ~10:46–11:00 WIB. **Status: BUILD ONLY — no repo, no push, no submit.**
**Dir:** `~/workspace/makefun/news-image-25/` (local commit, see bottom).
**Spec:** `~/workspace/makefun/NEWS-IMAGE-20261125-SCOUT.md` §3 (canon) + §6 (concept).
**Concept:** "THE WORLD IN ONE DAY" — one-page newspaper, 1024×1024, cream
paper `#f7f3e8`, navy masthead, red accents. HTML/CSS rendered to PNG with
headless Chromium; illustrations are inline SVG vectors only (no AI photos).

## Files

| File | Size | Note |
|---|---|---|
| `entry.png` | 94,015 B | 1024×1024, palette PNG (256 colours) |
| `page.html` | 16,767 B | hand-written source of the newspaper |
| `main.ts` | 758 B | own code, stdlib only, copies entry.png |
| `LICENSE` | 1,073 B | MIT |
| `README.md` | 2,447 B | short readme |
| `.makefun/owner.json` | 57 B | `{"wallet":"5xVQ2SVrL8aCFaBhcd3zpmRFHVrKFsQdSnxjnjZRQs4K"}` |

## What the image shows (verified by viewing it)

- Top strip: THE WORLD IN ONE DAY · ONE DAY · ONE PAGE · DAY 329 OF 2026
- Masthead: **Wednesday 25 November 2026**; subline "16 stories · 6 regions ·
  every one first reported on this one day"
- Numbers strip: **11** wounded in Riyadh · **700,000** Russian soldiers killed ·
  **10 of 12** Huawei counts guilty · **00:18** Shenzhou liftoff, UTC · **5.6** Nepal quake
- Lead 1 (rocket SVG): PAKISTAN'S FIRST ASTRONAUT BLASTS OFF — Shenzhou-24,
  Jiuquan, 00:18 UTC, Muhammad Zeeshan Ali, first Pakistani in orbit, first
  foreign astronaut to visit Tiangong. REUTERS · XINHUA, CONFIRMED.
- Lead 2 (tower + drone SVG): HOUTHI DRONE HITS RIYADH'S TALLEST TOWER —
  11 wounded, second strike on the PIF Tower in a week, Saudi civil defence
  says; coalition orders Hodeidah port cleared. REUTERS · AFP, REPORTED.
- Lead 3 (gavel SVG): HUAWEI GUILTY ON 10 OF 12 COUNTS — Brooklyn jury:
  trade secrets, bank/wire fraud, Iran sanctions; cleared of racketeering.
  DOJ · REUTERS, REPORTED.
- Map "WHERE IT HAPPENED", 9 numbered pins: 1 Jiuquan · 2 Riyadh · 3 Brooklyn ·
  4 Washington · 5 Gulf of Finland · 6 Kathmandu · 7 Paris · 8 Canberra ·
  9 Kinshasa.
- Briefs 4–16 (13 briefs): CIA/ODNI breach; Zelenskiy confirms ship strikes
  (Sparta II + Benghazi); Nepal 5.6 quake, Koshi, 07:17 local, no casualties;
  Sarkozy + Bruni to trial (Libya funding, pre-trial 1 Apr 2027); Giuliani
  Medal of Freedom + turkeys Freedom & Feathers; NATO jets for Poland; Dow
  tops 50,000 (+0.9%), Nvidia −6%; Australia CPI 4.9% + Solomons pact;
  England beat Australia, 2nd T20I by 8 wickets, chasing 185; three tankers
  hit by mines, Hormuz; Houthis 60 km from Aden; **DR Congo military aircraft
  missing**; **Malaysia to return 6,500 Rohingya** (5 days after ICJ ruling).
  Plus an unnumbered TODAY note: International Day for the Elimination of
  Violence against Women.
- DATE CHECK (red band, fully visible): "Left out because they were not this
  day's news: COP31 ends with no deal (23 Nov) · GTA 6 worldwide launch
  (19 Nov) · Nvidia reinstates Huang, +31.5% (23 Nov) · Ukraine's Benghazi
  sinking first reported Sunday. Every story above was first reported on
  Wednesday 25 November 2026, as the named outlets reported it."
- Footer: Sources: Reuters · AP · BBC · Bloomberg · RFE/RL · The Hindu.

## Numbers printed — source (fact-check 2× vs scout §3)

| Printed | Source in scout §3 |
|---|---|
| Shenzhou-24 liftoff 00:18 UTC 25 Nov, Jiuquan | §3a, verified via Reuters/Wikipedia |
| Muhammad Zeeshan Ali, 40, PAF pilot; first Pakistani in orbit; first foreign astronaut on Tiangong | §3a |
| Riyadh: 11 wounded; 2nd strike on PIF Tower in a week (first 19 Nov, no casualties) | §3a |
| Huawei: 10 of 12 counts; Brooklyn jury 24 Nov; trade secrets, bank/wire fraud, Iran sanctions; cleared of racketeering | §3a |
| 700,000+ Russian soldiers killed (new analysis, RFE/RL, 25 Nov) | §3a |
| Nepal quake 5.6 (local; EMSC 5.3), Koshi, 07:17 local, no casualties | §3a |
| Dow tops 50,000 (+0.9%); Nvidia −6% after +31.5% rally | §3a |
| Australia CPI 4.9% (Oct, released 25 Nov); Solomons security pact | §3a |
| England beat Australia 2nd T20I by 8 wickets, chasing 185 | §3a |
| Houthis 60 km from Aden; army says city will hold | §3a |
| DR Congo military aircraft missing (Kinshasa) | §3a + §3b gap #1 |
| Malaysia to return 6,500+ Rohingya (5 days after ICJ genocide ruling) | §3b gap #3 |
| COP31 ended 23 Nov (no deal); GTA 6 launch 19 Nov; Huang reinstated 23 Nov | §3a/§3c + concept §6 |
| DAY 329 OF 2026 | day count: 31+28+31+30+31+30+31+31+30+31 = 304; +25 = 329 |

Framing rule applied: no event is given a false time of day — 24 Nov stories
are framed as "reported"/"confirms"/"says", per scout §3c. The DATE CHECK
sentence follows the winning leaders' own framing (scout §6, as specified
in the build brief).

## Verification results

- **PNG:** 1024×1024, 94,015 bytes — under the 1 MiB cap and the <200 KB
  target (tie-break: smaller file wins an exact-rate tie). sha256
  `bfee520189e17e8ed3efb5a6a6b325e506c273c72bb52eacf5a4a39bdc4cf058`.
- **main.ts 2×:** run to two different directories with
  `MAKEFUN_OUTPUT_DIR` — both outputs byte-identical to `entry.png`
  (same sha256). Deterministic.
- **Screenshot pipeline 2×:** full re-render (Chromium → crop → quantize)
  produced byte-identical `entry.png` (same sha256). Deterministic.
- **300 px legibility:** downscaled to 300×300 — masthead, the three lead
  headlines, the numbers strip and the DATE CHECK band all remain readable;
  brief body text is small at that size, as in the leading entries.
- **Viewed at full resolution:** masthead, 3 leads, map + 9 pins + key,
  all 13 briefs, DATE CHECK band and sources footer are all present and
  legible; no garbled text anywhere (HTML render, not AI generation).

## Notes / deviations

1. **Brief count:** the brief lists 12 items but the last item holds two
   stories (DR Congo + Malaysia). They are printed as two separate briefs
   (15 and 16), so there are 13 briefs and 3 leads + 13 = **16 stories** —
   the masthead subline counts 16, which matches what is printed.
2. **Screenshot quirk:** headless Chromium's `--window-size=1024,1024`
   gives an effective viewport of only ~936 px, cutting the footer off.
   Fix: screenshot at 1024×1100 and crop to 1024×1024 with PIL.
   (DOM measurement confirmed the page itself is exactly 1024 tall;
   datecheck 920–989, footer 989–1010.)
3. **PNG size:** raw Chromium output was 259–263 KB; palette quantization
   (PIL, 256 colours, adaptive) brought it to 94,015 B with no visible
   quality loss at full resolution.
4. **Chromium used:** puppeteer-managed Chrome 131 at
   `~/.cache/puppeteer/chrome/linux-131.0.6778.204/chrome-linux64/chrome`
   (the system `/opt/meta-chromium/chrome` refuses to start headless:
   "Hatch WebGL domain policy is required for browser startup").
5. **Not done (by design):** no GitHub repo created, no push, no submit —
   parent does that; planned submit 26 Nov siang WIB.

## Local commit

`git init` + commit in `~/workspace/makefun/news-image-25/` (commit hash
recorded in the parent's report; see `git log` in that directory).
