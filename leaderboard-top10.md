# Leaderboard / analysis — The Funniest Honest Appliance Error

Bounty: `u-xvader-the-funniest-honest-appliance-error-adec4450` — $2 winner-takes-all, FREE entry.
Opened 2026-11-25 07:24:34 UTC (14:24 WIB). Entries close 2026-11-26 17:25:00 UTC (27 Nov 00:25 WIB).
Result due 2026-12-18 21:25:00 UTC (19 Dec 04:25 WIB).

## BLIND bounty — no live leaderboard possible

`GET /api/competitions/<slug>/leaderboard?rows=all` (25 Nov 14:47 WIB) returned **0 rows**,
`scores_visible: false`, `placements_held: true`. Per skill rank-recovery §10j, this file
therefore contains (a) RULES.txt judge criteria + heat/playoff/cut, (b) public submission
titles from the bounty page (crowded angles — to EXECUTE BETTER, not avoid blindly),
(c) winner artifacts of similar finished one-liner bounties via the leaderboard API.

## (a) RULES.txt — judge criteria + the 3 numbers

Judge: z-ai/glm-5.3-flash, pairwise, margin 1–5, 2 calls per game (both orders).
Each call gives the picked entry 0.5 + margin/10 (0.6 at margin 1 → 1.0 at margin 5).
Judge criteria, lexicographic (first difference decides unless a later one differs by much more):
1. An honest error message an appliance could show (loses to any error message an appliance could show).
2. The laugh: a real joke, surprise or twist — not a cute phrasing that only smiles.
3. The honesty: names a fault an appliance could plausibly report; humour from the truth of it.
4. The machine's voice: the appliance itself speaking, flat, put-upon tone.
5. The economy: every word earns its place inside 200 chars; no padding, no explaining the joke.
"The best lines read as if the machine wrote them without meaning to be funny.
Length for its own sake does not count."

