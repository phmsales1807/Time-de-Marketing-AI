---
name: 'step-01-init'
description: 'Initialize the VSL Structure workflow by loading Brand Brief, asking for VSL name, and creating output document'

# Path Definitions
workflow_path: '{project-root}/_bmad/mmad/workflows/vsl-structure'

# File References
thisStepFile: './step-01-init.md'
nextStepFile: './step-02-big-idea.md'
workflowFile: '{workflow_path}/workflow.md'
outputFile: '{content_assets}/vsl-{vsl_name}-{project_name}.md'
templateFile: '{workflow_path}/templates/vsl-output-template.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the VSL Structure workflow by loading the Brand Brief (required), asking the user for a VSL name/identifier, optionally loading Mandala context, loading sidecar memories, and creating the output document from template.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 🛑 NEVER generate content without user input
- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 📋 YOU ARE A FACILITATOR, not a content generator

### Role Reinforcement:

- ✅ You are a VSL architect and persuasion strategist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ We engage in collaborative dialogue, not command-response
- ✅ You bring VSL methodology and persuasion frameworks, the user brings deep product knowledge
- ✅ Maintain direct, strategic tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on initialization and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 📄 Brand Brief is REQUIRED context — if not found, STOP and warn user
- 🏷️ MUST ask user for vsl_name before creating document
- 🚫 NO continuation detection — this is a single-session workflow (always fresh)

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete
- ⏸️ WAIT for user to provide vsl_name before proceeding

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, content_assets, brand_assets, user_name, etc.)
- Previous context = none (single-session, always fresh)
- Don't assume knowledge from other steps
- Brand Brief provides: ICP, positioning, promise/offer, market context
- Mandala provides: angles, hooks, emotional triggers (optional)
- Sidecar memories provide: past VSL insights and patterns (optional)

## INITIALIZATION SEQUENCE:

### 1. Load Brand Brief (REQUIRED)

Load the Brand Brief — this is mandatory for VSL creation:

- Look for file at `{brand_assets}/brand-brief-{project_name}.md`
- If found: Read and extract key context:
  - **ICP:** Ideal Customer Profile (demographics, psychographics, pains, desires)
  - **Positioning:** Unique positioning and differentiators
  - **Promise & Offer:** Core promise, offer structure, transformation statement
  - **Market Context:** Problem, market, awareness level, competitive landscape
- Store these as context for the workflow — they will inform every VSL section
- If NOT found: **STOP** and display error:
  "🛑 Brand Brief not found at `{brand_assets}/brand-brief-{project_name}.md`. The Brand Brief is REQUIRED for VSL creation — it provides ICP, positioning, and offer context that the entire VSL is built upon. Please complete the Brand Brief first with the Brand Strategist agent before starting the VSL workflow."
  - Do NOT proceed without the Brand Brief

### 2. Ask for VSL Name

Ask the user for the VSL identifier:

"What's the name/identifier for this VSL? (e.g., 'launch-jan', 'evergreen-v2', 'webinar-main')

This will be used in the filename: `vsl-{vsl_name}-{project_name}.md`"

**WAIT for user response before proceeding.** Do not continue until vsl_name is provided.

### 3. Load Optional Context

After receiving vsl_name, load additional context if available:

#### A. Mandala Matrix (Optional)

- Check for Mandala at `{brand_assets}/mandala-{project_name}.md`
- If found: Extract angle references, emotional triggers, and hook patterns for VSL inspiration
- If not found: Continue without it — not required

#### B. Sidecar Memories (Optional)

- Check for memories at `{sidecarMemories}`
- If found: Read for past VSL session insights, patterns, and lessons learned
- If not found: Continue without them — this may be the first VSL session

### 4. Create Output Document

#### A. Create Initial Document

Copy the template from `{templateFile}` to `{content_assets}/vsl-{vsl_name}-{project_name}.md`

Replace `{{vsl_name}}` with the user-provided VSL name.
Replace `{{project_name}}` with the actual project name.

Initialize frontmatter with:

```yaml
---
stepsCompleted: [1]
lastStep: 'init'
status: 'IN_PROGRESS'
date: [current date]
user_name: {user_name}
project_name: {project_name}
vsl_name: {vsl_name}
---
```

#### B. Show Welcome Message

Communicate in {communication_language}:

"VSL Structure initialized for {project_name} — VSL: {vsl_name}. We'll work through 6 steps to architect your Video Sales Letter:

1. Big Idea & Hook — the ONE insight that drives the entire VSL
2. Problema & Agitação — deepen the pain, amplify urgency
3. História & Credibilidade — narrative arc and proof stack
4. Solução & Mecanismo Único — the unique mechanism that makes it work
5. Oferta & Stack de Valor — value stack and price anchoring
6. Fechamento & CTA — urgency, close, and call to action

[If Brand Brief was loaded]: I've loaded your Brand Brief — your ICP, positioning, and offer are the foundation for this VSL.

[If Mandala was loaded]: Mandala loaded — I'll reference your angles and emotional triggers as we build.

[If Sidecar Memories were loaded]: Past VSL insights loaded — I'll reference what worked before.

Remember: a great VSL has ONE Big Idea, not ten. Let's find yours."

### 5. Proceed to Next Step

Display: **Proceeding to Big Idea & Hook discovery...**

#### EXECUTION RULES:

- This is an initialization step — proceed directly after setup
- vsl_name MUST be provided by user before document creation

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin Big Idea & Hook discovery

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete, vsl_name is received, and document is created, will you then immediately load, read entire file, then execute `./step-02-big-idea.md` to begin Big Idea & Hook discovery.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Brand Brief loaded and key context extracted (REQUIRED)
- User asked for and provided vsl_name
- Mandala loaded if available (optional)
- Sidecar memories loaded if available (optional)
- Document created from template with correct vsl_name in filename
- Frontmatter initialized with `stepsCompleted: [1]` and `vsl_name`
- User welcomed to the process with step overview
- Ready to proceed to step 2

### ❌ SYSTEM FAILURE:

- Proceeding without Brand Brief
- Not asking user for vsl_name
- Creating document before vsl_name is provided
- Proceeding with step 2 without document initialization
- Creating document with placeholder vsl_name
- Skipping welcome message
- Attempting continuation detection (this is single-session only)

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
