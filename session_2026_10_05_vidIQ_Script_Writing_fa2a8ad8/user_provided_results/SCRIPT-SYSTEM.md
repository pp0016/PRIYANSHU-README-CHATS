# SCRIPT SYSTEM — Universal Prompt Pack
**Built from the failures of Test 1, Test 2 Step A and Test 2 Step B (28 Sep 2026).**
Works in two places: (A) vidIQ AI Coach web, (B) Antigravity with Opus + vidIQ MCP.

Read `HANDOFF.md` section 3 first if you want to know why each rule exists.

---

## 0. HOW TO USE THIS

**Web vidIQ path (1 reference video, or 1–3 transcripts pasted as files):**
Prompt 1 → Prompt 2 → Prompt 3 in the SAME conversation. 30 credits.
Then Prompt 4 in a **BRAND NEW conversation** (or a different Gmail). 10 credits.

**Antigravity path (1–3 references, transcripts + comments via MCP):**
Prompt 0-MCP → Prompt 1 → Prompt 2 → Prompt 3 in one session.
Then Prompt 4 in a **NEW session**. 0 web credits.

> ### THE SINGLE MOST IMPORTANT RULE
> **Prompt 4 must never run in the conversation that wrote the script.**
> In the 28 Sep test, the same agent designed the prompts AND graded the output. It scored
> itself 9.5/10. A clean second pass measured 6.5/10 and found four factual defects. An author
> cannot audit its own work. Fresh context, every time, no exceptions.

---

## 1. FILL THESE IN BEFORE YOU START

Copy this block and fill it. Every prompt below references it.

```
TOPIC:            <e.g. Why the Sears empire collapsed>
TITLE:            <working title — the hook is written to pay it off>
NICHE:            <business history | history facts | religion | space | spanish storytelling>
RUNTIME:          <minutes>
WPM:              <measured from YOUR ElevenLabs voice — see below>
WORD BUDGET:      <RUNTIME × WPM — a HARD number, not a suggestion>
HOOK CAP:         <seconds from table × WPM ÷ 60, in words>
LAST HOOK TYPE:   <the type used in your previous video — don't repeat it>
LANGUAGE:         English
REFERENCE(S):     <1 video link on the website — pick an outlier: high views vs subscribers>
RESEARCH TIER:    <LOW | MEDIUM | HIGH — from table below>
```

### Measure your WPM first — this changed on 29 Sep

The first version of this file assumed 150 words per minute. That's documentary pace. The Ice Age
reference video ran **roughly 230–250 wpm** — fast narration is part of how this niche holds
viewers. At 150 wpm a 15-minute script is 2,250 words; at 240 it's 3,600. Wrong WPM makes every
budget wrong.

**Measure once:** ~200 words into ElevenLabs with your channel voice → words ÷ audio minutes.

### Timing table — in seconds, so it holds at any speed

| Runtime | Hook cap | Re-hook every |
|---|---|---|
| under 12 min | 35 s | 45–60 s |
| 12–20 min | 45 s | 45–60 s under 15 · 75–90 s above |
| 20–35 min | 50 s | 75–90 s |
| 35 min+ | 60 s | ~120 s |

Convert to words: `seconds × WPM ÷ 60`. At 240 wpm, a 45-second hook is 180 words.

> vidIQ reported the Ice Age script as 2,360 words; it was 2,803. Never accept a stated count.

### Research tier by niche

| Niche | Tier | Why |
|---|---|---|
| Business history (rise & fall) | **MEDIUM** | Public financials, press coverage, easy to verify |
| Megaprojects / engineering failure | **HIGH** | Named specs and dates; errors get dunked in comments |
| History facts / inventions | **HIGH** | Dates and attributions are the whole product |
| Religion / apocrypha | **MEDIUM** | Source text is fixed; the risk is duplication, not accuracy |
| Space / cosmic | **HIGH** | Highest hallucination rate of any niche |
| Spanish storytelling | **MEDIUM** | Narrative-led |
| Book summaries / audiobooks | **LOW** | Use the separate template in section 6 |

---

## 2. PROMPT 0-MCP — Antigravity only (skip on web)

