---
name: 'step-02-scope'
description: 'Define the research scope: niche, ICP, and key research questions'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-02-scope.md'
nextStepFile: './step-03-sources.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 2: Definir Escopo da Pesquisa

## STEP GOAL:

To define the research scope — the specific niche, ICP characteristics, and key research questions that will guide the Voice Mining process. If a Brand Brief exists, extract and leverage its ICP definition. This step ensures we know exactly WHAT to research before we start looking.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🔍 This is a balanced workflow — prescriptive framework, flexible interpretation

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative research, not command-response
- ✅ You bring research methodology, the user brings market knowledge
- ✅ Maintain direct, analytical tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on defining research scope — WHAT to research
- 🚫 FORBIDDEN to start searching or collecting data (that comes in steps 3-4)
- 💬 Ask 1-2 sharp questions per turn — never more
- 🔍 If Brand Brief exists, extract ICP data to pre-fill scope
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 📖 Track what the user reveals — build understanding progressively
- 🚫 FORBIDDEN to begin web research here — scope definition only

## CONTEXT BOUNDARIES:

- Available context: project_name, project_type from config + Brand Brief ICP (if loaded in step-01)
- Focus: Research scope and questions ONLY
- Limits: Do not start source mapping or Voice Mining yet
- Dependencies: Output document must exist (created in step-01)

## MANDATORY SEQUENCE

### 1. Load Context

Read the existing output document to confirm it's initialized.

If Brand Brief was loaded in step-01 (check if ICP context is in memory), use it to pre-populate scope:

- Extract: ICP demographics, psychographics, pains, desires
- Extract: Market/niche definition, competitive landscape
- Present this as a starting point: "Based on your Brand Brief, here's what I have about your ICP: [summary]. Let me confirm a few things to sharpen the research focus."

If no Brand Brief available, start from scratch:

"Let's define what we're researching. First — who is your ideal customer? Paint me a picture. Not demographics only — I need to understand their world."

### 2. Define ICP for Research

If Brand Brief provided the ICP, confirm and sharpen:

- "Is this still accurate? Any evolution since the Brand Brief?"
- "What specific aspect of their experience do you most need to understand?"

If no Brand Brief, probe with 1-2 questions per turn:

- "What's their daily reality? What frustrates them about [topic]?"
- "Where are they in their journey? Beginners, intermediate, advanced?"
- "What have they already tried that didn't work?"

Typically 2-3 exchanges to get a clear ICP picture.

### 3. Define Research Questions

Once ICP is clear, define what specifically to research:

"Now — what do we need to find out? Here are the research questions I'd propose:

1. **What exact words** does the ICP use to describe their pain?
2. **What solutions** have they tried and what do they say about them?
3. **What objections** do they raise before buying?
4. **What desires** do they express — in their own language?
5. **What triggers** push them to take action?

Which of these are most critical for you? Any questions I should add?"

Let the user prioritize and add questions. 1-2 exchanges.

### 4. Define Niche Boundaries

Clarify the research boundaries:

- "What's the specific niche within this market? (e.g., 'digital marketing for coaches' vs 'digital marketing' broadly)"
- "Any geographic or language boundaries? (e.g., Brazilian Portuguese speakers only)"
- "Any specific product/service category to focus on?"

1-2 exchanges.

### 5. Synthesize and Confirm

Compile the scope into a structured summary and present for validation:

"Here's the research scope I'm capturing:

**Nicho:** [niche definition]
**ICP:** [synthesized ICP description]
**Perguntas-Chave de Pesquisa:**
1. [question 1]
2. [question 2]
3. [question 3]
...
**Limites da Pesquisa:** [geographic, language, category boundaries]
**Fonte de ICP:** [Brand Brief / Defined in this session]

Does this capture it? Anything to adjust?"

Note: The synthesis should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Research Scope section content to {outputFile} under the `## 1. Escopo da Pesquisa` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `2`, update `lastStep` to `scope`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Research Scope section has been saved to the output file, will you then load and read fully `./step-03-sources.md` to execute and begin source mapping.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- ICP clearly defined for research purposes (from Brand Brief or conversation)
- Research questions prioritized and specific
- Niche boundaries established
- User validated the scope
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Starting web research before scope is defined
- Asking more than 2 questions per turn
- Skipping Brand Brief data when it's available
- Proceeding without user validation of scope
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