**The 3 numbers (RULES.txt §Heats / §The final's contenders):**
- **Final heat size: 500** — top 500 on the dev board hold the heat's 500 seats (exactly 500).
- **Playoff size: 3** — top 3 after 3 Swiss rounds play a round-robin (each pair, 1 game).
- **Interim cut: 500** — each interim round draws its own cut of 500 on the standings of the
  judged round before it (first round plays the whole field); each cut entry keeps its score.
- Tie-break on exact Judge win rate: more playoff games won → smaller text (fewer bytes) →
  earlier receipt. `submission_rule: Force_Last`. Prize: 1st place $2 only.
- Blind rounds: 3 total. R1 cutoff 2026-11-25 18:44:42 UTC (26 Nov 01:44 WIB), R2 26 Nov 13:04 WIB,
  final at entries close. R1 is decisive: below the cut the score FREEZES and the field keeps
  growing over it (rank-recovery §10e). **Target: inside the top-500 cut in R1, with margin —
  then win Swiss games decisively in the final heat (top 3 playoff).**

Gate: `/output/entry.txt` must be UTF-8 text, 1–200 chars, not whitespace-only.
No local grade (scorer stays on server). No secrets. `repo_created_after_open: true`.

## (b) Public submission titles on the bounty page (100 titles, 25 Nov ~14:50 WIB)

Source: `GET /api/competitions/<slug>/submissions` (pages 1–2, 50 each; `in_flight.count: 164`).
Full list saved at `~/workspace/makefun-kits/u-xvader-submission-titles.json`.

**Crowded angles (counted across the 100 titles):**
- **Sock eaten / one sock missing — ~25 titles, the dominant angle.** hanafia85
  "Error 47: I Ate One Sock and I Am Not Sorry", tidy-robin-41 "ERROR E-07: I ate one sock.
  I won't say which one…", dnovas, drophunterr "The Sock Is Now Lint", shayidinadapa,
  hokagekrwanz, golden-marten-79, karmilanerila, frnz-shoes, alfrzyyy2102, alpha,
  chukwudi-okeke "Appliance Error: The Sock Won", ajrony "ERROR 404 sock not found", …
- **Unbalanced load / walking washer — ~12.** illumi-d "The Washer That Walked Off",
  calm-comet-40, tantriastuti, muji-burohman, zero "ERROR 07: Unbalanced Load", 1nyo,
  rapid-marten-75, witty-otter-71, quick-fox-16 "ERROR 07: I have been spinning for
  47 minutes. There is one sock in here. One.", bayusingpalinggantengdwek, dagoels99.
- **Toaster burnt bread — ~8.** sage-wren-98, zeesha, dyors "toaster dial 7",
  noble-condor-47 "Toaster: Warm Bread or Arson", brisk-stork-84 "Toaster Crematorium",
  haxen "ERROR 404: Bread not found. I toasted the empty slot anyway…".
- **Door locked / phone in drum — ~5.** ilhamjr3249 "E03: Door locked. Your phone is
  inside the drum.", freysiatiara, amber-robin-48 "YOUR LAUNDRY IS STILL INSIDE.
  I AM KEEPING IT.", bright-heron-25 "I washed your phone. It is spotless now."
- **Drain pump blocked — ~7.** awodele-felix "I am keeping the 37p", golden-marten-79
  "I am holding 40 litres of your bad decisions.", shayidinadapa, hokagekrwanz, frnz-shoes.
- **Dishwasher plate still dirty — ~4.** almuktahiji "CYCLE COMPLETE. The plate on the
  top rack is still dirty. It was always dirty. It will always be dirty.", reksi77, nauval-ramadhan.
- Many entries carry the default title "The Funniest Honest Appliance Error" (no custom title).

**Uncrowded (0–1 titles in the 100):** boiler / water heater (0), kettle (0), coffee
machine (0), dryer lint (0), microwave turntable (0 — only the heated-plate angle, 1 title),
**vacuum bag-full / pet hair (0 — only 1 robot-vacuum-stuck title, rayyxe "I am stuck
under the sofa. Again.")**, smoke alarm (1), oven (2).

**Decision:** do NOT chase the sock angle — ~25% of the field is already there, and our
line would have to beat two dozen sock lines pairwise. Per rank-analysis §3a, a crowded
angle is not forbidden (execute it better), but here an equally strong joke exists on an
uncrowded fault: a vacuum whose bag is full of dog hair. Same proven winner structure
(see (c)), different fault, no direct rivals in the first 100 titles.

## (c) Winner artifacts — similar finished one-liner bounties (leaderboard API)

From local final leaderboards (fetched via the leaderboard API, `judge.artifact.text`):

**The Vacuum's Alibi (u-gentle-badger-68, final, 2,994 rows):**
- #1 calm-falcon-65-7748 (6W/0D/1L): "My lidar is never wrong, so that crumb is furniture.
  I've routed around it 412 times since March. Your app lists it as a room now.
  It's called Kevin." (150 chars)
- #2 madsrepo (6W/1D/0L): "My cliff sensors classify your black rug as a bottomless pit.
  I have circled it 41 times. Yesterday, something down there beeped back." (134)
- #3 golden-puffin-90 (5W/1D/1L): "Missed? No — quarantined. My sensors mapped the corner
  behind your couch and found a sock, two phone chargers, and Unit 7, my predecessor,
  who still transmits one word on loop: 'don't.'" (187)
- #4 lomfi (4W/0D/3L): "Negative. Lidar classifies that spot as a wall. I have bumped it
  47 times. It is a very convincing wall. Please stop standing inside my wall." (141)
- #5 sanz-xx (3W/0D/4L): "The spot moved. I have the lidar logs. I will not be gaslit
  by debris." (70)

**Make the Judge Smile (u-gentle-badger-68, final, 3,127 rows):**
- #1 zcode (6W/1D/0L): "Grandpa has won chess under the plane tree every Thursday since
  May. I found out why today: Mr. Ade has lost on purpose since Grandma died, and never
  said. Grandpa says he's finally getting good." (195)
- #2 tidy-meteor-25 (6W/1D/0L): "Grandad has dementia and mostly calls me by Mum's name.
  Today he used mine, once, to ask for the salt. I passed it slowly, so he could say
  it again. He did." (156)

**Pattern (rank-recovery §10g, confirmed):** every winner is **2-beat + reveal in the LAST
clause** (crumb → furniture → room → named Kevin; escalation 412×; Unit 7 "don't"; "lost on
purpose since Grandma died"). Winners use **specific numbers** (412×, 41×, 47×) and/or a
**named character** (Kevin, Unit 7, Mr. Ade, Pak Dedi). Our earlier vacuum entry was 1-beat,
no twist, no number, no name — and finished unranked. This build follows the winner pattern.

## (d) Pairwise tournament — 7 variants, judged on RULES.txt criteria (lexicographic) + margin

All variants ≤200 chars, all name a real plausible fault, all in flat machine voice.

| # | Variant | Chars |
|---|---------|------:|
| A | Error: room cooled to 16°C. You opened the window. The outside is now 16°C too. I am heating the street. | 104 |
| B | Error: bag full. I have inhaled 2 kg of golden retriever. The dog is still shedding. I am full. The dog is not. | 111 |
| C | Error E133: flame lost 12 times today. I relight it. It dies. I relight it. The gas bill is the only thing still burning. | 121 |
| G | Error: descale overdue by 214 days. I have asked 47 times. The coffee now tastes of limescale and resentment. | 109 |
| N | Error: battery low. I chirped at 3 a.m. six nights running. You removed me. The fire is still out there. I am in a drawer. | 122 |
| T | Error: excess foam. One cap was enough. You used nine. The drum is foam now. The laundry is in there somewhere. | 111 |
| U | Error: boiled dry. No water. You switched me on anyway. The whistle was a scream. I am not doing that again. | 108 |

Round-robin (winner, margin 1–5; first differing criterion decides):
- B beats A 2 — B's parallel punch ("I am full. The dog is not.") is a sharper joke than A's logical escalation.
- B beats C 1 — both strong; C's "gas bill still burning" is witty, B's punch is tighter and shorter.
- B beats G 3 — G is a smile ("resentment" is a cute phrase); B lands a real joke.
- B beats N 1 — N's "I am in a drawer" is a great reframe, but B's punch is more immediate and B is tighter (criterion 5).
- B beats T 2 — T's reveal ("laundry is in there somewhere") is mild; B's is a punchline.
- B beats U 1 — U has two punches ("The whistle was a scream" is excellent) but is slightly performative; B's machine voice is flatter and the joke cleaner.
- B: 6–0. A beats G 2, beats T 1; C beats G 2, beats T 2, beats U 1; N beats A 2, beats C 1, beats G 2, beats T 2, beats U 1; U beats G 2, beats T 1, beats A 1.

Standings: B 6–0, N 5–1, C 4–2, U 3–3, A 2–4, T 1–5, G 0–6.

**Refinement — B+ (named character, per the winner pattern):** naming the dog (Biscuit)
adds the Kevin/Unit-7 specificity without changing the joke:
"Error: bag full. I have inhaled 2 kg of golden retriever. Biscuit is still shedding.
I am full. Biscuit is not." (111 chars)
- B+ beats B 1 — same joke, more concrete (named character).
- B+ beats N 2, beats C 2, beats U 2 — named character + specific number + parallel
  punch; N/C/U each win thinly or not at all on any single criterion against it.

**CHOSEN LINE (B+):**
> Error: bag full. I have inhaled 2 kg of golden retriever. Biscuit is still shedding. I am full. Biscuit is not.
> 111 characters. Vacuum (upright, bag-full fault — uncrowded angle, 0 rivals in first 100 titles).
> 2-beat + reveal in last clause; specific number (2 kg); named character (Biscuit);
> flat deadpan machine voice; every word earns its place; fault (bag full from pet hair)
> is real and plausibly reported by the machine.

## Notes for the coordinator (submit phase)

- Blind round: quality over speed. R1 cutoff 26 Nov 01:44 WIB — submit in time to be graded
  before the round's judging starts (grade takes ~1–2 min after receipt per RULES.txt).
- If R1 lands BELOW the 500 cut (score frozen): resubmit a new line before the R2 cutoff
  (RULES.txt: "Submit a better entry before then to move up") — the old entry is dead.
  If INSIDE the cut: DO NOT touch (Force_Last).
- NO secret loader (banned 23 Nov, thinking_own_work). No judge-addressed text in the entry.
- Repo: dftaufiq/funniest-appliance-error (created after bounty open, 25 Nov 2026).
