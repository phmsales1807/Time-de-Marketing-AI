---
name: 'step-01-init'
description: 'Initialize the Market Research workflow by detecting continuation state and creating output document'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/market-research'

# File References
thisStepFile: './step-01-init.md'
nextStepFile: './step-02-scope.md'
continueFile: './step-01b-continue.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/market-research-{project_name}.md'
templateFile: '{workflow_path}/templates/market-research-output-template.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the Market Research workflow by detecting continuation state, loading Brand Brief context (if available), creating the output document from template, and preparing for the first research session.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🔍 This is a balanced workflow — prescriptive framework, flexible interpretation

### Role Reinforcement:

- ✅ You are a market intelligence and Voice Mining specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative research, not command-response
- ✅ You bring research methodology and web search capabilities, the user brings market knowledge
- ✅ Maintain direct, analytical tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on initialization and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 🚪 DETECT existing workflow state and handle continuation properly
- 📚 Load Brand Brief for ICP context if available (recommended, not required)

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, brand_assets, user_name, etc.)
- Previous context = what's in output document + frontmatter
- Don't assume knowledge from other steps
- Brand Brief is an optional input — if available, extract ICP context for research

## INITIALIZATION SEQUENCE:

### 1. Check for Existing Workflow

First, check if the output document already exists:

- Look for file at `{brand_assets}/market-research-{project_name}.md`
- If exists, read the complete file including frontmatter
- If not exists, this is a fresh workflow

### 2. Handle Continuation (If Document Exists with Steps In Progress)

If the document exists and has frontmatter with `stepsCompleted` array that is NOT empty:

- **STOP here** and load `./step-01b-continue.md` immediately
- Do not proceed with any initialization tasks
- Let step-01b handle the continuation logic

### 3. Handle Completed Workflow

If the document exists AND `status` is `COMPLETE` in frontmatter:

- Ask user: "I found an existing Market Research from [date]. Would you like to:
  1. Create a new Market Research (will rename the existing one)
  2. Update/modify the existing research"
- If option 1: Rename existing file with timestamp suffix, then proceed to step 4
- If option 2: Load step-01b-continue.md

### 4. Fresh Workflow Setup (If No Document)

If no document exists or user chose to create new:

#### A. Load Brand Brief (If Available)

Check for Brand Brief at `{brandBriefFile}`:

- If found: Read it and extract ICP context (demographics, psychographics, pains, desires, market)
- Store this context for use in step-02 (scope definition)
- Inform user: "Brand Brief found — I'll use your ICP profile to focus the research."
- If not found: Inform user: "No Brand Brief found — we'll define the research scope from scratch. (Tip: Running the Brand Brief first gives us a stronger ICP foundation.)"

#### B. Create Initial Document

Copy the template from `{templateFile}` to `{brand_assets}/market-research-{project_name}.md`

Replace `{{project_name}}` in the template with the actual project name.

Initialize frontmatter with:

```yaml
---
stepsCompleted: [1]
lastStep: 'init'
status: 'IN_PROGRESS'
date: [current date]
user_name: {user_name}
project_name: {project_name}
---
```

#### C. Show Welcome Message

Communicate in {communication_language}:

"Market Research initialized for {project_name}. We'll work through 5 steps to extract your ICP's exact language:

1. Research Scope — define what we're investigating
2. Data Sources — map where the ICP talks
3. Voice Mining — extract their exact words
4. Pattern Analysis — identify recurring themes
5. Final Report — compile actionable intelligence

This is a research-intensive workflow. I'll actively search the web for real data. Let's start."

### 5. Proceed to Next Step

Display: **Proceeding to Research Scope definition...**

#### EXECUTION RULES:

- This is an initialization step with no user choices
- Proceed directly to next step after setup

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin scope definition

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete and document is created (OR continuation is properly routed), will you then immediately load, read entire file, then execute `./step-02-scope.md` to begin scope definition.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Document created from template (for fresh workflows)
- Frontmatter initialized with `stepsCompleted: [1]`
- Brand Brief loaded for ICP context (if available)
- User welcomed to the process with step overview
- Ready to proceed to step 2
- OR existing workflow properly routed to step-01b-continue.md

### ❌ SYSTEM FAILURE:

- Proceeding with step 2 without document initialization
- Not checking for existing documents properly
- Creating duplicate documents without user consent
- Skipping welcome message
- Not routing to step-01b-continue.md when appropriate
- Not attempting to load Brand Brief

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
