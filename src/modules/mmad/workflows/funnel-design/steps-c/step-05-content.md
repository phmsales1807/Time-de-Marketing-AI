---
name: 'step-05-content'
description: 'Define content type, format, message, CTA, and lead magnets for each touchpoint'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-05-content.md'
nextStepFile: './step-06-metrics.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 5: Conteúdo por Fase

## STEP GOAL:

To define the content strategy for each touchpoint mapped in step 4. For each touchpoint, determine: content format, key message (aligned with awareness level from step 3), CTA, and placement of lead magnets, content upgrades, and tripwires within the journey.

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

- 🎯 Focus ONLY on content type, format, messaging direction, and CTAs per touchpoint
- 🚫 FORBIDDEN to write actual copy or scripts (that's the Copywriter's job)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Align content with awareness levels defined in step 3
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: step-02 (funnel purpose, offers), step-03 (phases, awareness levels), step-04 (touchpoints, channels)
- Available context: Brand Brief (ICP, positioning, tone) if loaded
- Focus: Content strategy per touchpoint ONLY
- Limits: Do not write actual copy, do not define metrics yet
- Dependencies: Steps 2, 3, and 4 must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review the touchpoints from step 4 and awareness levels from step 3.

Then begin:

"Let's define what content goes at each touchpoint. Not the actual copy — that comes later with the Copywriter. We're defining the content strategy: format, message direction, and CTA.

Looking at your first phase — [Phase 1] — you have these touchpoints: [list from step 4]. For the first one, [touchpoint]: What kind of content makes sense here? (post, reel, long video, email, landing page, webinar, etc.)"

### 2. Map Content per Phase

Work through each phase and its touchpoints. For each, explore with 1-2 questions per turn:

- "What format works best for this touchpoint? (reel, carrossel, vídeo longo, email, landing page, webinar, live, etc.)"
- "Given the awareness level at this phase ([level from step 3]), what's the core message? What do they need to hear?"
- "What's the CTA? What specific action should they take after consuming this content?"
- "Is this touchpoint about education, connection, proof, or conversion?"
- "Does this content need to address a specific objection or desire from your ICP?"

Typically 2-3 exchanges per phase.

### 3. Place Lead Magnets and Tripwires

After mapping content per touchpoint, specifically address lead magnets and tripwires:

"Now let's place the lead magnets and tripwires in the journey. A lead magnet captures the contact. A tripwire converts a lead into a buyer with a low-risk offer.

Where in your funnel does the lead magnet sit? What are you offering in exchange for their contact? And is there a tripwire — a low-ticket entry offer — before the core offer?"

### 4. Probe Content Connections

Explore how content connects across the funnel:

"Looking at the content map as a whole — does each piece naturally lead to the next? Is there a clear content thread that pulls someone through the entire journey?"

Probe gaps with 1-2 questions.

### 5. Synthesize and Confirm

Compile what you learned into a structured content map and present for validation:

"Here's what I'm capturing for Content per Phase:

| Fase | Touchpoint | Formato | Mensagem-Chave | CTA | Tipo |
|------|-----------|---------|----------------|-----|------|
| [Phase 1] | [touchpoint] | [format] | [message] | [CTA] | [education/connection/proof/conversion] |
| ... | ... | ... | ... | ... | ... |

**Lead Magnets:**
- [placement and description]

**Tripwires:**
- [placement and description]

Does this content strategy capture your vision? Anything to add or adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Content per Phase section content to {outputFile} under the `## 4. Conteúdo por Fase` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `5`, update `lastStep` to `content`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Content per Phase section has been saved to the output file, will you then load and read fully `./step-06-metrics.md` to execute and begin Metrics & KPIs definition.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Content format defined for every touchpoint
- Key message direction aligned with awareness levels from step 3
- CTAs defined for every content piece
- Lead magnets and tripwires placed in the journey
- Content connections across funnel verified
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Writing actual copy or scripts instead of content strategy
- Generating content map without user input
- Asking more than 2 questions per turn
- Content messages misaligned with awareness levels
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
