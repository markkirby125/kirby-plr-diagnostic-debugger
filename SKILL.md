---
name: kirby-plr-diagnostic-debugger
description: "Use when auditing or surgically repairing rewritten PLR for tone drift, forced stories, or residual PLR slop."
category: quality
triggers: [audit-plr, fix-plr-tone, check-plr-slop, debug-plr-rewrite, content-doctor, tone-debugger]
risk: unverified
author: william-fitzpatrick
tags: [kirby, ai-agent, workflow]
---

# SOP: 15-Point PLR Diagnostic & Surgical Debugging Suite

> Standard Operating Procedure for auditing, diagnosing, and repairing flawed or partially personalized PLR content. Uses a strict 15-point heuristic to identify and eliminate synthetic tone, forced anecdotes, and residual PLR stench.

**Related:** Rewrites from raw PLR are `kirby-plr-personalizer`. Voice/audience/story files are `voice_dna.yaml`, `audience_profile.yaml`, `storyline_bank.json`. Do not use `de-genericize` here — that trigger belongs to the personalizer.

---

## 1. The 15-Point Diagnostic Breakdown & Repair Protocols

### Cluster 1: Tone & Voice Correction

#### 1. Too Formal / Corporate Sounding
* **Symptom:** Reads like a legal brief or enterprise whitepaper. Uses passive voice (*"Mistakes were made by the team"*).
* **Repair:** Force contractions (*don't, can't, wouldn't*), swap multisyllabic Latinate verbs for Anglo-Saxon root words (*utilize -> use, elucidate -> show*), and insert conversational transitions (*"Look,"*, *"Here's the deal:"*).

#### 2. Too Casual / Unprofessional
* **Symptom:** Sloppy grammar, excessive slang, juvenile jokes that destroy author authority.
* **Repair:** Strip forced slang; maintain peer-level respect while keeping crisp, authoritative sentence boundaries.

#### 3. Inconsistent Voice Throughout (Tone Drift)
* **Symptom:** Intro is punchy and personal; middle sections revert to textbook dry advice.
* **Repair:** Re-anchor paragraphs 3-8 with the author's Voice DNA cadence; add 1-2 sentence parenthetical reactions.

#### 4. Missing Personality Completely
* **Symptom:** Accurate facts, zero emotional pulse. Indistinguishable from raw PLR.
* **Repair:** Inject strong, polarizing opinions. Challenge a common belief in the topic area.

#### 5. Wrong Emotional Tone for Topic
* **Symptom:** Overly cheerful while discussing financial crisis, or overly dramatic while discussing minor productivity tips.
* **Repair:** Calibrate mood to match the reader's real emotional state (empathy for struggle, urgency for deadline).

---

### Cluster 2: Story Integration Fixes

#### 6. Story Feels Forced / Disconnected
* **Symptom:** *"Goal setting is key. Once I went to Mexico and drank coffee. Anyway, goals are..."*
* **Repair:** Build an explicit pivot bridge: identify the precise moment of realization in the story that directly caused the rule/lesson being taught.

#### 7. Story Is Too Vague / Generic
* **Symptom:** *"A while ago, I faced a challenge with a client and it was tough."*
* **Repair:** Add sensory and numeric specificity: *"On a Tuesday in October 2022, a client withholding a $4,500 check sent an email saying..."*

#### 8. Multiple Stories Are Competing
* **Symptom:** Two different anecdotes in a 500-word post confusing the reader's focus.
* **Repair:** Cull the secondary story; expand the emotional depth and concrete details of the primary story.

#### 9. Story Doesn't Connect to Audience
* **Symptom:** Author talks about a $500,000 corporate software bug to an audience of solo handmade soap makers.
* **Repair:** Swap or re-frame the stakes so the financial or emotional scale matches the reader's reality.

#### 10. Missing the Lesson / Application
* **Symptom:** Great entertainment, zero takeaway. The reader says *"Cool story, but what do I do?"*
* **Repair:** Add the **"Now What?" Hand-Off Protocol**: 3 concrete action items the reader can take today based on the lesson.

---

### Cluster 3: Audience Alignment Adjustments

#### 11. Examples Don't Match Audience Reality
* **Symptom:** Recommending expensive enterprise tools (Salesforce, Marketo) to bootstrap solopreneurs.
* **Repair:** Replace tool names with accessible, low-friction alternatives (Airtable, Make, ConvertKit).

#### 12. Wrong Language / Terminology for Audience
* **Symptom:** Using academic marketing terms where the niche uses street slang.
* **Repair:** Run `kirby-audience-intel-profiler` lexicon swap to replace all generic labels.

#### 13. Addressing Wrong Pain Points
* **Symptom:** Focusing on time management when the audience is losing sleep over cash flow.
* **Repair:** Pivot the framing: show how the time bottleneck is the hidden culprit behind their cash crunch.

---

### Cluster 4: Generic-to-Authentic Transformation

#### 14. Content Still Sounds Like PLR
* **Symptom:** Sentences begin with: *"It is important to remember that..."*, *"Moreover, another crucial factor..."*
* **Repair:** Delete the first 2 sentences of every section. Start directly with the core friction or strong verb.

#### 15. Missing Unique Value Proposition (UVP)
* **Symptom:** The advice is identical to the top 10 Google search results.
* **Repair:** Introduce a **Proprietary Counter-Intuitive Rule** (e.g., *"Why you should intentionally ignore 80% of your incoming leads"*).

---

## 2. Surgical Diagnostic Audit Execution

Execute the diagnostic audit using the following directives:

**Inputs Required:**
1. **CANDIDATE DRAFT:** {{INSERT_DRAFT_TEXT}}
2. **AUDIENCE:** `audience_profile.yaml` (run `kirby-audience-intel-profiler` if missing)
3. **VOICE:** `voice_dna.yaml` (run `kirby-voice-dna-extractor` if missing)
4. **STORIES:** `storyline_bank.json` (run `kirby-storyline-bank` if a story swap is needed)

**Audit Instructions:**
1. Scan for the 15 defect classes across the 4 clusters.
2. Flag every detected defect with an exact quote and line location.
3. For each flagged defect, provide the immediate surgical rewrite that fixes the problem without expanding fluff.
4. Output the final, clean, production-certified version.
5. Confirm `audience_profile.yaml` and `voice_dna.yaml` were loaded before certifying.


## Examples

*(Add specific conversational examples here showing how the agent should behave.)*


## Limitations (When NOT to Use)

- Do not use this skill outside of its intended scope.
- Stop and ask the user for clarification if the requirements are ambiguous.
