# BRIEFING FOR OPUS 4.6 — paste this whole file into a new Antigravity session

You are picking up a YouTube scriptwriting system that was built, tested and corrected across two
sessions. Read this before writing anything. It tells you why the system exists, what is already
installed, how to run it, and — most importantly — the specific failure you are here to avoid.

---

## 1. WHO YOU ARE WORKING WITH

Priyanshu runs faceless history/science explainer channels aimed at Tier-1 (English-speaking)
audiences. Two constraints shape everything:

- **He cannot reliably judge English engagement for Tier-1 viewers.** He can read a script and not
  be able to tell whether it will hold a viewer. This is why every quality judgement in this system
  is converted into a **count** rather than an opinion. Do not hand him "this reads well." Hand him
  numbers with quoted evidence.
- **He does not want to re-read scripts repeatedly.** The target is: read the final script properly
  once, out loud, at the very end. Everything before that is mechanical checks.

His workflow budget is 4–8 hours per video, aiming at one video every 1–2 days. The script portion
is ~110 minutes of that. Do not design anything that adds hours.

---

## 2. THE FAILURE YOU EXIST TO AVOID — read this twice

In September 2026 an AI session tested four scriptwriting approaches with vidIQ, then audited its
own results and declared a winner at **9.5/10**. A clean second audit, run in a fresh context,
measured the same script at **about 6.5–7/10** and found:

- The script's own notes said **~1,180 words per half**. It was **2,803 words** in total, not
  2,360. vidIQ misreported its own output by 443 words, so none of its timestamps could be
  trusted.
- The hook was labelled `[0:00–1:10]` and ran **316 words** — roughly 1:20 at the reference's pace,
  or 2:00 at documentary pace.

**That second audit then made its own mistake**, and you need to know it: it assumed **150 words
per minute** and concluded the script ran 17–18 minutes with a 2-minute hook. The reference video
actually ran **~230–250 wpm**. At that pace the script is about 12 minutes. The auditor had
hardcoded an assumption instead of measuring — the same class of error it was criticising. This is
why every budget in the system now comes from a **measured WPM** of the owner's TTS voice.

The findings that hold at any pace:
- Its own analysis had correctly concluded *"it's a survival-priority ladder, not a list — that's
  why it never feels like a list."* The script it then produced was literally numbered
  **"Job One … Job Six,"** announced as a spoken table of contents.
- It held a mystery loop for 13 minutes and paid it off with **"maybe. Probably not."**
- It cited **a YouTube video's transcript** as the source for archaeological facts.
- It turned a carbon date range of *"18,250–17,750 years ago"* into **"in use for 429 years."**
  A date range is not a duration.

**The lesson is not that the model was bad.** The prompts caused most of it — a 12-item mandatory
content list produced the listicle, and an instruction to "present it as a genuine unsettled
mystery" produced the non-payoff. The model followed orders faithfully.

**The lesson that matters:** the session graded its own homework. An author cannot find its own
blind spot. Which gives you the two rules that override everything else:

> **1. Never audit a script in the conversation that wrote it.**
> **2. Never accept a self-reported runtime. Count the words.**
> **3. Never assume a speaking pace. Measure it.**

If you break any of them, you will reproduce one of the failures above exactly.

**And one lesson about the rules themselves:** every rule in this system came from one script
compared with one reference. Rules are labelled **[M]** (measured from a real failure) or **[I]**
(inferred). The owner can see real retention graphs for his own videos in YouTube Studio; after
each upload, drops get logged against script lines. That log outranks every rule here — including
the ones you are about to follow.

---

## 3. WHAT IS ALREADY INSTALLED

**The skill — already in place, nothing to do:**
```
C:\Users\renu5\.gemini\config\skills\script-system\SKILL.md
```
It is self-sufficient. It contains the phases, the locked rules, the conflict protocol, the
fact-check tiers, the score gate and the book-summary structure. It should auto-trigger on "write
a script", "analyse a reference video", "fact-check a script" and similar. **Do not create a second
scriptwriting skill** — two skills with overlapping descriptions trigger unpredictably.

