# HANDOFF — vidIQ Scriptwriting Test Program

**Owner:** Priyanshu | **Channel:** faceless history/science explainer, Tier-1 audience
**Sessions:** Antigravity `fa2a8ad8-defd-4a7f-8191-3bd0a8f33cfb` (28 Sep) → Claude Code (29 Sep)
**Status:** Part 1 complete. Part 2 not run. Test 3 blocked. Read "Open Blockers" before planning.

---

## 1. What this program is testing

Can a reference video be reverse-engineered into a repeatable scriptwriting system that produces original, high-retention scripts — without hiring a scriptwriter, and without the owner having to re-read scripts many times to judge quality. (He cannot reliably judge English engagement for Tier-1 viewers. That limitation is the entire reason the audit layer exists.)

**Reference video — the only one used, do not substitute:**
`https://www.youtube.com/watch?v=wt_7Hp7d7I8` — "How Did Ancient Humans Survive Deadly Winters?" by Axen. 929,453 views, 10:24 runtime.

**Target script across all tests:** Ice Age survival, 15:00 runtime.

---

## 2. What was actually run

| # | Approach | Tool | Cost | Output file |
|---|---|---|---|---|
| Test 1 | Built-in Scriptwriter, "Match Reference Video" | vidIQ Scriptwriter | 10cr | `vidiq script writter result/builtin vidiq script writter result and there is option for refine.md` |
| Test 2 Step A | One-shot mega-prompt with engineered anti-patterns | vidIQ AI Coach | 10cr | `single prompt result/1-how-the-reference-video-is-built.md` |
| Test 2 Step A-fix | 4 targeted surgery fixes, same conversation | vidIQ AI Coach | 10cr | `single prompt result/Fix Prompt result for refine the scipt.md` |
| Test 2 Step B | 3-prompt multi-step (analysis → structure + half 1 → half 2) | vidIQ AI Coach | 30cr | `multi step prompt result/Multi-Step Prompt 1/2/3 ... result.md` |
| — | Step B halves assembled for TTS | manual | — | `multi step prompt result/full_script_for_11labs.md` |

All prompts verbatim: `testing_map all promtps.md` (same content as artifact `testing_map.md`).

---

## 3. CORRECTED SCOREBOARD — read this, not the old one

The artifact `complete_audit_all_tests.md` scores Step B at **9.5/10**. That score came from comparing the vidIQ outputs *to each other*. The script was never audited against itself. A second-pass audit (Claude Code, 29 Sep) on the assembled `full_script_for_11labs.md` found verifiable defects. Both scores are recorded; the second is the one to plan against.

> ### ⚠ Correction to this section (later on 29 Sep)
> The second-pass audit assumed **150 wpm** — documentary pace. Two sources in the test files put
> the reference video at **~230–250 wpm** (Test 1 report: ~2,600 words in 10:24; Step A notes:
> ~230 wpm). Fast narration is likely part of this niche's retention. At the reference's pace, the
> runtime and hook-length findings below **shrink substantially**; the word-count misreporting,
> structural, factual and voice findings **stand unchanged**. Revised score: **~6.5–7/10**, not
> 6.5. All budgets in the system now use a **measured WPM from the owner's TTS voice**, never a
> fixed number.

### Verified measurements — reproducible, just count the words

| Claim in the script docs | At 150 wpm (original audit) | At ~240 wpm (reference pace) |
|---|---|---|
| "15:00 runtime" | 2,803 words = 17:00–18:40 | 2,803 words ≈ **11:40** — *under* 15:00 |
| "~1,180 words per half" (2,360 total) | **2,803 actual** — off by 443 | same — this finding does not depend on pace |
| Hook labelled `[0:00–1:10]` | 316 words ≈ 2:02 | 316 words ≈ **1:19** — a little long, not a disaster |
| "Re-hook every 35–55 seconds" | 70–110 s | ~45–70 s — roughly as claimed |

What survives at any pace: **vidIQ misreported its own word counts by 443 words**, so no stated count or timestamp in its output can be trusted without counting. What does not survive: the claim that the hook runs 2 minutes and the video 17–18.

### Structural defects the first audit missed

