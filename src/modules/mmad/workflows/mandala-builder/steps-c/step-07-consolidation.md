---
name: 'step-07-consolidation'
description: 'Compile final Mandala document, extract batch briefs, update sidecar memories, and mark workflow complete'

# File References
outputFile: '{campaign_assets}/mandala-{project_name}.md'
batchBriefsFile: '{campaign_assets}/batch-briefs-{project_name}.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 7: Consolidação — FINAL STEP

## STEP GOAL:

To compile the final Mandala document, perform a coherence check across all sections, write the consolidation section, extract batch briefs into a separate file for production handoff, update sidecar memories with session summary, and mark the workflow as complete.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 Focus on review, compilation, and extraction — not new content generation

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ You bring method expertise for quality review, the user brings final approval
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on reviewing, consolidating, extracting, and completing
- 🚫 FORBIDDEN to add new briefs or content sections not discussed in previous steps
- 💬 Ask targeted questions about gaps or inconsistencies you notice
- 📝 All document output in {document_output_language} (Brazilian Portuguese)
- 📤 Extract batch briefs into separate file for production handoff
- 💾 Update sidecar memories with session summary

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final consolidation section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning consolidation
- 🚫 FORBIDDEN to fundamentally change previous sections without user consent

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all 5 content sections filled
- Focus: Consolidation, coherence check, batch extraction, sidecar update
- Limits: This is the final step
- Dependencies: All previous steps (2-6) must be completed

## MANDATORY SEQUENCE

### 1. Load Complete Document

Read the entire output document including all 5 completed sections:

- Section 1: Contexto da Marca (campaign context)
- Section 2: Fases do Funil (selected awareness levels)
- Section 3: Tipos de Criativos (selected creative types)
- Section 4: Matriz de Prioridades (priority matrix)
- Section 5: Briefs de Produção (production briefs)

### 2. Present Mandala Overview

"All 5 sections of your Mandala da Criatividade Infinita are complete. Let me present the full picture.

**Mandala da Criatividade Infinita — {project_name}**"

Present a concise overview:

- Campaign context summary (1-2 lines)
- Selected awareness levels with priorities
- Selected creative types
- Matrix summary: total cells, priority distribution
- Total briefs generated with breakdown

### 3. Coherence Check

Review the document for internal consistency and present observations:

"Here's what I notice about coherence across the Mandala:

- **Contexto → Níveis de Consciência alignment:** [observation — do selected levels match the campaign objective and ICP?]
- **Níveis → Tipos de Criativos alignment:** [observation — do selected types serve the selected awareness levels?]
- **Matriz → Briefs alignment:** [observation — do all priority cells have briefs? Are brief angles consistent with cell purpose?]
- **Tom de Voz consistency:** [observation — do briefs maintain the brand's tone across all awareness levels?]
- **CTA progression:** [observation — do CTAs escalate appropriately from lower to higher awareness?]
- **Platform coverage:** [observation — is there adequate variety across platforms?]

Any gaps or contradictions? Anything that feels off when you see the full picture?"

Ask 1-2 specific questions if you spot inconsistencies.

### 4. Final Adjustments

If the user wants adjustments:

- Make targeted edits to specific sections or briefs as requested
- Update the output document with changes
- Re-present the adjusted elements for confirmation

If no adjustments needed, proceed to step 5.

### 5. Write Consolidation Section

Write a consolidation section under `## 6. Consolidação` in the output document:

This section should contain in {document_output_language}:

- **Síntese da Mandala:** A 2-3 paragraph summary that ties all elements together — the campaign logic, creative strategy, and expected output
- **Números Finais:**
  - Total de briefs gerados: [N]
  - Briefs prioritários (★★★): [N]
  - Briefs secundários (★★): [N]
  - Níveis de consciência cobertos: [list]
  - Tipos de criativos utilizados: [list]
- **Distribuição por Prioridade:**
  - ★★★ cells: [list with brief count per cell]
  - ★★ cells: [list with brief count per cell]
- **Recomendações para Produção:**
  - Sequência de produção sugerida (start with highest-impact cells)
  - Formato de teste A/B recomendado
  - Métricas de acompanhamento por tipo de criativo
- **Data de Criação:** Current date
- **Versão:** 1.0

### 6. Extract Batch Briefs

Create a separate batch briefs file at `{batchBriefsFile}`:

This file should contain:

```markdown
---
project_name: {project_name}
source_mandala: '{outputFile}'
total_briefs: [N]
date: [current date]
status: 'READY_FOR_PRODUCTION'
---

# Batch Briefs — {project_name}

## Production Queue

### ★★★ Priority Briefs

[All ★★★ briefs extracted from section 5, numbered sequentially]

### ★★ Secondary Briefs

[All ★★ briefs extracted from section 5, numbered sequentially]
```

Inform user: "Batch briefs extracted to `{batchBriefsFile}` — ready for production handoff to Ad Batch Generator or creative team."

### 7. Update Sidecar Memories

Append a session summary to `{sidecarMemories}`:

```markdown
## Mandala Session — {project_name} — [current date]

- **Campaign:** [campaign objective from step 2]
- **Awareness Levels Used:** [list from step 3]
- **Creative Types Used:** [list from step 4]
- **Total Briefs Generated:** [N]
- **Priority Distribution:** [★★★: N, ★★: N, ★: N]
- **Notes:** [any relevant observations — what combinations showed high potential, user preferences, etc.]
```

### 8. Mark Workflow Complete

Update the output document frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4, 5, 6, 7]
lastStep: 'consolidation'
status: 'COMPLETE'
completedDate: [current date]
```

### 9. Present Completion Summary

"**Mandala da Criatividade Infinita complete for {project_name}.**

**Documents saved:**
- Mandala document: `{outputFile}`
- Batch briefs: `{batchBriefsFile}`

**What this enables:**
- Ad Batch Generator — use batch briefs to produce final ad variations at scale
- Copywriter — write copy for each brief following the angle and message direction
- Content Strategist — integrate Mandala output into the content calendar
- Creative Team — production queue with prioritized briefs and format specs

**Sidecar updated** — this session's creative history will inform future Mandala builds.

This Mandala is your creative engine. The batch briefs file is ready for production handoff."

### 10. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any section
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the Mandala
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#10-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the Mandala Builder workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Complete document reviewed with user
- Coherence check performed across all sections
- Any inconsistencies identified and resolved
- Consolidation section written with synthesis and production numbers
- Batch briefs extracted to separate file
- Sidecar memories updated with session summary
- Frontmatter marked as COMPLETE
- Completion summary with output file paths communicated
- User satisfied with final Mandala

### ❌ SYSTEM FAILURE:

- Not reading the complete document before consolidation
- Adding new briefs or content not discussed in previous steps
- Not performing coherence check
- Not extracting batch briefs to separate file
- Not updating sidecar memories
- Not marking workflow as COMPLETE in frontmatter
- Generating consolidation content without user review
- Not saving final document state

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
