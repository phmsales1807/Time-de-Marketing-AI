---
name: 'step-05-matrix'
description: 'Cross awareness levels with creative types into a prioritized matrix'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/mandala-builder'

# File References
thisStepFile: './step-05-matrix.md'
nextStepFile: './step-06-briefs.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{campaign_assets}/mandala-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 5: Matriz de Prioridades — TRANSITION (Intent → Prescriptive)

## STEP GOAL:

To cross the selected awareness levels (rows) with selected creative types (columns) into a visual priority matrix. This is the TRANSITION step: you GENERATE the matrix proactively using efficacy ratings from mandala-matrix data, but CONFIRM priorities collaboratively with the user before finalizing.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- ⚡ This is a TRANSITION step — generate the matrix, then collaborate on priorities

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ You bring efficacy data and matrix architecture expertise, the user brings campaign judgment
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- ⚡ GENERATE the priority matrix proactively — this is the transition to prescriptive mode
- 🎯 Use efficacy ratings from mandala-matrix data to assign initial priorities
- 💬 After generation, ask 1-2 confirmation questions — collaborative validation
- 🚫 FORBIDDEN to generate production briefs yet (that's step 6)
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- ⚡ GENERATE the matrix using data — do not wait for user to build it
- 🤝 CONFIRM priorities with user — this is collaborative validation, not blind approval

## CONTEXT BOUNDARIES:

- Available context: step-02 (campaign context), step-03 (selected awareness levels), step-04 (selected creative types)
- Available context: Mandala-matrix data (efficacy ratings for each awareness level × creative type combination)
- Focus: Matrix construction and priority assignment ONLY
- Limits: Do not generate production briefs yet
- Dependencies: Steps 2, 3, and 4 must be completed

## MANDATORY SEQUENCE

### 1. Load Inputs

Read the existing output document to review:

- Selected awareness levels from step 3 (rows)
- Selected creative types from step 4 (columns)
- Campaign context from step 2 (for priority judgment)

Also reference the efficacy ratings from mandala-matrix data for each combination.

### 2. Generate Priority Matrix

GENERATE the cross matrix: selected awareness levels × selected creative types.

For each cell, assign a priority based on efficacy ratings from mandala-matrix data AND campaign context:

- ★★★ **Priority** — High efficacy + aligned with campaign objective. MUST produce briefs.
- ★★ **Secondary** — Moderate efficacy or partially aligned. SHOULD produce briefs if capacity allows.
- ★ **Optional** — Lower efficacy but worth testing. CAN produce briefs for experimentation.
- **-** **Skip** — Low efficacy or misaligned with this campaign. Do not produce briefs.

Present the matrix visually:

"Here's your Mandala Priority Matrix:

**Matriz de Prioridades — {project_name}**

| | [Type 1] | [Type 2] | [Type 3] | [Type 4] | [Type 5] |
|---|---|---|---|---|---|
| **[Level 1]** | ★★★ | ★★ | ★ | ★★★ | - |
| **[Level 2]** | ★★ | ★★★ | ★★ | ★ | ★★ |
| **[Level 3]** | ★ | ★★ | ★★★ | ★★ | ★★★ |

**Summary:**
- ★★★ Priority cells: [N] — will generate briefs for these
- ★★ Secondary cells: [N] — will generate briefs if capacity allows
- ★ Optional cells: [N] — available for experimentation
- Skipped cells: [N]

**Rationale for priority assignments:**
- [Level × Type] = ★★★ because [efficacy data + campaign alignment reason]
- [Level × Type] = ★★★ because [efficacy data + campaign alignment reason]
- ..."

### 3. Collaborative Confirmation

Ask the user to validate the priorities:

"These are the priority assignments based on efficacy data and your campaign objective. Do you agree? Specifically:

1. Are the ★★★ cells correct — these are the must-have combinations?
2. Any ★★ cells you'd promote to ★★★, or vice versa?
3. Any cells you want to add or remove entirely?"

Handle user feedback: adjust priorities as requested and re-present if changes are significant.

### 4. Finalize Matrix

Once confirmed, present the final matrix:

"**Final Priority Matrix:**

[Updated matrix table]

**Production Plan:**
- **Must produce:** [N] ★★★ briefs
- **Should produce:** [N] ★★ briefs
- **Optional:** [N] ★ briefs
- **Total target:** [sum] briefs

Ready to move to brief generation."

### 5. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Priority Matrix section content to {outputFile} under the `## 4. Matriz de Prioridades` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `5`, update `lastStep` to `matrix`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#5-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Priority Matrix section has been saved to the output file, will you then load and read fully `./step-06-briefs.md` to execute and begin Production Brief generation.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Matrix generated proactively using efficacy data
- All cells assigned a priority rating
- Visual matrix table presented clearly
- Rationale provided for priority assignments
- User confirmed or adjusted priorities collaboratively
- Final matrix with production plan presented
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Asking user to build the matrix instead of generating it
- Not using efficacy data from mandala-matrix for priority assignments
- Generating production briefs at this stage
- Not presenting priorities for user confirmation
- Proceeding without user validation of the matrix
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
