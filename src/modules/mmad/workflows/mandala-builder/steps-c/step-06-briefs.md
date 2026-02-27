---
name: 'step-06-briefs'
description: 'Generate production briefs for each prioritized cell in the Mandala matrix'

# File References
nextStepFile: './step-07-consolidation.md'
outputFile: '{campaign_assets}/mandala-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 6: Briefs de Produção — PRESCRIPTIVE

## STEP GOAL:

To generate production briefs for each ★★★ and ★★ cell in the priority matrix. This is a fully PRESCRIPTIVE step — use the Speed Protocol: Batch Generation to produce briefs at volume, presenting batches of 3-5 for review. Target: 15-30 briefs total.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- ⚡ GENERATE content proactively — YOU ARE A CONTENT GENERATOR
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🚀 Speed Protocol: Batch Generation — optimize for volume and variety

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ You bring creative brief expertise and format knowledge, the user brings approval and direction
- ✅ Maintain direct, productive tone — focus on output quality and volume

### Step-Specific Rules:

- ⚡ GENERATE content proactively — YOU ARE A CONTENT GENERATOR
- 🚀 Speed Protocol: Batch Generation — optimize for volume and variety
- 📦 Present for review in batches (3-5 briefs per batch)
- 🎯 Each brief must reference its specific awareness level + creative type cell
- 📝 All document output in {document_output_language} (Brazilian Portuguese)
- 🔄 User can approve, modify, or request alternatives per brief

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- ⚡ GENERATE briefs proactively — do not wait for user to dictate content
- 📦 Present in batches of 3-5 — collect feedback — iterate — continue
- 🎯 Cover all ★★★ cells first, then ★★ cells

## CONTEXT BOUNDARIES:

- Available context: step-02 (campaign context, ICP, tone, offer), step-03 (awareness levels), step-04 (creative types), step-05 (priority matrix)
- Focus: Production brief generation ONLY
- Limits: Do not write actual ad copy — these are briefs/directions for production
- Dependencies: Steps 2-5 must be completed

## MANDATORY SEQUENCE

### 1. Load Matrix and Context

Read the existing output document to review:

- Priority matrix from step 5 (which cells are ★★★, ★★, ★)
- Campaign context from step 2 (product/offer, objective, ICP, tone)
- Selected awareness levels from step 3
- Selected creative types from step 4

Calculate production plan:

"**Production Plan:**
- ★★★ Priority cells: [list] — generating briefs now
- ★★ Secondary cells: [list] — generating after priorities
- Target: [N] briefs total

Starting with ★★★ cells. Here's the first batch:"

### 2. Generate Briefs — Batch by Batch

For each prioritized cell, GENERATE a production brief containing:

**Brief Template:**

```
### Brief [#]: [Awareness Level] × [Creative Type]

**Nível de Consciência:** [level]
**Tipo de Criativo:** [type]
**Ângulo/Gancho:** [suggested angle or hook — what grabs attention]
**Formato Recomendado:** [reels, carrossel, story, estático, vídeo longo, UGC, etc.]
**Mensagem-Chave:** [the core message this ad must communicate]
**CTA:** [specific call-to-action type and direction]
**Plataforma:** [Instagram, Facebook, YouTube, TikTok, etc.]
**Notas de Produção:** [any specific production notes — visual style, duration, references]
```

Present in batches of 3-5 briefs:

"**Batch 1 — ★★★ Priority Briefs:**

[Brief 1]
[Brief 2]
[Brief 3]

Review these briefs:
- ✅ Approve as-is
- ✏️ Request modifications (specify which brief and what to change)
- 🔄 Request alternative angle for any brief
- ➡️ All good, show me the next batch"

### 3. Iterate per Batch

For each batch:

- Collect user feedback
- Modify briefs as requested
- Generate alternative angles if requested
- Once batch is approved, move to next batch
- Track approved briefs count

Continue until all ★★★ cells have briefs.

### 4. Secondary Briefs (★★ Cells)

After all ★★★ briefs are approved:

"All [N] priority briefs approved. Moving to ★★ secondary cells. These expand your creative variety.

**Batch [N] — ★★ Secondary Briefs:**

[Brief N+1]
[Brief N+2]
[Brief N+3]"

Continue batch generation for ★★ cells.

### 5. Production Summary

After all briefs are generated and approved:

"**Brief Generation Complete:**

- ★★★ Priority briefs: [N] approved
- ★★ Secondary briefs: [N] approved
- Total briefs: [N]

**Breakdown by Awareness Level:**
- [Level 1]: [N] briefs
- [Level 2]: [N] briefs
- [Level 3]: [N] briefs

**Breakdown by Creative Type:**
- [Type 1]: [N] briefs
- [Type 2]: [N] briefs
- [Type 3]: [N] briefs
- ...

All briefs are ready for the next step — consolidation and batch extraction."

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save all approved Production Briefs to {outputFile} under the `## 5. Briefs de Produção` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `6`, update `lastStep` to `briefs`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting each batch
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and all Production Briefs have been saved to the output file, will you then load and read fully `./step-07-consolidation.md` to execute and begin Consolidation.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Briefs generated proactively using Speed Protocol
- All ★★★ cells have at least one approved brief
- All ★★ cells have at least one approved brief (if capacity allows)
- Briefs presented in batches of 3-5 for review
- User feedback incorporated per batch
- Each brief contains: awareness level, creative type, angle, format, message, CTA, platform
- Production summary with breakdowns presented
- Target of 15-30 briefs achieved
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Waiting for user to dictate brief content instead of generating proactively
- Presenting all briefs at once instead of in batches
- Generating briefs for skipped (-) cells
- Briefs missing required fields (level, type, angle, format, message, CTA, platform)
- Not collecting feedback per batch
- Producing fewer than 15 briefs without explicit user decision
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