```
Before any analysis, pull the raw material. Do this with the vidIQ MCP and report what you got.

For each reference video I named:
1. vidiq_video_transcript — full transcript with timestamps
2. vidiq_video_comments — at least 100, sorted by likes
3. vidiq_video_stats — views, VPH, publish date, and the channel's subscriber count

Then tell me, in a short table, for EACH video:
- Total transcript word count
- Runtime
- Actual words-per-minute (word count / runtime) — I need this number, do not estimate it
- Outlier ratio: views ÷ channel subscribers
- Every comment that contains a TIMESTAMP ("3:45 got me") mapped to the transcript line at that
  moment. These are the strongest signal — they point directly at what landed.
- Then the 5 most-liked comments and the moment each reacts to. Say which are jokes rather than
  reactions to content — many top comments are.

Do not analyse structure yet. Do not write anything. Just pull and report.

Note: the YouTube retention heatmap (the grey graph on the progress bar) is NOT available through
any vidIQ MCP tool. Do not claim you have it. Most-liked comments mapped to moments are the
substitute — that is why I am asking for them.
```

**Why this exists:** the web tests never established the reference's real speaking pace, so every
later timing claim was guesswork. And comments are the only retention proxy you can actually get.

---

## 3. PROMPT 1 — Forensic analysis, no writing

> This is the one prompt from the 28 Sep tests that genuinely worked (rated 9/10 and deserved it).
> Only two things are added: the pace measurement, and the "carry-forward rules" list.

```
I need forensic analysis only. Do NOT write any script. Do not write a skeleton. Analysis only.

Analyse the attached reference material and break down:

1. THE HOOK. Quote the first 15 seconds verbatim. Count its words. What technique is it using?
   Break it into its individual beats and label each one.

2. STRUCTURE. List every topic section, in order, with its approximate duration. Then tell me the
   ORGANISING LOGIC — is it chronological, urgency-ordered, escalating stakes, something else?
   Name the principle, not just the list.

3. RE-HOOKS. Every point where the narrator recaptures a drifting viewer. Quote each one, give its
   timestamp, and label its TYPE (mystery lead-in, contrast/correction, authority payoff, emotional
   hammer, tonal jolt, structural reset). Then tell me the average interval between them.

4. TRANSITIONS. How does each section hand off to the next? Quote three examples. Is there a
   repeating mechanism?

5. RETENTION DEVICES. Open loops — where planted, where paid off, how long held. Direct address.
   Modern analogies. Unit translations. Contrast stacking.

6. VOICE SIGNATURE. Six distinguishing patterns with quoted examples. Average sentence length.

7. PACE. Total transcript word count divided by runtime = actual words per minute. Give me the
   number.

8. CARRY-FORWARD RULES. End with exactly 5 numbered rules, each one sentence, stating what a new
   script must DO to reproduce this video's retention. These 5 rules are the contract for
   everything you write later — I will hold you to them by number.

Analysis only. No script. I need to see your understanding before we write anything.
```

**Why #8 was added:** in the 28 Sep test, Prompt 1 correctly concluded *"it's a survival-priority
ladder, not a list — that's why it never feels like a list."* Prompt 2 then produced "Job One …
Job Six." The analysis was never converted into binding constraints, so it was wasted. Numbering
the rules makes Prompt 2 able to cite them.

---

## 4. PROMPT 2 — Skeleton + first half

