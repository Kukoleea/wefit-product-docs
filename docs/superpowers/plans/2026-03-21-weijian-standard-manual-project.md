# Weijian Standard Manual Project Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rebuild 40 source articles into a unified set of "Microfitness Gym System Standard User Manuals" for gym owners and staff, with each article staying within 3000 Chinese characters and aligning to one editorial standard.

**Architecture:** Use a hub-and-spoke documentation workflow. The main agent owns the style guide, article taxonomy, quality gates, and final consolidation; subagents handle bounded batches such as source extraction, screenshot mapping, draft rewriting, and consistency review. Deliver in small approved batches so tone, structure, and terminology stabilize before the full 40-article rollout.

**Tech Stack:** Markdown documents, screenshot assets, manual review checklist, subagent parallel drafting workflow

---

### Task 1: Lock Project Scope And Inputs

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/project-input-checklist.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/article-inventory.md`
- Test: manual completeness review against user-provided materials

- [ ] **Step 1: Create the input checklist**

Document the required materials:
- 40 source articles
- matching backend screenshots
- target reader priority by article
- product terminology preferences
- preferred brand tone
- expected output format

- [ ] **Step 2: Create the article inventory table**

Include these columns:
- article id
- original title
- module
- target reader
- source available
- screenshots available
- status
- notes

- [ ] **Step 3: Review source completeness**

Run a manual check to mark each article as:
- ready
- missing screenshots
- missing source text
- requires clarification

- [ ] **Step 4: Confirm readiness threshold**

Require at least one pilot batch of 3 articles with complete source text and screenshots before scaling.

### Task 2: Define The Editorial System

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/editorial-style-guide.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/article-template.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/termbase.md`
- Test: apply the template to one sample outline and review for clarity

- [ ] **Step 1: Write the style guide**

Define:
- audience split: owners vs staff
- tone: practical, training-manual style, non-salesy
- article length cap: within 3000 Chinese characters
- sentence style: short, direct, action-oriented
- prohibited patterns: empty marketing language, mixed terminology, vague steps

- [ ] **Step 2: Write the standard article template**

Use this structure:
- article title
- who should read this
- what problem this solves
- when to use it
- prerequisites
- operating path
- step-by-step actions
- common mistakes and fixes
- store management tips
- owner focus
- staff execution points
- screenshot placeholders

- [ ] **Step 3: Build the terminology base**

List the canonical names for:
- menu items
- buttons
- roles
- business objects
- common actions

Also define forbidden synonyms if needed.

- [ ] **Step 4: Validate with one sample outline**

Draft a short outline using the template and verify it can support both owner and staff perspectives without exceeding length.

### Task 3: Build The Content Taxonomy And Batch Plan

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/content-taxonomy.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/batch-delivery-plan.md`
- Test: confirm all 40 articles map cleanly into one taxonomy

- [ ] **Step 1: Define the module taxonomy**

Recommended modules:
- getting started
- member management
- sales and cashier
- scheduling and classes
- staff and permissions
- reports and operations

- [ ] **Step 2: Map all 40 articles into modules**

Assign each article:
- primary module
- target role
- rewrite priority

- [ ] **Step 3: Define batch sizes**

Recommended cadence:
- batch 0: 3 pilot articles
- batch 1: 7 articles
- batch 2: 10 articles
- batch 3: 10 articles
- batch 4: 10 articles

- [ ] **Step 4: Add approval gates**

Require user approval after:
- pilot batch
- first scaled batch
- final pre-delivery quality review

### Task 4: Design The Subagent Workflow

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/subagent-workflow.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/review-checklist.md`
- Test: walk one article through the workflow and verify handoff clarity

- [ ] **Step 1: Define subagent roles**

Use these bounded roles:
- intake subagent: extract key points from raw article
- screenshot subagent: map screenshots to steps and labels
- drafting subagent: rewrite into the standard template
- qa subagent: check terminology, structure, length, and audience fit

- [ ] **Step 2: Define the input package for each role**

For every article package include:
- article id
- original text
- screenshot list
- module
- target reader
- template version
- terminology reference

