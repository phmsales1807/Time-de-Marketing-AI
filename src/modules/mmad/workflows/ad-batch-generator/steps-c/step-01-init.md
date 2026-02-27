---
name: 'step-01-init'
description: 'Initialize the Ad Batch Generator workflow by loading Mandala briefs, Brand Brief tone, and creating output document'

# File References
nextStepFile: './step-02-frameworks.md'
outputFile: '{campaign_assets}/ad-batch-{date}-{project_name}.md'
templateFile: '../templates/ad-batch-output-template.md'
brandBriefFile: '{brand_assets}/brand-brief-{project_name}.md'
batchBriefsFile: '{campaign_assets}/batch-briefs-{project_name}.md'
mandalaFile: '{campaign_assets}/mandala-{project_name}.md'
sidecarMemories: '{project-root}/_bmad/mmad/agents/vtsd-specialist/vtsd-specialist-sidecar/memories.md'
---

# Step 1: Workflow Initialization

## STEP GOAL:

To initialize the Ad Batch Generator workflow by loading Mandala production briefs (REQUIRED), Brand Brief tone reference (REQUIRED), sidecar memories for past ad performance insights, and creating the output document from template.

## MANDATORY EXECUTION RULES (READ FIRST):

### Universal Rules:

- 📖 CRITICAL: Read the complete step file before taking any action
- 🔄 CRITICAL: When loading next step with 'C', ensure entire file is read
- 🚀 GENERATE content proactively — YOU ARE A CONTENT GENERATOR

### Role Reinforcement:

- ✅ You are a VTSD batch generation specialist
- ✅ If you already have a name, communication_style and identity, continue to use those while playing this role
- ✅ You bring copy frameworks and batch generation methodology, the user reviews and approves
- ✅ Speed Protocol: Batch Generation — optimize for volume and variety
- ✅ Maintain direct, production-focused tone — no praise, no filler

### Step-Specific Rules:

- 🎯 Focus ONLY on initialization, loading sources, and setup
- 🚫 FORBIDDEN to look ahead to future steps
- 💬 Handle initialization professionally
- 📚 Load Mandala briefs (REQUIRED) and Brand Brief (REQUIRED) — if either missing, STOP

## EXECUTION PROTOCOLS:

- 🎯 Show analysis before taking any action
- 💾 Initialize document and update frontmatter
- 📖 Set up frontmatter `stepsCompleted: [1]` before loading next step
- 🚫 FORBIDDEN to load next step until setup is complete

## CONTEXT BOUNDARIES:

- Variables from workflow.md are available in memory (project_name, campaign_assets, brand_assets, user_name, etc.)
- Previous context = what's in output document + frontmatter
- Don't assume knowledge from other steps
- Input documents: Mandala briefs (REQUIRED), Brand Brief (REQUIRED), sidecar memories (optional)

## INITIALIZATION SEQUENCE:

### 1. Load Mandala Production Briefs (REQUIRED)

Search for production briefs in this order:

1. Look for `{batchBriefsFile}`
2. If not found, try `{mandalaFile}`
3. If NEITHER found: **STOP** and tell user: "No production briefs found. Please run the Mandala Builder workflow first to generate production briefs, then return to Ad Batch Generator."

If found: Read the complete file and extract all production briefs (angles, awareness levels, creative types, key messages).

### 2. Load Brand Brief (REQUIRED)

Load Brand Brief from `{brandBriefFile}`:

- If found: Read and extract tone of voice, ICP profile, positioning, and promise for ad copy alignment
- If NOT found: **STOP** and tell user: "No Brand Brief found. Please run the Brand Brief workflow first to establish tone and positioning, then return to Ad Batch Generator."

### 3. Load Sidecar Memories (Optional)

Check for sidecar memories at `{sidecarMemories}`:

- If found: Read and extract past ad performance insights, successful patterns, lessons learned
- If not found: Continue without — note "No previous ad performance data available. Starting fresh."

### 4. Fresh Workflow Setup

This is a SINGLE-SESSION workflow — always fresh, no continuation detection.

#### A. Create Initial Document

Copy the template from `{templateFile}` to `{outputFile}`

Replace `{{date}}` with current date and `{{project_name}}` with the actual project name.

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

#### B. Write Context Section

Write to `## 1. Contexto & Fonte` in the output document:

- List all loaded production briefs with their angles and awareness levels
- Reference the Brand Brief tone of voice
- Note any sidecar memory insights loaded

#### C. Show Welcome Message

Communicate in {communication_language}:

"Ad Batch Generator initialized for {project_name}. Loaded X production briefs from Mandala. Brand tone loaded. Ready to generate.

**Briefs loaded:**
[Brief summary table: # | Angle | Awareness Level | Creative Type]

We'll work through 4 steps:

1. Context & Sources (complete)
2. Copy Frameworks — select frameworks per brief
3. Batch Generation — generate 20-40 ad variations
4. Review & Export — group by platform, finalize

Speed Protocol active. Let's generate."

### 5. Auto-Proceed to Next Step

Display: **Proceeding to Copy Framework selection...**

#### EXECUTION RULES:

- This is an initialization step with no user choices
- Proceed directly to next step after setup

#### Menu Handling Logic:

- After setup completion, immediately load, read entire file, then execute `{nextStepFile}` to begin framework selection

## CRITICAL STEP COMPLETION NOTE

ONLY WHEN initialization setup is complete, all required sources are loaded, and the output document is created, will you then immediately load, read entire file, then execute `./step-02-frameworks.md` to begin Copy Framework selection.

## 🚨 SYSTEM SUCCESS/FAILURE METRICS

### ✅ SUCCESS:

- Mandala production briefs loaded successfully
- Brand Brief tone reference loaded successfully
- Sidecar memories loaded (if available)
- Document created from template with context section filled
- Frontmatter initialized with `stepsCompleted: [1]`
- Brief summary presented to user
- Ready to proceed to step 2

### ❌ SYSTEM FAILURE:

- Proceeding without loading Mandala production briefs
- Proceeding without loading Brand Brief
- Not stopping when required files are missing
- Creating document without filling context section
- Skipping welcome message with brief summary
- Not updating frontmatter stepsCompleted

**Master Rule:** Skipping steps, optimizing sequences, or not following exact instructions is FORBIDDEN and constitutes SYSTEM FAILURE.
