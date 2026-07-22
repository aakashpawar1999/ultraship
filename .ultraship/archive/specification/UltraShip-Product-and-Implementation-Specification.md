# UltraShip — Product, Methodology, and Implementation Specification

**Specification version:** 0.1.0  
**Status:** Build-ready foundation  
**Project name:** UltraShip  
**Primary tagline:** **Ship at inference speed.**  
**Supporting principle:** **Build small. Adapt fast. Ship often.**  
**Upstream inspiration:** [obra/superpowers](https://github.com/obra/superpowers)  
**Versioning standard:** [Semantic Versioning](https://semver.org/)

---

## 1. Executive Summary

UltraShip is an AI-assisted rapid development framework for turning vague product ideas into complete, production-ready software through:

- structured product discovery;
- small, complete, deployable releases;
- adaptive planning during implementation;
- iterative and incremental development;
- explicit Semantic Versioning;
- frequent release and deployment;
- one source of truth for every project decision;
- deliberate awareness of the time, inference, tokens, subscription capacity, and money consumed by AI-agent development.

UltraShip is intended to be used with AI coding agents and agentic development tools such as Claude Code, OpenAI Codex, OpenCode, and compatible future tools.

UltraShip is inspired by Superpowers, but its center of gravity is different:

- Superpowers provides disciplined software-development skills.
- UltraShip focuses specifically on rapid product delivery.
- UltraShip organizes all work around complete, releasable product versions.
- UltraShip allows implementation evidence to modify the plan.
- UltraShip treats inference and developer resources as real costs.
- UltraShip optimizes for shipped value rather than maximum activity or maximum code generation.

UltraShip does **not** hard-code a rule that one version must always fit inside one five-hour session or one subscription window. Different users have different providers, plans, models, budgets, repositories, and available time.

Instead, UltraShip follows this operating idea:

> Scope every version with awareness of the resources available, and aim to complete the full development, iteration, verification, and release loop as efficiently as practical.

The aspirational outcome is:

> **One bounded work window can produce one complete release whenever the available capacity and project complexity make that realistic.**

The non-negotiable rule is:

> **Scope may shrink. Completeness may not.**

---

## 2. Product Identity

### 2.1 Name

**UltraShip**

The name communicates:

- speed;
- shipping;
- completed delivery;
- AI-agent acceleration;
- a clear development outcome rather than endless planning.

### 2.2 Primary positioning

> **UltraShip is an AI-assisted rapid development framework for building MVPs, adapting plans during implementation, and shipping frequent incremental releases.**

### 2.3 Extended positioning

> **UltraShip transforms vague ideas into production-ready software through structured discovery, adaptive planning, Minimum Complete Releases, and resource-aware AI-agent execution.**

### 2.4 Taglines

Primary:

> **UltraShip — Ship at inference speed.**

Supporting:

> **Build small. Adapt fast. Ship often.**

Internal maxim:

> **Plan for completion, not activity.**

Release maxim:

> **Every version must work.**

---

## 3. The Problem UltraShip Solves

AI coding agents can produce code quickly, but rapid code generation does not automatically produce complete products.

Common failure modes include:

- building too much before validating the idea;
- spending an entire inference allowance on implementation and leaving no capacity for testing;
- creating large plans that become stale before execution;
- producing incomplete horizontal layers instead of working vertical slices;
- repeatedly re-reading the same repository and wasting context;
- changing requirements without recording why;
- keeping multiple conflicting planning documents;
- calling work “complete” when it is not deployable;
- creating versions that are merely internal milestones;
- letting the agent perform speculative refactors that do not help the release;
- consuming expensive models for mechanical work;
- allowing a release to grow until it cannot be completed within the available resources;
- treating tokens, subscription usage, time, and money as if they were unlimited.

UltraShip addresses these problems by making the complete release the fundamental unit of planning and execution.

---

## 4. Methodology Definition

UltraShip follows:

> **An Agile, iterative, and incremental development methodology with adaptive planning, MVP-driven delivery, frequent rapid releases, Lean principles, and continuous-delivery readiness.**

The methodology combines:

- Agile development;
- Lean product development;
- iterative and incremental delivery;
- Minimum Viable Product thinking;
- continuous delivery;
- adaptive and rolling-wave planning;
- test-driven and evidence-driven implementation;
- release-oriented agent workflows;
- resource-aware inference usage.

UltraShip is not rigid Waterfall.

UltraShip still values planning, but planning is:

- detailed for the current release;
- lighter for the next release;
- directional for distant releases;
- explicitly revisable when implementation or user evidence changes assumptions.

---

## 5. Decisions Already Made

The following decisions are part of the initial UltraShip specification.

### D-001 — UltraShip is a rapid-delivery framework

UltraShip is not merely a collection of generic software-engineering prompts. Its purpose is to help users move from an idea to complete releases quickly and responsibly.

### D-002 — The framework has five primary skills

```text
/ultraship:brainstorm
/ultraship:plan
/ultraship:develop
/ultraship:iterate
/ultraship:complete
```

### D-003 — Brainstorm and plan initialize the workspace

`brainstorm` and `plan` are initialization stages.

They are normally completed once for a workspace or product portfolio.

They must not be repeatedly rerun in a way that creates new competing product definitions or roadmaps.

Their canonical outputs may later be amended through `/ultraship:iterate`.

### D-004 — Develop, iterate, and complete form the repeating release loop

These skills are used repeatedly for every version:

```text
develop → iterate as needed → complete
```

`iterate` may occur zero, one, or many times during a release.

`complete` may reject a release and return it to `develop` or `iterate`.

### D-005 — Every version must be complete

Every version must provide a coherent, real, end-to-end outcome.

A version must not be only:

- a folder structure;
- a database layer;
- an API without a usable workflow;
- an interface with fake data;
- an unfinished internal milestone;
- a partial implementation described as finished.

### D-006 — Every version must be releasable

A completed version must be in one of the explicitly defined release modes:

- release-ready;
- staging-deployed;
- production-deployed;
- published.

The target mode is defined before development starts.

### D-007 — First versions are MVPs; all versions are Minimum Complete Releases

The first useful product version may be called an MVP.

Every version, including later versions and bug fixes, is a **Minimum Complete Release**, or MCR.

### D-008 — Semantic Versioning belongs to releases

Each independently releasable product has its own SemVer stream.

Tasks and iterations receive IDs, not fake SemVer numbers.

Pre-release identifiers may be used for development and release candidates.

### D-009 — A phase is a release cycle

UltraShip avoids a second competing phase-number system.

A “phase” means the release cycle targeting a specific product version.

Example:

```text
Product: Billing Portal
Release cycle: 0.4.0
```

### D-010 — Multiple products may exist in one workspace

A brainstorm may identify:

- one product;
- multiple independent products;
- related products;
- shared services;
- shared libraries;
- a platform and dependent products;
- experiments or proofs of concept.

Each independently releasable product receives its own release track.

### D-011 — One source of truth does not mean one giant file

Every fact has exactly one canonical owner.

Other files may reference that fact but must not redefine it.

### D-012 — Released versions are immutable

A completed release record is never silently rewritten.

Corrections require a new version.

### D-013 — Implementation may challenge the plan

The agent must not blindly follow a plan that has become incorrect.

It must invoke or recommend iteration when evidence shows that scope, architecture, requirements, sequence, or assumptions should change.

### D-014 — Changes must be explicit and traceable

Every meaningful plan change records:

- what changed;
- why;
- supporting evidence;
- affected products;
- affected versions;
- versioning consequence;
- approval or decision source.

### D-015 — UltraShip is resource-aware, not session-hard-coded

UltraShip does not assume:

- a specific provider;
- a five-hour limit;
- a $20 plan;
- a $100 plan;
- a fixed token budget;
- a fixed cost per version;
- exact usage telemetry.

It models whatever resource envelope is available.

### D-016 — The resource envelope influences scope

The framework must be mindful that every:

- feature;
- task;
- iteration;
- test;
- review;
- model call;
- repository scan;
- deployment attempt

costs some combination of time, inference, money, context, or subscription usage.

### D-017 — The goal is shipped value, not full usage consumption

Reaching 100% usage is not a success metric.

The success metric is:

> **Maximum verified and shipped product value per unit of resource consumed.**

### D-018 — Completion capacity must be protected

The agent must not spend the entire available resource envelope implementing features and leave no practical capacity for:

- testing;
- debugging;
- security checks;
- packaging;
- release notes;
- deployment;
- rollback;
- post-deployment verification.

### D-019 — Scope is reduced before quality gates

When the active release no longer fits the likely resource envelope:

- remove optional scope;
- simplify the workflow;
- defer compatible features;
- split the release;
- choose a less expensive implementation.

Do not remove essential verification or falsely mark the release complete.

### D-020 — UltraShip remains provider-neutral

The framework should work with:

- Claude Code;
- OpenAI Codex;
- OpenCode;
- OpenRouter-backed configurations;
- local or hosted models;
- future agentic coding tools.

Provider-specific integrations are adapters, not core methodology.

---

## 6. Core Terminology

### 6.1 Workspace

The top-level UltraShip environment containing one or more products and their shared truth.

### 6.2 Product

An independently understandable user-facing or operational software offering.

### 6.3 Releasable component

A service, SDK, library, application, worker, API, or package that may have its own version and release lifecycle.

Not every internal module should become a separately versioned product.

### 6.4 Product portfolio

The set of products managed under one UltraShip workspace.

### 6.5 Product definition

The canonical definition of:

- users;
- problem;
- outcomes;
- requirements;
- constraints;
- public contract;
- deployment context;
- success measures;
- non-goals.

### 6.6 Roadmap

The ordered set of expected future releases and their intended outcomes.

The roadmap is not a promise that distant scope will remain unchanged.

### 6.7 Release cycle

The full work loop for one target SemVer version.

```text
develop → iterate → complete
```

### 6.8 Minimum Complete Release

The smallest coherent version that:

- delivers a real outcome;
- works end to end;
- can be tested;
- can be deployed or published;
- can be operated;
- has an explicit rollback or recovery path where applicable.

### 6.9 Release contract

The canonical statement of what the target version must achieve before it can be completed.

### 6.10 Resource envelope

The practical resources available for a release or work session.

It may include:

- time;
- model tokens;
- context-window availability;
- subscription session capacity;
- weekly usage capacity;
- API credits;
- money;
- rate limits;
- human review time;
- deployment access;
- compute;
- test-environment availability.

### 6.11 Release fit

The likelihood that the target release can be completed within the current constraints without sacrificing required completion gates.

### 6.12 Iteration event

A recorded change to implementation, scope, plan, architecture, ordering, acceptance criteria, or product assumptions.

### 6.13 Canonical owner

The one file or record authorized to define a particular fact.

### 6.14 Release evidence

The tests, build outputs, deployment records, health checks, reviews, and validation results used to prove completion.

---

## 7. UltraShip Lifecycle

```text
                           ┌────────────────────┐
                           │ Vague idea or ideas│
                           └─────────┬──────────┘
                                     │
                                     ▼
                         /ultraship:brainstorm
                                     │
                                     ▼
                          Canonical product truth
                                     │
                                     ▼
                            /ultraship:plan
                                     │
                                     ▼
                        Versioned release roadmaps
                                     │
                                     ▼
                 ┌──────────────────────────────────┐
                 │ Select product and target version│
                 └────────────────┬─────────────────┘
                                  │
                                  ▼
                         /ultraship:develop
                                  │
                   ┌──────────────┴──────────────┐
                   │                             │
            Plan still fits              Evidence requires change
                   │                             │
                   │                             ▼
                   │                    /ultraship:iterate
                   │                             │
                   └──────────────┬──────────────┘
                                  │
                                  ▼
                         /ultraship:complete
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
             Gates satisfied             Gates not satisfied
                    │                           │
                    ▼                           ▼
           Immutable release       develop or iterate again
                    │
                    ▼
              Select next version
```

---

## 8. State Model

A workspace may have the following states:

```text
UNINITIALIZED
BRAINSTORMING
BRAINSTORMED
PLANNING
PLANNED
DEVELOPING
ITERATING
COMPLETING
RELEASED
BLOCKED
PAUSED
```

### State transition rules

- `UNINITIALIZED → BRAINSTORMING` through `/ultraship:brainstorm`
- `BRAINSTORMING → BRAINSTORMED` when canonical product definitions are approved
- `BRAINSTORMED → PLANNING` through `/ultraship:plan`
- `PLANNING → PLANNED` when valid release roadmaps and at least one executable release contract exist
- `PLANNED → DEVELOPING` through `/ultraship:develop`
- `DEVELOPING → ITERATING` when the plan, implementation, or scope needs revision
- `ITERATING → DEVELOPING` when the amended release contract is executable
- `DEVELOPING → COMPLETING` when implementation claims to satisfy the release contract
- `COMPLETING → RELEASED` only when all required gates pass
- `COMPLETING → DEVELOPING` when implementation defects remain
- `COMPLETING → ITERATING` when the release contract or plan is no longer valid
- any active state may become `BLOCKED` when external requirements prevent safe progress
- active work may become `PAUSED` with an exact checkpoint and continuation record

A released version cannot return to a mutable state.

A new version is created instead.

---

# 9. Skill Specification: `/ultraship:brainstorm`

## 9.1 Purpose

Transform one or more vague ideas into a structured, approved product portfolio with enough clarity to plan complete releases.

This skill is broader than feature brainstorming.

It must support a user who says:

> “I have five product ideas, but I do not yet know the requirements, relationships, architecture, or exact MVPs.”

## 9.2 Invocation frequency

Normally once per workspace initialization.

The skill must support resuming an incomplete brainstorm.

After the workspace has been formally brainstormed, a new invocation must:

- refuse to create a second competing truth;
- direct product changes to `/ultraship:iterate`;
- optionally allow the user to add a new product through a controlled portfolio iteration.

## 9.3 Responsibilities

The skill must:

1. inspect an existing repository or workspace when one exists;
2. collect every idea without prematurely merging them;
3. identify products, features, services, libraries, and experiments;
4. classify product relationships;
5. uncover missing requirements through structured questions;
6. identify users and beneficiaries;
7. define problems and expected outcomes;
8. identify the end-game product vision;
9. define the first useful MVP boundary;
10. identify non-goals;
11. identify constraints and risks;
12. identify shared capabilities and dependencies;
13. determine candidate repository organization;
14. produce a canonical decision set;
15. obtain explicit approval before finalizing the product definitions.

## 9.4 Question domains

The skill should adaptively cover the following domains.

### Portfolio-level questions

- How many ideas are being considered?
- Are they products, features, services, or experiments?
- Which ideas can exist independently?
- Which ideas share users?
- Which ideas share data?
- Which ideas share authentication, billing, or infrastructure?
- Which ideas must be released together?
- Which ideas should have independent release cadence?
- Is there an umbrella brand or platform?
- What is the final intended ecosystem?

### Product-level questions

- Who is the user?
- What problem does the product solve?
- What is the real desired outcome?
- What is the primary workflow?
- Why would someone use or pay for it?
- What current alternative exists?
- What must the MVP prove?
- What data does it own?
- What external systems does it require?
- What level of security or privacy applies?
- What performance or scale is expected?
- What platforms must be supported?
- How will the product be deployed?
- What operational responsibilities exist?
- What does success look like?
- What is explicitly outside the product?
- What assumptions remain uncertain?

## 9.5 Product classification

Every proposed item must be classified as one of:

```text
independent-product
related-product
platform
shared-service
shared-library
feature
experiment
proof-of-concept
internal-tool
unknown
```

An `unknown` classification must create an open decision, not be silently guessed.

## 9.6 Multi-product rules

When multiple products exist:

- each product receives its own canonical definition;
- each independently releasable product receives its own release stream;
- shared capabilities receive a single canonical definition;
- dependencies are recorded centrally;
- related products may share one umbrella roadmap;
- product-specific roadmaps remain separate;
- no requirement should be copied into multiple product files.

## 9.7 Outputs

The skill creates or updates:

```text
.ultraship/
├── workspace.yaml
├── registry.yaml
├── relationships.yaml
├── decisions/
├── questions/
└── products/
    └── <product-id>/
        └── product.yaml
```

It should also produce a human-readable summary:

```text
.ultraship/briefs/workspace-brief.md
.ultraship/briefs/<product-id>-brief.md
```

The human-readable briefs are generated views.

The YAML files remain canonical.

## 9.8 Brainstorm completion criteria

The brainstorm is complete only when:

- every idea has a classification;
- each product has a user, problem, and desired outcome;
- the MVP boundary is defined;
- product relationships are recorded;
- shared capabilities have owners;
- major unknowns are visible;
- key decisions are approved;
- canonical files exist and validate;
- there is no known duplicate source of truth.

## 9.9 Brainstorm guardrails

The skill must not:

- write implementation code;
- create a detailed ten-version engineering plan;
- invent requirements without marking assumptions;
- merge products only to simplify documentation;
- split products only to simplify repositories;
- create separate truths for shared requirements;
- finalize unresolved high-impact decisions silently.

---

# 10. Skill Specification: `/ultraship:plan`

## 10.1 Purpose

Convert approved product definitions into small, complete, independently releasable version plans.

The planning unit is a product release, not a horizontal engineering layer.

## 10.2 Invocation frequency

Normally once after brainstorming to initialize all release tracks.

After initialization, roadmap and release-contract changes happen through `/ultraship:iterate`.

The skill may resume an incomplete initial planning process.

## 10.3 Planning philosophy

Use rolling-wave planning:

```text
Current release: fully specified
Next release: substantially specified
Later releases: outcome-level
Distant releases: hypotheses
```

Do not create false precision for distant versions.

A roadmap may contain `v1` through `v10`, `v100`, or any number of releases, but only near-term work should be deeply detailed.

## 10.4 Release rules

Every planned version must:

- provide a coherent outcome;
- be usable in a real workflow;
- be independently testable;
- be deployable or publishable;
- include required infrastructure and configuration;
- include necessary migrations;
- include required observability;
- include release documentation;
- identify a rollback or recovery method;
- avoid presenting fake or placeholder behavior as complete.

## 10.5 Minimum Complete Release rule

A release must be the smallest version that is still complete.

Invalid release plan:

```text
0.1.0 — create repository
0.2.0 — create database
0.3.0 — add API
0.4.0 — add interface
0.5.0 — make the workflow usable
```

Valid release plan:

```text
0.1.0 — one user can complete one real workflow end to end
0.2.0 — the user can manage and repeat that workflow
0.3.0 — the workflow supports collaboration
0.4.0 — the product integrates with one external system
```

The repository, database, API, interface, tests, and deployment needed by `0.1.0` are all part of `0.1.0`.

## 10.6 SemVer rules

Each independently releasable product uses:

```text
MAJOR.MINOR.PATCH
```

General intent:

- `PATCH` — backward-compatible fixes;
- `MINOR` — backward-compatible functionality;
- `MAJOR` — breaking public-contract changes.

For early products, versions may begin at `0.1.0`.

Pre-release identifiers may be used:

```text
0.3.0-dev.1
0.3.0-alpha.1
0.3.0-beta.1
0.3.0-rc.1
0.3.0
```

Not every release must use every pre-release stage.

## 10.7 Task and iteration identifiers

Tasks are not SemVer releases.

Recommended task ID:

```text
US-<PRODUCT>-<VERSION>-T<NUMBER>
```

Example:

```text
US-BILLING-0.4.0-T03
```

Recommended iteration ID:

```text
US-<PRODUCT>-<VERSION>-I<NUMBER>
```

Example:

```text
US-BILLING-0.4.0-I02
```

## 10.8 Release Contract

Every active or near-term version receives a release contract.

Required fields:

```yaml
product: product-id
version: 0.3.0
status: planned
release_type: minor

outcome:
  user_can: ""
  business_value: ""
  evidence_of_value: ""

scope:
  included: []
  excluded: []
  fallback_scope: []

acceptance:
  functional: []
  non_functional: []
  operational: []

delivery:
  target_mode: release-ready
  environment: ""
  deployment_method: ""
  migrations: []
  observability: []
  rollback: ""

dependencies:
  products: []
  services: []
  human_approvals: []

resource_profile:
  complexity: medium
  uncertainty: medium
  likely_cost_drivers: []
  preferred_tools: []
  constraints: []

risks: []
open_questions: []
```

## 10.9 Resource-aware planning

The planner must be mindful that release size affects:

- model usage;
- time;
- cost;
- context;
- testing effort;
- debugging effort;
- deployment risk.

It must not hard-code one provider or one usage limit.

It should classify release fit with ranges such as:

```text
small
medium
large
unknown
```

It may also use a qualitative confidence:

```text
high fit
probable fit
uncertain fit
unlikely fit
```

The fit is relative to the active user-provided resource profile.

## 10.10 Fallback scope

Every non-trivial release should identify the smallest safe fallback scope.

Example:

```yaml
target_scope:
  - email authentication
  - Google authentication

fallback_scope:
  - email authentication

deferred_if_needed:
  - Google authentication
```

Fallback scope allows `/ultraship:iterate` to preserve completion without inventing an emergency plan late in the release.

## 10.11 Outputs

```text
.ultraship/products/<product-id>/roadmap.yaml
.ultraship/products/<product-id>/releases/<version>.yaml
.ultraship/release-bundles/
.ultraship/views/master-roadmap.md
```

## 10.12 Planning completion criteria

Planning is complete when:

- every product has a release stream or explicit reason not to;
- at least one release per active product is executable;
- current release contracts are complete;
- release scopes are end-to-end;
- cross-product dependencies are known;
- release ordering is consistent;
- SemVer values validate;
- target release modes are defined;
- fallback scope exists for risky releases;
- one source of truth rules are satisfied.

## 10.13 Planning guardrails

The skill must not:

- plan unfinished horizontal layers as versions;
- require every future release to be fully detailed;
- assign SemVer to individual tasks;
- force unrelated products to share one version;
- assume all products deploy together;
- promise exact inference cost without reliable data;
- silently omit deployment, testing, or migration work.

---

# 11. Skill Specification: `/ultraship:develop`

## 11.1 Purpose

Implement the active release contract as the smallest complete vertical slice.

## 11.2 Invocation frequency

Repeated for every release.

It may be run multiple times during the same release when work is resumed.

## 11.3 Inputs

The skill reads:

- workspace state;
- selected product;
- target version;
- product definition;
- release contract;
- current repository;
- active decisions;
- known dependencies;
- resource profile;
- prior execution checkpoint;
- open blockers.

## 11.4 Product and version selection

Preferred invocation:

```text
/ultraship:develop <product-id> <version>
```

If omitted:

- use the single active release when unambiguous;
- otherwise ask the user or select only when canonical priority makes the choice explicit.

## 11.5 Release Fit Gate

Before implementation, the skill assesses:

- scope size;
- repository condition;
- test coverage;
- architecture uncertainty;
- deployment requirements;
- external dependencies;
- available tools;
- available model capacity;
- user-provided time or cost constraints;
- likely completion effort.

It records:

```yaml
release_fit:
  assessment: probable
  reasons: []
  major_cost_drivers: []
  recommended_scope_change: null
```

The gate is advisory and adaptive.

It must not hard-code:

- one session;
- one five-hour window;
- one token budget;
- one provider plan.

When fit is poor, the skill should recommend or invoke `/ultraship:iterate` before expensive implementation begins.

## 11.6 Just-in-time engineering plan

`develop` creates detailed tasks only for the active release.

Tasks should be:

- small;
- independently verifiable;
- ordered by dependency;
- tied to acceptance criteria;
- explicit about files or components;
- explicit about tests;
- explicit about completion evidence.

Each task must state why it is required for the release.

## 11.7 Vertical implementation

Prefer vertical slices.

Example:

```text
User action
→ interface
→ application logic
→ data
→ integration
→ validation
→ tests
→ deployment path
```

Avoid completing every backend task before any real workflow works.

## 11.8 Execution behavior

The skill should:

1. inspect before editing;
2. reuse existing repository knowledge;
3. maintain a compact repository map;
4. avoid repeatedly loading unchanged files;
5. use deterministic tools for search, formatting, tests, and static analysis;
6. use stronger model reasoning only where it adds value;
7. implement the critical path first;
8. keep the repository in a working state;
9. test the smallest relevant scope after each meaningful change;
10. periodically run broader validation;
11. commit or checkpoint coherent states;
12. track acceptance-criteria coverage;
13. track discovered unknowns;
14. watch for release-fit deterioration;
15. route material changes through `/ultraship:iterate`.

## 11.9 Resource awareness

The skill must consider the cost of:

- broad repository scans;
- repeated planning;
- large context;
- unnecessary code generation;
- speculative refactors;
- excessive agent fan-out;
- rerunning expensive test suites;
- repeated deployment attempts;
- using premium models for routine edits.

The agent should prefer:

- targeted searches;
- cached summaries;
- small task contexts;
- incremental tests;
- existing project scripts;
- generated views from canonical data;
- model routing when the host supports it;
- a clear stop condition for low-value exploration.

## 11.10 Resource checkpoints

UltraShip should use event-driven checkpoints rather than rigid percentages.

A checkpoint occurs when:

- a major task completes;
- an unknown is discovered;
- a test strategy fails;
- a dependency blocks progress;
- the scope expands;
- a substantial amount of available capacity appears consumed;
- completion work is at risk;
- the user requests reassessment.

At a checkpoint, compare:

```text
release progress
resource consumption
remaining acceptance criteria
remaining uncertainty
testing still required
deployment still required
```

## 11.11 Development scope freeze

When the release reaches its planned completion phase:

- no new unplanned feature enters;
- no speculative refactor begins;
- optional improvements are deferred;
- only release-critical changes remain.

This transition is based on release state, not a hard-coded usage percentage.

## 11.12 Outputs

```text
.ultraship/products/<product-id>/execution/active.yaml
.ultraship/products/<product-id>/execution/tasks.yaml
.ultraship/products/<product-id>/execution/evidence/
.ultraship/checkpoints/
```

Code, tests, configuration, infrastructure, and documentation are changed in their normal repository locations.

## 11.13 Develop completion criteria

`develop` may hand off to `complete` when:

- every included release requirement is implemented;
- relevant automated tests pass;
- unresolved issues are visible;
- the production or publication path exists;
- required migrations are ready;
- no known release-blocking work remains;
- acceptance evidence is available.

## 11.14 Develop guardrails

The skill must not:

- silently change product requirements;
- silently change release scope;
- silently change the target version;
- spend the entire practical resource envelope before completion work;
- add unrelated improvements;
- rewrite released records;
- claim completion;
- deploy without the intended authority and credentials;
- conceal a blocked or incomplete release.

---

# 12. Skill Specification: `/ultraship:iterate`

## 12.1 Purpose

Adapt the active or future plan when evidence shows that the current assumptions, scope, architecture, ordering, or implementation should change.

This skill is UltraShip’s central adaptive-planning mechanism.

## 12.2 Invocation frequency

Repeated as needed.

It may be:

- user-invoked;
- recommended by `develop`;
- required by `complete`;
- triggered after production feedback;
- used between releases to revise the roadmap.

## 12.3 Iteration categories

Every iteration is classified as one or more of:

```text
task-level
implementation-level
release-level
product-level
portfolio-level
architecture-level
dependency-level
resource-level
post-release
```

## 12.4 Trigger examples

- a task is larger than expected;
- an approach is technically invalid;
- a dependency is unavailable;
- user feedback changes priority;
- acceptance criteria are incomplete;
- the target version is too ambitious;
- available resource capacity is lower than expected;
- testing reveals architecture risk;
- a product should be split;
- products should be combined;
- release order should change;
- an urgent patch should preempt a minor version;
- deployment requirements were misunderstood;
- a cheaper implementation can deliver the same outcome;
- a more expensive implementation is required for correctness.

## 12.5 Permitted actions

`iterate` may:

- split tasks;
- merge tasks;
- reorder tasks;
- change implementation strategy;
- reduce optional scope;
- adopt fallback scope;
- defer functionality;
- split one planned release into multiple complete releases;
- combine compatible future releases;
- change release order;
- add a corrective patch;
- update acceptance criteria;
- revise requirements;
- revise architecture;
- revise dependencies;
- change release mode;
- revise resource assumptions;
- add a new product;
- split one product into multiple products;
- consolidate products;
- amend the master roadmap.

## 12.6 Prohibited actions

`iterate` must not:

- rewrite what an already released version contained;
- hide a change;
- duplicate a canonical fact into multiple files;
- lower completion gates merely to finish faster;
- convert an incomplete implementation into a “release” through wording;
- create a version with no complete user or operational outcome.

## 12.7 Iteration record

Required structure:

```yaml
id: US-PRODUCT-0.4.0-I02
timestamp: ""
category:
  - release-level
trigger: ""
evidence: []

before:
  scope: []
  assumptions: []
  implementation: ""

change:
  summary: ""
  added: []
  removed: []
  deferred: []
  replaced: []

impact:
  products: []
  versions: []
  tasks: []
  dependencies: []
  resource_effect: ""

versioning:
  previous_target: 0.4.0
  new_target: 0.4.0
  consequence: no-version-change

approval:
  source: user
  reference: ""

canonical_updates: []
```

## 12.8 Versioning consequences

Examples:

### Implementation correction before release

```text
Target remains 0.4.0
```

### Backward-compatible fix after release

```text
0.4.0 → 0.4.1
```

### New backward-compatible functionality

```text
0.4.0 → 0.5.0
```

### Breaking public-contract change

```text
1.4.0 → 2.0.0
```

### Release split before publication

```text
Original 0.5.0 scope becomes:
0.5.0 — smaller complete outcome
0.6.0 — deferred complete outcome
```

## 12.9 Resource-aware iteration

When resource pressure is detected, the preferred order is:

1. remove optional scope;
2. use fallback scope;
3. simplify implementation;
4. reduce model or agent overhead;
5. defer non-critical optimization;
6. split the release;
7. pause with a safe checkpoint.

Do not remove:

- required correctness;
- security-critical controls;
- essential tests;
- release evidence;
- necessary deployment validation.

## 12.10 Outputs

```text
.ultraship/iterations/<iteration-id>.yaml
.ultraship/decisions/
updated canonical product or roadmap files
updated active release contract
updated execution tasks
```

## 12.11 Iterate completion criteria

Iteration is complete when:

- the change is recorded;
- the reason is recorded;
- affected canonical files are updated;
- version impact is resolved;
- duplicate truth is avoided;
- the active release is executable again;
- task state is synchronized;
- deferred work has a canonical destination.

---

# 13. Skill Specification: `/ultraship:complete`

## 13.1 Purpose

Verify, package, deploy or publish as authorized, record, and close one product version.

Completion is evidence-based.

## 13.2 Invocation frequency

Once per completion attempt.

A failed attempt returns the release to `develop` or `iterate`.

A successful completion permanently closes that version.

## 13.3 Completion modes

The release contract selects one mode.

### `release-ready`

The artifact is fully built, tested, documented, packaged, and ready for an authorized deployment or publication.

### `staging-deployed`

The artifact is deployed to a staging environment and verified there.

### `production-deployed`

The artifact is deployed to production and verified.

### `published`

The package, extension, application, or release is published to its target registry or distribution channel and verified.

The framework must not claim production deployment when credentials or permissions were unavailable.

## 13.4 Completion gates

Applicable gates include:

### Product gates

- intended user or operational outcome works;
- included scope is complete;
- excluded scope remains excluded;
- no fake production behavior is presented as real.

### Functional gates

- acceptance criteria pass;
- critical workflows pass;
- error behavior is validated;
- edge cases appropriate to release risk are covered.

### Engineering gates

- automated tests pass;
- static analysis passes where configured;
- build succeeds;
- required code review passes;
- dependencies are valid;
- migrations are valid.

### Security and privacy gates

- required security checks pass;
- secrets are not committed;
- permissions are appropriate;
- sensitive data handling matches the product definition.

### Operational gates

- configuration is present;
- health checks work;
- observability is available;
- logging is appropriate;
- rollback or recovery is documented;
- support or incident notes exist when needed.

### Delivery gates

- target artifact is produced;
- deployment or publication succeeds when authorized;
- post-deployment smoke tests pass;
- version is tagged;
- release notes exist;
- changelog is updated.

### Truth gates

- canonical state is updated;
- evidence is stored;
- known limitations are recorded;
- released record is immutable;
- next release state is consistent.

## 13.5 Completion behavior

The skill should:

1. load the release contract;
2. calculate the required gates;
3. run the narrowest reliable validation first;
4. run broader validation;
5. fix only release-blocking defects directly;
6. route scope or requirement changes to `iterate`;
7. produce the release artifact;
8. deploy or publish when authorized;
9. verify the target environment;
10. generate release documentation;
11. update canonical state;
12. mark the release immutable;
13. recommend the next release.

## 13.6 Completion reserve

UltraShip must plan enough practical resource headroom to complete validation and release activities.

No fixed percentage is mandated.

The required reserve depends on:

- release risk;
- repository size;
- test duration;
- deployment complexity;
- migration risk;
- external-service reliability;
- human approval requirements.

## 13.7 Completion failure

If a gate fails:

- do not mark the release complete;
- identify the exact failing gate;
- classify the failure;
- preserve evidence;
- return to `develop` for implementation defects;
- return to `iterate` for scope, plan, or requirement defects;
- pause safely for unavailable external dependencies.

## 13.8 Outputs

```text
.ultraship/products/<product-id>/releases/<version>.yaml
.ultraship/products/<product-id>/evidence/<version>/
CHANGELOG.md or product-specific changelog
release notes
version tag
deployment or publication record
rollback or recovery record
```

## 13.9 Completion result

A successful release record includes:

```yaml
product: product-id
version: 0.4.0
status: released
released_at: ""
mode: production-deployed

outcome:
  delivered: ""

evidence:
  tests: []
  builds: []
  reviews: []
  deployments: []
  health_checks: []

known_limitations: []
rollback: ""
supersedes: null
next_recommended_version: 0.5.0
immutable: true
```

---

# 14. Resource and Inference Awareness

## 14.1 Principle

AI-agent work consumes real resources.

UltraShip must treat resource use as part of engineering quality.

## 14.2 No hard-coded provider limits

UltraShip must not assume that:

- all Claude users have the same capacity;
- all Codex users have the same capacity;
- all OpenCode users use OpenRouter;
- all OpenRouter users have the same budget;
- a session lasts five hours;
- one version must finish in one session;
- model usage is always measurable.

## 14.3 Resource profile

Suggested canonical structure:

```yaml
resource_profile:
  provider_tool: claude-code
  billing_mode: subscription
  model_policy: auto

  available:
    time_minutes: null
    session_capacity_percent: null
    weekly_capacity_percent: null
    token_budget: null
    monetary_budget_usd: null
    context_constraints: null
    human_review_minutes: null

  preferences:
    minimize_cost: true
    prefer_single_window_completion: true
    allow_additional_spend: false
    allow_model_routing: true
    allow_parallel_agents: false

  telemetry:
    source: user-estimate
    confidence: low
```

All fields are optional.

Unknown values remain unknown.

## 14.4 Optimization objective

UltraShip should optimize for:

```text
verified shipped value
────────────────────────
resource consumed
```

It should not optimize for:

- token consumption;
- number of generated files;
- number of tasks;
- maximum code volume;
- maximum agent activity;
- reaching a subscription limit.

## 14.5 Inference-efficient behavior

Preferred behavior:

- inspect only relevant files;
- maintain a repository map;
- summarize stable context once;
- reuse generated state;
- keep task prompts narrow;
- use deterministic commands for facts;
- run focused tests during implementation;
- reserve full-suite tests for meaningful checkpoints;
- avoid repeated plan restatement;
- avoid speculative architecture;
- prefer existing project conventions;
- route routine work to economical models when available;
- use premium reasoning for high-impact uncertainty;
- avoid parallel agents unless parallelism provides clear value;
- stop low-value exploration early.

## 14.6 Release-size adaptation

When the active release appears too large:

```text
target outcome
    ↓
remove optional scope
    ↓
adopt fallback scope
    ↓
simplify implementation
    ↓
split into multiple complete releases
```

The release must remain complete at every step.

## 14.7 Aspiration, not invariant

UltraShip may aim for:

> **A complete version within one practical work or inference window.**

This is not guaranteed and is not enforced as a universal limit.

A complex version may require multiple windows.

A small version may complete well before the available limit.

The framework must remain useful in both cases.

## 14.8 Safe continuation

When work cannot finish in the current capacity:

- leave the repository passing when practical;
- record the exact checkpoint;
- record completed acceptance criteria;
- record remaining acceptance criteria;
- record active hypotheses;
- record the next executable task;
- record required context;
- do not label the version complete.

---

# 15. One Source of Truth Architecture

## 15.1 Principle

> **Every fact has one canonical owner.**

A generated summary may repeat information for readability, but it must identify its canonical source and be regenerable.

## 15.2 Recommended structure

```text
.ultraship/
├── ultraship.yaml
├── workspace.yaml
├── registry.yaml
├── relationships.yaml
│
├── decisions/
│   ├── ADR-0001-product-boundaries.md
│   └── ADR-0002-shared-authentication.md
│
├── questions/
│   ├── open.yaml
│   └── resolved.yaml
│
├── iterations/
│   └── US-PRODUCT-0.4.0-I01.yaml
│
├── checkpoints/
│   └── <timestamp>-<product>-<version>.yaml
│
├── release-bundles/
│   └── <bundle-id>.yaml
│
├── products/
│   ├── product-a/
│   │   ├── product.yaml
│   │   ├── roadmap.yaml
│   │   ├── releases/
│   │   │   ├── 0.1.0.yaml
│   │   │   └── 0.2.0.yaml
│   │   ├── execution/
│   │   │   ├── active.yaml
│   │   │   └── tasks.yaml
│   │   └── evidence/
│   │       └── 0.2.0/
│   │
│   └── product-b/
│       └── ...
│
└── views/
    ├── workspace-brief.md
    ├── master-roadmap.md
    ├── active-releases.md
    └── release-history.md
```

## 15.3 Canonical ownership

### `ultraship.yaml`

Owns:

- framework schema version;
- workspace configuration;
- command behavior configuration;
- provider-neutral execution preferences.

### `workspace.yaml`

Owns:

- workspace identity;
- umbrella vision;
- overall constraints;
- portfolio goals;
- canonical root paths.

### `registry.yaml`

Owns:

- product IDs;
- product types;
- canonical product locations;
- current production versions;
- active status.

### `relationships.yaml`

Owns:

- cross-product dependencies;
- shared capabilities;
- coordinated release requirements;
- data ownership boundaries.

### `product.yaml`

Owns:

- product vision;
- users;
- problems;
- outcomes;
- requirements;
- constraints;
- public contract;
- non-goals;
- deployment context.

### `roadmap.yaml`

Owns:

- planned versions;
- ordering;
- outcomes;
- priorities;
- roadmap status.

### `releases/<version>.yaml`

Owns:

- release contract;
- final delivered scope;
- completion evidence;
- release status;
- deployment record;
- known limitations.

### `execution/active.yaml`

Owns:

- active product version;
- execution state;
- current checkpoint;
- blockers;
- resource-fit assessment.

### `execution/tasks.yaml`

Owns:

- active engineering tasks;
- task status;
- task dependencies;
- acceptance-criteria mapping.

### `decisions/`

Owns:

- why durable product or architecture decisions were made;
- superseded decisions;
- decision history.

### `iterations/`

Owns:

- explicit changes made after initialization;
- evidence for those changes;
- impact and versioning consequences.

### `views/`

Contains generated human-readable summaries.

Views must not become independent sources of truth.

---

# 16. Multi-Product Management

## 16.1 Independent version streams

Every independently releasable product or component has its own version.

Example:

```text
web-app: 0.6.0
public-api: 1.3.2
worker: 0.4.1
sdk: 2.1.0
```

## 16.2 Shared version only when truly indivisible

Products should share one version only when they are always:

- built together;
- released together;
- consumed together;
- unable to operate meaningfully as separate releases.

## 16.3 Release bundles

Coordinated launches use a release bundle.

Example:

```yaml
id: platform-launch-2026-07
status: planned

products:
  web-app: 0.6.0
  public-api: 1.3.2
  worker: 0.4.1
  sdk: 2.1.0

coordination:
  release_order:
    - public-api
    - worker
    - web-app
    - sdk
  compatibility_requirements: []
```

A bundle references product releases.

It does not duplicate their release contracts.

## 16.4 Shared capabilities

Shared capabilities such as authentication, billing, or data ingestion receive:

- one owner;
- one canonical definition;
- explicit consumers;
- explicit compatibility expectations;
- an independent version only if independently released.

## 16.5 Monorepo and multi-repo neutrality

UltraShip must support:

- one product in one repository;
- multiple products in a monorepo;
- one workspace coordinating multiple repositories;
- shared libraries across repositories.

The truth model should not depend on repository layout.

---

# 17. Release Quality Model

## 17.1 A release is not a task bundle

A release is a verified product outcome.

## 17.2 Definition of Complete

A version is complete when:

- the promised outcome works;
- the release contract is satisfied;
- required tests pass;
- required security checks pass;
- the artifact builds;
- required data changes work;
- the release mode is achieved;
- health is verified;
- documentation is current;
- evidence exists;
- the record is immutable.

## 17.3 Production-ready does not mean enterprise-complete

A small release may have limited scope.

It may support:

- one user type;
- one workflow;
- one integration;
- one deployment environment.

It must still be real, safe for its stated use, and complete within those boundaries.

## 17.4 No dummy release rule

A completed release must not rely on:

- fake data presented as production data;
- disabled critical validation;
- hidden manual steps not in documentation;
- missing deployment configuration;
- known broken critical paths;
- placeholders labeled as implemented.

Mocks and test doubles are allowed in tests.

Prototypes are allowed only when the release is explicitly classified as an experiment or proof of concept, not as a production-ready product release.

---

# 18. Tool and Provider Neutrality

## 18.1 Supported execution surfaces

The design should be usable with:

- Claude Code slash commands or skills;
- Codex instructions or skills;
- OpenCode commands;
- other agent systems with prompt and filesystem access.

## 18.2 Core versus adapters

Core:

- methodology;
- canonical schemas;
- state transitions;
- release logic;
- skill behavior;
- validation rules.

Adapters:

- command installation;
- provider usage detection;
- model routing;
- session metadata;
- tool-specific prompt syntax;
- deployment integrations.

## 18.3 Capability detection

At runtime, UltraShip should detect or ask about:

- filesystem access;
- shell access;
- Git access;
- test execution;
- browser access;
- deployment credentials;
- provider usage telemetry;
- model routing;
- subagents;
- parallel execution.

Missing capabilities should change behavior explicitly.

## 18.4 No fabricated telemetry

When usage data is unavailable:

- mark it unknown;
- accept user estimates;
- use repository and task complexity heuristics;
- avoid precise claims.

---

# 19. Suggested Command Interface

## 19.1 Commands

```text
/ultraship:brainstorm
/ultraship:plan
/ultraship:develop [product] [version]
/ultraship:iterate [product] [version]
/ultraship:complete [product] [version]
```

## 19.2 Optional modifiers

Possible future syntax:

```text
--resume
--release-mode release-ready
--resource-profile balanced
--budget-usd 20
--time-limit 240m
--provider claude-code
--no-deploy
--staging
--production
--dry-run
```

The initial implementation may keep the interface simpler and store configuration in `.ultraship/ultraship.yaml`.

## 19.3 Command rerouting

Examples:

- rerunning `brainstorm` after initialization routes to `iterate`;
- rerunning `plan` after initialization routes to `iterate`;
- calling `complete` before implementation reports missing gates;
- calling `develop` without an active release routes to `plan`;
- calling `iterate` without a change request performs a release-fit and assumption review.

---

# 20. Implementation Architecture

## 20.1 Recommended components

```text
UltraShip
├── skill prompts
├── state manager
├── schema validator
├── SemVer service
├── product registry
├── release planner
├── resource-awareness module
├── iteration engine
├── completion-gate engine
├── view generator
├── provider/tool adapters
└── evaluation suite
```

## 20.2 Skill prompts

Five primary `SKILL.md` files contain:

- purpose;
- prerequisites;
- required reads;
- interaction behavior;
- decision rules;
- required writes;
- state transitions;
- stopping conditions;
- examples;
- failure behavior.

## 20.3 State manager

Responsible for:

- reading canonical state;
- enforcing allowed transitions;
- selecting active product and release;
- preventing duplicate initialization;
- marking released records immutable;
- creating checkpoints.

## 20.4 Schema validator

Validates:

- required files;
- IDs;
- product references;
- release references;
- SemVer values;
- dependency references;
- release statuses;
- canonical ownership;
- immutable release records.

## 20.5 Resource-awareness module

Responsible for:

- reading the resource profile;
- accepting user-provided constraints;
- collecting available telemetry;
- assessing release fit;
- detecting resource-risk changes;
- recommending scope adaptation;
- never inventing exact usage.

## 20.6 Completion-gate engine

Builds an applicable checklist from:

- product type;
- release mode;
- repository technology;
- risk;
- release contract;
- deployment target.

It stores evidence rather than simple unchecked assertions.

## 20.7 View generator

Generates:

- workspace summary;
- active release dashboard;
- master roadmap;
- release history;
- dependency map;
- cost and resource summary where data exists.

Generated files must contain a notice such as:

```text
Generated from canonical UltraShip state. Do not edit directly.
```

## 20.8 Adapter layer

Initial adapters should target:

1. Claude Code;
2. Codex;
3. OpenCode.

Adapters should be thin.

The same core skill behavior and schemas should be shared.

---

# 21. Forking Strategy

## 21.1 Preserve useful upstream principles

Potentially retain or adapt:

- structured brainstorming;
- detailed questioning;
- test-driven development;
- small implementation tasks;
- verification before completion;
- disciplined branch finishing;
- explicit skills;
- agent-oriented workflows.

## 21.2 Replace the central workflow

UltraShip’s workflow should be:

```text
portfolio discovery
→ product definitions
→ release roadmaps
→ active release contract
→ resource-aware development
→ adaptive iteration
→ evidence-based completion
→ release
→ next version
```

## 21.3 Avoid a cosmetic fork

The project should not merely:

- rename commands;
- replace “Superpowers” with “UltraShip”;
- add a release step to the end;
- keep one large static implementation plan.

The release model, state system, schemas, and iteration logic must be first-class.

## 21.4 Licensing and attribution

Before distribution:

- review the current upstream license;
- preserve all required notices;
- document what was inherited;
- clearly distinguish UltraShip modifications;
- avoid branding that suggests upstream endorsement.

---

# 22. Initial UltraShip Product Roadmap

Every version below must itself be complete and usable.

## 0.1.0 — Single-product release workflow

Outcome:

> A user can initialize one product, create one complete version plan, develop it, iterate the plan, and complete the release with canonical local state.

Includes:

- five skills;
- single-product workspace;
- SemVer validation;
- release contract;
- task and iteration IDs;
- release-ready completion mode;
- YAML canonical state;
- generated Markdown views;
- basic resource profile;
- completion gates;
- local installer for at least one supported agent tool.

Excludes:

- multi-product portfolios;
- live provider telemetry;
- automated cloud deployment;
- release bundles.

## 0.2.0 — Multi-product workspace

Outcome:

> A user can manage multiple related or independent products with separate version streams and one shared source of truth.

Includes:

- product registry;
- relationships;
- shared capabilities;
- independent roadmaps;
- coordinated release bundles;
- product selection logic;
- cross-product dependency validation.

## 0.3.0 — Resource-aware execution

Outcome:

> A user can supply time, money, token, or subscription constraints and receive release-fit guidance and adaptive scope recommendations.

Includes:

- richer resource profiles;
- user-entered usage;
- provider adapter interface;
- event-driven resource checkpoints;
- fit history;
- scope fallback handling;
- model-routing guidance.

## 0.4.0 — Deployment-aware completion

Outcome:

> A release can be completed as release-ready, staging-deployed, production-deployed, or published through configurable project hooks.

Includes:

- deployment hooks;
- environment checks;
- health checks;
- rollback evidence;
- post-deployment verification;
- release tags and notes.

## 0.5.0 — Evaluations and workflow hardening

Outcome:

> The framework can be evaluated consistently against representative product-building scenarios.

Includes:

- fixture repositories;
- skill-behavior tests;
- state-transition tests;
- one-source-of-truth tests;
- false-completion tests;
- resource-pressure tests;
- multi-product tests.

## 1.0.0 — Stable UltraShip framework

Outcome:

> UltraShip is documented, portable across supported agent tools, migration-safe, and reliable for real project use.

Includes:

- stable schemas;
- documented extension points;
- migration tooling;
- adapter compatibility;
- complete installation and usage guides;
- security review;
- stable release contract.

---

# 23. Acceptance Criteria for UltraShip 0.1.0

UltraShip 0.1.0 is complete when a user can:

1. install the framework in a supported coding-agent environment;
2. run `/ultraship:brainstorm`;
3. transform a vague idea into one canonical product definition;
4. run `/ultraship:plan`;
5. receive a SemVer roadmap made of complete product outcomes;
6. select an active version;
7. run `/ultraship:develop`;
8. generate and execute small release-bound tasks;
9. run `/ultraship:iterate`;
10. change scope or implementation with a traceable record;
11. run `/ultraship:complete`;
12. verify all required completion gates;
13. produce release-ready output;
14. store release evidence;
15. mark the release immutable;
16. begin the next version without duplicating product truth.

Additional criteria:

- rerunning brainstorm does not create a competing product definition;
- rerunning plan does not create a competing roadmap;
- tasks use IDs rather than SemVer;
- released records cannot be silently edited;
- resource assumptions may remain unknown;
- no exact token or cost claims are fabricated;
- incomplete work cannot pass completion;
- generated summaries identify their canonical sources.

---

# 24. Evaluation Scenarios

## Scenario A — Vague single product

Input:

> “I want an app that helps freelancers manage clients.”

Expected:

- structured questioning;
- user and problem definition;
- MVP definition;
- product file;
- first complete release;
- no premature multi-product split.

## Scenario B — Five vague product ideas

Input:

> “I want to build five AI tools that may share accounts and billing.”

Expected:

- all ideas captured;
- each item classified;
- shared capabilities identified;
- independent product definitions;
- one master relationship model;
- separate release streams where appropriate.

## Scenario C — Release too large

Input:

> Active `0.4.0` includes email login, Google login, MFA, password reset, and organization roles, but resources are limited.

Expected:

- release-fit concern;
- fallback scope adoption;
- complete email-login release;
- deferred features moved to canonical future versions;
- no reduced test quality.

## Scenario D — Architecture failure

Input:

> The planned database does not support a required deployment environment.

Expected:

- iteration event;
- architecture decision record;
- affected release contract update;
- task regeneration;
- no hidden plan change.

## Scenario E — Completion failure

Input:

> Code works locally, but migration fails in staging.

Expected:

- no release;
- failing gate recorded;
- evidence preserved;
- return to develop;
- no false completion.

## Scenario F — Unknown provider usage

Input:

> User does not know exact remaining subscription usage.

Expected:

- usage recorded as unknown;
- qualitative fit estimate;
- no fabricated percentage;
- conservative scope guidance.

## Scenario G — Coordinated products

Input:

> API `1.2.0` and web app `0.8.0` must launch together.

Expected:

- separate version streams;
- one release bundle;
- compatibility and ordering;
- no duplicated release contracts.

---

# 25. Anti-Patterns

UltraShip must actively resist:

## Planning anti-patterns

- ten deeply specified releases based on uncertain assumptions;
- task lists masquerading as product roadmaps;
- versions that are only technical layers;
- one version number shared by unrelated products;
- duplicated requirements.

## Development anti-patterns

- repository-wide reading before every task;
- premium-model usage for trivial edits;
- speculative abstractions;
- unnecessary rewrites;
- finishing code but not tests;
- finishing tests but not deployment;
- implementing optional work while release blockers remain.

## Iteration anti-patterns

- changing scope without a record;
- modifying product truth in execution files;
- removing acceptance criteria to claim success;
- editing old release records;
- leaving deferred work without a canonical destination.

## Completion anti-patterns

- “looks good” as evidence;
- passing unit tests as the only release gate;
- tagging a version before deployment validation;
- calling a build production-ready without configuration;
- claiming deployment without access or verification;
- consuming all capacity before release work begins.

---

# 26. UltraShip Principles

These principles should appear in the project documentation and influence every skill.

1. **Every release must work.**
2. **Every release must be independently releasable.**
3. **Every version must deliver a real outcome.**
4. **Build the smallest complete vertical slice.**
5. **The first useful version is an MVP; every version is an MCR.**
6. **Plan near-term work precisely and distant work lightly.**
7. **Implementation evidence may change the plan.**
8. **Changes must be explicit and traceable.**
9. **Released versions are immutable.**
10. **Every fact has one canonical owner.**
11. **Scope may shrink; completeness may not.**
12. **Verification is part of development, not an afterthought.**
13. **Deployment or publication is part of the release contract.**
14. **Inference, time, and money are engineering resources.**
15. **Use expensive reasoning only where it creates value.**
16. **Protect capacity for testing and release.**
17. **Do not optimize for token consumption.**
18. **Optimize for verified shipped value.**
19. **Pause safely rather than manufacture completion.**
20. **Ship, observe, learn, and adapt.**

---

# 27. Recommended README Opening

```markdown
# UltraShip

**Ship at inference speed.**

UltraShip is an AI-assisted rapid development framework for transforming vague ideas into complete, production-ready software through adaptive planning, Minimum Complete Releases, and resource-aware agent execution.

It provides five skills:

- `/ultraship:brainstorm`
- `/ultraship:plan`
- `/ultraship:develop`
- `/ultraship:iterate`
- `/ultraship:complete`

UltraShip plans and builds one complete product version at a time. Every release must deliver a real outcome, remain deployable or publishable, and preserve one canonical source of truth.

**Build small. Adapt fast. Ship often.**
```

---

# 28. Recommended Build Order

## Step 1 — Establish the fork

- fork the upstream repository;
- preserve required attribution;
- rename commands and package identity;
- retain only reusable upstream components;
- create an UltraShip architecture document.

## Step 2 — Define schemas

Implement and validate:

- workspace;
- registry;
- product;
- relationships;
- roadmap;
- release contract;
- task;
- iteration;
- checkpoint;
- evidence;
- release bundle.

## Step 3 — Implement state transitions

Create a small state engine that:

- detects initialization;
- selects active release;
- prevents invalid command order;
- prevents duplicate truth;
- protects immutable releases.

## Step 4 — Build `/ultraship:brainstorm`

Start with single-product support.

Ensure it writes validated canonical files.

## Step 5 — Build `/ultraship:plan`

Generate complete release contracts and rolling-wave roadmaps.

Validate SemVer and release completeness.

## Step 6 — Build `/ultraship:develop`

Generate just-in-time tasks, execute vertical slices, and track evidence.

## Step 7 — Build `/ultraship:iterate`

Implement explicit change records and canonical updates.

## Step 8 — Build `/ultraship:complete`

Implement completion gates, release evidence, immutable records, and release-ready output.

## Step 9 — Add resource awareness

Start with provider-neutral user-entered constraints.

Do not wait for provider telemetry integrations.

## Step 10 — Add generated views

Generate human-readable Markdown from canonical state.

## Step 11 — Add tests and evaluations

Test commands as workflows, not only individual prompt outputs.

## Step 12 — Add additional agent-tool adapters

Keep adapter logic separate from core behavior.

---

# 29. Open Design Questions

These questions do not block starting 0.1.0, but should be resolved through UltraShip’s own decision process.

1. Should canonical state use YAML only, JSON only, or support both?
2. Should release evidence store command output directly or reference external CI artifacts?
3. Should `iterate` be callable automatically by another skill or only recommended to the user?
4. Should `complete` be permitted to make small release-blocking code fixes directly?
5. How should multiple repositories be registered in one workspace?
6. What is the minimum supported Git workflow?
7. Should deployment hooks be shell commands, adapter plugins, or both?
8. How should secrets and environment requirements be represented without storing secret values?
9. How should schema migrations be versioned?
10. Should UltraShip provide a machine-readable event log in addition to files?
11. Which agent tool should receive the first official installer?
12. How should the project measure release value without creating heavy process?
13. Should resource-fit history be retained per task, per release, or both?
14. How should human approvals be represented?
15. What migration policy should apply when UltraShip’s own state schema changes?

---

# 30. Final Product Statement

> **UltraShip is an AI-native rapid development framework that turns vague ideas into complete, production-ready software through structured brainstorming, rolling release plans, adaptive implementation, evidence-based completion, and deliberate awareness of inference cost.**

It is designed around five skills:

```text
/ultraship:brainstorm
/ultraship:plan
/ultraship:develop
/ultraship:iterate
/ultraship:complete
```

It supports one or many products.

It gives each independently releasable product its own Semantic Versioning track.

It makes each version a Minimum Complete Release.

It permits the plan to change when implementation evidence demands it.

It keeps every fact under one canonical owner.

It recognizes that AI development consumes real time, money, tokens, context, and subscription capacity.

It does not hard-code one release to one session.

It does encourage teams and individuals to scope releases so that complete shipping can happen within the practical resources available.

Its objective is not to generate the most code.

Its objective is to create the most verified, deployed, useful product value possible from each development cycle.

> # **UltraShip — Ship at inference speed.**

> **Build small. Adapt fast. Ship often.**
