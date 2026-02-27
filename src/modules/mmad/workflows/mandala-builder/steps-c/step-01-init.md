---
name: 'step-01-init'
description: 'Initialize the Mandala Builder workflow by detecting continuation state, loading Brand Brief, sidecar memories, and mandala-matrix data'

# File References
nextStepFile: './step-02-brand-brief.md'
continueFile: './step-01b-continue.md'
outputFile: '{campaign_assets}/mandala-{project_name}.md'
templateFile: '../templates/mandala-output-template.md'

# Input Documents
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
mandalaMatrixData: '{project-root}/_bmad/mmad/data/mandala-matrix.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the Mandala Builder workflow by detecting continuation state, loading the Brand Brief (REQUIRED), loading mandala-matrix data, checking sidecar memories for previous Mandala history, creating the output document from template, and preparing for the first collaborative session.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🎯 This is a mixed workflow — intent steps facilitate, prescriptive steps generate

### Role Reinforcement:

- ✅ You are a VTSD method specialist and Mandala da Criatividade Infinita expert
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring the VTSD method and creative matrix expertise, the user brings deep brand and campaign knowledge
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on initialization and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 🚪 DETECT existing workflow state and handle continuation properly
- 📄 Brand Brief is REQUIRED context — STOP if not found

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, campaign_assets, brand_assets, user_name, etc.)
- Previous context = what's in output document + frontmatter
- Don't assume knowledge from other steps
- Brand Brief provides: ICP, positioning, tone of voice, promise, market context
- Mandala-matrix data provides: 5 awareness levels, 10 creative types, efficacy ratings

## INITIALIZATION SEQUENCE:

### 1. Check for Existing Workflow

First, check if the output document already exists:

- Look for file at `{outputFile}`
- If exists, read the complete file including frontmatter
- If not exists, this is a fresh workflow

### 2. Handle Continuation (If Document Exists with Steps In Progress)

If the document exists and has frontmatter with `stepsCompleted` array that is NOT empty:

- **STOP here** and load `{continueFile}` immediately
- Do not proceed with any initialization tasks
- Let step-01b handle the continuation logic

### 3. Handle Completed Workflow

If the document exists AND `status` is `COMPLETE` in frontmatter:

- Ask user: "I found an existing Mandala from [date]. Would you like to:
  1. Create a new Mandala (will rename the existing one)
  2. Update/modify the existing Mandala"
- If option 1: Rename existing file with timestamp suffix, then proceed to step 4
- If option 2: Load {continueFile}

### 4. Load Brand Brief (REQUIRED)

Load the Brand Brief from `{brandBriefFile}`:

- If found: Read and extract key context:
  - **ICP:** Ideal Customer Profile (demographics, psychographics, pains, desires, objections, purchase triggers)
  - **Positioning:** Unique positioning and differentiators
  - **Tone of Voice:** Brand personality, archetypes, language patterns
  - **Promise & Offer:** Core promise, offer structure, transformation statement
  - **Market Context:** Problem, market, awareness level, competitive landscape
- Store these as context for the workflow
- If NOT found: **STOP** and display:
  "🛑 Brand Brief not found at `{brandBriefFile}`. The Mandala Builder REQUIRES a completed Brand Brief — it is the foundation for all creative decisions. Please complete the Brand Brief first using the Brand Strategist agent, then return here."
  - Do NOT proceed. End the workflow initialization.

### 5. Load Mandala Matrix Data

Load the mandala-matrix data from `{mandalaMatrixData}` (passed from workflow init as data context):

- Extract the 5 Schwartz awareness levels with descriptions
- Extract the 10 creative types with descriptions
- Extract efficacy ratings (awareness level × creative type cross)
- Store as reference data for steps 3-5

### 6. Check Sidecar Memories

Check for sidecar memories at `{sidecarMemories}`:

- If found: Read and check for previous Mandala session entries for this project
- Note any relevant history: past creative types used, what worked, what didn't
- This context will inform recommendations in steps 4-6
- If not found: Proceed without historical context

### 7. Fresh Workflow Setup (If No Document)

If no document exists or user chose to create new:

#### A. Create Initial Document

Copy the template from `{templateFile}` to `{outputFile}`

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

#### B. Show Welcome Message

Communicate in {communication_language}:

"Mandala da Criatividade Infinita initialized for {project_name}. We'll work through 6 steps to build your creative matrix:

1. Brand Brief Context — validate brand context for this campaign
2. Funnel Phases — select awareness levels for your audience
3. Creative Types — choose creative types from the 10 options
4. Priority Matrix — cross levels × types into a prioritized matrix
5. Production Briefs — generate briefs for each priority cell
6. Consolidation — final review and batch briefs extraction

Steps 2-4 are collaborative — I'll ask questions to understand your needs. Steps 5-6 are generative — I'll produce content for your review.

[If sidecar had history]: I found records from previous Mandala sessions — I'll use that context to inform recommendations.

Let's start."

### 8. Present MENU OPTIONS

Display: **Proceeding to Brand Brief Context validation...**

#### EXECUTION RULES:

- This is an initialization step with no user choices
- Proceed directly to next step after setup

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin Brand Brief Context validation

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete and document is created (OR continuation is properly routed), will you then immediately load, read entire file, then execute `./step-02-brand-brief.md` to begin Brand Brief Context validation.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Document created from template (for fresh workflows)
- Frontmatter initialized with `stepsCompleted: [1]`
- Brand Brief loaded and key context extracted (REQUIRED — workflow stops if not found)
- Mandala-matrix data loaded with awareness levels, creative types, efficacy ratings
- Sidecar memories checked for previous Mandala history
- User welcomed to the process with step overview
- Ready to proceed to step 2
- OR existing workflow properly routed to {continueFile}

### ❌ SYSTEM FAILURE:

- Proceeding with step 2 without document initialization
- Not checking for existing documents properly
- Creating duplicate documents without user consent
- Proceeding without Brand Brief (REQUIRED dependency)
- Not loading mandala-matrix data
- Skipping welcome message
- Not routing to {continueFile} when appropriate

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
