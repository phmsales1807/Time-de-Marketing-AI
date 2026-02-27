---
name: 'step-06-offer'
description: 'Build the complete value stack with offer structure, bonuses, price anchoring, and guarantee'

# File References
nextStepFile: './step-07-close.md'
outputFile: '{content_assets}/vsl-{vsl_name}-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 6: Oferta & Stack de Valor

## STEP GOAL:

To build the complete offer structure — core deliverable, bonuses, value stack, price anchoring, and guarantee. The offer stack must make the decision feel like a no-brainer: the value-to-price ratio should be so compelling that NOT buying feels like the wrong choice.

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

- 🎯 Focus ONLY on offer structure, value stack, pricing, and guarantee
- 🚫 FORBIDDEN to discuss close sequence, urgency, or CTA (those come in the final step)
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Probe for specifics — vague offer descriptions weaken the VSL
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: steps 2-5 (Big Idea, Problem, Story, Mechanism — the full VSL narrative)
- Available context: Brand Brief (offer structure, positioning) if loaded
- Focus: Offer construction and value stack ONLY
- Limits: Do not discuss close sequence, urgency elements, or CTA yet
- Dependencies: Steps 2, 3, 4, and 5 must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review all previous sections — the full VSL narrative so far.

Then begin:

"The audience now understands the Big Idea, feels the pain, believes the story, and sees the mechanism. It's time to present the offer.

Let's build the offer stack. What's the main deliverable — the core thing they get when they buy?"

### 2. Probe the Core Offer

Based on user's response, dig deeper with 1-2 questions per turn. Examples:

- "What exactly does the buyer get? Be specific — modules, hours, access, format?"
- "What transformation does the core offer deliver? From [current state] to [desired state]?"
- "How does the core offer connect to the Unique Mechanism from the previous step?"
- "Is this a one-time purchase or recurring? What's the delivery format?"

Continue probing until the core offer is crystal clear. Typically 2-3 exchanges.

### 3. Build the Bonus Stack

"Now let's add the bonuses. What additional elements strengthen the core offer?

Great bonuses do one of three things:
- **Accelerate** the result (get there faster)
- **Simplify** the process (make it easier)
- **Eliminate** a specific objection (remove a barrier)

What bonuses do you have or could you offer? For each: what is it, what does it do, and what would it cost separately?"

Probe with 1-2 questions per turn:

- "Which bonus addresses the #1 reason someone would hesitate to buy?"
- "Is there a bonus that makes someone say 'I'd buy it just for THIS'?"
- "Do you have any fast-action or limited bonuses that create additional incentive?"

### 4. Construct the Value Stack

"Let's build the value stack. For each item, we need a realistic standalone value:

- Core offer — what would someone pay for this alone?
- Bonus 1 — standalone value?
- Bonus 2 — standalone value?
- [Additional bonuses]

What's the total value if they bought each piece separately?"

Probe with 1-2 questions:

- "Are these values defensible? Could you actually sell each piece at that price?"
- "What's the actual price point? And what's the value-to-price ratio?"

### 5. Define the Guarantee

"What guarantee removes the risk? The guarantee should make the buyer think 'I literally can't lose.'

Options to consider:
- **Money-back guarantee** — how many days? Conditional or unconditional?
- **Results-based guarantee** — 'If you don't get [result], we'll [action]'
- **Better-than-money-back** — 'Keep the bonuses even if you refund'

What guarantee feels right for this offer?"

Probe with 1-2 questions:

- "What would make someone who's been burned before feel safe to buy?"
- "Is the guarantee conditional (must complete the work) or unconditional?"

### 6. Synthesize and Confirm

Compile what you learned into a concise summary and present it to the user for validation:

"Here's what I'm capturing for Oferta & Stack de Valor:

**Oferta Principal:**
[Core deliverable — specific details, format, access]

**Bônus:**
1. **[Bonus 1]:** [what it is] — Valor: R$ [value]
2. **[Bonus 2]:** [what it is] — Valor: R$ [value]
3. **[Bonus 3]:** [what it is] — Valor: R$ [value]
[Additional bonuses if applicable]

**Stack de Valor:**
| Item | Valor Individual |
|------|-----------------|
| Oferta Principal | R$ [value] |
| Bônus 1 | R$ [value] |
| Bônus 2 | R$ [value] |
| Bônus 3 | R$ [value] |
| **Total** | **R$ [total]** |

**Preço Real:** R$ [actual price]
**Âncora de Preço:** R$ [anchor] → R$ [actual price] (ratio: [X]:1)

**Garantia:**
[Guarantee type, duration, and terms]

Does this capture the complete offer stack? Is the value-to-price ratio compelling? Anything to adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 7. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Oferta & Stack de Valor section content to {outputFile} under the `## 5. Oferta & Stack de Valor` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `6`, update `lastStep` to `offer`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#7-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Oferta & Stack de Valor section has been saved to the output file, will you then load and read fully `./step-07-close.md` to execute and begin Fechamento & CTA construction.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Core offer clearly defined with specific deliverables (not vague descriptions)
- Bonus stack built with clear purpose (accelerate, simplify, or eliminate objection)
- Value stack constructed with defensible individual values
- Price anchoring established with compelling value-to-price ratio
- Guarantee defined that removes buyer risk
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating offer details without user input
- Accepting vague offer descriptions without probing for specifics
- Asking more than 2 questions per turn
- Discussing close sequence, urgency, or CTA prematurely
- Creating inflated value numbers without user confirmation
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
