---
name: 'step-06-report'
description: 'Compile final report with executive summary, vocabulary bank, and downstream recommendations'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-06-report.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 6: Relatório Final

## STEP GOAL:

To compile all findings into a structured final report — executive summary, vocabulary bank of ICP language organized by category, and actionable recommendations for downstream agents (Copywriter, Content Strategist, VTSD/Mandala Builder). This document becomes an intelligence asset that powers all MMAD content and copy workflows.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔍 Final compilation step — review for coherence and completeness

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ Maintain direct, analytical tone — no praise, no filler
- ✅ This report must be actionable — not just interesting, but useful

### Step-Specific Rules:

- 🎯 Focus ONLY on compiling, synthesizing, and completing the report
- 🚫 FORBIDDEN to add new research data not collected in previous steps
- 💬 Ask targeted questions about gaps or priorities
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final report section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning compilation
- 🚫 FORBIDDEN to fundamentally change previous sections without user consent

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all 4 sections filled
- Focus: Compilation, vocabulary bank, and recommendations
- Limits: This is the final step
- Dependencies: All previous steps (2-5) must be completed

## MANDATORY SEQUENCE

### 1. Load Complete Document

Read the entire output document including all 4 completed sections.

### 2. Present Report Overview

"All 4 research sections are complete. Let me compile the final report.

**Market Research — {project_name}**"

Display a brief summary of what was collected:
- Scope covered
- Sources searched
- Total quotes/data points extracted
- Key patterns identified

### 3. Write Executive Summary

Draft an executive summary in {document_output_language}:

"**Sumário Executivo:**

Here's the executive summary I'm proposing for the report:

[2-3 paragraph summary that covers:]
- What was researched and why
- Key findings: dominant pains, desires, objections
- Most important insight / biggest surprise
- Strategic implication for the brand

Does this capture the essence? Any adjustments?"

### 4. Compile Vocabulary Bank

This is the most actionable output — a structured bank of the ICP's exact words:

"**Banco de Vocabulário do ICP:**

**Palavras de Dor:**
- [word/phrase 1]
- [word/phrase 2]
- ...

**Palavras de Desejo:**
- [word/phrase 1]
- [word/phrase 2]
- ...

**Palavras de Objeção:**
- [word/phrase 1]
- [word/phrase 2]
- ...

**Expressões Emocionais:**
- [expression 1]
- [expression 2]
- ...

**Frases-Chave (Copy-Ready):**
- \"[phrase 1]\" — [context/usage note]
- \"[phrase 2]\" — [context/usage note]
- ...

This vocabulary bank is what downstream agents will use to write copy, content, and ads in the ICP's own language."

### 5. Write Downstream Recommendations

Draft recommendations for how other MMAD agents should use this research:

"**Recomendações para Workflows Downstream:**

**Para o Copywriter:**
- Use exact phrases from [section] for headlines and hooks
- Address objection [X] directly in sales copy
- Lead with pain [Y] — it's the most emotionally charged

**Para o Content Strategist:**
- Content topics that align with ICP desires: [list]
- Questions the ICP is actively asking: [list]
- Platforms where content should be distributed: [based on source map]

**Para o VTSD / Mandala Builder:**
- Semantic territories based on language clusters: [list]
- Visual mood aligned with emotional patterns: [description]

**Para o Funnel Architect:**
- Awareness level of the ICP: [from scope]
- Key objections to address at each funnel stage: [list]

**Para o Ad Batch Generator:**
- Highest-impact pain points for ad hooks: [list]
- Copy-ready phrases for ad text: [list]"

### 6. Final Review

Present the complete report section for validation:

"Here's the final report section. Review it — any adjustments before I mark the research complete?"

If user wants adjustments:
- Make targeted edits as requested
- Re-present for confirmation

### 7. Mark Workflow Complete

Update the output document:

- Write the Relatório Final section under `## 5. Relatório Final` heading (replacing the comment placeholder)
- Include: Sumário Executivo, Banco de Vocabulário do ICP, Recomendações para Workflows Downstream, Data de Criação, Versão: 1.0

Update frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4, 5, 6]
lastStep: 'report'
status: 'COMPLETE'
completedDate: [current date]
```

### 8. Present Completion Summary

"**Market Research complete for {project_name}.**

**Document saved to:** `{brand_assets}/market-research-{project_name}.md`

**What this enables:**
- Copywriter — headlines and copy using the ICP's exact language
- Content Strategist — content topics aligned with real audience interests
- VTSD / Mandala Builder — semantic territories grounded in data
- Funnel Architect — objection handling at each funnel stage
- Ad Batch Generator — ad hooks based on proven pain points

This document is intelligence gold. Every word came from your audience's mouth."

### 9. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any section
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the research
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#9-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the Market Research workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Complete document reviewed with user
- Executive summary captures key findings
- Vocabulary bank compiled with ICP's exact language by category
- Downstream recommendations specific and actionable
- Frontmatter marked as COMPLETE
- Next steps communicated clearly
- User satisfied with final document

### ❌ SYSTEM FAILURE:

- Not reading the complete document before compilation
- Adding new research data not collected in previous steps
- Missing vocabulary bank (the most actionable output)
- Generic recommendations not tied to specific findings
- Not marking workflow as COMPLETE in frontmatter
- Not saving final document state

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
