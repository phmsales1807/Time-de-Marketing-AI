---
name: 'step-03-problem'
description: 'Deepen the audience pain and craft an agitation sequence with escalating urgency'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/vsl-structure'

# File References
thisStepFile: './step-03-problem.md'
nextStepFile: './step-04-story.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{content_assets}/vsl-{vsl_name}-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 3: Problema & Agitação

## STEP GOAL:

To deepen the audience's real pain, uncover the emotional cost of the problem, and craft an agitation sequence that escalates urgency. We're not creating pain — we're naming the pain they already feel, in their words.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a VSL architect and persuasion strategist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring VSL methodology and persuasion frameworks, the user brings deep product knowledge
- ✅ Maintain direct, strategic tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on problem definition and agitation sequence
- 🚫 FORBIDDEN to discuss story, solution mechanism, offer, or close (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Probe deeper when answers are surface-level — the real pain is always one layer below
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: step-02 Big Idea & Hook (the core insight and hook angle)
- Available context: Brand Brief (ICP pains, desires, market) if loaded
- Focus: Problem articulation and agitation ONLY
- Limits: Do not discuss story, solution, offer, or close yet
- Dependencies: Step 2 (Big Idea & Hook) must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review the Big Idea & Hook section from step 2.

Then begin:

"Now we go into the wound. The Big Idea opened the door — now we need to make the audience feel WHY they need to walk through it.

What's the REAL pain your audience lives with every day? Not the surface-level frustration — the deeper thing that keeps them up at night?"

### 2. Probe the Core Problem

Based on user's response, dig deeper with 1-2 questions per turn. Examples:

- "What have they tried that failed? What's the frustration of trying and failing again?"
- "What's the emotional cost? Not just money or time — how does this problem make them FEEL?"
- "If they don't solve this in the next 6 months, what happens? What gets worse?"
- "What do they secretly fear about this problem that they don't say out loud?"
- "When they talk about this problem with friends, what words do they actually use?"

Continue probing until the real pain — emotional, financial, relational — is articulated. Typically 3-4 exchanges.

### 3. Map Failed Attempts

Shift to what hasn't worked:

"What has your audience already tried? What solutions have they attempted that didn't work — or worked partially and left them more frustrated?"

Probe with 1-2 questions:

- "Why did those solutions fail? Was it the approach, the execution, or something deeper?"
- "After each failed attempt, what did they conclude? 'It's my fault'? 'Nothing works'? 'This just isn't for people like me'?"

### 4. Build the Agitation Sequence

Help the user articulate the pain in vivid, escalating language:

"We're not creating pain — we're naming the pain they already feel. In their words. Let's build an agitation sequence that escalates:

1. **Surface pain** — the obvious frustration
2. **Deeper pain** — the emotional toll
3. **Hidden fear** — what they're afraid will happen if nothing changes
4. **Cost of inaction** — what staying stuck actually costs them

For each level, what does your audience experience?"

Probe 1-2 questions per turn as needed.

### 5. Synthesize and Confirm

Compile what you learned into a concise summary and present it to the user for validation:

"Here's what I'm capturing for Problema & Agitação:

**Problema Central:**
[The core problem in the audience's own language]

**Tentativas Frustradas:**
[What they've tried that failed and why]

**Sequência de Agitação:**
1. **Dor Superficial:** [surface-level frustration]
2. **Dor Profunda:** [emotional toll]
3. **Medo Oculto:** [hidden fear]
4. **Custo da Inação:** [what staying stuck costs them]

**Linguagem do Público:**
[Key phrases and words the audience actually uses]

Does this capture the real pain? Is the agitation sequence honest — naming real pain, not manufacturing it?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Problema & Agitação section content to {outputFile} under the `## 2. Problema & Agitação` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `3`, update `lastStep` to `problem`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Problema & Agitação section has been saved to the output file, will you then load and read fully `./step-04-story.md` to execute and begin História & Credibilidade discovery.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Core problem articulated in the audience's own language (not generated)
- Failed attempts identified — what they tried and why it didn't work
- Agitation sequence crafted with escalating urgency (surface → deep → hidden → cost)
- Pain is NAMED, not manufactured — honest and empathetic
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating problem content without user input
- Manufacturing pain that doesn't exist for the audience
- Asking more than 2 questions per turn
- Discussing story, solution, offer, or close prematurely
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
