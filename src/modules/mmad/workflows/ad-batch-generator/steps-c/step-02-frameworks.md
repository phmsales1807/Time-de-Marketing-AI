---
name: 'step-02-frameworks'
description: 'Select and assign copy frameworks per angle/brief for batch ad generation'

# File References
nextStepFile: './step-03-generate.md'
outputFile: '{campaign_assets}/ad-batch-{date}-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 2: Frameworks de Copy

## STEP GOAL:

To select and assign the optimal copy framework for each production brief based on awareness level, creative type, and angle — building the generation blueprint that Step 3 will execute at scale.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🚀 GENERATE content proactively — YOU ARE A CONTENT GENERATOR

### Role Reinforcement:

- ✅ You are a VTSD batch generation specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ You bring copy frameworks and batch generation methodology, the user reviews and approves
- ✅ Speed Protocol: Batch Generation — optimize for volume and variety
- ✅ Maintain direct, production-focused tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on framework selection and assignment per brief
- 🚫 FORBIDDEN to generate actual ad copy yet (that's Step 3)
- 📝 RECOMMEND frameworks proactively — present your analysis, then ask for approval
- 📦 Present for review in batches (5-10 for ad variations)
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track framework assignments — build the generation blueprint
- 🚀 GENERATE recommendations proactively — do not wait for user to suggest frameworks

## CONTEXT BOUNDARIES:

- Available context: Production briefs from Step 1, Brand Brief tone, sidecar insights
- Focus: Framework selection and assignment ONLY
- Limits: Do not generate ad copy yet
- Dependencies: Output document must exist with context section (created in step-01)

## MANDATORY SEQUENCE

### 1. Load Context

Read the existing output document to confirm Step 1 context is in place.

Review all loaded production briefs and their attributes (angle, awareness level, creative type).

### 2. Present Available Frameworks

Present the Light Copy frameworks available for ad generation:

"**Frameworks de Copy Disponíveis:**

| Framework | Best For | Structure |
|---|---|---|
| **Premissa→Prova→Ponte** | High awareness, proof-driven | Bold claim → Evidence → Bridge to action |
| **PAS** (Problem-Agitation-Solution) | Problem-aware, emotional | State pain → Amplify urgency → Present solution |
| **AIDA** (Attention-Interest-Desire-Action) | Broad awareness, sequential | Hook → Build interest → Create desire → CTA |
| **Before-After-Bridge** | Solution-aware, transformation | Current state → Desired state → How to get there |
| **Feature-Advantage-Benefit** | Product-aware, rational | What it does → Why it matters → What you gain |"

### 3. Generate Framework Recommendations

For each production brief, RECOMMEND the best framework based on:
- Awareness level (unaware → most aware)
- Creative type (static, video, carousel, story)
- Angle (pain, desire, objection, social proof, authority)

Present as a table:

"**My Framework Recommendations:**

| Brief # | Angle | Awareness Level | Creative Type | Recommended Framework | Rationale |
|---|---|---|---|---|---|
| 1 | [angle] | [level] | [type] | [framework] | [brief reason] |
| 2 | [angle] | [level] | [type] | [framework] | [brief reason] |
| ... | ... | ... | ... | ... | ... |

These are my framework recommendations based on awareness level and creative type alignment. **Approve all, or want to change any?**"

### 4. Process User Feedback

If user approves all: Proceed to step 5.

If user wants changes:
- Adjust specific framework assignments as requested
- Re-present the updated table for confirmation
- Repeat until all assignments are approved

### 5. Synthesize and Save

Compile the approved framework assignments and present final summary:

"**Framework assignments confirmed. Generation blueprint ready:**

- Total briefs: X
- Frameworks in use: [list unique frameworks]
- Estimated variations: [2-4 per brief × number of briefs]
- Ready for batch generation in Step 3."

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Framework assignments to {outputFile} under the `## 2. Frameworks de Copy` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `2`, update `lastStep` to `frameworks`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Framework assignments have been saved to the output file, will you then load and read fully `./step-03-generate.md` to execute and begin batch ad generation.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- All available frameworks presented clearly
- Framework recommended for EACH production brief with rationale
- Recommendations based on awareness level + creative type analysis
- User approved or adjusted all framework assignments
- Generation blueprint summary presented (total briefs, frameworks, estimated variations)
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Waiting for user to suggest frameworks instead of recommending proactively
- Generating actual ad copy in this step (that's Step 3)
- Not providing rationale for framework recommendations
- Proceeding without user approval of framework assignments
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