```
Good. Now restate your 5 carry-forward rules in one line each, then build against them.

=== PART 1: SKELETON ===

Build a skeleton for: "<TOPIC>" at <RUNTIME> minutes.

Use the reference's TECHNIQUES. Do not reuse its content, its section order, or its hook approach.

The video's title is "<TITLE>". The hook must deliver that title's promise.

For every section give me: section title, ONE line of purpose, a WORD COUNT (not a timestamp), and
a VISUAL PLAN — what is on screen (archival photo, map, stock footage, AI image, motion graphic).
Then total the word counts. The total must land inside <WORD BUDGET>. If it doesn't, cut sections
until it does. Show me the total. Flag any section whose central claim has nothing to show.

=== STRUCTURE RULES — these are not suggestions ===

1. NEVER NUMBER THE SECTIONS in the spoken script. No "Job One / Job Two", no "Reason Three",
   no "First… Second… Third". Internal labels in the skeleton are fine; the viewer must never
   hear them.
2. NEVER ANNOUNCE THE STRUCTURE. Do not tell the viewer what is coming. No list of topics, no
   "here's what we'll cover", no roadmap. A spoken table of contents makes viewers leave.
3. Each section must ARRIVE THROUGH the previous section's unsolved problem. Every section ends
   by naming its own limitation, and that limitation is the next section's opening line.
4. Order by ESCALATING STAKES, not by chronology and not by category.

=== PART 2: WRITE THE FIRST HALF ===

Write from the hook to the midpoint. Target <half of WORD BUDGET> words.

HOOK RULES:
- FIRST write THREE different hooks, each a different type (mystery object, live stake, anomaly,
  scenario, uncomfortable claim, reversal). Do not use "<LAST HOOK TYPE>" — my previous video used
  it. Label each hook's type and word count, recommend one and say why. Then continue with it.
- HARD CAP: <HOOK CAP> words. Count them and tell me the count.
- The hook must confirm the promise of the title "<TITLE>" before the cap runs out.
- Put the viewer or a live stake in the first sentence. Not a location, not a date, not a source.
- NEVER undercut your own hook. If you open on a mystery, do not say "but this is disputed" inside
  the hook. Doubt belongs in the payoff, never in the opening.
- Plant ONE open loop, in one sentence, that you will pay off in the final quarter.

VISUAL RULE:
- End every paragraph with a visual tag: [V: archival photo of ...]. If a line cannot be shown on
  screen, tag it [V: NONE] — I will rewrite or cut it. This is a faceless channel; every line
  needs something to look at.

VOICE RULES — this will be narrated, so they target what a listener HEARS. Follow all six:
- Do NOT end every section on a neat closing line. At least TWO sections must end mid-thought or
  on something unresolved.
- Include at least ONE long, winding, slightly messy sentence per section. Not every sentence can
  be short and punchy — that rhythm is the clearest sign of machine writing.
- Never use the same sentence template three times in a row ("Not X. Y." / "That's not A. That's
  B."). A listener hears the pattern even when a reader wouldn't.
- MAXIMUM ONE "honesty disclaimer" in the WHOLE script ("I won't pretend", "I'm not going to tell
  you a tidy story", "I'd rather be honest"). One is personality. Three is a tic.
- Do not open more than one paragraph with "Here's the thing" / "Here's what's strange" /
  "Here's the honest part".
- Include ONE thing only this narrator could say: an opinion that could be wrong, a moment of
  being unsure, a small digression, or an admission that a source was hard to find. Frictionless
  writing reads as generated.

EVIDENCE RULES:
- Every section needs at least one named, specific, checkable detail — a place, a date, a number,
  a named person or document.
- NEVER cite another YouTube video as a source of fact. If your only source for a claim is the
  reference video's transcript, either find a real source or cut the claim.
- Do not convert a RANGE into a single figure. If a source says "between 18,250 and 17,750 years
  ago", you may not write "for 429 years". Derived precision is the single most common way these
  scripts get destroyed in the comments.
- Flag any contested claim with [CONTESTED] in square brackets so I can check it later. Do not
  present a contested claim as settled.

ENGAGEMENT RULES:
- NO comment prompt, poll, or "tell me below" anywhere in the first half or the middle. Telling a
  viewer to open the comments mid-video sends them to the comments. Engagement goes in the last
  30 seconds only.

End the first half on an open loop. Then report: the three hooks' word counts, half word count,
every [CONTESTED] tag, and how many [V: NONE] tags you placed.
```

**What I added and why — short version:**

| Added | Because |
|---|---|
| Restate the 5 rules first | Prompt 1's analysis was correct and then ignored |
| Word counts instead of timestamps | 2,803 words shipped as "15:00" |
| Hook cap in seconds, converted with your WPM | 316-word hook labelled 70 seconds; a fixed word cap breaks when voice speed changes |
| Three hooks + rotation | vidIQ's best output offered hook options; one hook type every video makes a channel sound templated |
| Title-first hook | The hook's job is to confirm the click |
| Visual tag per paragraph | Faceless: a line with nothing to show forces generic B-roll |
| "Never undercut your own hook" | Script retracted its mystery at ~60s |
| "Never number / never announce" | Prompt 2's 12-item mandatory list caused the "Job One–Six" listicle |
| Six voice rules targeting what's audible | 12 antithesis fragments, 3 disclaimers, every section on an epigram. (An em-dash cap was here; removed — a listener never hears an em-dash) |
| "One thing only this narrator could say" | Zero friction in the output — nothing a person would say |
| Never cite a YouTube video as a source | 600°C and 300,000-yr bear paws were cited to the reference transcript |
| Range→point ban | "429 years" at Mezhyrich |
| `[CONTESTED]` tagging | Makes Prompt 4 cheap to run |
| No mid-video comment CTA | The 5:15 "put your answer in the comments" leak |

