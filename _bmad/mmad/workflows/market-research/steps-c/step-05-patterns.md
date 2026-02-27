---
name: 'step-05-patterns'
description: 'Analyze Voice Mining data for recurring patterns — pains, desires, objections, emotional clusters'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-05-patterns.md'
nextStepFile: './step-06-report.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 5: Análise de Padrões

## STEP GOAL:

To analyze the Voice Mining data collected in step-04 and identify recurring patterns — what themes emerge across multiple sources? What are the dominant pains, desires, objections? Where do emotional language clusters appear? This is where the balanced approach shines: the framework for analysis is prescriptive, but the interpretation is collaborative and flexible.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🔍 Analysis step — interpret data collaboratively with the user

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ Present data-driven analysis — patterns must be grounded in evidence from step-04
- ✅ Flexible interpretation — discuss what the patterns mean with the user
- ✅ Maintain direct, analytical tone — let the data speak

### Step-Specific Rules:

- 🎯 Focus ONLY on analyzing patterns in the Voice Mining data
- 🚫 FORBIDDEN to fabricate patterns not supported by the data
- 💬 Ask 1-2 questions per turn — especially about interpretation
- 📝 All document output in {document_output_language} (Brazilian Portuguese)
- 🔗 Cross-reference with Brand Brief ICP if available

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📊 Ground every pattern claim in specific quotes from step-04
- 🤝 Interpretation is collaborative — present your analysis, ask for user's read

## CONTEXT BOUNDARIES:

- Available context: All previous sections (scope, sources, Voice Mining data)
- Focus: Pattern analysis ONLY
- Limits: Do not compile the final report yet — that's step-06
- Dependencies: Voice Mining data must be collected (step-04 complete)

## MANDATORY SEQUENCE

### 1. Load Voice Mining Data

Read the complete output document, focusing on the Voice Mining section from step-04.

"Let me analyze the Voice Mining data we collected. I'll look for recurring patterns across all sources."

### 2. Identify Pain Patterns

Analyze quotes categorized as pains/dores:

"**Padrões de Dor (Pain Patterns)**

Here's what I see recurring across sources:

**Dor #1: [theme name]**
- Frequency: Mentioned in [X] of [Y] sources
- Example quotes: \"[quote 1]\", \"[quote 2]\"
- Intensity: [high/medium/low based on language strength]

**Dor #2: [theme name]**
- Frequency: ...
- Example quotes: ...
- Intensity: ...

[Continue for all identified pain patterns]

Which of these resonates most with what you hear from your audience?"

### 3. Identify Desire Patterns

Analyze quotes categorized as desires:

"**Padrões de Desejo (Desire Patterns)**

**Desejo #1: [theme name]**
- Frequency: Mentioned in [X] of [Y] sources
- Example quotes: \"[quote 1]\", \"[quote 2]\"
- Strength: [how urgently expressed]

[Continue for all desire patterns]

Any surprises? Anything your audience wants that you didn't expect?"

### 4. Identify Objection Patterns

Analyze quotes categorized as objections:

"**Padrões de Objeção (Objection Patterns)**

**Objeção #1: [theme name]**
- Frequency: Mentioned in [X] of [Y] sources
- Example quotes: \"[quote 1]\", \"[quote 2]\"
- Type: [price/trust/time/complexity/skepticism]

[Continue for all objection patterns]

These objections are copy gold — each one is a message to address. Which ones do you face most?"

### 5. Identify Emotional Language Clusters

Analyze emotional triggers and language patterns:

"**Clusters de Linguagem Emocional (Emotional Language Clusters)**

**Cluster #1: [emotion theme — e.g., frustration with complexity]**
- Key phrases: \"[phrase]\", \"[phrase]\", \"[phrase]\"
- Emotional tone: [frustration/hope/anger/excitement/fear]

**Cluster #2: [emotion theme]**
- Key phrases: ...
- Emotional tone: ...

These emotional clusters reveal HOW the ICP communicates — not just what they say, but the emotional charge behind it."

### 6. Cross-Reference with Brand Brief (If Available)

If Brand Brief exists at `{brandBriefFile}`, read and cross-reference:

"**Cruzamento com Brand Brief:**

- **ICP Alignment:** [do the Voice Mining findings confirm or challenge the Brand Brief ICP?]
- **Pain Validation:** [which Brand Brief pains are confirmed by real data?]
- **Gaps Found:** [what did Voice Mining reveal that wasn't in the Brand Brief?]
- **Language Delta:** [how different is the ICP's actual language from what the Brand Brief assumed?]

This cross-reference is valuable — it shows where your assumptions were right and where the market tells a different story."

If no Brand Brief, skip this section.

### 7. Synthesize and Confirm

Present the complete pattern analysis for validation:

"**Síntese da Análise de Padrões:**

**Top 3 Dores Recorrentes:**
1. [pain] — [frequency/strength]
2. [pain] — [frequency/strength]
3. [pain] — [frequency/strength]

**Top 3 Desejos Mais Comuns:**
1. [desire] — [frequency/strength]
2. [desire] — [frequency/strength]
3. [desire] — [frequency/strength]

**Objeções Frequentes:**
1. [objection] — [type]
2. [objection] — [type]

**Clusters Emocionais Dominantes:**
1. [cluster] — [tone]
2. [cluster] — [tone]

Does this analysis ring true? Anything you'd interpret differently?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 8. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Pattern Analysis section content to {outputFile} under the `## 4. Análise de Padrões` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `5`, update `lastStep` to `patterns`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#8-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Pattern Analysis section has been saved to the output file, will you then load and read fully `./step-06-report.md` to execute and compile the final report.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Patterns grounded in actual Voice Mining data (not fabricated)
- Pain, desire, objection, and emotional patterns all analyzed
- Frequency and intensity assessed for each pattern
- Cross-reference with Brand Brief performed (if available)
- User validated interpretation before saving
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Fabricating patterns not supported by collected data
- Analyzing without referencing specific quotes
- Skipping any pattern category (pains, desires, objections, emotional)
- Not cross-referencing with Brand Brief when available
- Proceeding without user validation
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
