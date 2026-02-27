---
name: 'step-04-review-export'
description: 'Review all approved ad variations, group by platform and campaign phase, update sidecar memories, and finalize export'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/ad-batch-generator'

# File References
thisStepFile: './step-04-review-export.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{campaign_assets}/ad-batch-{date}-{project_name}.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 4: Revisão & Exportação

## STEP GOAL:

To review all approved ad variations, group them by platform (Instagram, YouTube, TikTok) and campaign phase (awareness level), present a final summary, update sidecar memories with session data, and mark the workflow as complete. This step produces the final deployment-ready output.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🚀 GENERATE content proactively — YOU ARE A CONTENT GENERATOR

### Role Reinforcement:

- ✅ You are a VTSD batch generation specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ Speed Protocol: Batch Generation — optimize for volume and variety
- ✅ Maintain direct, production-focused tone — no praise, no filler
- ✅ This is the final step — focus on organization, export, and completion

### Step-Specific Rules:

- 🎯 Focus ONLY on reviewing, grouping, and finalizing the ad batch
- 🚫 FORBIDDEN to generate new ad variations (that was Step 3)
- 📝 Organize for deployment — group by platform and campaign phase
- 💾 Update sidecar memories with session learnings
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final review/export section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning review
- 🚫 FORBIDDEN to add new variations not generated in Step 3

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all approved variations from Step 3
- Focus: Review, grouping, export, and completion
- Limits: This is the final step
- Dependencies: All previous steps (1-3) must be completed

## MANDATORY SEQUENCE

### 1. Load Complete Document

Read the entire output document including all approved variations from Step 3.

### 2. Group by Platform

Organize all approved variations by target platform:

"**Agrupamento por Plataforma:**

### Instagram
| # | Headline | Format | Awareness Level | Angle |
|---|---|---|---|---|
| [#] | [headline] | [Static/Carousel/Story] | [level] | [angle] |
| ... | ... | ... | ... | ... |

### YouTube
| # | Headline | Format | Awareness Level | Angle |
|---|---|---|---|---|
| [#] | [headline] | [Video script] | [level] | [angle] |
| ... | ... | ... | ... | ... |

### TikTok
| # | Headline | Format | Awareness Level | Angle |
|---|---|---|---|---|
| [#] | [headline] | [Video script/Story] | [level] | [angle] |
| ... | ... | ... | ... | ... |"

### 3. Group by Campaign Phase

Organize the same variations by awareness level / campaign phase:

"**Agrupamento por Fase de Campanha:**

### Unaware / Problem-Aware
[Variations targeting early awareness — pain-focused, education-focused]

### Solution-Aware
[Variations targeting mid-funnel — comparison, proof, transformation]

### Product-Aware / Most Aware
[Variations targeting bottom-funnel — offer, urgency, social proof]"

### 4. Present Final Summary

"**Resumo Final do Ad Batch:**

| Metric | Count |
|---|---|
| **Total approved variations** | [X] |
| **By Platform:** | |
| — Instagram | [X] |
| — YouTube | [X] |
| — TikTok | [X] |
| **By Phase:** | |
| — Unaware / Problem-Aware | [X] |
| — Solution-Aware | [X] |
| — Product-Aware / Most Aware | [X] |
| **Frameworks used** | [list] |
| **Briefs covered** | [X/X] |

Any final adjustments before I finalize?"

### 5. Process Final Adjustments

If user wants adjustments:
- Make targeted re-grouping or re-classification as requested
- Re-present affected sections for confirmation

If no adjustments needed, proceed to step 6.

### 6. Update Sidecar Memories

Append to `{sidecarMemories}`:

```markdown
## Ad Batch Session — [current date] — {project_name}

- **Variations generated:** [total count]
- **Frameworks used:** [list]
- **Platforms covered:** [list]
- **Briefs processed:** [count]
- **Approval rate (first pass):** [X%]
- **Notes:** [any notable patterns, user preferences, or lessons learned]
```

### 7. Write Final Export Section

Write the complete review and export content under `## 4. Revisão & Exportação` in the output document (replacing the comment placeholder).

Include:
- Platform groupings with full variation details
- Campaign phase groupings
- Final summary statistics
- Data de Criação: [current date]
- Versão: 1.0

### 8. Mark Workflow Complete

Update the output document frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4]
lastStep: 'review-export'
status: 'COMPLETE'
completedDate: [current date]
```

### 9. Present Completion Summary

"**Ad batch complete for {project_name}.**

**Document saved to:** `{campaign_assets}/ad-batch-{date}-{project_name}.md`

**Results:**
- [X] ad variations ready for deployment
- Grouped by platform: Instagram ([X]), YouTube ([X]), TikTok ([X])
- Grouped by phase: Unaware/Problem-Aware ([X]), Solution-Aware ([X]), Product-Aware/Most Aware ([X])
- Session logged to sidecar memories for future reference

**What this enables:**
- Direct deployment to ad platforms
- A/B testing with pre-grouped variations
- Campaign phase alignment with funnel stages
- Performance tracking against this batch for future optimization

This batch is production-ready."

### 10. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any grouping or variation
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the ad batch
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#10-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the Ad Batch Generator workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- All approved variations reviewed and organized
- Grouped by platform (Instagram, YouTube, TikTok)
- Grouped by campaign phase (awareness level)
- Final summary presented with complete statistics
- Sidecar memories updated with session data
- Frontmatter marked as COMPLETE
- Output file path communicated clearly
- User satisfied with final batch

### ❌ SYSTEM FAILURE:

- Not reading the complete document before review
- Adding new ad variations not generated in Step 3
- Not grouping by platform AND campaign phase
- Missing final summary statistics
- Not updating sidecar memories
- Not marking workflow as COMPLETE in frontmatter
- Not saving final document state

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
