---
name: 'step-05-solution'
description: 'Define the Unique Mechanism that makes the solution work and differentiate it from everything else'

# File References
nextStepFile: './step-06-offer.md'
outputFile: '{content_assets}/vsl-{vsl_name}-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 5: Solução & Mecanismo Único

## STEP GOAL:

To define the Unique Mechanism — not just "it works," but WHY it works. The mechanism is what differentiates the solution from everything else the audience has tried. It's the "secret engine" that makes the transformation possible and positions the offer as the only logical choice.

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

- 🎯 Focus ONLY on solution mechanism and differentiation
- 🚫 FORBIDDEN to discuss offer pricing, value stack, or close (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Probe until the mechanism is NAMED and its components are clear
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: steps 2-4 (Big Idea, Problem, Story — the full narrative arc so far)
- Available context: Brand Brief (positioning, differentiators) if loaded
- Focus: Solution mechanism and differentiation ONLY
- Limits: Do not discuss pricing, bonuses, value stack, guarantee, or close yet
- Dependencies: Steps 2, 3, and 4 must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review all previous sections — Big Idea, Problem, and Story.

Then begin:

"Your story showed the transformation. Now we need to reveal the ENGINE behind it — the Unique Mechanism.

This is the part of the VSL where the audience goes from 'I want that result' to 'I understand WHY this works.' Not just 'it works' — WHY does it work? What's different about your approach?"

### 2. Probe the Mechanism

Based on user's response, dig deeper with 1-2 questions per turn. Examples:

- "If a competitor copied your method step by step, what couldn't they replicate? What's the thing that's uniquely yours?"
- "What's the underlying principle that makes this approach work when others don't?"
- "Why does your method work BETTER or FASTER than the conventional approach?"
- "What's the counter-intuitive insight — the thing that goes against what most people believe?"

Continue probing until the mechanism's uniqueness is clear. Typically 3-4 exchanges.

### 3. Name the Mechanism

Help the user name it:

"A named mechanism is more powerful than a described one. 'The 3-Layer Method' is more memorable than 'my approach that has three parts.'

Can you name the mechanism? Think about:

- **Numbered frameworks:** 'The 5-Step Protocol', 'The 3-Pillar System'
- **Proprietary names:** 'The Clarity Engine', 'The Momentum Method'
- **Metaphor-based:** 'The Snowball Effect', 'The Foundation Framework'

What name captures the essence of how your solution works?"

Probe with 1-2 questions if needed:

- "What metaphor or image comes to mind when you think about how this works?"
- "If you had to explain the mechanism in a headline, what would it say?"

### 4. Map the Components

"Now let's break the mechanism down. What are the 3-5 key components or steps?

For each component:
- What is it?
- What does it do?
- Why is it necessary? (what breaks without it?)"

Probe with 1-2 questions per turn:

- "Which component is the most surprising or counter-intuitive?"
- "Is there a specific ORDER these must happen in, or are they parallel?"
- "Which component addresses the main reason previous solutions failed?"

### 5. Articulate the Differentiation

"Final piece — why is this different from everything they've tried before?

The audience has already heard promises. They've already tried solutions. What makes your mechanism the one that actually works? Connect it back to the failed attempts from step 3."

Probe with 1-2 questions:

- "What do conventional approaches get wrong that your mechanism gets right?"
- "If you had 10 seconds to explain why your approach is different, what would you say?"

### 6. Synthesize and Confirm

Compile what you learned into a concise summary and present it to the user for validation:

"Here's what I'm capturing for Solução & Mecanismo Único:

**Nome do Mecanismo:** [Named mechanism]

**Por Que Funciona:**
[Core principle — the underlying truth that powers the mechanism]

**Componentes:**
1. **[Component 1]:** [what it is] — [what it does] — [why it's necessary]
2. **[Component 2]:** [what it is] — [what it does] — [why it's necessary]
3. **[Component 3]:** [what it is] — [what it does] — [why it's necessary]
[Additional components if applicable]

**Diferencial:**
[Why this mechanism works when everything else failed — connected to audience's past failed attempts]

**Insight Contra-Intuitivo:**
[The counter-intuitive truth that makes this approach unique]

Does this capture the mechanism accurately? Is the naming right? Anything to refine?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 7. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Solução & Mecanismo Único section content to {outputFile} under the `## 4. Solução & Mecanismo Único` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `5`, update `lastStep` to `solution`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#7-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Solução & Mecanismo Único section has been saved to the output file, will you then load and read fully `./step-06-offer.md` to execute and begin Oferta & Stack de Valor construction.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Unique Mechanism clearly defined — not just "my approach" but a named, structured system
- Mechanism has a compelling name
- 3-5 components mapped with clear purpose
- Differentiation articulated — why this works when other approaches didn't
- Counter-intuitive insight identified
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating the mechanism without user input
- Accepting a generic approach without probing for uniqueness
- Asking more than 2 questions per turn
- Discussing pricing, bonuses, value stack, or close prematurely
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
