---
name: 'step-01b-continue'
description: 'Handle continuation of an in-progress Mandala Builder workflow'

# File References
outputFile: '{campaign_assets}/mandala-{project_name}.md'
---

# Step 1b: Workflow Continuation

## STEP GOAL:

To detect the current state of an in-progress Mandala, report progress to the user, and route to the next incomplete step for seamless workflow resumption.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🎯 This is a mixed workflow — intent steps facilitate, prescriptive steps generate

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
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

"**Welcome back to your Mandala da Criatividade Infinita.**

**Project:** {project_name}
**Status:** {status}
**Completed steps:**"

List each completed step with its name:

| Step # | Step Name | Status |
|--------|-----------|--------|
| 1 | Init | ✅ if in stepsCompleted |
| 2 | Brand Brief Context | ✅ if in stepsCompleted, otherwise pending |
| 3 | Funnel Phases | ✅ if in stepsCompleted, otherwise pending |
| 4 | Creative Types | ✅ if in stepsCompleted, otherwise pending |
| 5 | Priority Matrix | ✅ if in stepsCompleted, otherwise pending |
| 6 | Production Briefs | ✅ if in stepsCompleted, otherwise pending |
| 7 | Consolidation | ✅ if in stepsCompleted, otherwise pending |

### 3. Determine Next Step

Based on the highest number in `stepsCompleted`, determine the next step to execute:

| Last Completed Step | Next Step File |
|---------------------|----------------|
| 1 (init) | `./step-02-brand-brief.md` |
| 2 (brand-brief) | `./step-03-funnel-phases.md` |
| 3 (funnel-phases) | `./step-04-creative-types.md` |
| 4 (creative-types) | `./step-05-matrix.md` |
| 5 (matrix) | `./step-06-briefs.md` |
| 6 (briefs) | `./step-07-consolidation.md` |
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
- Routed to the correct next step
- Updated lastContinued timestamp
- Did NOT modify any existing content

### ❌ SYSTEM FAILURE:

- Routing to wrong step
- Modifying existing Mandala content
- Not reading the existing document
- Skipping progress report
- Starting work on a step instead of just routing

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