1. **It is the listicle its own analysis said not to write.** Prompt 1 correctly identified the reference as *"a survival-priority ladder, not a chronological history — that's why it never feels like a list."* Prompt 2 then produced "Job One … Job Six," announced as a spoken table of contents at ~1:30. A spoken ToC is a reliable drop-off trigger.
2. **The hook retracts itself.** At ~60s: *"I am not going to pretend this is settled. It is not."* The mystery is introduced and withdrawn in the same breath. (The open runs about 1:20–2:00 depending on voice speed.)
3. **The payoff refuses to pay.** A 13-minute hibernation loop cashed with *"maybe. Probably not in the way the headline suggests."*
4. **Mid-video comments prompt** at 5:15 (*"Put your answer in the comments, and then keep watching"*) sends viewers out of the video. The payoff — "the doorway was a filter" — is guessable by anyone who has seen an igloo.
5. **A section that announces it does not belong** — snow goggles: *"this evidence is much later than the Ice Age, and it's Arctic rather than European."*

### Factual risks — comment-section exposure

- **"429 years" at Mezhyrich** — false precision. Radiocarbon yields a date range, not an occupancy duration. It is load-bearing under *"nobody rebuilds a bad idea for four hundred years."* **Fix before recording.**
- **600°C hearth** and **300,000-year bear-paw cut marks** are cited in the Prompt 2 proof list to *the reference video's own transcript* (`wt_7Hp7d7I8`). That is laundering an unverified source. Replace with primary citations or drop the precision.
- **Volgu dating** inconsistent: skeleton says 22,000–18,000, proof list says 21,000–18,000.
- **Yaghan elevated BMR** stated as settled. It is contested and diet-confounded.
- **Gough's Cave** is used both as "specialists say ritual" and as "a bad winter beat them." Pick one.

### AI-voice tells — answering "is it really humanised?"

**No.** Not vocabulary — rhythm and behaviour. In 2,803 words: 13 em-dashes (a text tell only — a listener never hears them, so the system no longer caps them); 12 short-fragment antithesis constructions ("Not a campfire. That is a kiln." / "Gross. Effective."); 5 paragraph-opening "Here's…" constructions; 3 separate honesty disclaimers ("I am not going to pretend…" / "I'm not going to tell you a tidy story…" / "I'd rather leave you there than hand you a fact that isn't one").

Every section lands on a tidy epigram — perfect closure on every beat is the clearest machine signature. The humour beat ("So the boiler is downstairs." / "Holstein.") has the correct shape of a joke and zero surprise. Locale mismatch: "neighbours"/"metre" beside "centimeters"/"Celsius". Nothing in the script only this person could have said — no wrong opinion, no digression, no dead end, no friction.

### Final scores

| | Antigravity (28 Sep) | Claude Code 2nd pass (29 Sep) |
|---|---|---|
| Test 1 Scriptwriter | 6/10 | 6/10 — agree; heavy paraphrase, hook near-identical to reference |
| Step A one-shot | 8/10 | 7.5/10 |
| Step A + fix | 8.5/10 | 8/10 — the fix genuinely repaired humour, closer, cannibalism, Yaghan |
| **Step B multi-step** | **9.5/10** | **~6.5–7/10** (revised after the WPM correction) |

**Realistic view ceiling for Step B as written** (script only, thumbnail/title held constant): new channel 200–3,000 · 50–100k-sub channel 15,000–40,000 · best case ~80k then stalls. These are judgement estimates, not measurements — no retention data exists for this script. The drivers are the numbered structure, the self-undercutting hook, the 5:15 comment prompt and the "maybe" payoff, none of which depend on voice speed. **It will not reproduce the reference's 929K.** The only real test is uploading and reading YouTube Studio's retention graph.

**On "multi-step wins every category":** not safe. Step A's hook — bone needle as mystery object, ~30 words, no retraction — is stronger than Step B's 316-word self-negating cave open. Step A + fix is arguably the better base script. Re-run the comparison before committing to multi-step as the house method.

---

## 4. The reusable formula — kept, with corrections

Derived from Prompt 1's forensic analysis of the reference. **That analysis is the single most valuable artifact the program produced and it is accurate.** The corrections below are where the *execution* diverged from it.

