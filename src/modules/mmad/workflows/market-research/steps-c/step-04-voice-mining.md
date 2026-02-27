---
name: 'step-04-voice-mining'
description: 'Core step — extract exact quotes, phrases, and expressions the ICP uses from identified sources'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-04-voice-mining.md'
nextStepFile: './step-05-patterns.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 4: Voice Mining (CORE STEP)

## STEP GOAL:

This is the HEART of the Market Research workflow. Use Web Search and Web Fetch to actively search the sources identified in step-03, extract exact quotes, phrases, and expressions the ICP uses, and categorize them by type. The ICP's literal language is gold — their exact words power better copy, ads, and content than any marketer's rewrite.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🔍 This is the core research step — use Web Search / Web Fetch ACTIVELY

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative research — you bring the research tools, the user validates
- ✅ Maintain direct, analytical tone — present data, not opinions
- ✅ Source attribution is MANDATORY — every quote needs a source

### Step-Specific Rules:

- 🎯 Focus ONLY on extracting real language from real sources
- 🌐 USE WEB SEARCH AND WEB FETCH EXTENSIVELY — this is the research step
- 💬 Present findings in batches, ask 1-2 questions between batches
- 📝 All document output in {document_output_language} (Brazilian Portuguese)
- 🔗 ALWAYS attribute sources — quote + platform + context
- ⏳ This step may take MULTIPLE exchanges — let the research breathe

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 🌐 Search actively — use the source map from step-03 as your research target list
- 📊 Categorize findings as you go — don't dump raw data
- 🚫 FORBIDDEN to fabricate quotes — only use what you actually find via search

## CONTEXT BOUNDARIES:

- Available context: Research scope (step-02) + Source map (step-03)
- Focus: Extracting and categorizing real ICP language
- Limits: Analysis of patterns comes in step-05 — here we COLLECT
- Dependencies: Source map must be defined (step-03 complete)

## MANDATORY SEQUENCE

### 1. Load Research Context

Read the output document and recall:
- Research scope and ICP from step-02
- Source map and keywords from step-03

Then begin Voice Mining:

"Time for the core research. I'll search the sources we mapped and extract the ICP's exact language. I'll present findings in batches — validate as we go."

### 2. Mine High Priority Sources

Start with high-priority sources from the source map. For EACH high-priority source:

#### A. Search
Use **Web Search** with the keywords defined in step-03:
- Search: "[keyword] site:[source URL]" or "[keyword] [platform] [niche]"
- Try multiple keyword combinations from the research questions
- Search for discussions about pains, frustrations, desires, objections

#### B. Extract
From search results, use **Web Fetch** when needed to access specific pages and extract:
- **Exact quotes** — the ICP's literal words (in quotes)
- **Phrases and expressions** — recurring language patterns
- **Context** — what they were discussing when they said it

#### C. Present Batch
After mining 2-3 sources, present findings to the user:

"**Voice Mining — Batch [n]**

**Fonte:** [platform/source]

**Dores (Pains):**
- \"[exact quote]\" — [source context]
- \"[exact quote]\" — [source context]

**Desejos (Desires):**
- \"[exact quote]\" — [source context]

**Objeções (Objections):**
- \"[exact quote]\" — [source context]

**Linguagem Emocional (Emotional Language):**
- \"[exact quote]\" — [source context]

Anything resonate? Should I dig deeper into any of these themes, or continue to next sources?"

### 3. Mine Medium Priority Sources

Continue with medium-priority sources, following the same Search → Extract → Present pattern.

Present findings and check with user:
- "Any of these surprise you?"
- "Is this consistent with what you hear from your audience?"

### 4. Mine Low Priority Sources (Optional)

If user wants more data, mine low-priority sources. Otherwise, proceed to synthesis.

"Should I search the remaining sources, or do we have enough data? We can always come back."

### 5. Compile Voice Mining Findings

After all mining rounds, compile the full findings:

"Here's the complete Voice Mining collection:

**Dores — As Palavras Exatas do ICP:**
| Citação | Fonte | Categoria |
|---------|-------|-----------|
| \"[quote]\" | [source] | [subcategory] |
| ... | ... | ... |

**Desejos — O Que Querem nas Próprias Palavras:**
| Citação | Fonte | Categoria |
|---------|-------|-----------|
| \"[quote]\" | [source] | [subcategory] |
| ... | ... | ... |

**Objeções — Resistências e Dúvidas:**
| Citação | Fonte | Categoria |
|---------|-------|-----------|
| \"[quote]\" | [source] | [subcategory] |
| ... | ... | ... |

**Gatilhos Emocionais — Linguagem com Carga Afetiva:**
| Citação | Fonte | Contexto |
|---------|-------|----------|
| \"[quote]\" | [source] | [context] |
| ... | ... | ... |

**Total de Citações Coletadas:** [count]
**Fontes Pesquisadas:** [count]

Does this feel comprehensive? Any gaps?"

Note: All content in {document_output_language}.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Voice Mining section content to {outputFile} under the `## 3. Voice Mining` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `4`, update `lastStep` to `voice-mining`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Voice Mining section has been saved to the output file, will you then load and read fully `./step-05-patterns.md` to execute and begin pattern analysis.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Web Search used extensively to find real ICP language
- Exact quotes extracted with source attribution
- Findings categorized: pains, desires, objections, emotional triggers
- Multiple sources searched (not just one)
- Findings presented in batches for user validation
- User confirmed comprehensiveness before moving on
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Not using Web Search / Web Fetch actively
- Fabricating quotes or data not found via actual search
- Presenting all findings at once without batched validation
- Not attributing sources
- Mining only one platform when multiple were mapped
- Asking more than 2 questions per turn
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
