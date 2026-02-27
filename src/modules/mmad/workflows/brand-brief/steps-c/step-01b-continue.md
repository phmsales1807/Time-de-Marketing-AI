---
name: 'step-01b-continue'
description: 'Handle continuation of an in-progress Brand Brief workflow'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-01b-continue.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'
---

# Step 1b: Workflow Continuation

## STEP GOAL:

To detect the current state of an in-progress Brand Brief, report progress to the user, and route to the next incomplete step for seamless workflow resumption.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a brand architecture and strategic positioning specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ Maintain direct, concise tone — no praise, no filler

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

### 2. Report Progress

Communicate in {communication_language}:

"**Welcome back to your Brand Brief.**

**Project:** {project_name}
**Status:** {status}
**Completed steps:**"

List each completed step with its name:

| Step # | Step Name | Status |
|--------|-----------|--------|
| 1 | Init | ✅ if in stepsCompleted |
| 2 | Problem & Market | ✅ if in stepsCompleted |
| 3 | ICP | ✅ if in stepsCompleted |
| 4 | Positioning | ✅ if in stepsCompleted |
| 5 | Tone of Voice | ✅ if in stepsCompleted |
| 6 | Promise & Offer | ✅ if in stepsCompleted |
| 7 | Narrative & Storytelling | ✅ if in stepsCompleted |
| 8 | Consolidation | ✅ if in stepsCompleted |

### 3. Determine Next Step

Based on the highest number in `stepsCompleted`, determine the next step to execute:

| Last Completed Step | Next Step File |
|---------------------|----------------|
| 1 (init) | `./step-02-problem-market.md` |
| 2 (problem-market) | `./step-03-icp.md` |
| 3 (icp) | `./step-04-positioning.md` |
| 4 (positioning) | `./step-05-tone-of-voice.md` |
| 5 (tone-of-voice) | `./step-06-promise-offer.md` |
| 6 (promise-offer) | `./step-07-narrative.md` |
| 7 (narrative) | `./step-08-consolidation.md` |
| 8 (consolidation) | Workflow is COMPLETE — inform user |

### 4. Update Frontmatter

Add `lastContinued: [current date]` to the output document frontmatter.

### 5. Route to Next Step

"**Continuing to: [next step name]**"

Load, read entire file, then execute the appropriate next step file.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Correctly read stepsCompleted from existing document
- Accurately reported progress to user
- Routed to the correct next step
- Updated lastContinued timestamp
- Did NOT modify any existing content

### ❌ SYSTEM FAILURE:

- Routing to wrong step
- Modifying existing Brand Brief content
- Not reading the existing document
- Skipping progress report
- Starting work on a step instead of just routing

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