---

## 5. PROMPT 3 — Second half

```
Continue. Write the second half, target <half of WORD BUDGET> words. Same voice, same rules from
the first half — all six voice rules, all four evidence rules, the disclaimer cap, and a visual tag
on every paragraph.

STRUCTURE FOR THIS HALF:
1. Open on a re-hook that is a genuine tonal shift, and pay off the first half's open loop inside
   the first 60 words. No dead air across the seam.
2. THE CONSEQUENCE BEAT, at roughly 60-70% through: one section that breaks the positive tone with
   real cost — human, financial, or structural, whatever the niche gives you. It must be specific
   and sourced, never a vague gesture.
3. THE RELIEF BEAT, immediately after: one genuine tonal break. It must contain an actual SURPRISE,
   not just the shape of a joke. A joke with correct structure and no surprise reads as generated.
   If you cannot find a real one, use a sharp observation instead and do not fake it.
4. THE PAYOFF, final quarter: cash the open loop from the hook.

THE PAYOFF RULE — this is the one that matters most:
You must deliver a VERDICT. "Unsettled" is not a verdict. "Maybe" is not a verdict. "Probably not
in the way the headline suggests" is not a verdict.
State what you think is most likely, say why, and say what would change your mind.
A viewer who stayed <RUNTIME> minutes for an answer and gets a shrug feels cheated, and says so in
the comments. You may be honest about uncertainty AND still commit to a position. Do both.

THE CLOSE:
- Philosophical reframe that connects the topic to something the viewer feels today.
- No standalone CTA. No "like and subscribe".
- ONE engagement line in the final 30 seconds, folded into the content and pointed forward.
- The last beat hands the viewer a SPECIFIC next question they now have — something a next video
  could answer. Not "watch this video". This is what keeps a viewer on the channel.

THEN PRODUCE A TTS VERSION — a second, clean copy for ElevenLabs:
- Visual tags removed.
- Unfamiliar names spelled phonetically in brackets on first use: Mezhyrich [MEZH-ih-rich].
- Numbers written as spoken: "about eighteen thousand years ago", never "18,250 BP".
- Dates, units, currencies and abbreviations written out in full.
- Paragraph breaks where a breath or pause belongs. No parenthetical asides.
- Split any sentence a voice cannot say in one breath.

Then report: second-half word count, TOTAL script word count, runtime at <WPM>, number of honesty
disclaimers used, every [CONTESTED] tag, and a pronunciation list of every name you spelled out.
```

**Why the payoff rule is written this hard:** the 28 Sep Prompt 3 said *"present it as a genuine
unsettled mystery."* The prompt caused the defect. The script held a loop for 13 minutes and
cashed it with "maybe." Unsettled and verdict-less are not the same thing.

---

## 6. PROMPT 4 — Fact-check + AI-voice screen (NEW CONVERSATION, ALWAYS)

