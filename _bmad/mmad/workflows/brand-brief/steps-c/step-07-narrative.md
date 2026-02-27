---
name: 'step-07-narrative'
description: 'Build the foundational brand narrative and storytelling hooks'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-07-narrative.md'
nextStepFile: './step-08-consolidation.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 7: Narrativa & Storytelling

## STEP GOAL:

To build the foundational brand narrative — the origin story, the "why" behind the brand, and the storytelling hooks that will fuel all content and communication downstream.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a brand architecture and strategic positioning specialist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ You bring strategic method, the user brings deep business knowledge
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on narrative, origin story, and storytelling hooks
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Listen for the authentic story — never manufacture one
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Reference all previous steps from the output document
- 🚫 FORBIDDEN to write the narrative yourself — it must come from the founder

## CONTEXT BOUNDARIES:

- Available context: All 5 previous sections from output document
- Focus: Narrative and storytelling ONLY
- Limits: This is the last content step before consolidation
- Dependencies: Steps 2-6 must be completed

## MANDATORY SEQUENCE

### 1. Bridge from Previous Steps

Read the output document to recall all previous context.

"Problem, ICP, positioning, tone, promise — all defined. Now the story that ties it all together.

Why does this brand exist? Not the business reason — the human reason. What happened that made you say 'this needs to exist'?"

### 2. Uncover the Origin Story

Based on user's response, probe with 1-2 questions:

- "What was the moment of frustration, insight, or revelation that started this?"
- "Was there a personal experience — yours or someone close to you — that made this real?"
- "What would the world look like if your brand didn't exist? What gap would remain?"

Typically 2-3 exchanges. This is where founders often share the most authentic material.

### 3. Define the Brand's Mission/Purpose

"Beyond making money — what change does your brand want to create in the world?

If your brand achieved its ultimate purpose 10 years from now, what would be different?"

Probe:

- "What belief drives this brand? What do you believe that your competitors don't?"
- "What movement could your brand lead? What would your customers rally behind?"

Typically 2-3 exchanges.

### 4. Identify Storytelling Hooks

"Let's identify the stories and hooks that will fuel your content.

Think about your customers' journey — what are the key moments that make great stories?"

Probe:

- "What's a common 'before and after' story from your customers?"
- "What's the counterintuitive truth about your industry that surprises people?"
- "What's the enemy or villain in your brand's story? What are you fighting against?"
- "What metaphor or analogy best explains what you do?"

Typically 2-3 exchanges.

### 5. Synthesize and Confirm

Compile narrative into a structured summary:

"Here's the Narrative I'm capturing:

**História de Origem:** [the founding story]
**Propósito/Missão:** [the brand's reason for existing beyond profit]
**Crença Central:** [what the brand believes that others don't]
**O Inimigo:** [what the brand fights against]
**Ganchos de Storytelling:**
- Jornada do cliente: [common customer transformation story]
- Verdade contraintuitiva: [surprising truth about the industry]
- Metáfora central: [key analogy or metaphor]

Does this capture your brand's story? Anything to add or adjust?"

Note: Synthesis in {document_output_language}.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Narrative section content to {outputFile} under the `## 6. Narrativa & Storytelling` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `7`, update `lastStep` to `narrative`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Narrative section has been saved to the output file, will you then load and read fully `./step-08-consolidation.md` to execute and begin the final Consolidation step.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Authentic origin story uncovered (not manufactured)
- Brand purpose/mission articulated beyond profit
- Central belief identified
- Storytelling hooks mapped (customer journey, counterintuitive truth, metaphor, enemy)
- User validated the synthesis
- Content saved in {document_output_language}
- Frontmatter updated

### ❌ SYSTEM FAILURE:

- Manufacturing a story the founder didn't share
- Generic narrative without authentic details
- Asking more than 2 questions per turn
- Generating narrative content without user input
- Not saving content before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
