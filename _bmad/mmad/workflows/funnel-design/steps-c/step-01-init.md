---
name: 'step-01-init'
description: 'Initialize the Funnel Design workflow by detecting continuation state, loading Brand Brief, and creating output document'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/funnel-design'

# File References
thisStepFile: './step-01-init.md'
nextStepFile: './step-02-context.md'
continueFile: './step-01b-continue.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{funnel_assets}/funnel-design-{project_name}.md'
templateFile: '{workflow_path}/templates/funnel-design-output-template.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the Funnel Design workflow by detecting continuation state, loading the Brand Brief as required context, creating the output document from template, and preparing for the first collaborative design session.

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

- 🎯 Focus ONLY on initialization and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 🚪 DETECT existing workflow state and handle continuation properly
- 📄 Brand Brief is REQUIRED context — warn if not found

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, funnel_assets, user_name, etc.)
- Previous context = what's in output document + frontmatter
- Don't assume knowledge from other steps
- Brand Brief provides: ICP, positioning, promise/offer, market context

## INITIALIZATION SEQUENCE:

### 1. Check for Existing Workflow

First, check if the output document already exists:

- Look for file at `{funnel_assets}/funnel-design-{project_name}.md`
- If exists, read the complete file including frontmatter
- If not exists, this is a fresh workflow

### 2. Handle Continuation (If Document Exists with Steps In Progress)

If the document exists and has frontmatter with `stepsCompleted` array that is NOT empty:

- **STOP here** and load `./step-01b-continue.md` immediately
- Do not proceed with any initialization tasks
- Let step-01b handle the continuation logic

### 3. Handle Completed Workflow

If the document exists AND `status` is `COMPLETE` in frontmatter:

- Ask user: "I found an existing Funnel Design from [date]. Would you like to:
  1. Create a new Funnel Design (will rename the existing one)
  2. Update/modify the existing Funnel Design"
- If option 1: Rename existing file with timestamp suffix, then proceed to step 4
- If option 2: Load step-01b-continue.md

### 4. Load Brand Brief (REQUIRED)

Before creating the output document, load the Brand Brief:

- Look for file at `{brand_assets}/brand-brief-{project_name}.md`
- If found: Read and extract key context:
  - **ICP:** Ideal Customer Profile (demographics, psychographics, pains, desires)
  - **Positioning:** Unique positioning and differentiators
  - **Promise & Offer:** Core promise, offer structure, transformation statement
  - **Market Context:** Problem, market, awareness level, competitive landscape
- Store these as context for the workflow — they will inform funnel design decisions
- If NOT found: Display warning:
  "⚠️ Brand Brief not found at `{brand_assets}/brand-brief-{project_name}.md`. The Brand Brief provides critical context (ICP, positioning, offer) for funnel design. I recommend completing it first with the Brand Strategist agent. However, we can proceed — I'll ask you for this context directly during the workflow."

### 5. Fresh Workflow Setup (If No Document)

If no document exists or user chose to create new:

#### A. Create Initial Document

Copy the template from `{templateFile}` to `{funnel_assets}/funnel-design-{project_name}.md`

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

"Funnel Design initialized for {project_name}. We'll work through 6 steps to architect your customer journey:

1. Context & Objective — define the funnel's purpose
2. Funnel Phases — map the customer journey stages
3. Touchpoints & Channels — where and how you connect
4. Content per Phase — what content serves each touchpoint
5. Metrics & KPIs — how to measure what's working
6. Consolidation — final review and downstream recommendations

[If Brand Brief was loaded]: I've loaded your Brand Brief context — your ICP, positioning, and offer will guide the funnel design.

[If Brand Brief was NOT loaded]: We'll define the context directly as we go.

Remember: funnels are ecosystems, not linear paths. Let's design yours."

### 6. Present MENU OPTIONS

Display: **Proceeding to Context & Objective definition...**

#### EXECUTION RULES:

- This is an initialization step with no user choices
- Proceed directly to next step after setup

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin Context & Objective definition

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete and document is created (OR continuation is properly routed), will you then immediately load, read entire file, then execute `./step-02-context.md` to begin Context & Objective definition.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Document created from template (for fresh workflows)
- Frontmatter initialized with `stepsCompleted: [1]`
- Brand Brief loaded and key context extracted (or warning displayed if not found)
- User welcomed to the process with step overview
- Ready to proceed to step 2
- OR existing workflow properly routed to step-01b-continue.md

### ❌ SYSTEM FAILURE:

- Proceeding with step 2 without document initialization
- Not checking for existing documents properly
- Creating duplicate documents without user consent
- Skipping Brand Brief loading without warning
- Not routing to step-01b-continue.md when appropriate

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