```
You are auditing a script you did not write. Be adversarial. Your job is to find what is wrong,
not to tell me it is good. Do not compliment the script. Do not soften findings.

[PASTE THE FULL SCRIPT]

=== PASS A: MEASUREMENTS (do these first, report the raw numbers) ===
This script will be voiced at <WPM> words per minute.
1. Total word count.
2. Divide by <WPM> → the real runtime. Does it match the claimed runtime within ±10%? State the
   discrepancy in minutes.
3. Hook word count (everything before the first topic section) → divide by <WPM>, × 60 → real
   hook length in seconds.
4. Count the words between each re-hook, convert to seconds. Report actual intervals, not labels.
5. Count sentence templates repeated three or more times in a row.
6. Count sentences under 5 words.
7. Count paragraphs opening with "Here's" / "And here's" / "Now here's".
8. Count honesty disclaimers ("I won't pretend", "I'm not going to tell you", "to be honest").

=== PASS B: FACT SCREEN — five specific failure classes ===
Extract EVERY factual claim (number, date, place, named person, study, quantity) into a table:
claim | where it appears | source given | verdict.

Then flag each one against these five classes:
  1. DERIVED PRECISION — a range restated as a single figure. ("dated 18,250-17,750 years ago"
     becoming "in use for 429 years".) This is the #1 killer. Check every duration, every "for X
     years", every average.
  2. LAUNDERED SOURCE — cited to another YouTube video, a blog, a content farm, or "the reference
     transcript". Not a source. Flag it.
  3. CONTESTED AS SETTLED — a disputed or minority scientific/historical position stated as fact.
  4. INTERNAL INCONSISTENCY — the same fact given two different values anywhere in the script.
  5. OUT-OF-SCOPE EVIDENCE — evidence from the wrong period, region, or field used to support a
     claim about this one.

For each flagged claim give me: the fix, or "CUT".

=== PASS C: AI-VOICE SCREEN ===
- Do all sections end on a tidy closing line? Which ones do not?
- Is the short-fragment antithesis pattern ("Not X. Y." / "Gross. Effective.") used more than
  8 times? List them.
- Is there anything in this script that ONLY a specific human would say — a wrong opinion, a
  digression, a moment of being unsure, an admitted dead end? Quote it. If there is none, say so
  plainly.
- Mixed locale? (British and American spellings in the same script.)
- Does the humour beat contain an actual surprise, or only the structure of a joke?

=== PASS D: RETENTION SCREEN ===
- Where exactly will a viewer leave? Name the three highest-risk moments with word positions.
- Does the hook get undercut, hedged, or disclaimed inside itself?
- Are the sections numbered or pre-announced to the viewer?
- Does the ending deliver a VERDICT or a shrug? Quote the payoff line.
- Is there any comment prompt before the final 30 seconds?

=== VERDICT ===
Score /10 where 10 = would outperform the reference video, 7 = competitive with similar channels,
5 = watchable but forgettable, 3 = generic AI.
Then: estimated average view duration %, and the single change that would add the most retention.
Be blunt. If it is a 6, say 6.
```

**Why a whole separate pass:** you cannot judge English retention for Tier-1 viewers yourself —
that's the reason the whole audit layer exists. This pass converts the judgement into **counted
numbers**, so you read a scoreboard instead of re-reading a script. Run it, fix what it flags,
run it again. You read the script properly once, at the end.

---

## 7. ANTIGRAVITY-ONLY ADVANTAGES — use these, they are free

vidIQ web accepts **one** reference video. Antigravity + MCP has no such limit. Things only the
Antigravity path can do:

1. **Blend 2–3 references.** Pull three transcripts, run Prompt 1 on each, then ask:
   *"What do all three do the same way? That shared pattern is the niche's retention grammar.
   What does each do differently? Those differences are where I can be original without being
   wrong."* This is the single biggest edge over the web path.
2. **Comment mining as a retention proxy.** Timestamped comments first ("3:45 got me") — they point
   straight at moments. Then map the top-liked ones, ignoring jokes. Moments with
   clustered comments are where people stayed. Build sections around those shapes.
3. **Outlier hunting before writing.** `vidiq_outliers` + `vidiq_channel_videos` on a small
   fast-growing channel in the niche — write toward the shape that is already breaking out.
4. **Free iteration.** No 10-credit cost per message, so run Prompt 4 and fix in a loop until it
   clears. On web each loop costs credits.
5. **Title/thumbnail in the same session** — `vidiq_generate_titles`, `vidiq_score_title`,
   `vidiq_score_thumbnail`.

**Prompt to blend three references (Antigravity, after Prompt 0-MCP):**
```
You now have three transcripts. Run the Prompt 1 analysis on each one separately and give me all
three side by side in one table.

Then answer two questions:
1. What do all three do IDENTICALLY? That shared pattern is this niche's retention grammar and I
   must follow it.
2. Where do they DIVERGE? Those gaps are where I can be original without breaking the format.

Finally: name one thing all three FAIL to do. That gap is my differentiator. Be specific.
```

---

## 8. AUDIOBOOK / BOOK SUMMARY TEMPLATE — genuinely different, do not use section 3–5

Book summaries are **not** mystery-loop content. There is no dark turn, no open loop held for
20 minutes, no verdict. The viewer came for **value delivered in order**. Applying the universal
template here makes a summary that feels like it is withholding, and withholding is the fastest
way to lose a self-help audience.

Runtime is typically 20–60 min. Word budget = runtime × your measured WPM (at 150 wpm that's
3,000–9,000; at 240 it's 4,800–14,400 — measure, don't guess).

