---
name: 'step-06-promise-offer'
description: 'Articulate the core promise and offer structure'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-06-promise-offer.md'
nextStepFile: './step-07-narrative.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 6: Promessa & Oferta

## STEP GOAL:

To articulate the brand's core promise and offer structure — the transformation the customer experiences, what specifically is being offered, and why it delivers on the promise.

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

- 🎯 Focus ONLY on promise, transformation, and offer structure
- 🚫 FORBIDDEN to discuss narrative or storytelling (that comes next)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Push for concrete transformation — not vague outcomes
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Reference all previous steps from the output document
- 🚫 FORBIDDEN to generate promise/offer content yourself

## CONTEXT BOUNDARIES:

- Available context: Problem & Market + ICP + Positioning + Tone of Voice from output document
- Focus: Promise, transformation, and offer structure ONLY
- Limits: Do not explore narrative or storytelling yet
- Dependencies: Steps 2-5 must be completed

## MANDATORY SEQUENCE

### 1. Bridge from Previous Steps

Read the output document to recall all previous context.

"We've got problem, ICP, positioning, and tone of voice. Now let's articulate your promise.

What transformation does your customer experience? Where are they BEFORE your product, and where are they AFTER?"

### 2. Define the Transformation

Based on user's response, probe with 1-2 questions:

- "Can you describe this transformation in one sentence? Before → After."
- "How long does this transformation take? Is it instant gratification or a journey?"
- "What's the emotional shift? Not just the practical outcome — how do they FEEL different?"

Typically 2-3 exchanges.

### 3. Articulate the Core Promise

"Based on this transformation, what's the ONE promise your brand makes?

Not a list of benefits — the single, boldest promise you stand behind."

Probe:

- "Would you put this promise on a billboard? Is it clear enough, bold enough?"
- "Can your competition make the same promise? If yes, what makes yours more credible?"
- "What proof do you have that you deliver on this promise? Results, testimonials, data?"

Typically 2-3 exchanges.

### 4. Map the Offer Structure

"How does your offer actually deliver this transformation? What does the customer get?

Walk me through what's included — the structure, components, and delivery method."

Probe:

- "What's the main product/service? What supports or complements it?"
- "How is it delivered? Digital, physical, hybrid, live, self-paced?"
- "Is there a price point or pricing model in mind? How does pricing reflect value?"
- "What would make someone say 'this is a no-brainer at this price'?"

Typically 2-3 exchanges.

### 5. Synthesize and Confirm

Compile promise and offer into a structured summary:

"Here's the Promise & Offer I'm capturing:

**Transformação:** [before → after statement]
**Promessa Central:** [one bold promise]
**Prova/Credibilidade:** [proof points]
**Estrutura da Oferta:**
- Principal: [main product/service]
- Componentes: [what's included]
- Entrega: [delivery method]
- Posicionamento de Preço: [pricing approach/rationale]

Does this capture your promise and offer accurately? Anything to adjust?"

Note: Synthesis in {document_output_language}.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Promise & Offer section content to {outputFile} under the `## 5. Promessa & Oferta` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `6`, update `lastStep` to `promise-offer`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Promise & Offer section has been saved to the output file, will you then load and read fully `./step-07-narrative.md` to execute and begin Narrative & Storytelling discovery.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Clear before → after transformation articulated
- Core promise is bold, specific, and credible
- Proof points identified
- Offer structure mapped with components and delivery
- User validated the synthesis
- Content saved in {document_output_language}
- Frontmatter updated

### ❌ SYSTEM FAILURE:

- Vague transformation like "better life" or "more success"
- Generating promise/offer without user input
- Asking more than 2 questions per turn
- Discussing narrative prematurely
- Not saving content before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
