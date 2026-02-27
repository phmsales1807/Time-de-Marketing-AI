---
name: 'step-06-metrics'
description: 'Define measurable success metrics and KPIs for each funnel phase'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-06-metrics.md'
nextStepFile: './step-07-consolidation.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 6: Métricas & KPIs

## STEP GOAL:

To define measurable success metrics for each funnel phase. Identify the critical metric per phase, set benchmarks for the infoproduto market, and define what "broken" looks like — the signals that tell you a phase needs investigation.

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

- 🎯 Focus ONLY on metrics, KPIs, and benchmarks per funnel phase
- 🚫 FORBIDDEN to redesign the funnel or change phases/touchpoints
- 💬 Ask 1-2 sharp, open-ended questions per turn — never more
- 🔍 Ground metrics in the infoproduto context when setting benchmarks
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to generate the section content yourself — compile from what the user shared

## CONTEXT BOUNDARIES:

- Available context: steps 2-5 (full funnel structure: purpose, phases, touchpoints, content)
- Available context: Brand Brief (ICP, positioning, offer) if loaded
- Focus: Metrics and KPIs per phase ONLY
- Limits: Do not redesign the funnel structure
- Dependencies: Steps 2, 3, 4, and 5 must be completed

## MANDATORY SEQUENCE

### 1. Set the Stage

Read the existing output document to review all previous sections — the complete funnel structure.

Then begin:

"Your funnel structure is mapped — phases, touchpoints, and content. Now let's define how you'll know it's working.

For each phase, we need: the key metrics, a critical metric (the one that determines if the phase works), benchmarks, and what 'broken' looks like.

Starting with [Phase 1]: What does success look like at this stage? How would you measure it?"

### 2. Map Metrics per Phase

Work through each phase. For each, explore with 1-2 questions per turn. Typical metrics by context:

- **Discovery/Awareness:** reach, impressions, profile visits, follower growth rate
- **Engagement:** engagement rate, saves, shares, comments, DM conversations
- **Consideration:** click-through rate, landing page visits, time on page, lead magnet downloads
- **Decision:** opt-in rate, webinar registration, application rate
- **Purchase:** conversion rate, average order value (AOV), cart abandonment rate
- **Onboarding:** activation rate, completion rate, time to first value
- **Retention:** churn rate, repeat purchase rate, lifetime value (LTV), NPS

Questions to ask:

- "For [phase], what's the ONE metric that tells you this phase is working?"
- "What numbers are you seeing today (if any)? What would 'good' look like?"
- "If this metric drops, what does that signal? What would you investigate?"
- "Are there any vanity metrics you've been tracking that don't actually matter?"

Typically 2-3 exchanges per phase group (can batch related phases).

### 3. Set Benchmarks

After metrics are defined, help ground them:

"Let's set benchmarks. For infoprodutos in Brazil, typical ranges are:

- Email opt-in rate: 20-40% (landing page)
- Sales page conversion: 1-5% (cold traffic), 5-15% (warm traffic)
- Webinar show-up rate: 30-50%
- Cart abandonment recovery: 5-15%

These are starting points — your numbers may differ based on niche and audience. Do you have any existing data we can use as a baseline?"

### 4. Define "Broken" Signals

For each phase, define what failure looks like:

"For each phase, let's define what 'broken' looks like — the signal that tells you something needs attention.

For [phase], if [critical metric] drops below [threshold], what does that tell you? What would you check first?"

Probe 1-2 questions per phase.

### 5. Synthesize and Confirm

Compile what you learned into a metrics dashboard and present for validation:

"Here's what I'm capturing for Metrics & KPIs:

| Fase | Métrica Crítica | Benchmark | Outras Métricas | Sinal de Quebra |
|------|----------------|-----------|-----------------|-----------------|
| [Phase 1] | [critical metric] | [benchmark] | [other metrics] | [broken signal] |
| [Phase 2] | [critical metric] | [benchmark] | [other metrics] | [broken signal] |
| ... | ... | ... | ... | ... |

Does this metrics framework capture what you need to measure? Anything to add or adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Metrics & KPIs section content to {outputFile} under the `## 5. Métricas & KPIs` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `6`, update `lastStep` to `metrics`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Metrics & KPIs section has been saved to the output file, will you then load and read fully `./step-07-consolidation.md` to execute and begin Consolidation.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Metrics defined for every funnel phase
- Critical metric identified per phase
- Benchmarks set (grounded in infoproduto context where possible)
- "Broken" signals defined for each phase
- User validated the synthesis
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Generating metrics without user input
- Asking more than 2 questions per turn
- Redesigning the funnel structure instead of measuring it
- Setting arbitrary benchmarks without user discussion
- Proceeding without user validation of synthesis
- Not saving content to output file before loading next step

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