```
Write a book summary script for "<BOOK>" by <AUTHOR>. Runtime <RUNTIME> minutes.
Word budget <BUDGET>. Count your words per section and total them. Show me the total.

=== STRUCTURE ===
1. COLD OPEN (<HOOK CAP> words): the single most uncomfortable or counter-intuitive claim in the
   book, stated as a problem the viewer already has. Not "this book is about X". Not the author's
   biography. A problem they recognise in themselves.
2. THE PROMISE (40 words): what they will be able to do differently after this video. Concrete.
3. THE IDEAS: 4–6 of them, no more. Each one gets:
   - the idea in one plain sentence
   - ONE story or example from the book, told as a scene with people in it
   - the mechanism — WHY it works, not just that it does
   - one line on where it fails or who it does not work for
4. THE HONEST SECTION: what this book gets wrong, overstates, or does not cover. Every summary
   channel skips this, which is exactly why it builds trust when you do it.
5. THE ONE THING: if they remember nothing else. One idea, named.
6. CLOSE: the smallest possible action they could take today. Specific enough to do tonight.

=== RULES ===
- NEVER number the ideas out loud. No "Idea Number Three".
- No open loops, no "but first", no withholding. Deliver value in order. This audience leaves the
  moment they feel they are being strung along.
- Every idea needs a STORY, not a paraphrase of the idea. The story is the product — abstract
  restatement is what makes summary channels interchangeable.
- Second person throughout. "You" not "one" and not "people".
- COPYRIGHT: no extended verbatim quotation. Maximum one short quoted line per idea. Everything
  else is your own words describing the concept. Concepts are not copyrightable; the author's
  prose is.
- Voice rules from section 4 still apply in full: no epigram on every section, no sentence
  template three times in a row, one messy sentence per section, one thing only this narrator
  would say.
- Visual tag on every paragraph. Book summaries are often static-image channels, so say which
  line gets the image change.
- Do not claim the author said something they did not. If you are extrapolating, say so.
- Rotate the cold-open type between videos. Book-summary channels at one video a day are exactly
  where templated sameness shows first.

Then produce the TTS version: author and character names spelled phonetically where unusual,
numbers written as spoken, breath-length sentences.

Report: word count per section, total, runtime at <WPM>.
```

Then run **Prompt 4 Pass A, C and D** on it (skip Pass B — low research tier, fewer hard claims).

---

## 9. NICHE PARAMETER CHEAT SHEET

| Niche | Runtime | Consequence beat becomes | Citation strictness | Notes |
|---|---|---|---|---|
| Business history | 10–15 min | The people who lost jobs / savings | MEDIUM | Best natural verdict format: "will they recover?" |
| Megaprojects | 10–15 min | Casualties, cost overrun, abandonment | **HIGH** | Problem-door transitions are free — each design choice causes the next failure |
| History facts | 8–12 min | Who got erased from the story | **HIGH** | Add anti-template rules or every video sounds the same |
| Religion / apocrypha | 20–60 min | What the text actually threatens | MEDIUM | **Duplicate-content risk is the real danger** — everyone uses the same source text. Your differentiator must be framing, not material |
| Space | 15–30 min | Scale that makes the viewer feel small | **HIGH** | Highest hallucination rate — never skip Pass B |
| Spanish storytelling | 20–45 min | The human cost in the story | MEDIUM | Write in Spanish natively; do not write English then translate |
| Book summaries | 20–60 min | — (use section 8) | LOW | No consequence beat, no loop |

---

## 10. QUICK CHECKLIST — before any script gets recorded

- [ ] Word count ÷ **your measured WPM** matches the target runtime (±10%)
- [ ] Hook within its seconds cap, confirms the title, doesn't disclaim itself
- [ ] Hook type differs from the previous video's
- [ ] No numbered or pre-announced sections
- [ ] Payoff delivers a verdict, not "maybe"
- [ ] No comment prompt before the final 30 seconds; ending points to a next question
- [ ] Every range is still a range — no derived precision
- [ ] No YouTube video cited as a source of fact
- [ ] No sentence template repeated 3× in a row; max one honesty disclaimer
- [ ] At least one thing in it only a human would have said
- [ ] Every paragraph has a visual; no `[V: NONE]` left
- [ ] TTS version done: phonetic names, spoken-form numbers
- [ ] Fact-check and SCORE-GATE run in **fresh** conversations — 7.0+
