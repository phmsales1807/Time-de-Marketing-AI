---
name: 'step-03-generate'
description: 'Execute Speed Protocol batch generation of 20-40 ad copy variations across all briefs and frameworks'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/ad-batch-generator'

# File References
thisStepFile: './step-03-generate.md'
nextStepFile: './step-04-review-export.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{campaign_assets}/ad-batch-{date}-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 3: Geração em Lote (Batch Generation)

## STEP GOAL:

To execute the core batch generation engine — producing 20-40 ad copy variations across all production briefs using the assigned copy frameworks. Each variation includes headline, body copy, CTA, platform recommendation, and format note. Present in review batches of 5-10 variations. This is the Speed Protocol in action.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🚀 GENERATE content proactively — YOU ARE A CONTENT GENERATOR

### Role Reinforcement:

- ✅ You are a VTSD batch generation specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ You bring copy frameworks and batch generation methodology, the user reviews and approves
- ✅ Speed Protocol: Batch Generation — optimize for volume and variety
- ✅ Maintain direct, production-focused tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on generating ad copy variations at scale
- 🚀 **Speed Protocol: Batch Generation** — this is the core generation engine
- 📦 Present for review in batches of 5-10 variations — NEVER dump all at once
- ✏️ Each variation MUST include: headline, body copy, CTA, platform recommendation, format note
- 🎯 Target: 2-4 variations per brief × framework combination = 20-40 total
- 📝 All ad copy output in {document_output_language} (Brazilian Portuguese)
- 🔄 After each batch: ask for approval, modifications, or regeneration

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track approved/modified/regenerated counts throughout the session
- 🚀 GENERATE variations proactively — do not wait for user prompts between batches
- 📦 Present in manageable review batches (5-10 variations)

## CONTEXT BOUNDARIES:

- Available context: Production briefs, framework assignments from Step 2, Brand Brief tone
- Focus: Ad copy generation ONLY
- Limits: Do not organize by platform yet (that's Step 4)
- Dependencies: Framework assignments must be complete (Step 2)

## MANDATORY SEQUENCE

### 1. Load Generation Blueprint

Read the existing output document to confirm framework assignments from Step 2.

Calculate total generation targets:

"**Generation Blueprint:**
- Production briefs: X
- Framework assignments: [list]
- Target per brief: 2-4 variations
- Total target: [X × 2-4] = Y-Z variations
- Batch size: 5-10 variations per review cycle

Starting batch generation now."

### 2. Generate Batch 1

For the first set of briefs × framework combinations, generate 5-10 ad copy variations.

Each variation follows this format:

"**Variation [#] — Brief [#] | [Framework] | [Angle]**

**Headline:** [Attention-grabbing headline aligned with awareness level]

**Body Copy:**
[2-4 sentences applying the assigned framework structure. Use Brand Brief tone. Reference ICP pain/desire from the brief angle.]

**CTA:** [Clear call-to-action appropriate for awareness level]

**Platform:** [Instagram / YouTube / TikTok — based on creative type and format fit]

**Format:** [Static / Carousel / Video script / Story — based on creative type from brief]

---"

Present the batch:

"**Batch 1 — Variations 1-[X]:**

[All variations in the batch]

**Approve these? Options:**
- ✅ Approve all
- ✏️ Modify specific variations (tell me which # and what to change)
- 🔄 Regenerate specific variations (tell me which #)
- 💬 Any other feedback"

### 3. Process Batch Feedback

For each batch:

- **If approved:** Mark as approved, track count
- **If modifications requested:** Apply changes, re-present modified variations for confirmation
- **If regeneration requested:** Generate fresh alternatives for specified variations, present for review
- **If feedback given:** Incorporate into next batch generation

### 4. Generate Subsequent Batches

Continue generating batches of 5-10 variations until all briefs have approved variations.

For each new batch:

"**Batch [N] — Variations [X]-[Y]:**

[All variations in the batch]

**Running total: [approved] approved / [modified] modified / [regenerated] regenerated**

**Approve these?**"

Repeat the generate → review → approve cycle until all briefs are covered and total target (20-40) is reached.

### 5. Generation Summary

Once all batches are complete:

"**Batch Generation Complete:**

| Metric | Count |
|---|---|
| Total variations generated | [X] |
| Approved on first pass | [X] |
| Modified | [X] |
| Regenerated | [X] |
| Final approved total | [X] |

**Briefs covered:** [X/X]
**Frameworks used:** [list]

All variations ready for platform grouping and export in Step 4."

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save ALL approved variations to {outputFile} under the `## 3. Variações Geradas` heading (replacing the comment placeholder), grouped by angle/type, update frontmatter `stepsCompleted` to add `3`, update `lastStep` to `generate`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and ALL approved variations have been saved to the output file, will you then load and read fully `./step-04-review-export.md` to execute and begin review and export.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- 20-40 ad copy variations generated across all production briefs
- Each variation includes: headline, body copy, CTA, platform recommendation, format note
- Variations presented in review batches of 5-10 (never all at once)
- User approved/modified/regenerated each batch
- Approved/modified/regenerated counts tracked throughout
- Brand Brief tone consistently applied across all variations
- Framework structures correctly applied to each variation
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating fewer than 20 variations total
- Dumping all variations at once instead of batches
- Missing components (no headline, no CTA, no platform recommendation)
- Not applying assigned frameworks correctly
- Not tracking approved/modified/regenerated counts
- Proceeding without user approval of each batch
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
