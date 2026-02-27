---
name: 'step-04-positioning'
description: 'Discover unique positioning and differentiators'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-04-positioning.md'
nextStepFile: './step-05-tone-of-voice.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 4: Posicionamento

## STEP GOAL:

To discover the brand's unique positioning — what makes it different, why that difference matters, and how to articulate it. Positioning is discovered, not invented. The truth is already in the business; the job is to uncover it.

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

- 🎯 Focus ONLY on positioning and differentiation
- 🚫 FORBIDDEN to discuss tone of voice, offer structure, or narrative (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Challenge generic differentiators — "quality" and "customer service" are not positioning
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Reference Problem & Market AND ICP context from the output document
- 🚫 FORBIDDEN to generate positioning statements yourself — they emerge from conversation

## CONTEXT BOUNDARIES:

- Available context: Problem & Market + ICP sections from output document
- Focus: Positioning and differentiation ONLY
- Limits: Do not explore tone of voice or offer structure yet
- Dependencies: Steps 2-3 must be completed

## MANDATORY SEQUENCE

### 1. Bridge from Previous Steps

Read the output document to recall Problem & Market and ICP context.

"We know the problem, the market, and the ideal customer. Now: what makes YOUR approach different?

Why would your ideal customer choose you over every other option — including doing nothing?"

### 2. Explore Differentiation

Based on user's response, probe with 1-2 questions:

- "If a competitor copied your features tomorrow, what would still be uniquely yours?"
- "What do you do that others refuse to do, can't do, or don't know how to do?"
- "What's the ONE thing your best customers consistently say about you that they don't say about alternatives?"

Typically 2-3 exchanges. Push past surface-level answers.

### 3. Map the Competitive Landscape

"Let's look at the landscape. Who are the 2-3 closest competitors or alternatives your customer considers?

What do they promise? Where do they fall short?"

Probe:

- "What category does your customer mentally place you in? Is that the right category?"
- "Is there a category you could own or create rather than competing in an existing one?"

Typically 2-3 exchanges.

### 4. Craft Positioning Statement

"Based on everything we've discussed, let's articulate your positioning.

Complete this: 'For [ICP] who [problem/need], [brand] is the [category] that [key differentiator] because [reason to believe].'"

Work collaboratively with the user to refine this statement. This is not a tagline — it's an internal positioning compass.

### 5. Synthesize and Confirm

Compile positioning into a structured summary:

"Here's the positioning I'm capturing:

**Diferenciadores Únicos:** [from conversation]
**Cenário Competitivo:** [competitors and gaps]
**Categoria:** [category owned or created]
**Declaração de Posicionamento:** [positioning statement crafted together]
**Razão para Acreditar:** [proof points/reasons to believe]

Does this capture your positioning accurately? Anything to adjust?"

Note: Synthesis in {document_output_language}.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Positioning section content to {outputFile} under the `## 3. Posicionamento` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `4`, update `lastStep` to `positioning`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Positioning section has been saved to the output file, will you then load and read fully `./step-05-tone-of-voice.md` to execute and begin Tone of Voice discovery.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Unique differentiators identified (beyond "quality" and "service")
- Competitive landscape mapped with specificity
- Positioning statement co-created with user
- Category ownership or creation explored
- User validated the synthesis
- Content saved in {document_output_language}
- Frontmatter updated

### ❌ SYSTEM FAILURE:

- Generic positioning like "we offer the best quality"
- Generating positioning without user input
- Asking more than 2 questions per turn
- Discussing tone of voice or offer structure prematurely
- Not saving content before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
