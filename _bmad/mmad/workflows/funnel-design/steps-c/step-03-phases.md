---
name: 'step-03-phases'
description: 'Map the funnel phases tailored to the business — not generic TOFU/MOFU/BOFU'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-03-phases.md'
nextStepFile: './step-04-touchpoints.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 3: Mapeamento de Fases

## STEP GOAL:

To define the funnel phases tailored to this specific business — not generic TOFU/MOFU/BOFU. Map the customer's state of mind and awareness level at each phase. This creates the structural backbone of the entire funnel.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a customer journey and funnel design specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring funnel architecture expertise, the user brings deep business knowledge
- ✅ Maintain systematic, visual tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on defining funnel phases and awareness levels
- 🚫 FORBIDDEN to map specific touchpoints, channels, or content (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Design phases that reflect THIS business, not textbook models
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: step-02 Context & Objective (funnel purpose, conversion goal, offers)
- Available context: Brand Brief (ICP, positioning, market) if loaded
- Focus: Funnel phases and awareness levels ONLY
- Limits: Do not map specific channels, touchpoints, or content yet
- Dependencies: Step 2 (Context & Objective) must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review the Context & Objective section from step 2.

Then begin:

"Now let's map the phases of your funnel. Not the generic 'awareness, consideration, decision' — YOUR customer's actual journey.

For infoproduto context, phases typically look something like: Descoberta → Engajamento → Consideração → Decisão → Compra → Onboarding → Retenção. But that's just a starting point.

What does your customer's journey actually look like? Where do they start, and what stages do they go through before buying?"

### 2. Probe the Customer Journey

Based on user's response, dig deeper with 1-2 questions per turn. Examples:

- "At the [phase] stage — what is the customer thinking? What do they need to feel to move forward?"
- "Is there a phase between [X] and [Y] where people get stuck? What happens there?"
- "After the purchase — what happens? Is there an onboarding phase? A retention loop?"
- "Where do people drop off most? That tells us where a phase boundary exists."
- "Does your customer need education before they can even consider buying?"

Continue probing until phases are clear. Typically 3-5 exchanges.

### 3. Map Awareness Levels

Once phases are defined, map awareness levels:

"Let's layer in awareness levels for each phase. Eugene Schwartz's framework:

- **Unaware** — doesn't know they have a problem
- **Problem-Aware** — knows the pain but not the solution
- **Solution-Aware** — knows solutions exist but not yours
- **Product-Aware** — knows your product but hasn't decided
- **Most Aware** — ready to buy, needs the right trigger

For each phase you described, where does your customer sit on this spectrum?"

### 4. Probe Awareness per Phase

Dig deeper with 1-2 questions per turn:

- "In the [phase] phase — do they already know they have this problem, or do we need to create that awareness?"
- "When they reach [phase] — do they know about your specific product, or just that solutions exist?"
- "At what point do they shift from 'exploring options' to 'evaluating you specifically'?"

Continue until awareness levels are mapped per phase. Typically 2-3 exchanges.

### 5. Synthesize and Confirm

Compile what you learned into a structured overview and present it to the user for validation:

"Here's what I'm capturing for Funnel Phases:

| Fase | Estado Mental do Cliente | Nível de Consciência | O Que Ele Precisa |
|------|------------------------|---------------------|-------------------|
| [Phase 1] | [state of mind] | [awareness level] | [what they need] |
| [Phase 2] | [state of mind] | [awareness level] | [what they need] |
| ... | ... | ... | ... |

Does this capture your customer's journey accurately? Any phases missing or misplaced?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Funnel Phases section content to {outputFile} under the `## 2. Fases do Funil` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `3`, update `lastStep` to `phases`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Funnel Phases section has been saved to the output file, will you then load and read fully `./step-04-touchpoints.md` to execute and begin Touchpoints & Channels mapping.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Funnel phases defined specific to THIS business (not generic TOFU/MOFU/BOFU)
- Customer state of mind captured per phase
- Awareness levels mapped per phase (Schwartz framework)
- What the customer needs at each phase identified
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Using generic TOFU/MOFU/BOFU without customizing to the business
- Generating phases without user input
- Asking more than 2 questions per turn
- Discussing specific channels, touchpoints, or content prematurely
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
