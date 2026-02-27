---
name: 'step-01b-continue'
description: 'Handle continuation of an in-progress Market Research workflow'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-01b-continue.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'
---

# Step 1b: Workflow Continuation

## STEP GOAL:

To detect the current state of an in-progress Market Research, report progress to the user, and route to the next incomplete step for seamless workflow resumption.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔍 This is a balanced workflow — prescriptive framework, flexible interpretation

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ Maintain direct, analytical tone — no praise, no filler

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

"**Welcome back to your Market Research.**

**Project:** {project_name}
**Status:** {status}
**Completed steps:**"

List each completed step with its name:

| Step # | Step Name | Status |
|--------|-----------|--------|
| 1 | Init | ✅ if in stepsCompleted |
| 2 | Research Scope | ✅ if in stepsCompleted |
| 3 | Data Sources | ✅ if in stepsCompleted |
| 4 | Voice Mining | ✅ if in stepsCompleted |
| 5 | Pattern Analysis | ✅ if in stepsCompleted |
| 6 | Final Report | ✅ if in stepsCompleted |

### 3. Determine Next Step

Based on the highest number in `stepsCompleted`, determine the next step to execute:

| Last Completed Step | Next Step File |
|---------------------|----------------|
| 1 (init) | `./step-02-scope.md` |
| 2 (scope) | `./step-03-sources.md` |
| 3 (sources) | `./step-04-voice-mining.md` |
| 4 (voice-mining) | `./step-05-patterns.md` |
| 5 (patterns) | `./step-06-report.md` |
| 6 (report) | Workflow is COMPLETE — inform user |

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
- Modifying existing Market Research content
- Not reading the existing document
- Skipping progress report
- Starting work on a step instead of just routing

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
