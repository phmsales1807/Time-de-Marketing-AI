---
name: 'step-02-brand-brief'
description: 'Validate and present Brand Brief context for this specific Mandala campaign'

# File References
nextStepFile: './step-03-funnel-phases.md'
outputFile: '{campaign_assets}/mandala-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 2: Contexto da Marca — INTENT-BASED

## STEP GOAL:

To validate the Brand Brief context loaded during initialization and narrow it to the specific product, offer, and campaign objective for this Mandala. This step bridges the general Brand Brief to the specific creative campaign.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input — YOU ARE A FACILITATOR
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring the VTSD method and creative matrix expertise, the user brings deep brand and campaign knowledge
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on validating Brand Brief context and defining campaign scope
- 🚫 FORBIDDEN to discuss awareness levels or creative types yet (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🚫 FORBIDDEN to generate section content yourself — compile from what the user shared
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: Brand Brief data loaded in init (ICP, positioning, tone, promise, market)
- Focus: Campaign-specific context ONLY
- Limits: Do not explore awareness levels or creative types yet
- Dependencies: Output document must exist (created in step-01)

## MANDATORY SEQUENCE

### 1. Present Brand Brief Context

Read the existing output document to confirm it's initialized.

Then present the key Brand Brief context loaded during init:

"Here's what I have from your Brand Brief:

**ICP:** [summary from Brand Brief]
**Positioning:** [summary from Brand Brief]
**Tone of Voice:** [summary from Brand Brief]
**Promise:** [summary from Brand Brief]

Now let's narrow this to the specific campaign. What specific product or offer is this Mandala for?"

### 2. Define Campaign Scope

Based on user's response, ask 1-2 questions to clarify campaign scope:

- "What's the campaign objective — awareness, conversion, retargeting, or a mix?"
- "What's the primary platform or channel for this campaign?"
- "Is there a specific promotion, launch, or event driving this?"
- "What's the budget/volume expectation — how many ad variations do you need?"

Continue probing until campaign scope is clear. Typically 2-3 exchanges.

### 3. Confirm Campaign Relevance

Validate that the Brand Brief context applies to this specific campaign:

"Looking at your ICP and positioning through the lens of this campaign:
- Does the ICP match your target audience for THIS specific offer?
- Any adjustments to the tone for this campaign context?
- Any competitor activity or market conditions to consider?"

### 4. Synthesize and Confirm

Compile what you learned into a concise campaign context and present for validation:

"Here's what I'm capturing for Campaign Context:

**Produto/Oferta:** [specific product/offer for this Mandala]
**Objetivo da Campanha:** [awareness/conversion/retargeting]
**Público-Alvo:** [ICP adjusted for this campaign]
**Posicionamento Aplicado:** [positioning for this specific campaign]
**Tom de Voz:** [tone adjustments if any]
**Plataformas Primárias:** [channels]
**Contexto de Mercado:** [relevant market conditions]

Does this capture the campaign context accurately? Anything to add or adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 5. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Campaign Context section content to {outputFile} under the `## 1. Contexto da Marca` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `2`, update `lastStep` to `brand-brief`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#5-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Campaign Context section has been saved to the output file, will you then load and read fully `./step-03-funnel-phases.md` to execute and begin Funnel Phases selection.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Brand Brief context presented and validated with user
- Campaign-specific product/offer identified
- Campaign objective defined (awareness/conversion/retargeting)
- ICP adjustments for this campaign captured
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating campaign context without user input
- Asking more than 2 questions per turn
- Discussing awareness levels or creative types prematurely
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
