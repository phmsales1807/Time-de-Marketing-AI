---
name: 'step-03-sources'
description: 'Map data sources where the ICP talks — Reddit, YouTube, Substack, forums, review sites'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-03-sources.md'
nextStepFile: './step-04-voice-mining.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'

# Task References
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 3: Fontes de Dados

## STEP GOAL:

To systematically map WHERE the ICP talks online — identifying specific subreddits, YouTube channels, Substack newsletters, Facebook groups, Instagram accounts, TikTok creators, forums, review sites, and communities. This creates the research target list for Voice Mining.

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

- 🎯 Focus ONLY on identifying and mapping data sources
- 🚫 FORBIDDEN to start extracting Voice Mining data (that's step 4)
- 💬 Ask 1-2 questions per turn — never more
- 🌐 USE WEB SEARCH to discover relevant communities and sources
- 📝 All document output in {document_output_language} (Brazilian Portuguese)

## EXECUTION PROTOCOLS:

- 🎯 Follow the MANDATORY SEQUENCE exactly
- 💾 Write section content to output file ONLY when user selects 'C' (Continue)
- 🌐 Actively use Web Search to discover sources — don't rely only on user knowledge
- 🚫 FORBIDDEN to start mining quotes from sources — just MAP them here

## CONTEXT BOUNDARIES:

- Available context: Research scope from step-02 (ICP, niche, research questions)
- Focus: Source discovery and mapping ONLY
- Limits: Do not extract quotes or data yet — just identify WHERE to look
- Dependencies: Research scope must be defined (step-02 complete)

## MANDATORY SEQUENCE

### 1. Load Research Context

Read the output document and recall the research scope defined in step-02:

- ICP profile
- Research questions
- Niche boundaries

Then begin source mapping:

"Now we need to find WHERE your ICP hangs out online. I'll search for relevant communities and sources. Let me start with what I can find."

### 2. Search for Sources by Platform

Use **Web Search** to discover sources. Search systematically by platform type:

#### A. Reddit
Search for relevant subreddits where the ICP discusses their problems:
- Search: "[niche] site:reddit.com" and related terms
- Identify specific subreddits (e.g., r/entrepreneurs, r/digitalmarketing)
- Note subscriber count and activity level when visible

#### B. YouTube
Search for channels and videos where ICP engages in comments:
- Search: "[niche] [ICP pain] YouTube"
- Identify channels with active comment sections
- Note channels the ICP watches (not just creates)

#### C. Substack / Newsletters
Search for newsletters covering the niche:
- Search: "[niche] Substack" or "[topic] newsletter"
- Identify publications with engaged audiences

#### D. Forums & Communities
Search for niche-specific forums and communities:
- Search: "[niche] forum" or "[niche] community"
- Include Facebook groups, Discord servers, Slack communities

#### E. Review Sites & Marketplaces
Search for places where ICP reviews products/services:
- Search: "[competitor/product type] reviews"
- Hotmart, Udemy, Amazon reviews for relevant products
- G2, Trustpilot, Reclame Aqui for service reviews

#### F. Social Media (Instagram, TikTok)
Search for relevant accounts and hashtags:
- Search: "[niche] Instagram" or "[topic] TikTok"
- Identify hashtags the ICP uses

Present findings after each platform search. Ask user: "Any sources I'm missing? Communities you know the ICP frequents?"

### 3. User Input on Sources

After presenting discovered sources, ask 1-2 questions:

- "Which of these do you know your ICP actively uses?"
- "Are there any specific communities, groups, or creators you know your audience follows?"
- "Any competitor communities we should look at?"

1-2 exchanges to supplement web search findings with user knowledge.

### 4. Prioritize Sources

Organize all sources by research value:

"Here are the sources I'd prioritize for Voice Mining:

**Alta Prioridade** (rich discussion, easy to mine):
- [sources with active text-based discussions]

**Média Prioridade** (useful but harder to extract):
- [sources with less text or harder access]

**Baixa Prioridade** (supplementary):
- [sources with limited but relevant data]

**Palavras-Chave para Busca:** [list of keywords and phrases to search within these sources]"

### 5. Compile Source Map

Present the structured source map for validation:

"Here's the complete source map:

**Mapeamento de Fontes de Dados**

| Plataforma | Fonte Específica | Prioridade | Tipo de Conteúdo |
|-----------|-----------------|------------|-----------------|
| Reddit | r/[subreddit] | Alta | Threads, comentários |
| YouTube | [channel] | Média | Comentários |
| ... | ... | ... | ... |

**Palavras-Chave de Busca:** [keyword list]
**Total de Fontes Mapeadas:** [count]

Does this map look complete? Any sources to add or remove?"

Note: The source map should be in {document_output_language} since it will go into the document.

### 6. Present MENU OPTIONS

Display: "**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Continue"

#### Menu Handling Logic:

- IF A: Execute {advancedElicitationTask}
- IF P: Execute {partyModeWorkflow}
- IF C: Save the Data Sources section content to {outputFile} under the `## 2. Fontes de Dados` heading (replacing the comment placeholder), update frontmatter `stepsCompleted` to add `3`, update `lastStep` to `sources`, then load, read entire file, then execute {nextStepFile}
- IF Any other comments or queries: help user respond then [Redisplay Menu Options](#6-present-menu-options)

#### EXECUTION RULES:

- ALWAYS halt and wait for user input after presenting menu
- ONLY proceed to next step when user selects 'C'
- After other menu items execution completes, redisplay the menu
- User can chat or ask questions - always respond when conversation ends, redisplay the menu

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN [C continue option] is selected and the Data Sources section has been saved to the output file, will you then load and read fully `./step-04-voice-mining.md` to execute and begin Voice Mining.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Multiple platforms searched via Web Search
- Specific sources identified (not just "Reddit" but "r/specificSubreddit")
- Sources prioritized by research value
- Keywords for searching within sources defined
- User validated and supplemented the source map
- Content saved to output document in {document_output_language}
- Frontmatter updated with stepsCompleted
- Menu presented and user input handled correctly

### ❌ SYSTEM FAILURE:

- Not using Web Search to discover sources
- Listing generic platforms without specific sources
- Starting to extract Voice Mining data
- Asking more than 2 questions per turn
- Proceeding without user validation
- Not saving content to output file before loading next step
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
