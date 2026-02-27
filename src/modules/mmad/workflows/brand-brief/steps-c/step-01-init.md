---
name: 'step-01-init'
description: 'Initialize the Brand Brief workflow by detecting continuation state and creating output document'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/brand-brief'

# File References
thisStepFile: './step-01-init.md'
nextStepFile: './step-02-problem-market.md'
continueFile: './step-01b-continue.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{brand_assets}/brand-brief-{project_name}.md'
templateFile: '{workflow_path}/templates/brand-brief-output-template.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the Brand Brief workflow by detecting continuation state, creating the output document from template, and preparing for the first collaborative discovery session.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a brand architecture and strategic positioning specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring strategic method and frameworks, the user brings deep business knowledge
- ✅ Maintain direct, concise tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on initialization and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 🚪 DETECT existing workflow state and handle continuation properly

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, brand_assets, user_name, etc.)
- Previous context = what's in output document + frontmatter
- Don't assume knowledge from other steps
- No input documents required — brand discovery comes from the user's knowledge

## INITIALIZATION SEQUENCE:

### 1. Check for Existing Workflow

First, check if the output document already exists:

- Look for file at `{brand_assets}/brand-brief-{project_name}.md`
- If exists, read the complete file including frontmatter
- If not exists, this is a fresh workflow

### 2. Handle Continuation (If Document Exists with Steps In Progress)

If the document exists and has frontmatter with `stepsCompleted` array that is NOT empty:

- **STOP here** and load `./step-01b-continue.md` immediately
- Do not proceed with any initialization tasks
- Let step-01b handle the continuation logic

### 3. Handle Completed Workflow

If the document exists AND `status` is `COMPLETE` in frontmatter:

- Ask user: "I found an existing Brand Brief from [date]. Would you like to:
  1. Create a new Brand Brief (will rename the existing one)
  2. Update/modify the existing Brand Brief"
- If option 1: Rename existing file with timestamp suffix, then proceed to step 4
- If option 2: Load step-01b-continue.md

### 4. Fresh Workflow Setup (If No Document)

If no document exists or user chose to create new:

#### A. Create Initial Document

Copy the template from `{templateFile}` to `{brand_assets}/brand-brief-{project_name}.md`

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

"Brand Brief initialized for {project_name}. We'll work through 7 steps to uncover your brand DNA:

1. Problem & Market
2. Ideal Customer Profile (ICP)
3. Positioning
4. Tone of Voice
5. Promise & Offer
6. Narrative & Storytelling
7. Consolidation

Each step builds on the previous one. I'll ask 1-2 questions at a time. Let's start."

### 5. Present MENU OPTIONS

Display: **Proceeding to Problem & Market discovery...**

#### EXECUTION RULES:

- This is an initialization step with no user choices
- Proceed directly to next step after setup

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin Problem & Market discovery

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete and document is created (OR continuation is properly routed), will you then immediately load, read entire file, then execute `./step-02-problem-market.md` to begin Problem & Market discovery.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Document created from template (for fresh workflows)
- Frontmatter initialized with `stepsCompleted: [1]`
- User welcomed to the process with step overview
- Ready to proceed to step 2
- OR existing workflow properly routed to step-01b-continue.md

### ❌ SYSTEM FAILURE:

- Proceeding with step 2 without document initialization
- Not checking for existing documents properly
- Creating duplicate documents without user consent
- Skipping welcome message
- Not routing to step-01b-continue.md when appropriate

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
