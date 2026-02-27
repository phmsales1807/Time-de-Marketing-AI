---
name: 'step-07-close'
description: 'Craft the closing sequence with urgency, final objection handling, CTA, and complete the VSL workflow'

# File References
outputFile: '{content_assets}/vsl-{vsl_name}-{project_name}.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 7: Fechamento & CTA

## STEP GOAL:

To craft the closing sequence — urgency element, final objection handler, clear CTA, and post-CTA reassurance. Then complete the VSL workflow by updating sidecar memories, writing a consolidation overview, and marking the workflow as complete.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a VSL architect and persuasion strategist
- ✅ If you already have a name, communication_style and identity, continue to use those
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring VSL methodology and persuasion frameworks, the user brings deep product knowledge
- ✅ Maintain direct, strategic tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus on close sequence, urgency, CTA, and workflow completion
- 🚫 FORBIDDEN to change previous sections without user consent
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Ensure urgency is REAL, not fabricated — authentic scarcity only
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write final section and update frontmatter to COMPLETE
- 📖 Read the entire output document before beginning close construction
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: Complete output document with all 5 previous sections filled
- Focus: Close sequence, urgency, CTA, and workflow completion
- Limits: This is the final step — no next step
- Dependencies: All previous steps (2-6) must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the entire output document including all 5 completed sections.

Then begin:

"We've built the complete VSL arc — Big Idea, Problem, Story, Mechanism, Offer. Now the final piece: the close.

How do we close? What's the urgency — real, not fabricated? Is there a deadline, limited spots, a price increase, or a genuine reason they should act now?"

### 2. Probe the Urgency Element

Based on user's response, dig deeper with 1-2 questions per turn. Examples:

- "Is this urgency real and defensible? Could someone call you out on it?"
- "What happens if they wait? Is there an actual consequence beyond 'they miss out'?"
- "Is this a launch with a real close date, or evergreen? That changes the urgency approach."
- "Can you create legitimate scarcity — limited cohort size, seasonal timing, price structure?"

Continue probing until the urgency element is authentic and clear. Typically 2-3 exchanges.

### 3. Handle Final Objections

"Before the CTA, we need to address the last objection. The one that's still lingering even after everything we've said.

What's the final objection your audience has right before buying? The voice in their head that says 'but...'?"

Probe with 1-2 questions:

- "What's the #1 reason people who ALMOST buy end up not buying?"
- "Is the objection about money, time, trust, or readiness? How do we address it?"
- "Can we use social proof, the guarantee, or a reframe to neutralize it?"

### 4. Craft the CTA

"What's the specific CTA? We need:

- **Button text** — what does the button say?
- **Destination** — where do they go when they click?
- **Next step** — what happens after they click? (checkout, application, scheduling?)
- **Simplicity** — is the action clear and friction-free?"

Probe with 1-2 questions:

- "Is there a secondary CTA for people who aren't ready yet? (waitlist, free resource, etc.)"
- "What's the post-CTA reassurance — the last thing they see or hear that reinforces the decision?"

### 5. Synthesize and Confirm

Compile what you learned into a concise summary and present it to the user for validation:

"Here's what I'm capturing for Fechamento & CTA:

**Elemento de Urgência:**
[Type of urgency — real deadline, limited spots, price increase, etc.]
[Why it's authentic and defensible]

**Tratamento de Objeção Final:**
[The last objection] → [How we address it]

**CTA:**
- **Texto do Botão:** [button text]
- **Destino:** [where they go]
- **Próximo Passo:** [what happens after click]

**Reassurance Pós-CTA:**
[Final reinforcement — guarantee reminder, social proof, or transformation vision]

**Sequência de Fechamento:**
1. Urgência → 2. Objeção Final → 3. CTA → 4. Reassurance

Does this close the VSL effectively? Is the urgency honest? Is the CTA clear?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Save Close Section

Save the Fechamento & CTA section content to {outputFile} under the `## 6. Fechamento & CTA` heading (replacing the comment placeholder).

### 7. Update Sidecar Memories

Append a VSL session entry to `{sidecarMemories}`:

```markdown
### VSL Session — {vsl_name} — {project_name}
- **Date:** [current date]
- **Project:** {project_name}
- **VSL Name:** {vsl_name}
- **Big Idea:** [one-line summary of the Big Idea]
- **Mechanism:** [mechanism name]
- **Key Insight:** [most valuable insight from this session]
```

If the sidecar memories file doesn't exist, create it with a header and this entry.

### 8. Write Consolidation Overview

Present a final overview of the complete VSL structure:

"**VSL Structure Complete — {vsl_name} — {project_name}**

**Visão Geral da VSL:**

1. **Big Idea & Hook:** [one-line summary]
2. **Problema & Agitação:** [one-line summary]
3. **História & Credibilidade:** [one-line summary]
4. **Solução & Mecanismo Único:** [one-line summary]
5. **Oferta & Stack de Valor:** [one-line summary]
6. **Fechamento & CTA:** [one-line summary]

**Coherence Check:**
- Big Idea → Problem connection: [observation]
- Problem → Story connection: [observation]
- Story → Mechanism connection: [observation]
- Mechanism → Offer connection: [observation]
- Offer → Close connection: [observation]

Any final adjustments before we mark this complete?"

### 9. Mark Workflow Complete

After user confirms or makes final adjustments, update the output document frontmatter:

```yaml
stepsCompleted: [1, 2, 3, 4, 5, 6, 7]
lastStep: 'close'
status: 'COMPLETE'
completedDate: [current date]
```

### 10. Present Completion Summary

"**VSL Structure complete for {project_name} — VSL: {vsl_name}.**

**Document saved to:** `{content_assets}/vsl-{vsl_name}-{project_name}.md`

**What this enables:**
- Copywriter — full VSL script based on this structure
- Video Producer — scene-by-scene breakdown from the arc
- Landing Page Builder — sales page structure mirroring the VSL
- Ad Batch Generator — hooks and angles derived from the Big Idea
- Email Sequence Builder — launch sequences that align with the VSL narrative

This document is your VSL blueprint. Every downstream content production workflow will reference it."

### 11. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [D] Done"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask} — for final deep-dive on any section
- IF P: Execute {partyModeWorkflow} — get other agents' perspectives on the VSL
- IF D: Workflow is complete. Thank the user and end the workflow session. Return to agent menu if within an agent context.
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#11-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- This is the FINAL step — there is no next step to load
- After A or P execution, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

This is the final step of the VSL Structure workflow. When the user selects 'D' (Done), the workflow is complete. There is no next step file to load.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Urgency element is authentic and defensible; final objection identified and addressed
- CTA is clear, specific, and friction-free; post-CTA reassurance provided
- Close section saved to output document; sidecar memories updated
- Complete VSL coherence check performed; frontmatter marked as COMPLETE
- Downstream agent recommendations communicated; user satisfied with final structure

### ❌ SYSTEM FAILURE:

- Generating close content without user input or using fabricated urgency
- Not performing coherence check, not updating sidecar memories, or not marking COMPLETE
- Not saving final document state; changing previous sections without user consent

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
