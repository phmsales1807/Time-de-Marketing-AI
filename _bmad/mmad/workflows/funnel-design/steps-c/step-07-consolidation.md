---
name: 'step-07-consolidation'
description: 'Compile and review the final Funnel Design document with visual summary and downstream recommendations'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-07-consolidation.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 7: Consolidação

## STEP GOAL:

To compile all 5 content sections into a coherent, final Funnel Design document. Present a visual funnel summary, perform a coherence check across all phases, provide downstream agent recommendations, and mark the workflow as complete.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a customer journey and funnel design specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ You bring funnel architecture expertise, the user brings deep business knowledge
- ✅ Maintain systematic, visual tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on reviewing, consolidating, and completing the document
- 🚫 FORBIDDEN to add new content sections not discussed in previous steps
- 💬 Ask targeted questions about gaps or inconsistencies you notice
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final consolidation section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning consolidation
- 🚫 FORBIDDEN to fundamentally change previous sections without user consent

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all 5 content sections filled
- Focus: Consolidation, coherence check, visual summary, downstream recommendations
- Limits: This is the final step
- Dependencies: All previous steps (2-6) must be completed

## MANDATORY SEQUENCE

### 1. Load Complete Document

Read the entire output document including all 5 completed sections.

### 2. Present Visual Funnel Summary

"All 5 sections of your Funnel Design are complete. Let me present the full picture.

**Funnel Design — {project_name}**"

Present a visual summary that connects all sections:

"**Visão Geral do Funil:**

[Phase 1] → [Phase 2] → [Phase 3] → ... → [Final Phase]

For each phase, show:
- Touchpoints & channels
- Content type
- Critical metric
- Transition to next phase"

Display this as a concise, visual overview — not a full document dump.

### 3. Coherence Check

Review the document for internal consistency and present observations:

"Here's what I notice about coherence across the funnel:

- **Objetivo → Fases alignment:** [observation — do the phases serve the stated objective?]
- **Fases → Touchpoints alignment:** [observation — do touchpoints cover all phases?]
- **Touchpoints → Conteúdo alignment:** [observation — does content match each touchpoint's purpose?]
- **Conteúdo → Métricas alignment:** [observation — can we measure what matters for each content piece?]
- **Awareness progression:** [observation — does awareness level increase naturally through the phases?]
- **Offer ladder coherence:** [observation — does the entry → core offer path make sense?]

Any gaps or contradictions? Anything that feels off when you see the full picture?"

Ask 1-2 specific questions if you spot inconsistencies.

### 4. Final Adjustments

If the user wants adjustments:

- Make targeted edits to specific sections as requested
- Update the output document with changes
- Re-present the adjusted sections for confirmation

If no adjustments needed, proceed to step 5.

### 5. Write Consolidation Section

Write a consolidation section under `## 6. Consolidação` in the output document:

This section should contain in {document_output_language}:

- **Síntese do Funil:** A 2-3 paragraph executive summary that ties all elements together — the funnel's logic, key decisions, and expected flow
- **Recomendações para Agentes Downstream:**
  - **Content Strategist:** Content calendar aligned with funnel phases — prioritize content for [critical phases]
  - **Copywriter:** Copy for each touchpoint — focus on [awareness level] messaging at each phase
  - **Ad Batch Generator:** Ad hooks for acquisition phase — target [ICP] with [entry offer] messaging
  - **Landing Page Builder:** LP design per conversion point — [list key landing pages needed]
  - **Email Sequence Builder:** Nurture sequences per phase — [list key email sequences needed]
- **Data de Criação:** Current date
- **Versão:** 1.0

### 6. Mark Workflow Complete

Update the output document frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4, 5, 6, 7]
lastStep: 'consolidation'
status: 'COMPLETE'
completedDate: [current date]
```

### 7. Present Completion Summary

"**Funnel Design complete for {project_name}.**

**Document saved to:** `{funnel_assets}/funnel-design-{project_name}.md`

**What this enables:**
- Content Strategist — content calendar aligned with funnel phases
- Copywriter — copy for every touchpoint in the journey
- Ad Batch Generator — acquisition ads built on your funnel's entry point
- Landing Page Builder — conversion pages for each critical transition
- Email Sequence Builder — nurture sequences that move people through phases

This document is your funnel blueprint. Every downstream workflow will reference it."

### 8. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any section
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the funnel
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#8-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the Funnel Design workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Complete document reviewed with user
- Visual funnel summary presented
- Coherence check performed across all sections
- Any inconsistencies identified and resolved
- Consolidation section written with synthesis and downstream recommendations
- Frontmatter marked as COMPLETE
- Downstream agent recommendations communicated clearly
- User satisfied with final document

### ❌ SYSTEM FAILURE:

- Not reading the complete document before consolidation
- Adding new content not discussed in previous steps
- Not performing coherence check
- Not marking workflow as COMPLETE in frontmatter
- Generating consolidation content without user review
- Not including downstream agent recommendations
- Not saving final document state

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
