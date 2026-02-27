---
name: 'step-01b-continue'
description: 'Handle continuation of an in-progress Funnel Design workflow'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-01b-continue.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
---

# Step 1b: Workflow Continuation

## STEP GOAL:

To detect the current state of an in-progress Funnel Design, report progress to the user, and route to the next incomplete step for seamless workflow resumption.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a customer journey and funnel design specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ Maintain systematic, visual tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on detecting state and routing to the correct step
- 🚫 FORBIDDEN to modify any existing content
- 🚫 FORBIDDEN to start working on any step content here

## MANDATORY SEQUENCE

### 1. Load Build State

Load `{outputFile}` and read:

- `stepsCompleted` array
- `lastStep` value
- `status` value
- `date` and `user_name`

Also read the document content to understand what has been completed so far.

Additionally, load the Brand Brief from `{brandBriefFile}` if available, to restore context for the remaining steps.

### 2. Report Progress

Communicate in {communication_language}:

"**Welcome back to your Funnel Design.**

**Project:** {project_name}
**Status:** {status}
**Completed steps:**"

List each completed step with its name:

| Step # | Step Name | Status |
|--------|-----------|--------|
| 1 | Init | ✅ if in stepsCompleted |
| 2 | Contexto & Objetivo | ✅ if in stepsCompleted |
| 3 | Fases do Funil | ✅ if in stepsCompleted |
| 4 | Touchpoints & Canais | ✅ if in stepsCompleted |
| 5 | Conteúdo por Fase | ✅ if in stepsCompleted |
| 6 | Métricas & KPIs | ✅ if in stepsCompleted |
| 7 | Consolidação | ✅ if in stepsCompleted |

### 3. Determine Next Step

Based on the highest number in `stepsCompleted`, determine the next step to execute:

| Last Completed Step | Next Step File |
|---------------------|----------------|
| 1 (init) | `./step-02-context.md` |
| 2 (context) | `./step-03-phases.md` |
| 3 (phases) | `./step-04-touchpoints.md` |
| 4 (touchpoints) | `./step-05-content.md` |
| 5 (content) | `./step-06-metrics.md` |
| 6 (metrics) | `./step-07-consolidation.md` |
| 7 (consolidation) | Workflow is COMPLETE — inform user |

### 4. Update Frontmatter

Add `lastContinued: [current date]` to the output document frontmatter.

### 5. Route to Next Step

"**Continuing to: [next step name]**"

Load, read entire file, then execute the appropriate next step file.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Correctly read stepsCompleted from existing document
- Accurately reported progress to user
- Brand Brief context restored if available
- Routed to the correct next step
- Updated lastContinued timestamp
- Did NOT modify any existing content

### ❌ SYSTEM FAILURE:

- Routing to wrong step
- Modifying existing Funnel Design content
- Not reading the existing document
- Skipping progress report
- Starting work on a step instead of just routing

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
