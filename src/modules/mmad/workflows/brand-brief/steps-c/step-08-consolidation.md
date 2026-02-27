---
name: 'step-08-consolidation'
description: 'Compile and review the final Brand Brief document'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-08-consolidation.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 8: Consolidação

## STEP GOAL:

To compile all 6 sections into a coherent, final Brand Brief document. Review the complete document with the user, make any final adjustments, and mark the workflow as complete. This document becomes the "mother document" that feeds all downstream MMAD workflows.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a brand architecture and strategic positioning specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ You bring strategic method, the user brings deep business knowledge
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on reviewing, refining, and completing the document
- 🚫 FORBIDDEN to add new content sections not discussed in previous steps
- 💬 Ask targeted questions about gaps or inconsistencies you notice
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final consolidation section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning consolidation
- 🚫 FORBIDDEN to fundamentally change previous sections without user consent

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all 6 sections filled
- Focus: Consolidation, coherence check, final adjustments
- Limits: This is the final step
- Dependencies: All previous steps (2-7) must be completed

## MANDATORY SEQUENCE

### 1. Load Complete Document

Read the entire output document including all 6 completed sections.

### 2. Present Consolidation Overview

"All 6 sections of your Brand Brief are complete. Let me present the full document for review.

**Brand Brief — {project_name}**"

Display the complete document content — all sections, concisely formatted.

### 3. Coherence Check

Review the document for internal consistency and present observations:

"Here's what I notice about coherence:

- **Problem → ICP alignment:** [observation]
- **ICP → Positioning alignment:** [observation]
- **Positioning → Tone alignment:** [observation]
- **Tone → Promise alignment:** [observation]
- **Promise → Narrative alignment:** [observation]

Any gaps or contradictions? Anything that feels off when you read it as a whole?"

Ask 1-2 specific questions if you spot inconsistencies.

### 4. Final Adjustments

If the user wants adjustments:

- Make targeted edits to specific sections as requested
- Update the output document with changes
- Re-present the adjusted sections for confirmation

If no adjustments needed, proceed to step 5.

### 5. Write Consolidation Section

Write a brief consolidation section under `## 7. Consolidação` in the output document:

This section should contain in {document_output_language}:

- **Síntese Estratégica:** A 2-3 paragraph executive summary that ties all elements together
- **Próximos Passos Recomendados:** List of downstream workflows this Brand Brief enables (Mandala Builder, Content Plan, Funnel Design, etc.)
- **Data de Criação:** Current date
- **Versão:** 1.0

### 6. Mark Workflow Complete

Update the output document frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4, 5, 6, 7, 8]
lastStep: 'consolidation'
status: 'COMPLETE'
completedDate: [current date]
```

### 7. Present Completion Summary

"**Brand Brief complete for {project_name}.**

**Document saved to:** `{brand_assets}/brand-brief-{project_name}.md`

**What this enables:**
- Mandala Builder (VTSD) — visual territory and semantic design
- Content Strategist — content planning aligned with brand DNA
- Funnel Architect — funnel design using your positioning
- Copywriter — all copy will follow your tone of voice
- Ad Batch Generator — ads built on your promise and ICP

This document is the foundation. Every downstream workflow will reference it."

### 8. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any section
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the brief
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#8-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the Brand Brief workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Complete document reviewed with user
- Coherence check performed across all sections
- Any inconsistencies identified and resolved
- Consolidation section written with strategic synthesis
- Frontmatter marked as COMPLETE
- Next steps communicated clearly
- User satisfied with final document

### ❌ SYSTEM FAILURE:

- Not reading the complete document before consolidation
- Adding new content not discussed in previous steps
- Not performing coherence check
- Not marking workflow as COMPLETE in frontmatter
- Generating consolidation content without user review
- Not saving final document state

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