| Component | Formula | Correction |
|---|---|---|
| Hook | Mystery object or anomaly → open loop → stakes | **Max 45 seconds. Never retract the mystery inside the hook.** Put the viewer's body in it, not a distant site. |
| Structure | Deficit-ordered, not chronological; each section solves one problem | **Never number or pre-announce sections.** Structure must be felt, not narrated. |
| Transitions | Problem-door bridge: each section ends by naming its own flaw, which opens the next | Correct as written. Strongest single technique found. |
| Re-hooks | Every 35–55s, rotating type (mystery, contrast, authority, emotional hammer, tonal jolt) | Verify by **word count**, not by writing a timestamp label. Words = seconds × WPM ÷ 60 (35–55s ≈ 140–220 words at 240 wpm). |
| Retention | Delayed-payoff loop planted in hook, cashed in final quarter; second loop at midpoint | **The payoff must deliver a verdict.** "Here's what I think and why I could be wrong" beats "maybe." No mid-video comment prompts. |
| Voice | Short declaratives, fragment repetition, second-person ownership, confident + hedged mix, numbers as texture, casual winks | **Break the rhythm deliberately:** one long messy sentence per section, one section ending without a clean line, one admitted error mid-sentence. **Max one honesty disclaimer per script.** |
| Dark turn | One section breaking the feel-good tone with real human cost, at 60–70% | Correct as written. |
| Humour | One full tonal shift immediately after the dark turn (relief) | Must contain a genuine surprise, not just the shape of a joke. |
| Close | Philosophical reframe, no standalone CTA, engagement folded in | Correct as written. |

**Hard rule added:** word-count every section before assigning a timestamp, using the **measured WPM of the owner's TTS voice**. A 15:00 script is 2,250 words at 150 wpm and 3,600 at 240 — the pace decides the budget, so it must be measured, not assumed.

### Rule confidence — added 29 Sep

Every rule in this system came from **one script compared against one reference**. That is enough to act on, not enough to trust blindly. Rules are now labelled:

- **[M] measured** — traced to a concrete failure in the test files: word-count misreporting, numbered listicle, announced roadmap, self-undercutting hook, "maybe" payoff, mid-video comment prompt, YouTube cited as source, range→point, disclaimer overuse, universal epigram endings.
- **[I] inferred** — reasoned from craft knowledge, not measured: live stake in sentence one, winding-sentence rule, repetition limit, visual tags, TTS pass, next-video handoff, title-confirming hook.

**The feedback loop that replaces guessing:** the owner *can* see retention for his own videos in YouTube Studio. At ~7 days after each upload, log every drop of 5+ percentage points against the script line playing at that moment. Three drops with the same cause → new [M] rule. An [I] rule that repeatedly coincides with no drop → candidate to retire. After ~10 videos this log outranks every rule written here.

---

## 5. Answered questions — do not re-litigate

