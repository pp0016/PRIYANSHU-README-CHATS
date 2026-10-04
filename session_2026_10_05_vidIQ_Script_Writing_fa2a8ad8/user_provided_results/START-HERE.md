# START HERE

| File | When you open it | How often |
|---|---|---|
| **START-HERE.md** (this) | To remember the order | Until you know it |
| **OPUS-BRIEFING.md** | Paste into a new Antigravity session so Opus has full context | New session |
| **MCP-SCRIPTWRITER.md** | Antigravity path — one paste, it drives | Every video (preferred) |
| **SCRIPT-SYSTEM.md** | vidIQ website path — prompts you drive | When Antigravity isn't available |
| **FACT-CHECK.md** | Every script, in a NEW conversation | Every video |
| **SCORE-GATE.md** | Every script, in a NEW conversation | Every video |
| ~~HANDOFF.md~~ | Full history, only for a new AI that needs it | Rarely |

In Antigravity the `script-system` skill loads all of this automatically — you open nothing.

---

## ONE-TIME SETUP — 25 minutes, do it before the first script

| # | Do this | Why | Time |
|---|---|---|---|
| 1 | **Measure your WPM.** ~200 words into ElevenLabs with your channel voice. Words ÷ audio minutes. | Every word budget depends on it. At 150 wpm a 15-min script is 2,250 words; at 240 it's 3,600. Guessing wrong makes every runtime wrong. | 5 min |
| 2 | **Calibrate the score gate.** Score the 929K reference transcript and a flop in the same niche (SCORE-GATE, top section). | If the gate can't separate a hit from a flop by 2.5+ points, its scores are opinion. | 15 min |
| 3 | **Start a hook log.** One line per video: date · title · hook type. | Rotating hook types stops the channel sounding templated. | 1 min |
| 4 | **Start a drop-off log.** Empty for now; filled after uploads. | This becomes your real rulebook. | 1 min |

---

## THE SCRIPT PIPELINE — about 2 hours

| # | What you do | Where | Time | Cost |
|---|---|---|---|---|
| 1 | **Title + thumbnail concept first.** The hook is written to pay it off. | vidIQ titles / MCP | 10 min | 0 AG |
| 2 | Fill the brief: topic, title, runtime, **your WPM**, references (pick outliers), last 3 hook types | MCP-SCRIPTWRITER | 5 min | — |
| 3 | Paste the master prompt. Approve at its 3 stops. It gives you 3 hooks — pick one. | Antigravity | 50 min | 0 |
| — | *Website instead:* SCRIPT-SYSTEM prompts 1 → 2 → 3 | vidIQ web | 50 min | 30cr |
| 4 | **Fact-check — NEW conversation** | FACT-CHECK.md | 20 min | 0 / 10cr |
| 5 | Open the 3 spot-check URLs, apply fixes, delete the cut list | you | 10 min | — |
| 6 | **Score — NEW conversation.** Below 7.0 goes back. | SCORE-GATE.md | 10 min | 0 / 10cr |
| 7 | `humanizer` or `stop-slop` skill on the final text | Antigravity | 5 min | 0 |
| 8 | Paste the **TTS version** into ElevenLabs. Listen to the first 60 seconds. | you | 10 min | — |

**Always run steps 4 and 6 on a different platform from the one that wrote the script.** Written in
Antigravity → check on vidIQ web, and the reverse. Two models, two sets of blind spots.

Step 8 replaces "read it aloud". The viewer hears the voice, not the text, so listen to the voice.
If the first 60 seconds don't hold you, they won't hold anyone.

---

## AFTER UPLOAD — the step that makes the whole system get better

You can't see the retention graph for other people's videos, but you **can** see it for your own,
in YouTube Studio → Analytics → Engagement → Audience retention.

At about **7 days** after upload:
1. Find every drop of 5 percentage points or more.
2. Find the script line playing at that moment.
3. Log it: `video · timestamp · line · suspected cause`.

**Three drops with the same cause becomes a new locked rule.** A rule marked [I] (inferred) that
keeps coinciding with no drop at all can be retired.

The current rules come from one script compared with one reference. After ten videos, this log will
be a better rulebook than anything written here. Nothing else in the system is ground truth.

---

## 10 THINGS TRUE BEFORE YOU RECORD

1. Word count ÷ **your** WPM matches the target runtime (±10%)
2. Hook is within its seconds cap, confirms the title, and doesn't undercut itself
3. Hook type differs from the last video's
4. No numbered sections, no announced structure
5. Payoff gives a verdict, not "maybe"
6. No comment prompt before the final 30 seconds; the ending points to a next question
7. No range turned into a single figure; no YouTube video cited as a source
8. Every paragraph has a visual; no `[V: NONE]` left
9. TTS version has phonetic spellings and spoken-form numbers
10. Fact-check and score gate both run in **fresh** conversations — score 7.0+

---

## THREE RULES YOU NEVER BREAK

1. **The auditor is never the author.** A session once graded its own script 9.5/10; an independent
   pass found four factual errors and the numbered listicle it had been told to avoid.
2. **Never trust a stated word count or runtime. Count.** vidIQ reported 2,360 words and wrote 2,803.
3. **No quoted source sentence = no source.** The only defence against invented citations.

---

## ON RUNNING MANY CHANNELS FROM ONE TEMPLATE

YouTube's monetization policy targets **inauthentic content** (renamed from "repetitious content"
in July 2025): mass-produced, templated videos that are only superficially different. AI help with
scripts is not the problem. **Sameness is.**

The system guards against it: hook rotation, three hook options per video, outlier references
chosen fresh each time, and the one-thing-only-this-narrator-could-say rule. Don't reuse one
niche analysis across dozens of videos, and don't let two channels share a voice, intro or
structure.

---

## WHAT TO BUILD NEXT — once the script pipeline is routine

1. **Title + thumbnail** — `youtube-thumbnail-pro`, `youtube-thumbnail-design` skills;
   `vidiq_score_thumbnail`
2. **Visuals from the `[V:]` tags** — the tags in each script are a ready-made shot list
3. **Voice + render** — `voiceover-enhancer-skill`, `ffmpeg-render-farm`, `remotion-render-farm`
4. **Signature audio identity** — prompt drafted in `complete_audit_all_tests.md` Part 2 Q3, never run

Ship five videos first. You'll find out which step actually hurts.