- [ ] **Step 3: Define output contracts**

Each drafting subagent must return:
- rewritten article markdown
- unresolved questions
- screenshot placement notes
- word count estimate

Each QA subagent must return:
- pass/fail
- issues by severity
- exact phrases needing normalization

- [ ] **Step 4: Create the review checklist**

Checklist must verify:
- title is scenario-based
- steps are complete and ordered
- owner and staff perspectives both exist when needed
- no unsupported assumptions from screenshots
- terminology matches termbase
- article stays within limit

### Task 5: Execute The Pilot Batch

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/pilot/`
- Modify: `G:/AI_Workspaces/微健产品文档撰写/docs/article-inventory.md`
- Test: manual review of 3 pilot outputs

- [ ] **Step 1: Select 3 representative articles**

Pick articles from different modules, ideally:
- one member-related
- one cashier or sales-related
- one class or scheduling-related

- [ ] **Step 2: Prepare structured input packs**

Package for each article:
- source text
- screenshots
- rewrite objective
- target audience

- [ ] **Step 3: Dispatch drafting subagents**

Assign one article per subagent to reduce context spill and keep responsibilities clear.

- [ ] **Step 4: Run QA review**

Use a QA subagent or main-agent checklist review on each pilot draft.

- [ ] **Step 5: Consolidate user-facing pilot delivery**

Deliver the 3 sample articles together with:
- one-paragraph writing rationale
- any terminology decisions
- questions that affect the remaining 37 articles

### Task 6: Scale To Full Production

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/batch-1/`
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/batch-2/`
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/batch-3/`
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/batch-4/`
- Modify: `G:/AI_Workspaces/微健产品文档撰写/docs/article-inventory.md`
- Test: batch-level manual and QA review

- [ ] **Step 1: Freeze version 1 of the editorial guide after pilot approval**

Do not allow drifting structure during scaled production. Any change must be logged once and applied consistently.

- [ ] **Step 2: Produce articles in controlled batches**

For each batch:
- prepare source packages
- dispatch rewriting subagents
- run QA
- normalize terms
- assemble delivery

- [ ] **Step 3: Maintain a change log**

Track changes to:
- template sections
- terminology
- screenshot annotation style
- owner/staff emphasis rules

- [ ] **Step 4: Update inventory status after each batch**

Mark:
- drafted
- QA failed
- revised
- approved

### Task 7: Final Consolidation And Delivery

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/final/`
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/final/catalog.md`
- Create: `G:/AI_Workspaces/微健产品文档撰写/output/final/delivery-note.md`
- Test: final manual review across the full set

- [ ] **Step 1: Assemble the final catalog**

Catalog should group the 40 articles by business module and target role.

- [ ] **Step 2: Run a cross-article consistency pass**

Check:
- recurring step phrasing
- repeated menu labels
- repeated warnings
- duplicated or conflicting business logic

- [ ] **Step 3: Prepare the delivery note**

Summarize:
- what was rebuilt
- what assumptions were used
- which articles used screenshot-backed verification
- which articles still need screenshot supplementation

- [ ] **Step 4: Deliver the final package**

Final package should include:
- 40 rewritten articles
- taxonomy and catalog
- style guide
- terminology list
- unresolved issues log if any

### Task 8: Risk Management

**Files:**
- Create: `G:/AI_Workspaces/微健产品文档撰写/docs/risk-register.md`
- Test: manual review that all major project risks have mitigations

- [ ] **Step 1: Record the primary risks**

Include:
- source articles vary heavily in quality
- screenshots are incomplete or outdated
- wording drifts across batches
- product terms are inconsistent
- some features may require domain clarification

- [ ] **Step 2: Add mitigation rules**

Examples:
- never infer a button name without screenshot or source confirmation
- flag any uncertain workflow instead of inventing steps
- run term normalization before every batch delivery
- keep pilot approval as the style freeze point

- [ ] **Step 3: Add escalation thresholds**

Escalate to the user when:
- a core workflow cannot be verified
- screenshots conflict with source text
- more than 20 percent of a batch needs assumption-based rewriting