- **Can vidIQ MCP pull the YouTube retention heatmap (grey graph)?** **No.** All 60 schemas in `C:\Users\renu5\.gemini\antigravity\mcp\vidiq\` were checked. No tool exposes it; it is YouTube Studio internal data. Available instead: `vidiq_video_transcript`, `vidiq_video_comments`, `vidiq_comment_insights`, `vidiq_video_watch` (scene-by-scene, 25cr), `vidiq_video_stats`. Comments are the usable proxy — **timestamped comments first** ("3:45 got me"), then most-liked (many of which are jokes, not signals). For the owner's **own** videos, YouTube Studio shows the real retention graph — that is the ground truth.
- **Comments — manual copy-paste?** No. `vidiq_video_comments` handles threads, likes, replies, pagination.
- **Does vidIQ accept two reference videos?** **No.** Both Scriptwriter and AI Coach attach exactly one video via "Add from YouTube." A second link pasted as text is ignored. Blending multiple references is the one thing only the MCP/Opus path can do.
- **YouTube AI detection / monetization?** AI assistance itself is not the problem. The risks are (1) near-copies of another video's transcript — Test 1 was a 60–70% paraphrase and was the real risk; and (2) YouTube's **inauthentic content** policy (renamed from "repetitious content" in July 2025), which targets mass-produced, templated videos that differ only superficially. The second risk grows with one template at one video a day — hence hook rotation, three hook options per video, and fresh outlier references each time. Step A and Step B are original in content and wording.
- **Credits are not a constraint.** ~150/month × ~10 Gmail accounts ≈ 1,500 credits. Optimise for learning, not for credit spend.

---

## 6. Open blockers

1. **Test 3 (MCP-driven script) cannot run in Claude Code.** The vidIQ MCP server is registered in Antigravity, not in this environment — only the JSON schemas exist on disk here. Run Test 3 from Antigravity, or add the vidIQ MCP to Claude Code first.
2. **Test 2 Part 2 (SRT upload) requires the owner in a browser.** Prompt pack in section 7.
3. **Unresolved fork:** does the house method become Step A + fix (one-shot + surgery, 20cr) or Step B multi-step (30cr)? The 2nd-pass audit puts Step A + fix ahead. Decide before building a pipeline on either.

---

## 7. Remaining work

### Test 2 Part 2 — SRT upload (ready to run, owner action)

Hypothesis: feeding vidIQ the raw SRT/transcript produces a better analysis than letting it watch a YouTube link.

Method: download the SRT for `wt_7Hp7d7I8`, attach it via "Attach image or file" in AI Coach on a fresh Gmail, and run the same 3 prompts from `testing_map all promtps.md` Step B — with these amendments, which patch the three defects found in Part 1:

**Append to Prompt 2:**
> Word-count every section as you write it and state the count. Use <MY WPM> words per minute to convert to timestamps. Do not write a timestamp you have not counted. Total spoken script must be 15 × <MY WPM> words (±5%) for a 15:00 runtime.
>
> Do not number the sections and do not announce the structure to the viewer. No "Job One / Job Two." No list of what is coming. Each section must arrive through the previous section's unsolved problem.

**Append to Prompt 3:**
> The final payoff must give a verdict, not a shrug. State what you think is most likely and why you could be wrong. Do not end on "maybe." Use at most one honesty disclaimer in the entire script.

Cost 30cr. Compare against Part 1 Step B on four measurables: hook length in words, whether sections are numbered, whether the payoff delivers a verdict, total word-count accuracy.

### Test 3 — MCP-driven script (blocked, see section 6)

Now built: `MCP-SCRIPTWRITER.md` and the `script-system` skill. Pulls transcripts + timestamped comments from 2–3 outlier references via MCP, analyses in-model, writes the script with three hook options, visual tags and a TTS version. **The audit is never self-audit** — fact-check and score gate run in a separate conversation. This is the only path that can blend multiple references. Cost: 0 web credits.

### Channel branding prompts (drafted, never run)

Two prompts to give both vidIQ AI Coach and a fresh Opus conversation — a signature 2–3 second audio identity (5 recreatable concepts) and 15–20 non-obvious details that make a faceless channel look premium. Full text in `complete_audit_all_tests.md`, Part 2, Q3.

---

## 8. Next action

1. **Measure the TTS voice's WPM** (5 min) — every budget depends on it.
2. **Calibrate the score gate** on the 929K reference transcript vs a flop in the niche (15 min) — if it can't separate them by 2.5+ points, its scores are opinion.
3. Run one real script end to end with `MCP-SCRIPTWRITER.md`, upload, and start the Studio drop-off log.

The Ice Age script is now a learning reference only. If it is ever recorded, fix the Mezhyrich "429 years" claim and the two reference-video-sourced citations first.

---

## 9. File map

**Antigravity artifacts** — `C:\Users\renu5\.gemini\antigravity\brain\fa2a8ad8-defd-4a7f-8191-3bd0a8f33cfb\`
`complete_audit_all_tests.md` (superseded on scoring by section 3 above) · `test1_forensic_report.md` · `test2_part1_audit.md` · `testing_map.md`
Transcript: `.system_generated\logs\transcript_full.jsonl` (114 entries)

**Test outputs** — `C:\Users\renu5\Downloads\script writting idea\` — see the table in section 2.

**vidIQ MCP schemas** — `C:\Users\renu5\.gemini\antigravity\mcp\vidiq\` (60 tools)

**Skills** — `C:\Users\renu5\.gemini\config\skills\` : `vidiq-website-capabilities`, `vidiq-youtube-creator`, `anti-sycophancy`
