# SCORE GATE — 100 points, below 7.0 goes back

**Where:** a **new conversation**, never the one that wrote the script.
**Purpose:** turn "is this script good?" into arithmetic, so the answer is the same whoever runs it.
You read one number and a ranked fix list, not the script.

---

## CALIBRATE FIRST — a gate you haven't calibrated is an opinion

The earlier version calibrated against my own 6.5/10 on the Ice Age script. That's circular: if my
judgement is wrong, the gate inherits it — and my judgement *was* partly wrong (I assumed 150 wpm;
the reference ran ~230–250). So calibrate against reality instead:

1. **The winner.** Pull the transcript of `wt_7Hp7d7I8` (929K views) with `vidiq_video_transcript`.
   Score it. Award A4 (originality) in full — it is the original. **Expect 7.5 or higher.**
2. **A flop.** Pick a video in the same niche on a channel of similar size that got under a tenth
   of that channel's average views. Score its transcript. **Expect 5 or lower.**
3. **The gap must be 2.5 points or more.** If the gate cannot tell a 929K video from a flop, it is
   measuring taste, not retention, and none of its scores mean anything.

Then, for reference only, score the Ice Age script (`multi step prompt result/full_script_for_11labs.md`).
Expect roughly **6–7** — strong research and prose, weak structure and payoff. Supply the WPM the
script would actually be voiced at; its runtime verdict depends on it.

If the winner scores 9+ and the flop 8, the model is flattering. Fresh conversation, add:
*"You are scoring generously. Most scripts are a 6. Award only points you can quote evidence for."*

---

## THE BLOCKS

| Block | Points | Measures |
|---|---|---|
| **A. Craft** | 35 | Research, specificity, speakable prose, originality |
| **B. Retention** | 45 | Hook (20), structure, re-hooks, payoff, engagement placement |
| **C. Integrity** | 20 | Measurement honesty, evidence, audible AI-voice |

The hook now carries **20 points**, up from 10. The first 30 seconds is where the most viewers
leave; the old weighting treated it like any other section.

---

## THE PROMPT — copy everything below

```
Score this script against a fixed rubric. You are measuring, not reviewing. Award a point only
where the criterion is literally met, with a quote or a count as evidence. No evidence, no point.
When unsure, do not award it.

Do not compliment the script. A 6 is a normal score — most scripts are a 6. Drifting upward to be
agreeable costs me a video.

WPM this script will be voiced at: <number — measured from the TTS voice>
Claimed runtime: <minutes>
Title it is written for: <title, or "none">

[PASTE FULL SCRIPT]

============ BLOCK A — CRAFT (35) ============

A1 RESEARCH DEPTH (10)
  +3 every major section has at least one named, checkable detail
  +3 details are concrete (objects, places, people), not abstractions
  +2 at least 5 distinct named sources, sites, studies or documents
  +2 numbers are attached to an image the viewer can picture

A2 SPECIFICITY (7)
  +4 no paragraph could be deleted without losing information
  +3 no generic filler ("humans have always been resourceful")

A3 SPEAKABLE PROSE (8) — this is narrated, judge it as heard
  +3 read three random sentences aloud: each lands in one breath
  +3 no name or number a TTS voice is likely to mangle without a phonetic guide
  +2 vocabulary fits a general audience without dumbing down

A4 ORIGINALITY (10) — if scoring the reference video itself, award in full
  +4 hook approach differs from the reference's
  +3 section order differs from the reference's
  +3 zero sentences lifted or lightly paraphrased from the reference

BLOCK A: __/35

============ BLOCK B — RETENTION (45) ============

B1 HOOK (20)
  Hook cap in seconds: 35 under 12 min · 45 for 12-20 · 50 for 20-35 · 60 above.
  Hook seconds = hook words ÷ WPM × 60.
  +4 hook is within its cap in seconds
  +5 the viewer or a live stake appears in sentence one — not a location, date or source
  +4 exactly one open loop is planted
  +4 the hook does NOT disclaim, hedge or undercut itself anywhere inside it
  +3 the hook confirms the title's promise (if no title given: states a clear promise)

B2 STRUCTURE (10)
  +4 sections are NOT numbered out loud
  +3 structure is NOT announced to the viewer (no spoken roadmap)
  +3 each section arrives through the previous section's unsolved problem

B3 RE-HOOKS (5)
  Band: 45-60s under 15 min · 75-90s for 15-35 · ~120s above. Convert with WPM.
  +3 measured intervals between re-hooks fall within the band
  +2 re-hook types rotate; no two consecutive ones the same kind

B4 PAYOFF (7)
  +4 delivers a VERDICT. "Maybe", "unsettled", "probably not in the way the headline suggests"
     = 0. No partial credit.
  +2 the hook's open loop is explicitly cashed
  +1 the close reframes to something the viewer feels today

B5 ENGAGEMENT (3)
  +2 no comment prompt, poll or "tell me below" before the final 30 seconds
  +1 the ending hands the viewer to a specific next question

BLOCK B: __/45

============ BLOCK C — INTEGRITY (20) ============

C1 MEASUREMENT HONESTY (6)
  Runtime = total words ÷ WPM.
  +3 the claimed runtime is within ±10% of the measured runtime
  +2 the hook's real length matches any label or claim made about it
  +1 claimed re-hook spacing, if stated, matches measured spacing

C2 EVIDENCE (8) — start at 8, subtract 2 per failure class found, floor 0
  -2 DERIVED PRECISION: a range restated as a point figure
  -2 LAUNDERED SOURCE: a YouTube video, blog or content farm cited as fact
  -2 CONTESTED AS SETTLED: a disputed position stated as established
  -2 INTERNAL INCONSISTENCY: the same fact with two values
  -2 OUT-OF-SCOPE EVIDENCE: wrong period, region or field

C3 AUDIBLE AI-VOICE (6) — judge what a listener hears, not punctuation
  +1 at most one honesty disclaimer in the whole script
  +1 at least two sections end mid-thought, not on a tidy line
  +1 at least one long, winding sentence per section
  +1 no sentence template repeated three times in a row ("Not X. Y." / "Here's the...")
  +1 short-fragment antithesis used 8 times or fewer
  +1 one thing only a specific human would say — quote it, or award 0

BLOCK C: __/20

============ OUTPUT ============

1. Table: every criterion · awarded · available · evidence (a quote or a count).
2. Block subtotals, total /100, score /10 to one decimal.
3. Estimated average view duration %, and the three highest-risk moments by word position.
4. THE THREE HIGHEST-VALUE FIXES, ranked: criterion recovered, points gained, rewritten text ready
   to paste.
5. PASS or FAIL. Below 7.0 fails.

SCALE: 9-10 would beat the reference · 7-8 competitive in the niche · 5-6 watchable, forgettable,
no algorithmic push · 3-4 generic AI · 1-2 unwatchable
```

---

## READING THE RESULT

The block split tells you more than the total.

| Pattern | Diagnosis | Action |
|---|---|---|
| A high, B low | Good research, weak architecture | Rewrite structure, keep every fact |
| A low, B high | Well built, hollow | Back to sources |
| C low, A and B fine | Sloppy finishing | 30 minutes of counting fixes it |
| B1 (hook) under 12/20 | The video loses people before it starts | Fix this before anything else |

**The gate is a stand-in until you have real data.** Once your own videos are live, YouTube Studio
shows exactly where viewers left. If a script scored 8 and lost half its viewers at 0:40, the gate
got it wrong — log it (see START-HERE, "after upload") and adjust the weights. Real drop-off data
beats any rubric, including this one.