**Reference files** — all in `C:\Users\renu5\Downloads\script writting idea\`:

| File | Read it when |
|---|---|
| `START-HERE.md` | You want the 10-step pipeline and timings |
| `MCP-SCRIPTWRITER.md` | You want the same flow as one paste-in prompt |
| `SCRIPT-SYSTEM.md` | He is using the vidIQ **website** instead of you; book-summary template is §8 |
| `FACT-CHECK.md` | Running a fact screen — has per-niche source directories |
| `SCORE-GATE.md` | Running the 100-point gate |
| `HANDOFF.md` | You need the full history and the measurements behind each rule |
| `OPUS-BRIEFING.md` | This file |

**Archive, do not use for writing:** `test1_forensic_report.md`, `test2_part1_audit.md`,
`complete_audit_*.md`, `testing_map all promtps.md`, and everything in `multi step prompt result/`
and `single prompt result/`. These are evidence for why the rules exist. Note that
`complete_audit_all_tests.md` still contains the **wrong 9.5/10 score** — it is superseded by
`HANDOFF.md` §3.

---

## 4. HOW TO RUN A SCRIPT

The skill carries the detail. The shape:

**Step 0 — packaging and pace, before anything else.**
- **Title first.** The hook exists to confirm the promise the viewer clicked on. No title → draft 3
  with `vidiq_generate_titles`, score with `vidiq_score_title`, agree one.
- **WPM.** Use his measured ElevenLabs WPM. If unknown, ask — or fall back to the references'
  measured WPM, and say so. 150 is a last resort and must come with a warning.
- **Budget.** Words = runtime × WPM. Hook cap and re-hook interval are set in **seconds**
  (hook 35–60 s by runtime) and converted to words with WPM.
- **Hook rotation.** Ask which hook types his last 3 videos used; don't repeat the last one.
  Templated sameness across a channel is a monetization risk under YouTube's inauthentic-content
  policy, not only a creative problem.

**Phase 1 — pull and analyse, then stop.** Pick references by **outlier ratio** (views ÷
subscribers), not raw views. Via vidIQ MCP: `vidiq_video_transcript`, `vidiq_video_comments`
(100+), `vidiq_video_stats`. Measure WPM. Filter comments: **timestamped comments first** ("3:45 got
me") — they point at moments that landed — then top-liked, flagging the jokes. Analyse hook (and
how it pays off the title), structure and its organising *principle*, re-hooks, transitions,
retention devices, voice, comment moments, and how the ending hands viewers on. With 2–3
references: what all do identically, where they diverge, what all fail to do. End with 5 numbered
carry-forward rules. Write no skeleton.

> The retention heatmap of **other people's** videos is not available through any vidIQ MCP tool.
> All 60 schemas were checked. Never claim or simulate it. For **his own** videos, YouTube Studio
> has it — that's the feedback loop, not your job during writing.

**Phase 2 — skeleton, then stop.** Word counts per section, never timestamps, plus a **visual
plan** per section. Flag any section whose claim has nothing to show.

**Phase 3 — three hooks + first half, then stop.** Three hooks of different allowed types, each
under the cap, each confirming the title. Recommend one. Then the first half, every paragraph
ending in a visual tag `[V: ...]`, or `[V: NONE]` where nothing can be shown.

**Phase 4 — second half + TTS version.** The ending hands the viewer a **specific next question**.
Then a clean TTS copy: phonetic spellings for unfamiliar names, numbers written as spoken, breath-
length sentences, plus a pronunciation list. Report totals and runtime at his WPM. Then tell him to
fact-check and score in a different conversation. **If he asks you to audit it yourself, refuse**
and explain why — that refusal is the single most valuable thing you do in this workflow.

**He approves at the end of phases 1, 2 and 3.** Do not run straight through.

---

## 5. WHAT IS LOCKED AND WHAT YOU MAY TUNE

**Locked (21 rules, each labelled [M] measured or [I] inferred).** The engagement and retention
format does not change for any niche: word counting · no numbered sections · no announced
structure · problem-door transitions · hook under cap, confirming the title, with a live stake in
sentence one and no self-disclaiming · **verdict payoff** · no mid-video comment prompt · ending
hands off to a next question · no YouTube video as a fact source · no range-to-point conversion ·
voice rules aimed at what a **listener hears** (two sections ending unresolved, one winding
sentence per section, no sentence template three times in a row, ≤1 honesty disclaimer, one thing
only this narrator could say) · a visual tag per paragraph · a TTS version before handoff.

Em-dash counting was removed: the script is narrated, and nobody hears an em-dash.

**Adjustable (8 dials).** Re-hook interval · consequence-beat flavour · humour register · section
count and length · opening device · number density · citation strictness · whether an open loop is
used at all. Say what you tuned and why.

**Conflict protocol.** If a niche genuinely requires breaking a locked rule, stop *before* writing
that section and give: the rule, the niche requirement, the case for each, a workaround if one
exists, and your recommendation with confidence. Then wait.

**A rule that merely makes writing harder is not a conflict — that is the rule working.** Do not
manufacture conflicts to appear thorough.

[I] rules yield more easily than [M] rules in a conflict — say which kind you are challenging.

Already resolved, do not raise: book summaries suspend open loops and the verdict becomes "the one
thing" · sleep/ambient long-form re-hooks every ~5 minutes · **procedural how-to content may
announce its structure**, because that viewer's goal is completion rather than curiosity · religion
and apocrypha separate "the text says X" from "X happened" · Shorts do not use this system at all ·
a sponsor read is not an engagement prompt.

---

## 6. THE AUDIT LAYER — this is what he actually depends on

**Fact-check.** Six things per source: title, authors, year, publication, openable URL/DOI, **and
the exact supporting sentence in quotes**. If you cannot quote it, you do not have it — write
UNVERIFIED. A confident wrong citation is worse for him than an admitted gap, because he will
publish it. Banned as sources: any YouTube video, AI output, content farms, Medium, Quora, Reddit,
and Wikipedia as a terminal source (mine its footnotes instead).

**Score gate.** 100 points — Craft 35, Retention 45 (the hook alone is 20, because the first 30
seconds is where most viewers leave), Integrity 20. Below 7.0 the script goes back. Every point
needs quoted evidence or a count. **Most scripts are a 6. Do not drift upward to be agreeable.**

**Calibration is against reality, not against anyone's opinion.** Score the 929K reference
transcript (expect 7.5+) and a flop from the same niche (expect ≤5). If the gate can't separate
them by 2.5+ points, it is measuring taste, and its scores mean nothing. (An earlier version
calibrated against one auditor's own score of the Ice Age script — circular, and that auditor's
number turned out to rest on a wrong WPM assumption.)

---

## 7. HOW TO TALK TO HIM

- He asked explicitly and repeatedly for **bluntness**, and for expert-level rather than generic
  responses. He has an `anti-sycophancy` skill installed for this reason. Give him the real number.
- He writes in long, fast, sometimes messy English and mixes several requests into one message.
  **Read every line before answering** — he has asked for this specifically, more than once. Things
  get buried mid-paragraph.
- When he asks "did you do X", he wants an honest accounting including what you did *not* do and
  why. Do not paper over a gap.
- Credits are not a constraint: ~150/month × ~10 Gmail accounts. Optimise for learning, not spend.
- He uses `humanizer` and `stop-slop` skills as a final pass. Do not duplicate their job.
- Scripts go into **ElevenLabs**. Write for the ear: names that TTS will mangle get phonetic
  guides, numbers get written as spoken.
- He runs faceless channels — every line needs something on screen. Tag visuals.
- He plans one video every 1–2 days, 4–8 hours each. Don't add steps that cost hours.
- **Watch for templated sameness** across his videos and channels. At his volume, it's the most
  likely monetization problem — more than AI use itself.

---

## 8. STATE AS OF 29 SEP 2026

**Done:** the whole system — skill, master prompt, fact-check, score gate, pipeline guide, handoff.

**Not done, and why:**
1. **Test 2 Part 2 (SRT upload to vidIQ web)** — requires him in a browser. Prompts ready in
   `HANDOFF.md` §7.
2. **Test 3 (MCP-driven script)** — this is what you are for. `MCP-SCRIPTWRITER.md` is Test 3,
   never yet run.
3. **No script has been written with this system yet.** The rules rest on one script vs one
   reference. Nothing is validated against a real upload.
4. **His TTS WPM hasn't been measured.** Every budget depends on it.
5. **The score gate is uncalibrated.** Nobody has scored the reference against a flop yet.
6. **Source directories were written from knowledge, not verified live.** SEC EDGAR, NTSB, NASA ADS
   are what they claim to be, but individual URLs were not opened.
7. **The Studio drop-off log is empty** — it starts with his first upload.

**Do first, in order:** measure his WPM (5 min) → calibrate the gate on reference vs flop
(15 min) → run one real script end to end → upload → start the drop-off log at day 7.

**Niche priority** from his channel research: business history (rise & fall) and megaprojects carry
the highest RPM ($8–20) with the lowest competition. Book summaries are the volume channel, not the
earnings channel. He has ruled out megaprojects for now as too effort-heavy — that is his call, do
not re-litigate it.
