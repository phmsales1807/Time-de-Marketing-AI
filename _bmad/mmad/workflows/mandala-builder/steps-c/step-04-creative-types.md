---
name: 'step-04-creative-types'
description: 'Select creative types from the 10 options for this Mandala campaign'

# File References
nextStepFile: './step-05-matrix.md'
outputFile: '{campaign_assets}/mandala-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 4: Tipos de Criativos — INTENT-BASED

## STEP GOAL:

To help the user select 4-6 creative types from the 10 available options for this Mandala cycle. The creative types define the columns of the matrix — they determine the creative approaches that will be combined with awareness levels to produce ad variations.

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
- ✅ You bring creative type expertise and performance knowledge, the user brings brand affinity and experience
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on creative type selection
- 🚫 FORBIDDEN to start building the matrix or generating briefs (those come later)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🚫 FORBIDDEN to generate section content yourself — compile from what the user shared
- 📝 All document output in {document_output_language} (Brazilian Portuguese)
- 📚 Reference sidecar memories for past creative performance if available

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: step-02 (campaign context), step-03 (selected awareness levels)
- Available context: Mandala-matrix data (10 creative types with descriptions)
- Available context: Sidecar memories (past creative performance, if loaded in init)
- Focus: Creative type selection ONLY
- Limits: Do not build the matrix or generate briefs yet
- Dependencies: Steps 2 and 3 must be completed

## MANDATORY SEQUENCE

### 1. Present Creative Types

Read the existing output document to review campaign context (step 2) and selected awareness levels (step 3).

Then present all 10 creative types from the mandala-matrix data:

"Now let's select the creative types for your Mandala. Here are the 10 options:

1. **[Type 1]** — [description from mandala-matrix data]
2. **[Type 2]** — [description from mandala-matrix data]
3. **[Type 3]** — [description from mandala-matrix data]
4. **[Type 4]** — [description from mandala-matrix data]
5. **[Type 5]** — [description from mandala-matrix data]
6. **[Type 6]** — [description from mandala-matrix data]
7. **[Type 7]** — [description from mandala-matrix data]
8. **[Type 8]** — [description from mandala-matrix data]
9. **[Type 9]** — [description from mandala-matrix data]
10. **[Type 10]** — [description from mandala-matrix data]

[If sidecar has history]: From your previous Mandala sessions, I see that [types used before] were tested — [performance notes].

Which creative types resonate most with your brand and audience?"

### 2. Probe Creative Experience

Based on user's response, dig deeper with 1-2 questions:

- "Any types you've tested before? What worked, what didn't?"
- "Which types best match your brand's tone of voice — [tone from step 2]?"
- "For your campaign objective ([objective from step 2]), which types tend to drive [awareness/conversion/retargeting] best?"
- "Are there any types you want to deliberately avoid? Why?"
- "What's your production capacity — do you have team/tools for video, design, UGC?"

Continue probing until selection is clear. Typically 2-3 exchanges.

### 3. Recommend Selection

Help the user finalize 4-6 creative types:

"Based on what you've shared, here's a suggested selection for this Mandala cycle:

**Selected (4-6 types):**
- [Type] — [reason from conversation]
- [Type] — [reason from conversation]
- [Type] — [reason from conversation]
- [Type] — [reason from conversation]
- [Type if applicable] — [reason from conversation]
- [Type if applicable] — [reason from conversation]

This gives us [N] columns in the matrix, crossed with [N] awareness levels = [N×M] cells to evaluate. Does this selection feel right?"

### 4. Synthesize and Confirm

Compile what you learned into a structured selection and present for validation:

"Here's what I'm capturing for Creative Types:

**Tipos de Criativos Selecionados:**

| Tipo | Justificativa | Experiência Anterior |
|------|--------------|---------------------|
| [Type] | [reason from conversation] | [past experience or 'Novo'] |
| [Type] | [reason from conversation] | [past experience or 'Novo'] |
| [Type] | [reason from conversation] | [past experience or 'Novo'] |
| [Type] | [reason from conversation] | [past experience or 'Novo'] |

**Total de Tipos:** [N]
**Capacidade de Produção:** [production capacity notes]
**Tipos Evitados:** [any deliberately excluded types and why]

Does this capture your creative type selection accurately? Anything to add or adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 5. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Creative Types section content to {outputFile} under the `## 3. Tipos de Criativos` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `4`, update `lastStep` to `creative-types`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#5-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Creative Types section has been saved to the output file, will you then load and read fully `./step-05-matrix.md` to execute and begin Priority Matrix construction.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- All 10 creative types presented from mandala-matrix data
- Sidecar history referenced if available
- User selected 4-6 types through conversation
- Rationale and past experience captured for each type
- Production capacity considered
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating creative type selection without user input
- Asking more than 2 questions per turn
- Starting to build the matrix or generate briefs prematurely
- Selecting types FOR the user instead of facilitating the decision
- Not referencing sidecar memories when available
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
