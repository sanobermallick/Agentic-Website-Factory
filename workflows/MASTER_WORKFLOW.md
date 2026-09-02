# 1. Purpose

The **Agentic Website Factory** is a reusable, lean, agent-based workflow for transforming client requirements, business information, content, design direction, and technical requirements into a production-ready website.

The factory organizes website production into **11 specialized agents**, with each agent responsible for a clearly defined stage of the process.

The purpose of this workflow is to ensure that:

* Each stage of website production has a clear responsibility.
* Each agent receives the inputs required to perform its task.
* Each agent produces clearly defined outputs for downstream stages.
* Work is transferred between agents through explicit artifacts and handoffs.
* Quality assurance is performed systematically before production release.
* QA failures can return work to the responsible stage without unnecessarily restarting the entire workflow.
* Human approval is applied at meaningful decision points.
* The complete process can be executed manually by a project manager or developer.
* The workflow provides a clean foundation for future automation without introducing unnecessary complexity.

Version 1 of the Agentic Website Factory is intentionally **lean and practical**.

It is designed to establish a reliable production process first, while leaving more advanced orchestration, automation, and infrastructure for future versions when they provide clear operational value.

# 2. Scope

The Agentic Website Factory defines the end-to-end process for producing production-ready websites using a structured system of 11 specialized AI agents.

The scope of Version 1 includes the following stages:

1. Business discovery and requirement understanding
2. UX and information architecture
3. Content strategy
4. UI/UX design
5. Design system definition
6. Frontend architecture
7. Website development
8. Responsive quality assurance
9. Accessibility quality assurance
10. SEO and performance quality assurance
11. Production quality assurance
12. Human approval
13. Deployment readiness and release

The workflow covers the movement of information, decisions, and artifacts from one stage to the next, ensuring that each agent has clearly defined responsibilities and handoffs.

### 2.1 In Scope

Version 1 covers:

* Client requirement intake
* Business and project discovery
* Website structure and information architecture
* Content planning and content requirements
* UI/UX design direction
* Design system creation
* Frontend technical architecture
* Website implementation
* Responsive testing
* Accessibility testing
* SEO and performance validation
* Production QA
* QA rework and validation loops
* Design approval
* Final production approval
* Deployment readiness

### 2.2 Out of Scope

Version 1 does not attempt to provide:

* A fully autonomous website production system
* Complex multi-agent orchestration infrastructure
* A centralized workflow database
* Event-driven orchestration systems
* Micro-agents for individual tasks
* Excessive automation
* Complex approval-management platforms
* Fully automated deployment without human oversight

These capabilities may be considered in future versions when there is a clear operational need.

### 2.3 Operating Model

Version 1 is designed to be **human-led and agent-assisted**.

A project manager, developer, or other responsible human can execute the workflow manually by providing the appropriate inputs to each agent, reviewing its outputs, and moving approved artifacts to the next stage.

The workflow therefore establishes the **process and contracts between stages** without requiring a specific automation platform.

Future automation can be built around this workflow without changing the fundamental responsibilities of the 11 agents.
# 3. Core Principles

The Agentic Website Factory is designed around a small set of principles that keep the workflow reliable, understandable, and scalable without introducing unnecessary complexity.

## 3.1 Clear Agent Responsibility

Each agent has one clearly defined responsibility within the website production process.

An agent should focus on its assigned stage and should not silently take over responsibilities belonging to another agent.

This creates clear ownership of decisions, artifacts, and outcomes.

## 3.2 Defined Inputs and Outputs

Every agent must have:

* Clearly defined inputs
* A defined responsibility
* Clearly defined outputs
* A clear downstream handoff

The output of one stage should provide the information required by the next relevant stage.

## 3.3 Artifact-Driven Workflow

The factory uses artifacts as the primary mechanism for transferring information between stages.

Examples include:

* Business discovery documents
* UX and information architecture documents
* Content strategy documents
* Design specifications
* Design system artifacts
* Frontend architecture documentation
* Source code
* QA reports
* Production readiness results

Artifacts should be stored in the appropriate project location and treated as the working record for each stage.

## 3.4 Sequential by Default

The primary workflow follows a controlled sequence:

**Discovery → UX → Content → Design → Design System → Architecture → Development → QA → Approval → Deployment**

This sequence ensures that important decisions are made before dependent implementation work begins.

Where stages can safely operate independently, parallel execution may be used without breaking the overall dependency structure.

## 3.5 Human-in-the-Loop

The factory is not intended to remove humans from important decisions.

Human review is required at meaningful decision points, particularly where business, design, quality, or production decisions require approval.

Version 1 should therefore be considered **human-led and agent-assisted**.

## 3.6 Rework Instead of Restart

When a quality check fails, the workflow should return the work to the responsible stage rather than restarting the entire factory.

The preferred pattern is:

**Fail → Identify Responsible Stage → Fix → Re-run Validation**

This minimizes unnecessary work while maintaining quality.

## 3.7 Lean Architecture

Version 1 intentionally avoids unnecessary technical complexity.

The factory should not introduce additional agents, databases, orchestration frameworks, event systems, schemas, or automation unless they provide clear practical value.

The workflow must remain understandable to a human project manager or developer.

## 3.8 Tool Independence

The workflow defines **what needs to happen**, rather than requiring a specific AI model, design tool, development environment, or automation platform.

Agents may be executed using appropriate tools such as AI assistants, design platforms, development environments, or other supporting tools.

The workflow remains the source of truth for responsibilities, dependencies, handoffs, and approvals.

## 3.9 Traceability

Important decisions and outputs should be traceable to the stage that produced them.

A project should make it possible to understand:

* What was decided
* Which agent produced the relevant artifact
* Which inputs were used
* What was approved
* What was changed during rework
* Whether the project passed the required QA stages

## 3.10 Production Readiness

The workflow is not complete when the website merely works in development.

A website must pass the required quality checks and human approval before it is considered ready for production deployment.

Production readiness therefore includes appropriate consideration of:

* Functional correctness
* Responsive behavior
* Accessibility
* SEO
* Performance
* Visual consistency
* Production QA
* Final human approval

## 3.11 Automation Comes After Process Stability

Version 1 establishes a reliable manual workflow first.

Automation should be introduced only after the underlying process, artifacts, dependencies, and approval points are sufficiently stable.

The goal is to automate a proven workflow rather than automate an unclear process.
# 4. Factory Overview

The Agentic Website Factory is an end-to-end production workflow that moves a website project from initial client input to production deployment through 11 specialized agents and defined human approval points.

The factory is organized as a controlled pipeline. Each stage consumes the outputs of previous stages, performs its assigned responsibility, and produces artifacts for the next stage.

## 4.1 High-Level Factory Flow

The Version 1 factory follows this overall sequence:

**Client Input**
↓
**01. Business Discovery**
↓
**02. UX / Information Architecture**
↓
**03. Content Strategy**
↓
**04. UI/UX Design**
↓
**05. Design System**
↓
**06. Frontend Architecture**
↓
**07. Development**
↓
**08. Responsive QA**
↓
**09. Accessibility QA**
↓
**10. SEO & Performance QA**
↓
**11. Production QA**
↓
**Human Approval**
↓
**Deployment**

This represents the default execution path. Specific stages may operate in parallel where their dependencies allow it, as defined later in this document.

## 4.2 Factory Stages

The factory is divided into four broad phases.

### Phase 1 — Discovery and Planning

This phase establishes an understanding of the client, business, users, website goals, structure, and content requirements.

Agents involved:

* Agent 01 — Business Discovery
* Agent 02 — UX & Information Architecture
* Agent 03 — Content Strategy

### Phase 2 — Design and Technical Planning

This phase converts the approved business, UX, and content direction into a visual and technical foundation for implementation.

Agents involved:

* Agent 04 — UI/UX Design
* Agent 05 — Design System
* Agent 06 — Frontend Architecture

### Phase 3 — Development

This phase converts the approved design and technical specifications into the working website.

Agent involved:

* Agent 07 — Development

### Phase 4 — Quality and Release

This phase validates the website across the major production-quality dimensions before release.

Agents involved:

* Agent 08 — Responsive QA
* Agent 09 — Accessibility QA
* Agent 10 — SEO & Performance QA
* Agent 11 — Production QA

The phase concludes with human production approval and deployment.

## 4.3 Role of the Factory

The factory does not replace the individual agents.

Instead, it provides the structure that connects them.

The factory defines:

* Which agent runs at each stage
* What information each agent receives
* What artifacts each agent produces
* How artifacts move between stages
* Where dependencies exist
* Where parallel execution is possible
* Where human approval is required
* How QA failures return to the responsible stage
* When a project is considered ready for deployment

## 4.4 Default Execution Model

The default Version 1 execution model is manual.

A project manager or developer can:

1. Create the client project structure.
2. Provide the required inputs to the appropriate agent.
3. Review the agent's output.
4. Store the resulting artifacts.
5. Pass approved artifacts to the next stage.
6. Trigger QA stages after development.
7. Handle rework when QA identifies issues.
8. Obtain final human approval.
9. Deploy the approved website.

This allows the factory to operate without requiring a dedicated orchestration platform.

## 4.5 Factory Completion Criteria

A website is considered complete only when:

* All required workflow stages have been executed.
* Required artifacts have been produced.
* QA issues have been resolved or formally accepted.
* Required human approvals have been obtained.
* Production QA has passed.
* The website has been approved for deployment.

The factory therefore treats **production readiness and approval**, rather than code completion alone, as the definition of project completion.
# 5. The 11-Agent System

The Agentic Website Factory consists of 11 specialized agents.

Each agent owns a specific stage of the website production lifecycle. The agents work together through defined inputs, responsibilities, outputs, and handoffs.

The 11 agents are:

| #  | Agent                               | Primary Responsibility                                                                              |
| -- | ----------------------------------- | --------------------------------------------------------------------------------------------------- |
| 01 | Business Discovery Agent            | Understand the business, client requirements, goals, audience, and project context                  |
| 02 | UX & Information Architecture Agent | Define the website structure, user flows, navigation, and information architecture                  |
| 03 | Content Strategy Agent              | Define content requirements, messaging structure, content hierarchy, and content direction          |
| 04 | UI/UX Design Agent                  | Translate business, UX, and content requirements into the website's visual and interaction design   |
| 05 | Design System Agent                 | Define reusable visual tokens, components, patterns, and design-system rules                        |
| 06 | Frontend Architect Agent            | Define the frontend technical structure, implementation architecture, and development approach      |
| 07 | Development Agent                   | Build the website based on the approved design, design system, and frontend architecture            |
| 08 | Responsive QA Agent                 | Validate responsive behavior across required screen sizes and device conditions                     |
| 09 | Accessibility QA Agent              | Validate accessibility and identify issues affecting inclusive website usage                        |
| 10 | SEO & Performance Agent             | Validate search-engine readiness, technical SEO, performance, and related optimization requirements |
| 11 | Production QA Agent                 | Perform final end-to-end validation before production approval and deployment                       |

## 5.1 Agent 01 — Business Discovery Agent

**File:** `01_Business_Discovery_Agent.md`

The Business Discovery Agent establishes the foundation for the project.

It analyzes available client information and identifies the business context, objectives, target audience, requirements, constraints, and important project decisions.

Its outputs provide the foundation for the UX and subsequent stages.

---

## 5.2 Agent 02 — UX & Information Architecture Agent

**File:** `02_UX_Information_Architecture_Agent.md`

The UX & Information Architecture Agent converts the business requirements into a structured website experience.

It defines the website's information architecture, page structure, navigation, user flows, and related UX requirements.

Its outputs guide the Content Strategy and UI/UX Design stages.

---

## 5.3 Agent 03 — Content Strategy Agent

**File:** `03_Content_Strategy_Agent.md`

The Content Strategy Agent defines how information and messaging should be organized across the website.

It establishes content requirements, content hierarchy, messaging direction, page-level content needs, and related content considerations.

Its outputs support the UI/UX Design stage and provide content direction for development.

---

## 5.4 Agent 04 — UI/UX Design Agent

**File:** `04_UI_UX_Design_Agent.md`

The UI/UX Design Agent translates the approved business, UX, and content requirements into a visual website experience.

It defines page layouts, visual direction, interaction patterns, and other design requirements needed to build the website.

Its outputs become a primary input for the Design System and Frontend Architecture stages.

---

## 5.5 Agent 05 — Design System Agent

**File:** `05_Design_System_Agent.md`

The Design System Agent converts the visual direction into a reusable and consistent design system.

It defines applicable design tokens, components, patterns, and usage rules required for consistent implementation.

The design system provides a shared visual foundation for frontend architecture and development.

---

## 5.6 Agent 06 — Frontend Architect Agent

**File:** `06_Frontend_Architect_Agent.md`

The Frontend Architect Agent defines how the approved website design and design system should be implemented technically.

It establishes the frontend architecture, project structure, component strategy, technology considerations, and implementation boundaries required by the development stage.

Its outputs provide the technical implementation foundation for the Development Agent.

---

## 5.7 Agent 07 — Development Agent

**File:** `07_Development_Agent.md`

The Development Agent implements the website using the approved requirements, UX structure, design direction, design system, and frontend architecture.

It produces the working website and associated implementation artifacts.

The completed implementation becomes the primary input for the QA stages.

---

## 5.8 Agent 08 — Responsive QA Agent

**File:** `08_Responsive_QA_Agent.md`

The Responsive QA Agent validates the website across required screen sizes and responsive conditions.

It identifies layout, spacing, typography, component, navigation, overflow, and other responsive issues.

Failures are returned to the responsible implementation stage for correction before validation is repeated.

---

## 5.9 Agent 09 — Accessibility QA Agent

**File:** `09_Accessibility_QA_Agent.md`

The Accessibility QA Agent evaluates the website for accessibility-related issues.

It validates applicable areas such as semantic structure, keyboard interaction, focus behavior, accessible naming, contrast, and other relevant accessibility requirements.

Identified issues are returned to the responsible stage for correction and re-validation.

---

## 5.10 Agent 10 — SEO & Performance Agent

**File:** `10_SEO_Performance_Agent.md`

The SEO & Performance Agent validates the website's search-engine readiness and performance characteristics.

It evaluates applicable areas such as metadata, technical SEO, page performance, optimization opportunities, and other relevant production considerations.

Issues identified during this stage are returned to the responsible implementation stage for correction and re-validation.

---

## 5.11 Agent 11 — Production QA Agent

**File:** `11_Production_QA_Agent.md`

The Production QA Agent performs the final quality validation of the website before production release.

It validates the completed website as an integrated product and confirms that required functionality, quality expectations, and production-readiness requirements have been satisfied.

Production QA acts as the final quality checkpoint before final human production approval and deployment.

---

## 5.12 Agent System Principle

The 11 agents form a connected production system rather than 11 independent tools.

Each agent should:

1. Receive defined inputs.
2. Perform its assigned responsibility.
3. Produce defined outputs.
4. Preserve relevant decisions and artifacts.
5. Hand those outputs to the appropriate downstream stage.
6. Return issues to the responsible stage when rework is required.

The factory does not require every agent to communicate directly with every other agent.

Instead, information should flow through the workflow according to the dependencies defined in this document.

This keeps the Version 1 architecture understandable, maintainable, and lean.

# 6. Workflow Overview

The Agentic Website Factory follows a structured end-to-end workflow that moves a website project from client input to production deployment.

The workflow is designed to be **sequential by default**, while allowing controlled parallel execution where dependencies permit it.

## 6.1 End-to-End Workflow

The default Version 1 workflow is:

```text
CLIENT INPUT
    ↓
01. BUSINESS DISCOVERY
    ↓
02. UX / INFORMATION ARCHITECTURE
    ↓
03. CONTENT STRATEGY
    ↓
04. UI/UX DESIGN
    ↓
05. DESIGN SYSTEM
    ↓
06. FRONTEND ARCHITECTURE
    ↓
07. DEVELOPMENT
    ↓
08. RESPONSIVE QA
    ↓
09. ACCESSIBILITY QA
    ↓
10. SEO & PERFORMANCE QA
    ↓
11. PRODUCTION QA
    ↓
HUMAN APPROVAL
    ↓
DEPLOYMENT
```

This sequence represents the **default execution path** for Version 1.

Detailed dependencies, parallel opportunities, approval gates, and QA rework rules are defined in later sections of this document.

## 6.2 Workflow Stage Model

Each stage follows a common execution pattern:

```text
INPUT
  ↓
AGENT EXECUTION
  ↓
OUTPUT ARTIFACTS
  ↓
REVIEW / VALIDATION
  ↓
HANDOFF
  ↓
NEXT RELEVANT STAGE
```

The exact review requirements depend on the stage.

Not every stage requires a separate human approval. Human approval is reserved for meaningful project decisions.

## 6.3 Stage 1 — Business Discovery

The workflow begins with the available client information.

The Business Discovery Agent analyzes the provided information and establishes the business and project foundation.

**Primary outcome:**

A structured understanding of:

* Business
* Goals
* Audience
* Requirements
* Constraints
* Key decisions
* Project context

These outputs are passed to the UX stage.

## 6.4 Stage 2 — UX / Information Architecture

The UX & Information Architecture Agent uses the business discovery outputs to define the structure of the website.

This stage establishes:

* Website structure
* Page hierarchy
* Navigation
* User flows
* Information architecture
* UX requirements

The resulting UX artifacts become inputs for Content Strategy and UI/UX Design.

## 6.5 Stage 3 — Content Strategy

The Content Strategy Agent uses the business and UX context to define the website's content direction.

This stage establishes:

* Content requirements
* Messaging hierarchy
* Page-level content needs
* Content structure
* Content direction

The resulting content strategy supports the design stage.

## 6.6 Stage 4 — UI/UX Design

The UI/UX Design Agent converts the approved business, UX, and content direction into the visual website experience.

This stage establishes:

* Page layouts
* Visual hierarchy
* Interaction patterns
* Component usage
* Responsive design direction
* Visual design requirements

Where applicable, design tools such as Figma or Stitch may be used as part of this stage.

The resulting design becomes a key input to the Design System and Frontend Architecture stages.

## 6.7 Stage 5 — Design System

The Design System Agent converts the visual design direction into reusable design rules and components.

This stage establishes:

* Design tokens
* Typography
* Colors
* Spacing
* Component definitions
* Component behavior
* Reusable visual patterns

The design system provides a consistent foundation for implementation.

## 6.8 Stage 6 — Frontend Architecture

The Frontend Architect Agent translates the approved design and design system into an implementation architecture.

This stage establishes:

* Frontend project structure
* Component architecture
* Technology considerations
* Implementation patterns
* Reusability strategy
* Development boundaries

The resulting architecture guides the Development Agent.

## 6.9 Stage 7 — Development

The Development Agent implements the website using the approved upstream artifacts.

Development produces:

* Working frontend application
* Reusable components
* Page implementations
* Styling
* Responsive behavior
* Required functionality
* Supporting implementation artifacts

The completed implementation becomes the input for the QA stages.

## 6.10 Stage 8 — Responsive QA

The Responsive QA Agent validates the implementation across the required viewport sizes and responsive conditions.

Issues discovered during this stage are recorded as QA findings.

If issues are found, the workflow enters the QA rework loop rather than restarting the factory.

## 6.11 Stage 9 — Accessibility QA

The Accessibility QA Agent validates the implementation against applicable accessibility requirements.

Issues are recorded as findings and returned to the responsible implementation stage when correction is required.

After fixes are completed, accessibility QA is re-run.

## 6.12 Stage 10 — SEO & Performance QA

The SEO & Performance Agent validates the website's technical SEO and performance readiness.

The stage identifies issues requiring correction before production release.

Where fixes are required, the workflow returns to the responsible implementation stage and the relevant validation is repeated.

## 6.13 Stage 11 — Production QA

Production QA performs the final integrated validation of the website.

This stage confirms that:

* Required functionality works
* Major defects are resolved
* Required QA stages have passed
* The implementation is suitable for production
* No known blocking issues remain

A successful Production QA result moves the project toward final human approval.

## 6.14 Human Approval

After the required production checks have passed, the project is presented for final human production approval.

The human reviewer confirms that the website is acceptable for release.

Approval should be based on the completed artifacts, QA results, implementation, and production-readiness status.

## 6.15 Deployment

Only after final human production approval should the website proceed to deployment.

Deployment is the final operational step of the Version 1 workflow.

The workflow therefore distinguishes between:

**Development Complete**

and

**Production Approved**

and

**Deployed**

These are separate project states.

## 6.16 Workflow Completion

A website project reaches the end of the factory workflow when:

```text
Required Stages Complete
        ↓
Required QA Passed
        ↓
Production QA Passed
        ↓
Final Human Approval
        ↓
Deployment
```

The workflow is considered complete only after the approved website has reached its intended production environment.
# 7. Client Project Structure

Each website created using the Agentic Website Factory should follow a consistent project structure.

The structure provides a predictable location for client inputs, agent outputs, approvals, decisions, and the final website.

The exact implementation technology may vary between projects, but the workflow structure should remain consistent.

## 7.1 Standard Project Structure

The recommended Version 1 client project structure is:

```text
ClientName-Website/
│
├── INPUT/
│
├── 01-business-discovery/
│
├── 02-ux/
│
├── 03-content/
│
├── 04-design/
│
├── 05-design-system/
│
├── 06-architecture/
│
├── 07-development/
│
├── 08-qa/
│
├── 09-qa/
│
├── 10-qa/
│
├── 11-qa/
│
├── APPROVALS/
│
├── DECISIONS/
│
└── WEBSITE/
```

This structure is intentionally simple and maps directly to the 11-agent workflow.

## 7.2 INPUT

The `INPUT/` directory contains the information provided for the website project before agent processing begins.

Typical inputs may include:

* Client requirements
* Business information
* Existing website information
* Presentations
* Brand guidelines
* Logos
* Images
* Reference websites
* Existing content
* Product or service information
* Technical requirements
* Other relevant reference materials

The `INPUT/` directory represents the primary source material for the project.

## 7.3 Agent Output Directories

Each agent has a dedicated directory for its stage-specific artifacts.

```text
01-business-discovery/
02-ux/
03-content/
04-design/
05-design-system/
06-architecture/
07-development/
08-qa/
09-qa/
10-qa/
11-qa/
```

The directory names intentionally correspond to the agent sequence.

Each directory should contain the artifacts produced by that stage and any supporting files that are required for traceability.

## 7.4 Business Discovery Directory

```text
01-business-discovery/
```

Contains the outputs produced by the Business Discovery Agent.

Examples may include:

* Business discovery document
* Requirements summary
* Business goals
* Audience definition
* Constraints
* Key project decisions

## 7.5 UX Directory

```text
02-ux/
```

Contains the outputs produced by the UX & Information Architecture Agent.

Examples may include:

* Sitemap
* Information architecture
* User flows
* Navigation structure
* Page requirements
* UX documentation

## 7.6 Content Directory

```text
03-content/
```

Contains the outputs produced by the Content Strategy Agent.

Examples may include:

* Content strategy
* Messaging hierarchy
* Page content requirements
* Content structure
* Content guidance

## 7.7 Design Directory

```text
04-design/
```

Contains the outputs produced by the UI/UX Design Agent.

Examples may include:

* Design specifications
* Page designs
* Layout definitions
* Visual direction
* Design references
* Design-related documentation

External design tools may be used during this stage. The project directory should retain the relevant exported or documented artifacts needed by downstream stages.

## 7.8 Design System Directory

```text
05-design-system/
```

Contains the outputs produced by the Design System Agent.

Examples may include:

* Design tokens
* Component definitions
* Design system documentation
* Component usage rules
* Machine-readable design system artifacts where applicable

## 7.9 Architecture Directory

```text
06-architecture/
```

Contains the outputs produced by the Frontend Architect Agent.

Examples may include:

* Frontend architecture document
* Project structure
* Component architecture
* Technical implementation decisions
* Technology decisions
* Architecture-related machine-readable artifacts where applicable

## 7.10 Development Directory

```text
07-development/
```

Contains development-stage artifacts and implementation documentation.

The actual production website source code may be maintained in the `WEBSITE/` directory, depending on the project implementation model.

The development stage should maintain sufficient documentation or references to establish what was implemented and which approved artifacts were used.

## 7.11 QA Directories

The four QA stages have separate directories:

```text
08-qa/
09-qa/
10-qa/
11-qa/
```

They correspond to:

```text
08-qa/ → Responsive QA
09-qa/ → Accessibility QA
10-qa/ → SEO & Performance QA
11-qa/ → Production QA
```

These directories contain the relevant QA reports, findings, validation results, and machine-readable QA artifacts where applicable.

QA findings should provide enough information to identify:

* The issue
* Its severity
* The affected area
* The responsible stage
* The required correction
* The validation status

## 7.12 APPROVALS

```text
APPROVALS/
```

The `APPROVALS/` directory stores important human approval records.

Examples may include:

* Design approval
* Final production approval
* Approval notes
* Approval status
* Approval dates

Not every workflow transition requires a separate approval record.

Only meaningful human decision points should be recorded.

## 7.13 DECISIONS

```text
DECISIONS/
```

The `DECISIONS/` directory stores important project decisions that affect downstream work.

Examples may include:

* Technology decisions
* Design decisions
* UX decisions
* Scope decisions
* Client decisions
* Approved exceptions
* Decisions made during QA rework

The purpose of this directory is to preserve important project context and prevent significant decisions from being lost across agent handoffs.

## 7.14 WEBSITE

```text
WEBSITE/
```

The `WEBSITE/` directory contains the actual website implementation or the project's production-ready website codebase.

Depending on the development setup, this may contain:

* Application source code
* Components
* Pages
* Assets
* Styles
* Configuration
* Build configuration
* Package configuration
* Other required implementation files

The exact technology stack is project-dependent.

## 7.15 Structure Principle

The project structure should remain consistent enough that a human or future automation system can determine:

* Where inputs are located
* Which agent produced an artifact
* Where QA results are stored
* Where approvals are recorded
* Where important decisions are documented
* Where the website implementation exists

The structure is a **workflow convention**, not a requirement to use a particular development framework or tool.

## 7.16 Version 1 Simplicity

Version 1 does not require a centralized database or complex artifact-management system.

The project folder itself acts as the primary working record.

As long as artifacts are clearly named, stored in the appropriate stage directory, and handed off explicitly, the workflow can be executed manually.

Future automation may build on this structure without requiring the Version 1 workflow to become more complicated.
# 8. Workflow Inputs

The Agentic Website Factory begins with a defined set of client and project inputs.

These inputs provide the information required by the agents to understand the business, define the website experience, create the design, implement the website, and validate the final product.

The exact inputs will vary by project. Version 1 therefore defines input categories rather than requiring every project to provide the same files.

## 8.1 Primary Input Source

All available project inputs should initially be collected in:

```text
INPUT/
```

The `INPUT/` directory acts as the starting point for the factory.

Inputs may be provided directly by the client, collected by the project team, or generated during an initial project discussion.

## 8.2 Client and Business Information

Business information may include:

* Company or organization name
* Business description
* Products or services
* Business goals
* Website objectives
* Target audience
* Geographic markets
* Value proposition
* Competitive information
* Business differentiators
* Contact information
* Existing business documentation

The Business Discovery Agent uses this information to establish the project foundation.

## 8.3 Client Requirements

Client requirements may include:

* Required pages
* Required features
* Functional requirements
* Content requirements
* Technical requirements
* Integration requirements
* Business constraints
* Project constraints
* Timeline expectations
* Existing system constraints

Requirements should be captured clearly enough that downstream agents can use them without repeatedly requesting the same information.

## 8.4 Brand Assets

Available brand assets may include:

* Logo files
* Brand guidelines
* Brand colors
* Typography guidelines
* Existing design assets
* Icons
* Photography
* Illustrations
* Brand imagery
* Existing marketing materials

If formal brand guidelines are unavailable, the relevant agent may establish appropriate recommendations based on the available project information.

## 8.5 Existing Content

Existing content may include:

* Website copy
* Brochures
* Presentations
* Product descriptions
* Service descriptions
* Company profiles
* Blog content
* Marketing material
* Frequently asked questions
* Existing metadata

Existing content should be treated as source material and should not automatically be assumed to be final website copy.

The Content Strategy Agent determines how the available content should be organized and used.

## 8.6 Reference Materials

Reference materials may include:

* Reference websites
* Competitor websites
* Design references
* Screenshots
* Mood boards
* UX references
* Component references
* Industry examples

Reference materials provide context and inspiration but should not be treated as instructions to copy another website.

## 8.7 Technical Inputs

Technical inputs may include:

* Preferred frontend technology
* Existing codebase
* Hosting requirements
* Domain information
* API requirements
* Third-party integrations
* Analytics requirements
* CMS requirements
* Authentication requirements
* Existing repositories
* Deployment constraints

Technical inputs are evaluated by the Frontend Architect and Development stages.

## 8.8 Design Inputs

Design-related inputs may include:

* Existing Figma files
* Stitch designs
* Wireframes
* Design references
* Existing component libraries
* Brand guidelines
* Client visual preferences

Where a design tool is used, relevant design decisions should be documented or exported into project artifacts so downstream agents can use them reliably.

## 8.9 Input Quality

Before an agent begins work, available inputs should be checked for basic completeness and usability.

The project team should identify:

* Missing critical information
* Conflicting requirements
* Unclear requirements
* Unsupported assumptions
* Missing assets
* Technical constraints
* Client decisions that require clarification

Critical ambiguity should be resolved before it creates downstream rework.

## 8.10 Input Assumptions

Agents may make reasonable assumptions when required information is unavailable.

However, important assumptions should be documented rather than silently treated as confirmed requirements.

Significant assumptions that could affect downstream work should be recorded in the project's decision or discovery artifacts.

## 8.11 Input Changes

Client requirements and project inputs may change during production.

When a significant input changes, the responsible stage should determine whether downstream artifacts need to be updated.

A change should not automatically trigger a complete factory restart.

Instead:

```text
INPUT CHANGE
    ↓
IDENTIFY AFFECTED STAGE
    ↓
UPDATE RESPONSIBLE ARTIFACT
    ↓
REVIEW DOWNSTREAM IMPACT
    ↓
RE-RUN AFFECTED STAGES
```

The objective is to minimize unnecessary rework while preserving consistency across the project.

## 8.12 Input-to-Agent Relationship

The initial client inputs are not necessarily passed unchanged to every agent.

Each stage should receive the **relevant upstream artifacts and project information** required for its responsibility.

For example:

```text
CLIENT INPUT
    ↓
BUSINESS DISCOVERY
    ↓
BUSINESS DISCOVERY OUTPUT
    ↓
UX AGENT
    ↓
UX OUTPUT
    ↓
CONTENT / DESIGN
```

This keeps agent context focused and prevents unnecessary duplication of information.

## 8.13 Minimum Input Principle

The factory should provide each agent with enough information to perform its responsibility effectively, but should avoid unnecessary context.

The goal is:

**Relevant information in → Clear work → Defined artifact out**

This supports the lean architecture of Version 1 and makes the workflow easier to execute manually and automate later.
# 9. Artifact Management

Artifacts are the primary mechanism used by the Agentic Website Factory to preserve work, transfer information between agents, and maintain project traceability.

Each agent should produce clearly defined artifacts that can be reviewed, stored, and consumed by downstream stages.

Version 1 uses the project file structure as the primary artifact-management mechanism rather than requiring a centralized artifact database or complex orchestration system.

## 9.1 Artifact Principle

Every significant stage of the workflow should produce one or more usable artifacts.

An artifact should communicate the relevant outcome of a stage clearly enough for another agent or human to understand and use it.

The basic pattern is:

```text
AGENT INPUT
    ↓
AGENT PROCESSING
    ↓
OUTPUT ARTIFACT
    ↓
REVIEW / APPROVAL IF REQUIRED
    ↓
DOWNSTREAM HANDOFF
```

## 9.2 Artifact Ownership

The agent responsible for a stage owns the creation of that stage's artifacts.

For example:

```text
Business Discovery Agent
        ↓
Business Discovery Artifacts

UX Agent
        ↓
UX Artifacts

Design Agent
        ↓
Design Artifacts

Development Agent
        ↓
Implementation Artifacts

QA Agents
        ↓
QA Artifacts
```

An agent may consume artifacts from previous stages but should not silently modify the source artifact owned by another stage.

If an upstream artifact needs to change, the change should be made through the appropriate responsible stage.

## 9.3 Artifact Locations

Artifacts should be stored in the directory associated with the stage that produced them.

For example:

```text
01-business-discovery/
02-ux/
03-content/
04-design/
05-design-system/
06-architecture/
07-development/
08-qa/
09-qa/
10-qa/
11-qa/
```

Approvals and significant decisions should be stored separately:

```text
APPROVALS/
DECISIONS/
```

The production website implementation is maintained in:

```text
WEBSITE/
```

## 9.4 Artifact Naming

Artifacts should use descriptive and consistent filenames.

A filename should make it reasonably clear:

* What the artifact represents
* Which stage produced it
* Whether it is a report, specification, configuration, or machine-readable output

Examples:

```text
business-discovery.md
ux-information-architecture.md
content-strategy.md
ui-ux-design.md
design-system.md
frontend-architecture.md
responsive-qa.md
accessibility-qa.md
seo-performance-qa.md
production-qa.md
```

Where the existing agent definitions specify particular artifact filenames, those filenames should be followed rather than creating unnecessary alternatives.

## 9.5 Human-Readable Artifacts

Human-readable artifacts should generally use Markdown or another appropriate documentation format.

They should be:

* Clear
* Structured
* Concise
* Reviewable
* Easy to reference during downstream work

Human-readable artifacts provide the project team with a persistent record of important decisions and outputs.

## 9.6 Machine-Readable Artifacts

Where an agent already produces structured machine-readable artifacts, those artifacts should be preserved.

Examples may include JSON artifacts for:

* Design tokens
* Design system components
* Frontend architecture
* Responsive QA results
* SEO and performance QA results

Machine-readable artifacts should only be introduced where they provide practical value.

Version 1 does not require every artifact to have a JSON representation.

## 9.7 Artifact as Handoff Contract

An artifact acts as the practical handoff between stages.

For example:

```text
Business Discovery
        ↓
business-discovery artifact
        ↓
UX Agent
```

and:

```text
Design System
        ↓
design-system artifacts
        ↓
Frontend Architect
        ↓
Development
```

The downstream agent should be able to identify which artifacts it is expected to consume.

## 9.8 Controlled Changes After Handoff

Once an artifact has been formally handed off, it should not be silently modified.

If a meaningful change becomes necessary:

```text
IDENTIFY CHANGE
      ↓
UPDATE RESPONSIBLE ARTIFACT
      ↓
DOCUMENT IMPORTANT DECISION
      ↓
IDENTIFY DOWNSTREAM IMPACT
      ↓
UPDATE AFFECTED STAGES
```

This prevents downstream work from being based on undocumented changes.

## 9.9 Artifact Versioning

Version 1 does not require a sophisticated artifact-versioning system.

Normal Git version control may be used to track changes to project files.

For significant changes, the project should make the change understandable through:

* Git history
* Updated artifacts
* Decision records where appropriate
* QA rework records where applicable

The goal is traceability without creating unnecessary administrative overhead.

## 9.10 Artifact Review

Artifacts should be reviewed at the point where their correctness matters.

Not every artifact requires formal human approval.

Review may be performed by:

* The next agent
* The project manager
* The developer
* A designated reviewer
* A human approval gate

The required review level depends on the importance of the artifact.

## 9.11 Artifact Status

Where useful, an artifact may have a simple status such as:

```text
DRAFT
↓
REVIEW
↓
APPROVED
```

For QA artifacts:

```text
IN PROGRESS
↓
PASS / FAIL
↓
RE-TEST IF REQUIRED
```

Version 1 does not require a centralized status-management system.

The status may be communicated through the artifact itself, project documentation, Git history, or the relevant approval record.

## 9.12 Artifact Traceability

Important artifacts should make it possible to determine:

* Which agent produced them
* Which stage they belong to
* What inputs informed them
* Whether they were reviewed
* Whether they were approved when approval was required
* Which downstream stages depend on them

This allows the workflow to remain understandable even when work is performed across multiple tools.

## 9.13 Artifact Changes During Rework

QA rework may require an existing artifact or implementation to change.

The preferred approach is:

```text
QA FINDING
    ↓
RESPONSIBLE STAGE IDENTIFIED
    ↓
RESPONSIBLE ARTIFACT / IMPLEMENTATION UPDATED
    ↓
AFFECTED QA RE-RUN
    ↓
RESULT UPDATED
```

Only the affected stages should be repeated unless the change has a broader downstream impact.

## 9.14 Artifact Management Principle

The Version 1 artifact-management model can be summarized as:

**Create clearly → Store consistently → Handoff explicitly → Change responsibly → Preserve traceability**

The objective is not to build a complex document-management system.

The objective is to ensure that every important piece of work has a clear home and can be reliably consumed by the next stage of the factory.
# 10. Agent Execution Model

The Agentic Website Factory uses a structured execution model in which each specialized agent performs a defined responsibility and produces artifacts for the next relevant stage.

Version 1 is designed to be **manually executable** while maintaining enough structure to support future automation.

## 10.1 Standard Agent Execution Pattern

Every agent should follow the same basic execution pattern:

```text
DEFINED INPUTS
      ↓
AGENT EXECUTION
      ↓
OUTPUT ARTIFACTS
      ↓
REVIEW / VALIDATION
      ↓
HANDOFF
      ↓
NEXT RELEVANT STAGE
```

The exact inputs, outputs, validation requirements, and handoff rules vary by agent.

The execution pattern itself remains consistent across the factory.

## 10.2 Agent Responsibilities

Each agent is responsible for performing the work defined for its assigned stage.

An agent should:

1. Review its available inputs.
2. Understand the requirements relevant to its responsibility.
3. Perform the assigned work.
4. Identify important assumptions or ambiguities.
5. Produce the defined outputs.
6. Record important decisions where required.
7. Make the outputs available to the next relevant stage.
8. Clearly identify unresolved issues that require attention.

An agent should not silently perform work that belongs to another specialized stage.

## 10.3 Agent Inputs

An agent should receive only the information required to perform its responsibility effectively.

Inputs may include:

* Client-provided information
* Upstream agent artifacts
* Approved decisions
* Brand assets
* Design references
* Technical requirements
* Existing implementation
* QA findings
* Other relevant project information

The project workflow determines which inputs are relevant to each agent.

## 10.4 Agent Processing

The agent processes its inputs according to the instructions defined in its corresponding agent specification.

The agent should use the available information to produce a practical output rather than creating unnecessary documentation or artifacts.

The objective is:

```text
Relevant Context
      ↓
Focused Agent Responsibility
      ↓
Useful Output
```

## 10.5 Agent Outputs

Each agent should produce the artifacts defined by its agent specification.

Outputs may include:

* Markdown documentation
* Design specifications
* Design-system artifacts
* Machine-readable JSON
* Technical architecture documents
* Source code
* QA reports
* QA findings
* Validation results

The agent should not create additional artifacts unless they provide a clear practical purpose.

## 10.6 Output Quality

Before an output is handed to the next stage, it should be sufficiently complete for its intended purpose.

At minimum, the output should:

* Address the assigned responsibility.
* Contain the required information.
* Identify important assumptions.
* Avoid unresolved contradictions where possible.
* Be stored in the appropriate project location.
* Be understandable by the downstream stage.

An incomplete output should be corrected before it becomes a dependency for downstream work.

## 10.7 Handoff

A handoff occurs when the output of one stage becomes an input to another stage.

A handoff should make clear:

* What artifact is being provided.
* Which stage produced it.
* Which stage should consume it.
* Whether human approval is required before consumption.
* Whether any important assumptions or decisions accompany the artifact.

The handoff does not require a separate orchestration platform in Version 1.

A clearly stored artifact and documented workflow relationship are sufficient.

## 10.8 Agent-to-Agent Communication

Agents should not be treated as independent conversational participants that need direct communication with every other agent.

The preferred model is:

```text
Agent A
   ↓
Artifact
   ↓
Agent B
```

rather than:

```text
Agent A ↔ Agent B ↔ Agent C ↔ Agent D
```

This keeps dependencies explicit and reduces unnecessary coupling between agents.

## 10.9 Upstream and Downstream Dependencies

An agent may depend on artifacts produced by one or more upstream stages.

Likewise, its outputs may become dependencies for one or more downstream stages.

For example:

```text
Business Discovery
        ↓
UX / Information Architecture
        ↓
Content Strategy
        ↓
UI/UX Design
```

The detailed dependency relationships between all 11 agents are defined later in **Section 22 — Agent Dependencies and Handoffs**.

## 10.10 Human Review During Execution

Not every agent execution requires human approval.

Routine agent outputs can proceed through the workflow when they satisfy the requirements of the stage.

Human intervention should occur when:

* A meaningful project decision must be made.
* Requirements are ambiguous or conflicting.
* A significant design direction requires approval.
* A scope decision affects downstream work.
* A quality issue requires a business decision.
* A defined approval gate is reached.

This keeps the workflow human-controlled without creating unnecessary approval overhead.

## 10.11 Handling Ambiguity

When an agent encounters missing or ambiguous information, it should not silently convert a significant assumption into a confirmed requirement.

The agent should:

1. Identify the ambiguity.
2. Determine whether it can reasonably proceed.
3. Record important assumptions.
4. Request clarification when the ambiguity materially affects the outcome.
5. Continue only when the assumption is acceptable for the stage.

Material ambiguities should be resolved as early as practical to reduce downstream rework.

## 10.12 Handling Agent Failure

If an agent cannot successfully complete its responsibility, the workflow should not automatically move to the next stage.

The issue should first be identified and resolved.

Possible causes include:

* Missing inputs
* Invalid inputs
* Conflicting requirements
* Insufficient information
* Tool limitations
* Output quality problems
* Technical constraints

The responsible stage should be corrected or re-executed before downstream work proceeds.

## 10.13 Re-Execution

An agent may need to be re-executed when:

* Its output is incomplete.
* A significant upstream decision changes.
* A downstream issue reveals a problem in its output.
* A QA finding identifies an issue originating from that stage.
* A human approval decision requires a meaningful change.

Re-execution should use the latest valid project artifacts and decisions.

The workflow should avoid unnecessary repetition of unaffected stages.

## 10.14 Agent Execution States

Version 1 does not require a sophisticated workflow engine.

However, a simple conceptual state model is useful:

```text
NOT STARTED
     ↓
READY
     ↓
IN PROGRESS
     ↓
OUTPUT READY
     ↓
REVIEWED
     ↓
HANDED OFF
```

If rework is required:

```text
QA / REVIEW
     ↓
REWORK REQUIRED
     ↓
IN PROGRESS
     ↓
OUTPUT READY
     ↓
REVIEWED
     ↓
HANDED OFF
```

These states may be represented through project documentation, filenames, Git history, task tracking, or simple manual tracking.

## 10.15 Manual Execution Model

A human project manager or developer can execute the factory manually by:

1. Identifying the next ready stage.
2. Gathering its required inputs.
3. Running the appropriate agent.
4. Reviewing the output.
5. Storing the artifacts.
6. Recording important decisions.
7. Completing any required approval.
8. Handing the artifacts to the next relevant stage.
9. Continuing until the workflow reaches QA and release.

No dedicated orchestration platform is required for Version 1.

## 10.16 Future Automation Compatibility

The execution model is intentionally structured so that future automation can be added without redesigning the factory.

Future automation could eventually automate:

* Detecting available inputs
* Triggering agents
* Moving artifacts
* Tracking stage status
* Detecting QA failures
* Routing rework
* Recording approvals
* Checking release readiness

However, these capabilities are not required for Version 1.

The core principle remains:

**Define the process first. Automate the stable process later.**
# 11. Agent 01 — Business Discovery

The **Business Discovery Agent** is the first specialized agent in the Agentic Website Factory.

Its purpose is to transform the available client and project inputs into a clear, structured understanding of the business, website objectives, target audience, requirements, constraints, and important project context.

The output of this stage establishes the business foundation for the downstream UX, Content Strategy, and Design stages.

## 11.1 Objective

The primary objective of the Business Discovery Agent is to answer:

* What is the business?
* What does the business offer?
* What is the purpose of the website?
* Who is the website intended for?
* What should the website achieve?
* What are the important business and project requirements?
* What constraints or risks exist?
* What information is confirmed versus assumed?
* What decisions require clarification?

The agent should establish enough context for downstream agents to make informed decisions without repeatedly returning to the original client inputs.

## 11.2 Primary Inputs

The Business Discovery Agent may receive:

* Client requirements
* Business information
* Existing website information
* Company presentations
* Product or service information
* Existing content
* Brand information
* Reference materials
* Competitor information
* Technical requirements
* Project constraints
* Client communications
* Other relevant project materials

All available source material should initially be considered from:

```text
INPUT/
```

The agent should use only information relevant to understanding the business and project.

## 11.3 Core Responsibilities

The Business Discovery Agent is responsible for:

1. Understanding the business and its offerings.
2. Identifying the purpose and objectives of the website.
3. Identifying the target audience.
4. Understanding the business value proposition.
5. Identifying important products, services, or offerings.
6. Capturing functional and non-functional requirements.
7. Identifying project constraints.
8. Identifying important assumptions.
9. Identifying gaps or ambiguities in the available information.
10. Recording important business and project decisions.
11. Producing the business discovery artifacts required by downstream stages.

## 11.4 Business Understanding

The agent should establish a concise understanding of the business.

This may include:

* Business description
* Industry or business category
* Products or services
* Primary offerings
* Business differentiators
* Value proposition
* Geographic or market focus
* Business positioning
* Relevant competitive context

The purpose is not to create an exhaustive business analysis report.

The purpose is to provide enough reliable context for website planning and production.

## 11.5 Website Objectives

The agent should identify what the website is expected to accomplish.

Possible objectives include:

* Generate leads
* Explain products or services
* Increase inquiries
* Build credibility
* Support sales
* Present a portfolio
* Provide information
* Improve online presence
* Support an existing business process
* Enable specific user actions

Where multiple objectives exist, the agent should identify their relative importance when the available information allows it.

## 11.6 Target Audience

The agent should identify the primary audiences for the website.

Relevant information may include:

* Primary audience
* Secondary audience
* Customer types
* User roles
* User needs
* User expectations
* Relevant pain points
* Purchase or decision-making context

Audience information should remain grounded in available project information.

The agent should avoid inventing detailed personas when the source material does not support them.

## 11.7 Requirements

The agent should capture requirements that could affect downstream website production.

Requirements may include:

* Required pages
* Required features
* Business requirements
* Content requirements
* Functional requirements
* Technical requirements
* Integration requirements
* Compliance requirements
* Analytics requirements
* Deployment requirements

Requirements should be expressed clearly enough that downstream agents can use them.

## 11.8 Constraints

The agent should identify constraints that may affect the project.

Examples include:

* Existing technology
* Existing website structure
* Required technologies
* Hosting constraints
* Timeline constraints
* Content limitations
* Brand restrictions
* Third-party dependencies
* Integration limitations
* Client preferences
* Budget-related constraints when relevant

Important constraints should be carried forward into the appropriate downstream stages.

## 11.9 Assumptions and Unknowns

The agent should distinguish between:

**Confirmed information**

and:

**Assumptions**

and:

**Unknown or unresolved information**

For example:

```text
CONFIRMED
The business provides commercial HVAC services.

ASSUMPTION
The primary website objective is lead generation.

UNKNOWN
Whether online quotation submission is required.
```

Important assumptions should not silently become confirmed requirements.

## 11.10 Questions and Clarifications

When critical information is missing, the agent should identify the questions that need clarification.

Questions should be prioritized according to their potential impact on downstream work.

For example:

```text
HIGH PRIORITY
What is the primary conversion goal?

MEDIUM PRIORITY
Which service should receive the greatest emphasis?

LOW PRIORITY
Are there preferred secondary visual references?
```

The objective is to resolve high-impact ambiguity early without blocking the entire workflow for minor details.

## 11.11 Key Business Decisions

Important decisions identified during discovery should be recorded in the appropriate project artifacts.

Examples include:

* Primary website objective
* Target audience
* Primary conversion action
* Business positioning
* Required website scope
* Major functional requirements
* Important exclusions
* Technology constraints
* Client priorities

Where a decision has significant downstream impact, it may also be recorded in:

```text
DECISIONS/
```

## 11.12 Primary Output

The Business Discovery Agent should produce a structured business discovery artifact containing the relevant findings from this stage.

The exact artifact filename should follow the artifact definition established by the Business Discovery Agent.

The artifact should provide downstream stages with a reliable summary of:

```text
Business
Goals
Audience
Requirements
Constraints
Assumptions
Unknowns
Important Decisions
```

## 11.13 Output Quality Check

Before the Business Discovery stage is considered complete, the output should be checked for:

* Business context completeness
* Clear website objectives
* Identified target audience
* Captured major requirements
* Captured important constraints
* Clearly identified assumptions
* Clearly identified unresolved questions
* No major contradictions
* Sufficient context for the UX stage

If critical information remains unresolved, the project should address it before proceeding where practical.

## 11.14 Handoff to Agent 02

The primary downstream consumer of the Business Discovery output is:

```text
02 — UX & Information Architecture Agent
```

The handoff should provide the UX Agent with the relevant business context required to define:

* Website structure
* Navigation
* Information architecture
* User flows
* Page hierarchy
* UX requirements

The basic handoff is:

```text
CLIENT INPUT
     ↓
01 — BUSINESS DISCOVERY
     ↓
BUSINESS DISCOVERY ARTIFACT
     ↓
02 — UX / INFORMATION ARCHITECTURE
```

## 11.15 Downstream Impact

Business Discovery decisions can influence almost every later stage.

For example:

```text
Business Goals
      ↓
UX Structure
      ↓
Content Direction
      ↓
Design
      ↓
Development
      ↓
QA
```

Therefore, significant changes to business objectives or requirements after this stage may require downstream artifacts to be reviewed.

However, a change does not automatically require restarting the entire factory.

The affected stages should be identified and re-executed only where necessary.

## 11.16 Completion Criteria

Agent 01 is considered complete when:

* Available business information has been analyzed.
* Website objectives are sufficiently understood.
* Target audiences are identified.
* Major requirements are captured.
* Important constraints are documented.
* Significant assumptions are identified.
* Critical unknowns are highlighted.
* Required discovery artifacts are produced.
* The output is usable by the UX stage.

The stage is then handed off to:

```text
02 — UX & Information Architecture Agent
```

## 11.17 Version 1 Principle

The Business Discovery Agent should remain focused on **understanding and structuring the project**, not solving every downstream website problem.

It should not independently:

* Design the website
* Define the complete information architecture
* Create the final content strategy
* Create the final visual design
* Define the complete frontend architecture
* Implement the website
* Perform final QA

Those responsibilities belong to the appropriate specialized agents.

The Business Discovery Agent establishes the foundation on which those later decisions can be made.
# 12. Agent 02 — UX & Information Architecture

The **UX & Information Architecture Agent** is the second specialized agent in the Agentic Website Factory.

Its purpose is to transform the business and project foundation established by the Business Discovery stage into a clear, structured website experience.

The agent defines how information is organized, how users move through the website, how pages relate to one another, and what each major page needs to accomplish.

Its outputs provide the structural foundation for the Content Strategy and UI/UX Design stages.

## 12.1 Objective

The primary objective of the UX & Information Architecture Agent is to answer:

* What pages should the website contain?
* How should those pages be organized?
* How should users navigate the website?
* What information belongs on each page?
* What are the primary user journeys?
* What actions should users be able to take?
* How should content and functionality be prioritized?
* What UX requirements should guide the design?

The agent should transform business requirements into a practical website structure without prematurely solving visual design or implementation problems.

## 12.2 Primary Inputs

The UX & Information Architecture Agent primarily receives:

* Business Discovery artifacts
* Client requirements
* Website objectives
* Target audience information
* Business offerings
* Functional requirements
* Technical constraints where relevant
* Important project decisions
* Relevant reference materials

The primary upstream relationship is:

```text
01 — BUSINESS DISCOVERY
        ↓
BUSINESS DISCOVERY ARTIFACTS
        ↓
02 — UX / INFORMATION ARCHITECTURE
```

The agent should use the latest valid upstream artifacts and approved project decisions.

## 12.3 Core Responsibilities

The UX & Information Architecture Agent is responsible for:

1. Defining the website's information architecture.
2. Defining the page hierarchy.
3. Defining the sitemap.
4. Defining primary navigation.
5. Identifying important user flows.
6. Defining page-level structural requirements.
7. Identifying important user actions and conversion paths.
8. Establishing content hierarchy from a UX perspective.
9. Identifying UX requirements and constraints.
10. Identifying structural ambiguities or gaps.
11. Producing the required UX artifacts.

## 12.4 Information Architecture

The agent should organize the website's information into a logical structure.

The information architecture should consider:

* Business priorities
* User needs
* Website objectives
* Content relationships
* Page hierarchy
* Navigation requirements
* User journeys
* Conversion goals

The resulting structure should make it easy for users to understand where they are and where they can go next.

## 12.5 Sitemap

The agent should define the proposed website sitemap.

A sitemap may be represented as:

```text
Home
├── About
├── Services
│   ├── Service A
│   ├── Service B
│   └── Service C
├── Projects
├── Contact
└── Other Required Pages
```

The exact structure depends on the project.

The sitemap should reflect actual business and user requirements rather than adding pages simply to make the website appear more comprehensive.

## 12.6 Page Hierarchy

The agent should establish relationships between pages.

This may include:

* Primary pages
* Secondary pages
* Supporting pages
* Detail pages
* Landing pages
* Utility pages

Page hierarchy should help downstream agents understand the relative importance and relationship of each page.

## 12.7 Navigation

The agent should define the website's navigation structure.

This may include:

* Primary navigation
* Secondary navigation
* Footer navigation
* Utility navigation
* Calls to action
* Mobile navigation requirements

Navigation decisions should reflect the website's information architecture and user priorities.

The agent should not define detailed visual styling for navigation. Those decisions belong to the UI/UX Design stage.

## 12.8 User Flows

The agent should identify the most important user journeys through the website.

Examples may include:

```text
Landing Page
    ↓
Service Information
    ↓
Service Detail
    ↓
Contact / Inquiry
```

or:

```text
Landing Page
    ↓
Portfolio
    ↓
Project Detail
    ↓
Contact
```

The focus should be on meaningful journeys that support the website's objectives.

Not every possible user path needs to be documented.

## 12.9 Conversion Paths

Where the website has a business conversion objective, the agent should identify the primary conversion paths.

Possible conversion actions include:

* Contacting the business
* Requesting a quote
* Booking a consultation
* Calling the business
* Submitting an inquiry
* Purchasing a product
* Registering for a service
* Downloading information

The UX structure should make important actions accessible without overwhelming users with competing calls to action.

## 12.10 Page Requirements

For each important page, the agent should identify its structural purpose and required information.

A page definition may include:

```text
Page
Purpose
Primary User
Key Information
Primary Action
Supporting Actions
Required Sections
Dependencies
```

These definitions provide useful input for the Content Strategy and UI/UX Design stages.

## 12.11 Content Hierarchy

The UX Agent may define the high-level hierarchy of information on a page.

For example:

```text
Primary Message
      ↓
Supporting Value Proposition
      ↓
Key Information
      ↓
Supporting Evidence
      ↓
Primary Call to Action
```

This is a structural UX decision.

Detailed messaging, copywriting, tone, and content production remain the responsibility of the Content Strategy stage.

## 12.12 UX Requirements

The agent should identify important UX requirements that may influence later design and development.

Examples include:

* Mobile-first considerations
* Navigation requirements
* Important interaction flows
* Form requirements
* Conversion requirements
* Content discoverability
* User guidance
* Important states
* Error or empty states where relevant

Only requirements relevant to the project should be included.

## 12.13 Responsive UX Considerations

The agent should identify structural behavior that may need to change across viewport sizes.

Examples include:

* Navigation transformation
* Content stacking
* Priority changes
* Mobile interaction patterns
* Table or data presentation
* Form behavior
* Component visibility

The UX Agent defines the expected user experience.

Detailed responsive implementation and validation remain responsibilities of the Design, Development, and Responsive QA stages.

## 12.14 Accessibility Considerations

Accessibility should be considered during UX planning rather than being treated only as a final QA activity.

The agent should identify relevant structural considerations such as:

* Logical navigation
* Clear content hierarchy
* Understandable interactions
* Form usability
* Meaningful user flows
* Appropriate interaction alternatives

The Accessibility QA Agent remains responsible for validating the implemented website later in the workflow.

## 12.15 Assumptions and Open Questions

If the available business information does not provide enough information to make a structural decision, the agent should identify the issue.

Important questions may include:

* Is a particular page required?
* Which service should receive priority?
* Is a particular user journey business-critical?
* Is a specific feature required?
* Should a particular action be available globally?

Significant assumptions should be documented rather than silently treated as confirmed requirements.

## 12.16 Primary Outputs

The UX & Information Architecture Agent should produce the artifacts defined by its agent specification.

These may include:

* Sitemap
* Information architecture
* Navigation structure
* User flows
* Page requirements
* UX documentation
* Related structured artifacts where applicable

The exact artifact filenames should follow the existing Agent 02 specification.

## 12.17 Output Quality Check

Before the UX stage is considered complete, the outputs should be checked for:

* Clear website structure
* Logical page hierarchy
* Usable navigation
* Identified primary user flows
* Clear conversion paths where applicable
* Defined page-level requirements
* Alignment with business objectives
* Alignment with target audiences
* Important assumptions identified
* No major structural contradictions

The resulting UX artifacts should provide sufficient direction for the Content Strategy and UI/UX Design stages.

## 12.18 Handoff to Agent 03

The primary downstream consumer is:

```text
03 — Content Strategy Agent
```

The Content Strategy Agent uses the UX outputs to understand:

* Which pages require content
* What each page needs to accomplish
* How information should be prioritized
* Which user journeys content must support
* Which calls to action are important

The handoff is:

```text
01 — BUSINESS DISCOVERY
        ↓
02 — UX / INFORMATION ARCHITECTURE
        ↓
UX ARTIFACTS
        ↓
03 — CONTENT STRATEGY
```

## 12.19 Handoff to Agent 04

The UX outputs also provide a major input to:

```text
04 — UI/UX Design Agent
```

The Design Agent uses the UX structure to determine how the website should visually and interactively represent the defined experience.

The relationship is:

```text
UX / INFORMATION ARCHITECTURE
        ↓
PAGE STRUCTURE
        ↓
USER FLOWS
        ↓
UI/UX DESIGN
```

The UX Agent defines the structure and experience requirements.

The UI/UX Design Agent defines the visual and interaction design.

## 12.20 Downstream Impact

UX decisions can affect nearly every downstream stage.

For example:

```text
UX Structure
    ↓
Content
    ↓
Design
    ↓
Design System
    ↓
Frontend Architecture
    ↓
Development
    ↓
QA
```

Therefore, significant changes to the information architecture after design or development has started should trigger an impact review.

Only affected stages should be re-executed.

## 12.21 What the UX Agent Does Not Own

The UX & Information Architecture Agent should not independently own:

* Final website copy
* Final visual design
* Design tokens
* Complete component design
* Frontend architecture
* Source-code implementation
* Responsive QA
* Accessibility QA
* SEO validation
* Production QA

These responsibilities belong to the appropriate specialized stages.

## 12.22 Completion Criteria

Agent 02 is considered complete when:

* The website information architecture is defined.
* The sitemap is sufficiently clear.
* Page hierarchy is established.
* Navigation requirements are defined.
* Important user flows are documented.
* Conversion paths are identified where applicable.
* Page-level structural requirements are defined.
* Important UX requirements are captured.
* Assumptions and unresolved structural questions are identified.
* Required UX artifacts are produced.
* The outputs are usable by Content Strategy and UI/UX Design.

The workflow can then proceed to:

```text
03 — Content Strategy Agent
```

and, where appropriate, provide the UX outputs to:

```text
04 — UI/UX Design Agent
```

## 12.23 Version 1 Principle

The UX & Information Architecture Agent should remain focused on **structuring the website experience**.

Its purpose is not to solve every content, visual, or technical implementation problem.

The guiding principle is:

**Structure the experience clearly → document the important user paths → hand a reliable foundation to Content and Design.**
# 13. Agent 03 — Content Strategy

The **Content Strategy Agent** is the third specialized agent in the Agentic Website Factory.

Its purpose is to transform the business and UX foundations into a clear content direction for the website.

The agent determines what information each page needs, how messaging should be organized, how content should support user journeys and business objectives, and what content requirements should guide the UI/UX Design and Development stages.

The Content Strategy Agent focuses on **content structure and direction** rather than treating content as an isolated copywriting task.

## 13.1 Objective

The primary objective of the Content Strategy Agent is to answer:

* What information does the website need?
* What should each page communicate?
* What is the primary message of each page?
* How should information be prioritized?
* What content supports the intended user journey?
* What calls to action should be emphasized?
* What existing content can be reused, adapted, or replaced?
* What content is missing?
* What content requirements should be communicated to Design and Development?

The goal is to establish a content foundation that supports both the business objectives and the UX structure.

## 13.2 Primary Inputs

The Content Strategy Agent primarily receives:

* Business Discovery artifacts
* UX and Information Architecture artifacts
* Client requirements
* Existing website content
* Business information
* Product and service information
* Brand guidelines
* Existing marketing materials
* Reference materials
* Approved project decisions
* Relevant content constraints

The primary workflow relationship is:

```text
01 — BUSINESS DISCOVERY
        ↓
02 — UX / INFORMATION ARCHITECTURE
        ↓
03 — CONTENT STRATEGY
```

The agent should use the latest valid upstream artifacts and approved decisions.

## 13.3 Core Responsibilities

The Content Strategy Agent is responsible for:

1. Defining the content requirements for the website.
2. Establishing page-level content direction.
3. Defining messaging hierarchy.
4. Identifying primary and supporting messages.
5. Mapping content requirements to the website structure.
6. Identifying required calls to action.
7. Reviewing existing content for potential reuse.
8. Identifying missing content.
9. Establishing content priorities.
10. Identifying content-related assumptions and gaps.
11. Providing content direction for UI/UX Design.
12. Producing the required Content Strategy artifacts.

## 13.4 Content Strategy vs Content Production

The Content Strategy Agent does not necessarily need to produce every final piece of website copy.

Its primary responsibility is to define **what the content needs to accomplish and how it should be structured**.

For example:

```text
Page: Services

Primary Message:
Clearly communicate the company's core services.

Supporting Content:
Service categories
Key benefits
Proof / credibility
Process

Primary CTA:
Request a Consultation
```

The exact level of copy production may vary by project and by the capabilities defined in the existing Content Strategy Agent.

The workflow should not create a separate copywriting agent solely to handle this responsibility in Version 1.

## 13.5 Content Requirements

The agent should identify the information required for each major page.

A page-level content requirement may include:

```text
Page
Purpose
Primary Message
Supporting Messages
Required Information
Proof / Evidence
Primary CTA
Secondary CTA
Content Dependencies
```

This provides a clear bridge between UX structure and visual design.

## 13.6 Messaging Hierarchy

The agent should establish the relative importance of messages.

A typical hierarchy may be:

```text
Primary Message
      ↓
Supporting Value Proposition
      ↓
Key Benefits
      ↓
Supporting Evidence
      ↓
Secondary Information
      ↓
Call to Action
```

The exact hierarchy depends on the project.

The objective is to prevent important business information from being buried beneath lower-priority content.

## 13.7 Page-Level Content Strategy

Each important page should have a clear content purpose.

For example:

```text
Home
→ Establish positioning and guide users toward key actions.

About
→ Build credibility and explain the organization.

Services
→ Explain the available services and their value.

Projects
→ Demonstrate experience and provide evidence.

Contact
→ Enable users to take the primary conversion action.
```

The agent should define page purposes based on the actual project rather than applying a fixed website template.

## 13.8 Content Hierarchy and UX

The Content Strategy Agent should use the UX structure established by Agent 02.

The relationship is:

```text
UX Structure
     ↓
Content Requirements
     ↓
Messaging Hierarchy
     ↓
Page Content Direction
```

Content should support the user journeys and page objectives defined during UX planning.

The Content Strategy Agent should not redefine the website's information architecture without documenting the required change and its downstream impact.

## 13.9 Calls to Action

The agent should identify important calls to action where applicable.

Examples include:

* Contact Us
* Request a Quote
* Book a Consultation
* Schedule a Call
* Get Started
* Learn More
* View Projects
* Purchase
* Register

CTA recommendations should reflect the business objective and user journey.

The agent should avoid creating excessive competing calls to action simply to fill page sections.

## 13.10 Existing Content

Existing client content should be treated as source material.

It may be:

* Reused
* Edited
* Reorganized
* Condensed
* Expanded
* Rewritten
* Replaced
* Identified as requiring client confirmation

The agent should preserve important business facts and avoid introducing unsupported claims.

## 13.11 Content Gaps

The agent should identify information that is required but unavailable.

Examples may include:

* Missing service descriptions
* Missing product information
* Missing company details
* Missing testimonials
* Missing case studies
* Missing imagery
* Missing contact information
* Missing legal or policy content
* Missing proof points

Content gaps should be prioritized according to their effect on the website.

Critical gaps should be identified before they create downstream design or development problems.

## 13.12 Content Sources and Confidence

Where content is derived from different sources, the agent should distinguish between:

* Client-provided information
* Existing published content
* Approved project information
* Reasonable assumptions
* Information requiring confirmation

Important business claims should not be presented as confirmed facts when their source is uncertain.

## 13.13 Tone and Brand Direction

Where sufficient brand information is available, the agent should define appropriate content direction.

This may include:

* Tone of voice
* Communication style
* Formality
* Brand personality
* Messaging characteristics
* Vocabulary preferences
* Words or claims to avoid

The purpose is to create consistent communication across the website.

Detailed visual expression of the brand remains the responsibility of the UI/UX Design and Design System stages.

## 13.14 SEO Content Considerations

The Content Strategy Agent may identify content considerations that support later SEO work.

Examples include:

* Important topics
* Search-intent considerations
* Page relevance
* Content hierarchy
* Heading structure requirements
* Important terminology
* Content gaps

The agent should not attempt to replace the dedicated SEO & Performance stage.

SEO-specific validation remains the responsibility of Agent 10.

## 13.15 Content for Responsive Experiences

Content should be considered in relation to different screen sizes.

The agent may identify content that should:

* Remain prominent on mobile
* Be condensed
* Be progressively revealed
* Be reorganized
* Be prioritized differently

These are content and experience considerations.

Detailed responsive implementation belongs to the Design, Development, and Responsive QA stages.

## 13.16 Content Dependencies

Some content may depend on information that is not yet available.

For example:

```text
Case Study Content
      ↓
Requires Client Project Information
```

or:

```text
Testimonials
      ↓
Requires Approved Client Testimonials
```

The agent should identify such dependencies so they do not become hidden blockers during design or development.

## 13.17 Assumptions and Open Questions

If important content decisions cannot be confirmed from available information, the agent should document them.

Examples include:

* Which service should receive primary emphasis?
* Which customer segment should be prioritized?
* Which claims can be used publicly?
* Which testimonials are approved?
* Which case studies are available?
* What CTA should be primary?

Significant unresolved questions should be recorded for client or project-team clarification.

## 13.18 Primary Outputs

The Content Strategy Agent should produce the artifacts defined by its existing agent specification.

These may include:

* Content strategy
* Page-level content requirements
* Messaging hierarchy
* Content structure
* CTA direction
* Content gap analysis
* Content guidance
* Related structured artifacts where applicable

The exact artifact filenames should follow the existing Agent 03 specification.

## 13.19 Output Quality Check

Before the Content Strategy stage is considered complete, the outputs should be checked for:

* Alignment with business objectives
* Alignment with UX structure
* Clear page-level content requirements
* Clear messaging hierarchy
* Identified primary CTAs
* Identified content gaps
* Identified important content dependencies
* Appropriate brand and tone direction
* Important assumptions identified
* No unsupported business claims

The resulting artifacts should provide sufficient content direction for the UI/UX Design stage.

## 13.20 Handoff to Agent 04

The primary downstream consumer is:

```text
04 — UI/UX Design Agent
```

The Design Agent uses the Content Strategy outputs to understand:

* What each page needs to communicate
* Which information is most important
* What content hierarchy should be represented visually
* Which CTAs require emphasis
* What content constraints exist

The handoff is:

```text
01 — BUSINESS DISCOVERY
        ↓
02 — UX / INFORMATION ARCHITECTURE
        ↓
03 — CONTENT STRATEGY
        ↓
CONTENT ARTIFACTS
        ↓
04 — UI/UX DESIGN
```

## 13.21 Relationship With UX

UX and Content Strategy are closely connected but remain separate responsibilities.

The UX Agent primarily defines:

**How the user moves through and understands the website structure.**

The Content Strategy Agent primarily defines:

**What the website needs to communicate and how that information should be prioritized.**

The relationship can be represented as:

```text
UX
↓
Structure + User Journey

CONTENT
↓
Message + Information

UX + CONTENT
↓
UI/UX DESIGN
```

Neither stage should silently replace the responsibility of the other.

## 13.22 Downstream Impact

Content decisions can affect:

* UI/UX Design
* Design System
* Frontend Architecture
* Development
* SEO
* Responsive behavior
* Production QA

For example, a significant change in the amount of content on a page may affect:

```text
Content
  ↓
Layout
  ↓
Components
  ↓
Implementation
  ↓
Responsive Behavior
```

Significant content changes after design or development has started should therefore trigger an impact review.

## 13.23 What the Content Strategy Agent Does Not Own

The Content Strategy Agent should not independently own:

* Website information architecture
* Final visual design
* Design tokens
* Complete component design
* Frontend architecture
* Source-code implementation
* Responsive QA
* Accessibility QA
* Technical SEO validation
* Production QA

Those responsibilities remain with the appropriate specialized agents.

## 13.24 Completion Criteria

Agent 03 is considered complete when:

* Website content requirements are defined.
* Major pages have clear content objectives.
* Messaging hierarchy is established.
* Important CTAs are identified.
* Existing content has been assessed where applicable.
* Critical content gaps are identified.
* Important content dependencies are documented.
* Relevant tone and brand direction is established where possible.
* Important assumptions and unresolved questions are identified.
* Required Content Strategy artifacts are produced.
* The outputs are usable by the UI/UX Design stage.

The workflow can then proceed to:

```text
04 — UI/UX Design Agent
```

## 13.25 Version 1 Principle

The Content Strategy Agent should remain focused on **content direction, structure, and messaging priorities**.

It should not become a separate content-production factory inside the website factory.

The guiding principle is:

**Define what needs to be communicated → prioritize the information → support the user journey → provide clear direction to Design.**
# 14. Agent 04 — UI/UX Design

The **UI/UX Design Agent** is the fourth specialized agent in the Agentic Website Factory.

Its purpose is to transform the approved business, UX, and content direction into a coherent visual and interactive website experience.

The agent defines page layouts, visual hierarchy, interaction patterns, responsive design direction, and other visual requirements needed to implement the website.

The output of this stage becomes a primary input for the Design System, Frontend Architecture, and Development stages.

## 14.1 Objective

The primary objective of the UI/UX Design Agent is to answer:

* How should the website look and feel?
* How should information be visually organized?
* How should users interact with the interface?
* How should the brand be expressed visually?
* How should important content and calls to action be emphasized?
* How should layouts behave across different screen sizes?
* What visual and interaction decisions are required for implementation?

The agent should translate the previously established business, UX, and content requirements into a practical website design.

## 14.2 Primary Inputs

The UI/UX Design Agent primarily receives:

* Business Discovery artifacts
* UX and Information Architecture artifacts
* Content Strategy artifacts
* Brand guidelines
* Brand assets
* Design references
* Client visual preferences
* Existing design systems where applicable
* Approved project decisions
* Relevant technical constraints

The primary workflow relationship is:

```text
01 — BUSINESS DISCOVERY
        ↓
02 — UX / INFORMATION ARCHITECTURE
        ↓
03 — CONTENT STRATEGY
        ↓
04 — UI/UX DESIGN
```

The agent should use the latest valid upstream artifacts and approved decisions.

## 14.3 Core Responsibilities

The UI/UX Design Agent is responsible for:

1. Defining the visual direction of the website.
2. Translating UX structure into page layouts.
3. Establishing visual hierarchy.
4. Defining interaction patterns.
5. Establishing page composition.
6. Defining component usage from a design perspective.
7. Defining responsive design direction.
8. Applying the available brand identity.
9. Establishing visual emphasis for important content and actions.
10. Identifying design assumptions and open questions.
11. Producing the required UI/UX design artifacts.

## 14.4 Design Direction

The agent should establish a coherent visual direction based on the available brand and project information.

This may include:

* Visual personality
* Overall aesthetic
* Layout character
* Typography direction
* Color direction
* Imagery direction
* Iconography direction
* Shape language
* Spacing character
* Interaction style

The design direction should support the business positioning and target audience.

It should not introduce visual decisions that conflict with confirmed brand requirements without documenting the reason.

## 14.5 Page Layouts

The agent should translate the UX page structure and content requirements into visual layouts.

A page layout may define:

```text
Page
├── Header / Navigation
├── Hero / Primary Message
├── Supporting Content
├── Key Information
├── Supporting Evidence
├── Primary CTA
└── Footer
```

The actual structure depends on the project.

The agent should avoid adding sections simply for visual complexity.

Every major section should have a clear purpose.

## 14.6 Visual Hierarchy

The design should establish a clear hierarchy between:

* Primary messages
* Supporting messages
* Important information
* Supporting content
* Calls to action
* Navigation
* Secondary information

Visual hierarchy may be established through:

* Typography
* Scale
* Spacing
* Position
* Contrast
* Grouping
* Alignment
* Visual emphasis

The objective is to help users understand the page quickly and move toward relevant actions.

## 14.7 Interaction Design

The agent should define important interaction patterns required by the website.

These may include:

* Navigation interactions
* Buttons
* Links
* Forms
* Cards
* Accordions
* Tabs
* Modals
* Menus
* Hover states
* Focus states
* Loading states
* Error states
* Success states

Only interactions relevant to the project should be defined.

The agent should avoid introducing complex interactions when a simpler pattern provides the same user value.

## 14.8 Component-Oriented Design

The design should identify reusable interface patterns.

Examples include:

* Buttons
* Cards
* Navigation elements
* Form controls
* Content sections
* Testimonials
* Service blocks
* Feature sections
* Footers
* Alerts
* Modal patterns

The goal is to create a consistent interface that can later be represented through the Design System and implemented through reusable frontend components.

The Design System Agent formalizes the reusable tokens and component rules in the next stage.

## 14.9 Responsive Design Direction

The UI/UX Design Agent should establish how the design adapts across different viewport sizes.

This may include:

* Desktop layouts
* Tablet behavior
* Mobile layouts
* Navigation changes
* Content stacking
* Typography scaling
* Spacing adjustments
* Image behavior
* Component transformations
* Visibility changes

The design should consider responsive behavior as part of the design rather than treating mobile as an afterthought.

Detailed implementation and validation remain the responsibility of Development and Responsive QA.

## 14.10 Accessibility-Aware Design

Accessibility should be considered during design.

The agent should consider:

* Sufficient visual distinction
* Readable typography
* Clear interactive elements
* Logical focus considerations
* Meaningful states
* Understandable navigation
* Appropriate contrast
* Usable controls

The Accessibility QA Agent remains responsible for validating the implemented website.

Design should establish a strong foundation for that validation.

## 14.11 Brand Integration

Where brand assets and guidelines are available, the agent should incorporate them into the design.

This may include:

* Logo usage
* Brand colors
* Typography
* Imagery
* Brand tone expressed visually
* Existing visual patterns

Where formal guidelines are unavailable, the agent may establish a proposed visual direction based on the available information.

Important assumptions should be documented.

## 14.12 Design References

Reference websites, screenshots, mood boards, and other visual references may be used to establish direction.

References should be treated as inspiration and context.

The agent should not simply copy another website's design.

The resulting design should be appropriate to the client's business, audience, objectives, and brand.

## 14.13 Design Tools

The UI/UX Design stage may use external design tools where appropriate.

Examples include:

* Figma
* Stitch
* Other suitable design tools

Where external tools are used, important design decisions should be represented in project artifacts so downstream agents do not depend exclusively on access to the external tool.

The project should retain relevant exports, specifications, screenshots, or documentation as appropriate.

## 14.14 Design States

Where relevant, the design should account for important interface states.

These may include:

```text
DEFAULT
HOVER
FOCUS
ACTIVE
DISABLED
LOADING
ERROR
SUCCESS
EMPTY
```

Not every component requires every state.

The agent should identify only states relevant to the actual interface.

## 14.15 Content and Design Relationship

The UI/UX Design Agent should use the Content Strategy outputs when defining layouts.

The relationship is:

```text
UX
 ↓
Structure

CONTENT
 ↓
Message + Information

UX + CONTENT
 ↓
UI/UX DESIGN
 ↓
Visual Experience
```

The design should accommodate the expected content rather than relying on unrealistic placeholder content.

Significant content changes after design may require layout review.

## 14.16 Design Assumptions and Open Questions

The agent should identify important design decisions that cannot be confirmed from available information.

Examples include:

* Preferred visual style
* Brand color interpretation
* Typography availability
* Image direction
* Animation expectations
* Interaction preferences
* Client-specific design requirements

Important assumptions should be documented rather than silently treated as approved decisions.

## 14.17 Primary Outputs

The UI/UX Design Agent should produce the artifacts defined by its existing agent specification.

These may include:

* UI/UX design documentation
* Page design specifications
* Layout definitions
* Visual direction
* Interaction requirements
* Responsive design direction
* Design references
* Relevant design exports
* Supporting structured artifacts where applicable

The exact artifact filenames should follow the existing Agent 04 specification.

## 14.18 Design Review

The completed design should be reviewed before downstream implementation planning proceeds.

The review should verify:

* Alignment with business objectives
* Alignment with UX structure
* Alignment with content requirements
* Brand consistency
* Clear visual hierarchy
* Usable interaction patterns
* Responsive direction
* Sufficient implementation detail
* Major design assumptions identified

Where the project requires formal approval, this stage leads to the **Design Approval** gate defined later in this workflow.

## 14.19 Design Approval Gate

Design approval is a meaningful human decision point in Version 1.

The purpose of the gate is to confirm that the proposed website experience is acceptable before significant downstream implementation work proceeds.

The conceptual flow is:

```text
UI/UX DESIGN
      ↓
DESIGN REVIEW
      ↓
HUMAN DESIGN APPROVAL
      ↓
DESIGN SYSTEM
      ↓
FRONTEND ARCHITECTURE
      ↓
DEVELOPMENT
```

Design approval does not require approval of every small visual detail.

The goal is to obtain agreement on the overall website direction and major design decisions.

The detailed approval process is defined later in **Section 24 — Human Approval Gates**.

## 14.20 Handoff to Agent 05

The primary downstream consumer is:

```text
05 — Design System Agent
```

The Design System Agent uses the UI/UX design outputs to identify and formalize reusable:

* Design tokens
* Components
* Patterns
* Typography rules
* Spacing rules
* Color rules
* Component behavior

The handoff is:

```text
04 — UI/UX DESIGN
        ↓
DESIGN ARTIFACTS
        ↓
05 — DESIGN SYSTEM
```

## 14.21 Handoff to Agent 06

The UI/UX Design outputs also provide an important input to:

```text
06 — Frontend Architect Agent
```

The Frontend Architect uses the design direction to understand:

* Page structures
* Component requirements
* Interaction requirements
* Responsive expectations
* Implementation complexity
* Design-system dependencies

The relationship is:

```text
UI/UX DESIGN
      ↓
DESIGN REQUIREMENTS
      ↓
FRONTEND ARCHITECTURE
```

## 14.22 Handoff to Agent 07

The approved design ultimately becomes an implementation input for:

```text
07 — Development Agent
```

Development should use the approved design together with the Design System and Frontend Architecture rather than treating the design as an isolated visual reference.

The implementation relationship is:

```text
UI/UX DESIGN
      ↓
DESIGN SYSTEM
      ↓
FRONTEND ARCHITECTURE
      ↓
DEVELOPMENT
```

## 14.23 Downstream Impact

Design decisions can affect:

* Design System
* Frontend Architecture
* Development
* Responsive behavior
* Accessibility
* SEO and Performance
* Production QA

A significant design change after downstream work has started should therefore trigger an impact review.

Only affected stages should be re-executed.

## 14.24 What the UI/UX Design Agent Does Not Own

The UI/UX Design Agent should not independently own:

* Business discovery
* Final information architecture
* Complete content strategy
* Final design-system governance
* Frontend architecture
* Source-code implementation
* Responsive QA
* Accessibility QA
* SEO validation
* Production QA
* Final production approval

These responsibilities remain with the appropriate specialized stages.

## 14.25 Completion Criteria

Agent 04 is considered complete when:

* Visual direction is established.
* Major page layouts are defined.
* Visual hierarchy is clear.
* Important interaction patterns are identified.
* Responsive design direction is established.
* Brand requirements are incorporated where available.
* Relevant accessibility considerations are included.
* Required design artifacts are produced.
* Important assumptions and open questions are documented.
* Design review has been completed.
* Required human design approval has been obtained before downstream implementation proceeds.

The workflow can then proceed to:

```text
05 — Design System Agent
```

## 14.26 Version 1 Principle

The UI/UX Design Agent should remain focused on **turning structure and content into a coherent visual and interactive experience**.

It should not become responsible for solving the complete technical implementation.

The guiding principle is:

**Structure + Content + Brand → Clear Visual Experience → Implementation-ready Design Direction**
# 15. Agent 05 — Design System

The **Design System Agent** is the fifth specialized agent in the Agentic Website Factory.

Its purpose is to transform the approved UI/UX design direction into a reusable, consistent, and implementation-ready design system.

The agent establishes the visual rules, reusable tokens, components, patterns, and usage guidance required to maintain consistency across the website.

The Design System becomes a shared foundation for the Frontend Architecture and Development stages.

## 15.1 Objective

The primary objective of the Design System Agent is to answer:

* What are the reusable visual rules of the website?
* Which design values should become tokens?
* Which interface elements should become reusable components?
* How should components behave and be used?
* How should visual consistency be maintained across pages?
* What design decisions need to be represented in a form that development can reliably consume?

The goal is to convert the approved design into a **reusable implementation foundation**, rather than creating isolated styling decisions for individual pages.

## 15.2 Primary Inputs

The Design System Agent primarily receives:

* Approved UI/UX design artifacts
* UI/UX design specifications
* Page layouts
* Visual direction
* Interaction requirements
* Responsive design direction
* Brand guidelines
* Brand assets
* Relevant UX artifacts
* Content context where required
* Approved project decisions

The primary workflow relationship is:

```text
04 — UI/UX DESIGN
        ↓
DESIGN ARTIFACTS
        ↓
05 — DESIGN SYSTEM
```

The Design System Agent should use the approved design direction as its primary source of truth.

## 15.3 Core Responsibilities

The Design System Agent is responsible for:

1. Identifying reusable design values.
2. Defining design tokens.
3. Establishing typography rules.
4. Establishing color rules.
5. Defining spacing and sizing conventions.
6. Identifying reusable UI components.
7. Defining component variants and states where required.
8. Defining component usage rules.
9. Establishing consistency across the interface.
10. Producing human-readable design-system documentation.
11. Producing machine-readable artifacts where they provide practical value.

## 15.4 Design Token Foundation

The agent should identify visual values that should be represented as reusable tokens.

Depending on the project, these may include:

* Colors
* Typography
* Font sizes
* Font weights
* Line heights
* Spacing
* Border radius
* Borders
* Shadows
* Breakpoints
* Component dimensions
* Other reusable visual values

The objective is to avoid repeatedly defining the same value in different parts of the website.

## 15.5 Color System

The design system should establish a consistent color structure.

This may include:

* Primary colors
* Secondary colors
* Accent colors
* Background colors
* Surface colors
* Text colors
* Border colors
* Interactive colors
* Success states
* Warning states
* Error states

Colors should be mapped according to their purpose rather than simply listed as unrelated values.

For example:

```text
Primary
Secondary
Background
Surface
Text
Muted Text
Border
Success
Warning
Error
```

The exact categories depend on the project.

## 15.6 Typography System

The agent should define a consistent typography system.

This may include:

* Font families
* Heading hierarchy
* Body text
* Supporting text
* Labels
* Buttons
* Navigation text
* Font sizes
* Font weights
* Line heights
* Letter spacing

The system should provide sufficient flexibility for the website while avoiding unnecessary typography variations.

## 15.7 Spacing System

A reusable spacing approach should be established where appropriate.

The system may define values for:

* Section spacing
* Component spacing
* Element spacing
* Page padding
* Grid gaps
* Card spacing
* Form spacing

The objective is to establish visual rhythm and consistency.

The Design System Agent should avoid creating a large number of spacing values without a practical reason.

## 15.8 Layout and Sizing Rules

Where appropriate, the design system should document common layout rules such as:

* Container widths
* Grid behavior
* Column structures
* Content widths
* Alignment rules
* Section proportions
* Common component dimensions

These rules should support the layouts defined by the UI/UX Design Agent.

## 15.9 Component Identification

The agent should identify interface elements that should be reusable.

Examples include:

* Buttons
* Links
* Navigation
* Cards
* Form fields
* Inputs
* Selects
* Checkboxes
* Badges
* Alerts
* Modals
* Tabs
* Accordions
* Testimonials
* Feature blocks
* Section headers
* Footer elements

Not every visual element needs to become a separate component.

The goal is **useful reuse**, not maximum component fragmentation.

## 15.10 Component Variants

Where a component has meaningful variations, the design system should define them explicitly.

For example:

```text
Button
├── Primary
├── Secondary
└── Ghost
```

Or:

```text
Card
├── Default
├── Featured
└── Compact
```

Variants should exist only when they represent meaningful differences in behavior or visual purpose.

## 15.11 Component States

Where applicable, components should define important states.

Examples include:

```text
Default
Hover
Focus
Active
Disabled
Loading
Error
Success
```

The design system should document states that are relevant to implementation and accessibility.

It should not create unnecessary states for components that do not require them.

## 15.12 Responsive Design Rules

The Design System should support the responsive behavior established during UI/UX Design.

This may include:

* Responsive typography
* Responsive spacing
* Breakpoint rules
* Container behavior
* Grid behavior
* Component transformations
* Mobile-specific component behavior

The Design System Agent establishes reusable rules.

The Development Agent implements them, while Responsive QA validates the actual behavior.

## 15.13 Accessibility Considerations

The design system should provide a foundation that supports accessible implementation.

Where relevant, it should consider:

* Color contrast
* Text readability
* Focus states
* Interactive target sizes
* Visible interaction states
* Form-state clarity
* Semantic component expectations

The Design System Agent does not replace Accessibility QA.

The Accessibility QA Agent remains responsible for validating the implemented website.

## 15.14 Component Usage Rules

The design system should document how reusable components are intended to be used.

For example:

```text
Button
→ Use for actions.

Link
→ Use for navigation.

Card
→ Use for grouped content.

Alert
→ Use for important status information.
```

These rules help prevent inconsistent component usage during development.

## 15.15 Design-System Documentation

The Design System Agent should produce human-readable documentation that explains the system.

The documentation should be sufficiently clear for:

* Frontend architects
* Developers
* Designers
* QA reviewers
* Future maintainers

The documentation should focus on practical implementation guidance rather than theoretical design-system terminology.

## 15.16 Machine-Readable Design-System Artifacts

Where useful, the agent may produce machine-readable artifacts.

Examples include:

```text
design-system.tokens.json
design-system.components.json
```

These artifacts may represent:

* Design tokens
* Component definitions
* Component variants
* Component states
* Other structured design information

Machine-readable artifacts should be used where they provide real downstream value.

Version 1 does not require every design-system decision to be represented in JSON.

## 15.17 Artifact Consistency

Human-readable and machine-readable artifacts should represent the same approved design-system decisions.

For example:

```text
Design System Documentation
        +
Design System JSON
        ↓
Same Approved Design Rules
```

If a meaningful conflict exists between artifacts, the responsible design-system stage should resolve it before downstream implementation.

## 15.18 Design System as Shared Contract

The Design System acts as a shared visual contract between design and development.

The relationship is:

```text
UI/UX DESIGN
      ↓
DESIGN SYSTEM
      ↓
FRONTEND ARCHITECTURE
      ↓
DEVELOPMENT
```

This reduces ambiguity during implementation and helps prevent developers from independently inventing visual rules that already exist in the approved design system.

## 15.19 Relationship with Frontend Architecture

The Frontend Architect uses the Design System to determine how the visual system should be represented technically.

For example:

```text
Design Token
    ↓
Technical Token Representation

Design Component
    ↓
Frontend Component

Design Variant
    ↓
Component Variant
```

The Design System defines **what the interface should consistently use**.

The Frontend Architecture defines **how those requirements should be implemented technically**.

## 15.20 Relationship with Development

The Development Agent consumes the approved design system together with the UI/UX design and frontend architecture.

The implementation relationship is:

```text
UI/UX DESIGN
      ↓
DESIGN SYSTEM
      ↓
FRONTEND ARCHITECTURE
      ↓
DEVELOPMENT
```

Development should prefer the defined system components and tokens instead of creating unnecessary one-off alternatives.

## 15.21 Design-System Changes

If a significant design-system change is required after development begins, the impact should be assessed.

The preferred process is:

```text
DESIGN-SYSTEM CHANGE
        ↓
IDENTIFY IMPACT
        ↓
UPDATE DESIGN-SYSTEM ARTIFACTS
        ↓
REVIEW FRONTEND ARCHITECTURE
        ↓
UPDATE DEVELOPMENT
        ↓
RE-RUN AFFECTED QA
```

The entire factory should not automatically restart.

Only affected downstream work should be updated.

## 15.22 What the Design System Agent Does Not Own

The Design System Agent should not independently own:

* Business requirements
* Information architecture
* Content strategy
* Final page UX
* Frontend architecture
* Application implementation
* Responsive QA
* Accessibility QA
* SEO validation
* Production QA
* Final production approval

Its responsibility is to establish the reusable design foundation.

## 15.23 Primary Outputs

The Design System Agent should produce the artifacts defined by its existing agent specification.

These may include:

* Design system documentation
* Design tokens
* Component definitions
* Component usage rules
* Component states and variants
* Responsive design-system rules
* Machine-readable design-system artifacts where applicable

The exact artifact filenames should follow the existing Agent 05 specification.

## 15.24 Completion Criteria

Agent 05 is considered complete when:

* The approved visual direction has been translated into reusable design rules.
* Required design tokens are defined.
* Typography rules are established.
* Color rules are established.
* Spacing and sizing rules are established where applicable.
* Reusable components are identified.
* Relevant component variants and states are defined.
* Responsive rules are documented where required.
* Accessibility considerations are represented where relevant.
* Required design-system artifacts are produced.
* Human-readable and machine-readable artifacts are consistent where both exist.
* Important assumptions are documented.

The workflow can then proceed to:

```text
06 — Frontend Architect Agent
```

## 15.25 Version 1 Principle

The Design System Agent should remain focused on **turning approved visual design into a reusable implementation foundation**.

It should not become a separate governance platform or introduce unnecessary design-system complexity.

The guiding principle is:

**Approved Design → Reusable Rules → Consistent Components → Implementation Foundation**
# 16. Agent 06 — Frontend Architecture

The **Frontend Architect Agent** is the sixth specialized agent in the Agentic Website Factory.

Its purpose is to translate the approved UI/UX design and design system into a clear, practical, and implementation-ready frontend architecture.

The agent defines how the website should be structured technically so that the Development Agent can implement the approved experience consistently, efficiently, and maintainably.

The Frontend Architecture stage acts as the bridge between **design decisions** and **website implementation**.

## 16.1 Objective

The primary objective of the Frontend Architect Agent is to answer:

* How should the website be structured technically?
* What frontend technology and implementation approach should be used?
* How should pages and components be organized?
* How should the design system map to frontend implementation?
* Which components should be reusable?
* How should application-level concerns be handled?
* What technical constraints or decisions must Development follow?

The goal is to establish enough technical clarity for development without introducing unnecessary architecture or infrastructure.

## 16.2 Primary Inputs

The Frontend Architect Agent primarily receives:

* Approved UI/UX design artifacts
* Design system documentation
* Design tokens
* Component definitions
* UX and information architecture artifacts
* Content requirements
* Technical project requirements
* Existing codebase information where applicable
* Hosting and deployment requirements
* Approved project decisions
* Relevant client constraints

The primary workflow relationship is:

```text
04 — UI/UX DESIGN
        ↓
05 — DESIGN SYSTEM
        ↓
06 — FRONTEND ARCHITECTURE
```

Where appropriate, the architect may also reference earlier business, UX, and content artifacts.

## 16.3 Core Responsibilities

The Frontend Architect Agent is responsible for:

1. Defining the frontend technical approach.
2. Defining the project structure.
3. Defining page and route organization.
4. Defining component architecture.
5. Mapping design-system components to frontend components.
6. Defining reusable implementation patterns.
7. Identifying required application-level behavior.
8. Defining relevant data and state requirements.
9. Establishing technical boundaries for development.
10. Identifying implementation risks and constraints.
11. Producing the required frontend architecture artifacts.

## 16.4 Architecture Philosophy

Version 1 follows a **practical architecture principle**.

The architect should choose the simplest technical structure that can reliably support the approved website.

Architecture should be driven by actual project requirements rather than by the desire to demonstrate technical sophistication.

The guiding principle is:

**Required functionality → Appropriate architecture → Minimal necessary complexity**

## 16.5 Technology Selection

Where the technology stack has not already been specified, the Frontend Architect may recommend an appropriate frontend stack.

Considerations may include:

* Project requirements
* Existing codebase
* Team capabilities
* Design requirements
* Performance requirements
* Hosting environment
* Maintainability
* Integration requirements
* Expected project scale

The architect should avoid introducing technologies that do not provide meaningful value.

Where a technology has already been approved, the architect should work within that constraint unless a significant issue is identified.

## 16.6 Project Structure

The architect should define a practical frontend project structure.

For example:

```text
WEBSITE/
├── src/
│   ├── components/
│   ├── pages/
│   ├── layouts/
│   ├── assets/
│   ├── styles/
│   └── ...
├── public/
├── package.json
└── configuration files
```

The exact structure depends on the selected technology and project requirements.

The purpose is to establish predictable organization for development.

## 16.7 Page and Route Architecture

The agent should translate the approved information architecture into an implementation structure.

This may include:

* Pages
* Routes
* Nested routes
* Layouts
* Shared page structures
* Dynamic routes where required

For example:

```text
Website
├── Home
├── About
├── Services
├── Service Detail
├── Contact
└── Other Required Pages
```

The implementation should reflect the approved UX structure rather than independently redefining the website hierarchy.

## 16.8 Component Architecture

The architect should identify which interface elements should become reusable frontend components.

The component architecture may include:

```text
Global Components
├── Header
├── Navigation
├── Footer
└── Button

Content Components
├── Hero
├── SectionHeader
├── Card
├── FeatureBlock
└── Testimonial

Page Components
├── HomePage
├── AboutPage
├── ServicesPage
└── ContactPage
```

The exact structure depends on the project.

Components should be created where reuse, consistency, or maintainability provides a clear benefit.

## 16.9 Design System Mapping

The Frontend Architect should establish how the approved design system will be represented in the frontend.

For example:

```text
DESIGN SYSTEM
      ↓
Tokens
      ↓
CSS / Theme Variables

Components
      ↓
Reusable Frontend Components

Variants
      ↓
Component Props / Variants

Responsive Rules
      ↓
Responsive Implementation
```

This mapping helps ensure that the development implementation remains aligned with the approved design system.

## 16.10 Reusability Strategy

The architecture should identify opportunities for practical reuse.

Examples include:

* Shared navigation
* Shared footer
* Reusable buttons
* Reusable cards
* Shared section patterns
* Reusable form controls
* Common layouts
* Shared utility functions

The objective is not to create the maximum possible number of abstractions.

A component should be abstracted when doing so improves consistency, reuse, readability, or maintainability.

## 16.11 State and Data Requirements

Where the website contains dynamic behavior, the architect should identify the relevant state and data requirements.

These may include:

* Form state
* Navigation state
* Modal state
* API data
* Loading state
* Error state
* Authentication state
* Filters
* Search state

For a primarily static marketing website, the architecture should remain correspondingly simple.

## 16.12 External Integrations

Where integrations are required, the architect should identify them and establish their implementation boundaries.

Examples include:

* Contact forms
* Analytics
* CMS
* APIs
* Payment services
* Authentication
* Third-party widgets
* Marketing platforms

The architect should document the integration requirements without unnecessarily implementing them during the architecture stage.

## 16.13 Asset Strategy

The architect should establish how website assets should be organized and consumed.

This may include:

* Images
* Icons
* Fonts
* Logos
* Illustrations
* Videos
* Static assets

Asset handling should support the performance and maintainability requirements of the website.

## 16.14 Responsive Architecture

The architecture should support the responsive behavior defined by the UI/UX Design and Design System stages.

The architect may define:

* Breakpoint strategy
* Responsive component behavior
* Layout behavior
* Mobile navigation architecture
* Responsive image handling
* Responsive typography implementation

Responsive QA remains responsible for validating the final implementation.

## 16.15 Accessibility Architecture

The frontend architecture should support accessible implementation.

Where relevant, this includes:

* Semantic HTML
* Keyboard-accessible components
* Focus management
* Accessible component structures
* Form accessibility
* Appropriate heading hierarchy
* Accessible navigation patterns

The architect should establish implementation expectations without duplicating the Accessibility QA process.

## 16.16 SEO Architecture

The architect should consider technical requirements that affect SEO implementation.

These may include:

* Route structure
* Page metadata support
* Semantic HTML
* Heading structure
* Canonical URL support
* Sitemap requirements
* Robots configuration
* Structured data where applicable

The SEO & Performance Agent remains responsible for validation.

## 16.17 Performance Architecture

Performance considerations should be included in the architecture where relevant.

Examples include:

* Image optimization
* Lazy loading
* Asset loading strategy
* Code splitting where justified
* Font loading
* Dependency management
* Caching considerations

Performance architecture should remain proportional to the project's actual needs.

## 16.18 Environment and Configuration

Where required, the architect should identify project configuration needs.

These may include:

* Environment variables
* Build configuration
* Development configuration
* Production configuration
* API endpoints
* Deployment configuration

Sensitive credentials should not be stored directly in source code or workflow artifacts.

## 16.19 Technical Decisions

Important architectural decisions should be documented.

Examples include:

* Framework choice
* Styling approach
* Component strategy
* Routing approach
* Data-fetching approach
* State-management approach
* Integration strategy
* Hosting assumptions

Significant decisions may also be recorded in:

```text
DECISIONS/
```

This maintains traceability across the project.

## 16.20 Machine-Readable Architecture Artifact

Where defined by the existing Agent 06 specification, the architect should produce a machine-readable architecture artifact.

For example:

```text
frontend-architecture.json
```

The structured artifact should represent the same core architecture decisions documented in the human-readable architecture documentation.

Machine-readable output should be preserved when it provides practical downstream value.

## 16.21 Development Handoff

The primary downstream consumer of the Frontend Architecture is:

```text
07 — Development Agent
```

The handoff is:

```text
UI/UX DESIGN
      ↓
DESIGN SYSTEM
      ↓
FRONTEND ARCHITECTURE
      ↓
DEVELOPMENT
```

Development should receive sufficient information to understand:

* What needs to be built
* How the project should be structured
* Which components should be reusable
* Which technologies should be used
* Which design-system rules must be followed
* Which technical constraints apply
* Which integrations are required

## 16.22 Architecture Review

Before development begins, the architecture should be reviewed for practical completeness.

The review should verify:

* Technology choices are appropriate.
* Project structure is clear.
* Page and route structure is defined.
* Component strategy is practical.
* Design-system mapping is clear.
* Required integrations are identified.
* Responsive requirements are supported.
* Accessibility considerations are supported.
* SEO and performance requirements are considered.
* Important technical decisions are documented.

The review does not require a separate formal approval gate unless the project requires one.

## 16.23 Architecture Changes During Development

Architecture may occasionally need to change after development begins.

The preferred process is:

```text
ARCHITECTURE CHANGE
        ↓
IDENTIFY REASON
        ↓
ASSESS IMPACT
        ↓
UPDATE ARCHITECTURE ARTIFACT
        ↓
DOCUMENT SIGNIFICANT DECISION
        ↓
UPDATE DEVELOPMENT
        ↓
RE-RUN AFFECTED QA
```

A normal implementation adjustment should not automatically trigger a full architecture rewrite.

Only meaningful architectural changes require formal documentation.

## 16.24 What the Frontend Architect Agent Does Not Own

The Frontend Architect Agent should not independently own:

* Business discovery
* UX strategy
* Content strategy
* Visual design
* Design-system definition
* Final source-code implementation
* Responsive QA
* Accessibility QA
* SEO validation
* Production QA
* Deployment approval

Its responsibility is to define **how the approved website should be implemented technically**.

## 16.25 Primary Outputs

The Frontend Architect Agent should produce the artifacts defined by its existing agent specification.

These may include:

* Frontend architecture documentation
* Project structure
* Page and route architecture
* Component architecture
* Technical decisions
* Implementation guidelines
* Integration requirements
* Machine-readable architecture artifact where applicable

The exact artifact filenames should follow the existing Agent 06 specification.

## 16.26 Completion Criteria

Agent 06 is considered complete when:

* The frontend technology approach is established.
* The project structure is defined.
* Page and route architecture is defined.
* Component architecture is established.
* Design-system mapping is clear.
* Reusability requirements are identified.
* Required integrations are documented.
* Responsive requirements are considered.
* Accessibility requirements are considered.
* SEO and performance requirements are considered.
* Important technical decisions are documented.
* Required architecture artifacts are produced.
* Development has sufficient information to begin implementation.

The workflow can then proceed to:

```text
07 — Development Agent
```

## 16.27 Version 1 Principle

The Frontend Architect Agent should remain focused on **creating a practical technical blueprint for implementation**.

It should not introduce architecture that the website does not need.

The guiding principle is:

**Approved Design + Design System + Requirements → Practical Frontend Architecture → Development**

# 17. Agent 07 — Development

The **Development Agent** is the seventh specialized agent in the Agentic Website Factory.

Its purpose is to transform the approved UI/UX design, Design System, Frontend Architecture, content requirements, and project inputs into a functional website implementation.

The Development Agent is responsible for building the website according to the approved project artifacts and technical architecture.

It should prioritize **design fidelity, functional correctness, maintainability, responsiveness, accessibility, and implementation consistency**.

The Development stage produces the working website that will subsequently be evaluated by the specialized QA agents.

---

## 17.1 Objective

The primary objective of the Development Agent is to answer:

* How should the approved website be implemented?
* How should the defined pages and components be built?
* How should the Design System be represented in code?
* How should the approved responsive behavior be implemented?
* How should required interactions and functionality work?
* How should content and assets be integrated?
* How should the implementation remain maintainable and consistent with the architecture?
* Is the resulting website ready for specialized QA?

The Development Agent should transform approved project specifications into a working website without independently changing the intended product direction.

---

## 17.2 Primary Inputs

The Development Agent primarily receives:

* Approved UI/UX Design artifacts
* Approved Design System artifacts
* Design tokens
* Component definitions
* Frontend Architecture artifacts
* UX and Information Architecture artifacts
* Content Strategy artifacts
* Approved website content
* Brand assets
* Images and other media
* Technical requirements
* Integration requirements
* Approved project decisions
* Existing codebase where applicable
* Relevant implementation constraints

The primary workflow relationship is:

```text
04 — UI/UX DESIGN
        ↓
05 — DESIGN SYSTEM
        ↓
06 — FRONTEND ARCHITECTURE
        ↓
07 — DEVELOPMENT
```

The Development Agent should use the latest valid approved artifacts as its implementation source of truth.

---

## 17.3 Core Responsibilities

The Development Agent is responsible for:

1. Setting up or updating the frontend project.
2. Implementing the approved page structure.
3. Implementing reusable frontend components.
4. Implementing the approved Design System.
5. Integrating approved content and assets.
6. Implementing responsive behavior.
7. Implementing required interactions.
8. Implementing required forms and integrations.
9. Implementing accessibility-aware structures.
10. Implementing technical SEO requirements where defined by architecture.
11. Applying performance-conscious implementation practices.
12. Validating the implementation locally before QA.
13. Producing the working website implementation.
14. Documenting important implementation decisions or deviations.

---

## 17.4 Implementation Source of Truth

Development should not treat any single artifact in isolation as the complete implementation specification.

The implementation should be based on the combined approved project foundation:

```text
BUSINESS REQUIREMENTS
        +
UX / INFORMATION ARCHITECTURE
        +
CONTENT STRATEGY
        +
APPROVED UI/UX DESIGN
        +
DESIGN SYSTEM
        +
FRONTEND ARCHITECTURE
        ↓
DEVELOPMENT
```

Where conflicts exist, the Development Agent should identify them rather than silently choosing one source.

Significant conflicts should be resolved through the appropriate project decision or approval process.

---

## 17.5 Project Initialization

Where a project does not yet have an implementation, the Development Agent should initialize the frontend project according to the approved architecture.

This may include:

* Creating the project structure
* Installing required dependencies
* Configuring the selected framework
* Configuring styling
* Configuring routing
* Configuring asset handling
* Configuring build tools
* Configuring development scripts
* Configuring environment handling

The agent should not introduce unnecessary dependencies or tooling.

---

## 17.6 Existing Project Integration

Where an existing website or codebase is provided, the Development Agent should first understand the existing implementation.

This may include:

* Existing project structure
* Existing components
* Existing styling
* Existing dependencies
* Existing routes
* Existing integrations
* Existing configuration
* Existing technical limitations

The agent should reuse suitable existing implementation where practical rather than unnecessarily rebuilding the entire website.

---

## 17.7 Page Implementation

The Development Agent should implement the pages defined by the approved UX and architecture.

For example:

```text
Website
├── Home
├── About
├── Services
├── Service Detail
├── Projects
├── Project Detail
├── Contact
└── Other Approved Pages
```

The exact page structure depends on the project.

Development should not independently add major pages or remove approved pages without documenting the change.

---

## 17.8 Component Implementation

The Development Agent should implement reusable components according to the Frontend Architecture and Design System.

Examples may include:

```text
Global
├── Header
├── Navigation
├── Footer
└── Button

Content
├── Hero
├── SectionHeader
├── Card
├── FeatureBlock
└── Testimonial

Forms
├── Input
├── Select
├── Textarea
└── Form

Page-specific
├── Home Sections
├── Service Sections
└── Project Sections
```

The exact component structure depends on the project.

Development should avoid unnecessary duplication when a reusable component is appropriate.

---

## 17.9 Design System Implementation

The approved Design System should be implemented consistently.

This may include:

* Colors
* Typography
* Spacing
* Borders
* Radius
* Shadows
* Breakpoints
* Component variants
* Component states
* Responsive rules

Where machine-readable design-system artifacts exist, they should be used where technically practical.

For example:

```text
design-system.tokens.json
        ↓
Frontend Theme / CSS Variables

design-system.components.json
        ↓
Reusable Components
```

The implementation should remain aligned with the approved design system.

---

## 17.10 Design Fidelity

The Development Agent should aim for high fidelity to the approved UI/UX design.

This includes:

* Layout
* Spacing
* Typography
* Colors
* Component proportions
* Imagery
* Visual hierarchy
* Interaction behavior
* Responsive behavior

Where implementation limitations prevent exact reproduction, the difference should be identified and documented when materially significant.

Development should not silently redesign approved interfaces.

---

## 17.11 Content Integration

Approved content should be integrated according to the Content Strategy and UI/UX Design.

The implementation should account for realistic content lengths.

The agent should avoid relying exclusively on placeholder content when actual approved content is available.

Where content is unavailable, clearly identified placeholders may be used temporarily.

Placeholder content should not be mistaken for final production content.

---

## 17.12 Asset Integration

The Development Agent should integrate approved project assets.

These may include:

* Logos
* Images
* Icons
* Illustrations
* Videos
* Fonts
* Other media

Assets should be organized according to the Frontend Architecture.

Where possible, assets should be optimized appropriately for web delivery.

---

## 17.13 Responsive Implementation

Responsive behavior defined by the UI/UX Design, Design System, and Frontend Architecture should be implemented.

The implementation should account for:

* Desktop
* Tablet
* Mobile
* Intermediate viewport sizes
* Navigation changes
* Content stacking
* Responsive typography
* Responsive spacing
* Image behavior
* Component transformations

Responsive implementation should not be limited to checking only one desktop and one mobile viewport.

Detailed validation is performed later by the Responsive QA Agent.

---

## 17.14 Interaction Implementation

The Development Agent should implement the interactions defined by the approved design.

These may include:

* Navigation menus
* Dropdowns
* Accordions
* Tabs
* Modals
* Forms
* Buttons
* Carousels
* Hover states
* Focus states
* Loading states
* Error states
* Success states

Interactions should remain consistent with the approved UX and Design System.

The agent should avoid introducing unnecessary animation or interaction complexity.

---

## 17.15 Form Implementation

Where forms are required, the Development Agent should implement the defined form behavior.

This may include:

* Field structure
* Validation
* Error states
* Success states
* Loading states
* Submission handling
* API integration
* Third-party integration
* User feedback

Forms should be implemented in an accessibility-conscious manner.

Sensitive information should be handled according to the project's approved technical requirements.

---

## 17.16 Integration Implementation

Where external integrations are required, the Development Agent should implement them according to the Frontend Architecture.

Examples include:

* Contact form services
* Analytics
* APIs
* CMS
* Authentication
* Payment services
* Marketing tools
* Third-party widgets

The agent should not introduce an external integration that has not been approved or documented.

---

## 17.17 Accessibility-Aware Development

The Development Agent should implement the website in a manner that supports accessibility validation.

Where applicable, this includes:

* Semantic HTML
* Correct heading hierarchy
* Keyboard accessibility
* Accessible navigation
* Form labels
* Focus states
* Meaningful button and link labels
* Appropriate alternative text
* Accessible interactive components
* Appropriate ARIA usage where necessary

ARIA should not be used as a substitute for proper semantic HTML when semantic HTML is sufficient.

Final accessibility validation remains the responsibility of the Accessibility QA stage.

---

## 17.18 SEO Implementation

The Development Agent should implement the technical SEO requirements established by the project architecture and SEO strategy.

This may include:

* Page titles
* Meta descriptions
* Heading hierarchy
* Semantic HTML
* Canonical URLs
* Open Graph metadata
* Structured data where required
* Sitemap support
* Robots configuration
* SEO-friendly routes

The Development Agent implements the defined requirements.

The dedicated SEO & Performance QA Agent validates the final implementation.

---

## 17.19 Performance-Aware Development

Development should consider website performance from the beginning.

Relevant practices may include:

* Image optimization
* Appropriate image formats
* Lazy loading where appropriate
* Efficient asset loading
* Avoiding unnecessary dependencies
* Minimizing unnecessary JavaScript
* Efficient component rendering
* Appropriate font loading
* Code splitting where justified

Performance optimization should remain proportional to the actual project.

The objective is not to optimize blindly but to avoid introducing preventable performance problems.

---

## 17.20 Code Quality

The Development Agent should produce maintainable implementation.

Code should aim for:

* Clear structure
* Consistent naming
* Reusable components
* Appropriate separation of concerns
* Minimal unnecessary duplication
* Understandable logic
* Reasonable documentation
* Consistent formatting
* Maintainable configuration

The agent should avoid unnecessary abstraction or over-engineering.

---

## 17.21 Error Handling

The implementation should account for expected failure conditions where applicable.

These may include:

* Failed API requests
* Form submission errors
* Invalid user input
* Missing data
* Loading failures
* Empty states
* Integration failures

The interface should provide an understandable user experience rather than failing silently.

---

## 17.22 Environment and Secrets

The Development Agent should follow the environment and configuration rules established by the Frontend Architecture.

Sensitive values such as:

* API keys
* Passwords
* Authentication tokens
* Private credentials
* Secret configuration

must not be committed directly into source code or public repositories.

Environment variables or approved secret-management mechanisms should be used where required.

---

## 17.23 Local Validation Before QA

Before handing the implementation to QA, the Development Agent should perform basic validation.

This should include, where applicable:

* Application starts successfully.
* Build completes successfully.
* Routes load correctly.
* Major pages render.
* Major interactions work.
* No obvious console errors remain.
* Required assets load.
* Forms behave as expected.
* Responsive behavior is broadly functional.
* Required integrations are operational or appropriately stubbed.

This is an implementation readiness check.

It does not replace the specialized QA stages.

---

## 17.24 Development Handoff to QA

The Development Agent hands the working website to the QA stages.

The conceptual relationship is:

```text
DEVELOPMENT
      ↓
WORKING WEBSITE
      ↓
08 — RESPONSIVE QA
      ↓
09 — ACCESSIBILITY QA
      ↓
10 — SEO & PERFORMANCE QA
      ↓
11 — PRODUCTION QA
```

The actual QA execution and rework relationships are governed by the workflow orchestration defined elsewhere in the factory.

---

## 17.25 QA Rework Loop

Development is not necessarily complete after the first implementation.

QA findings may require development changes.

The preferred model is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
        ↓
10 — SEO & PERFORMANCE QA
        ↓
11 — PRODUCTION QA
        ↓
FINDING
        ↓
AFFECTED AGENT / DEVELOPMENT
        ↓
REWORK
        ↓
AFFECTED QA STAGE
        ↓
RE-VALIDATION
```

The Development Agent should address valid findings and avoid treating QA as a one-time handoff.

---

## 17.26 Handling Design or Architecture Conflicts

If the Development Agent discovers a conflict between:

* UI/UX Design
* Design System
* Frontend Architecture
* Content
* Technical constraints

it should not silently choose a solution when the conflict materially affects the approved outcome.

The preferred process is:

```text
CONFLICT IDENTIFIED
        ↓
DOCUMENT ISSUE
        ↓
ASSESS IMPACT
        ↓
REQUEST / RECORD DECISION
        ↓
UPDATE AFFECTED ARTIFACTS
        ↓
CONTINUE DEVELOPMENT
```

Minor implementation decisions may be resolved within the development stage when they do not materially change the approved experience.

---

## 17.27 Development Decisions

Important implementation decisions should be documented.

Examples include:

* Deviations from architecture
* Significant component restructuring
* Technology limitations
* Integration workarounds
* Major performance decisions
* Significant design implementation compromises

Significant decisions may also be recorded in:

```text
DECISIONS/
```

This preserves project traceability.

---

## 17.28 Development Scope Control

The Development Agent should implement the approved project scope.

It should not independently introduce:

* New major features
* New business requirements
* New pages
* Major visual redesigns
* New integrations
* Significant architecture changes

unless those changes are approved or documented through the appropriate decision process.

This protects the factory from uncontrolled scope expansion during implementation.

---

## 17.29 Primary Outputs

The Development Agent should produce the working website implementation defined by the project.

Outputs may include:
```text
07-development/
├── development-status.md
├── implementation-changelog.md
├── implementation-notes.md
└── development-qa.md

WEBSITE/
└── [frontend source tree]
```
The primary implementation output is:

```text
WEBSITE/
```

The exact internal structure should follow the approved Frontend Architecture.

---

## 17.30 Development Output Quality Check

Before the Development stage is considered ready for QA, the implementation should be checked for:

* Successful application startup
* Successful production build
* Correct page structure
* Correct routing
* Design-system consistency
* Responsive implementation
* Functional interactions
* Content integration
* Asset integration
* Basic accessibility implementation
* Basic SEO implementation
* Performance-conscious implementation
* No obvious blocking errors
* Required integrations implemented or clearly identified
* No major unexplained deviations from approved design

---

## 17.31 Handoff Requirements

The Development Agent should make the following available to the QA stages:

```text
WORKING WEBSITE
      +
SOURCE CODE
      +
RELEVANT CONFIGURATION
      +
APPROVED DESIGN REFERENCES
      +
DESIGN SYSTEM
      +
KNOWN LIMITATIONS
      +
IMPLEMENTATION NOTES
```

Known limitations should be explicitly communicated rather than hidden from QA.

---

## 17.32 Downstream Impact

Development changes can affect:

* Responsive QA
* Accessibility QA
* SEO & Performance QA
* Production QA
* Release readiness

For example:

```text
Development Change
        ↓
Responsive Behavior
        ↓
Accessibility
        ↓
SEO / Performance
        ↓
Production Validation
```

Therefore, meaningful development changes after QA has started may require affected QA stages to be re-run.

---

## 17.33 What the Development Agent Does Not Own

The Development Agent should not independently own:

* Business discovery
* UX strategy
* Content strategy
* Final visual design
* Design-system governance
* Frontend architecture decisions outside its defined implementation scope
* Final responsive QA
* Final accessibility QA
* Final SEO validation
* Final production QA
* Human release approval
* Production deployment approval

Its responsibility is to **build the approved website correctly**.

---

## 17.34 Completion Criteria

Agent 07 is considered complete when:

* The approved website structure has been implemented.
* Required pages are implemented.
* Reusable components are implemented.
* The Design System is represented consistently in code.
* Approved content and assets are integrated.
* Responsive behavior is implemented.
* Required interactions are implemented.
* Required integrations are implemented.
* Accessibility-aware implementation is in place.
* Technical SEO requirements are implemented where applicable.
* Performance-conscious implementation practices are applied.
* The application builds successfully.
* Basic implementation validation has been completed.
* Known limitations are documented.
* The working website is ready for specialized QA.

The workflow can then proceed to:

```text
08 — Responsive QA Agent
```

---

## 17.35 Version 1 Principle

The Development Agent should remain focused on **turning approved project artifacts into a working website**.

It should not redesign the project, redefine business requirements, or introduce unnecessary technical complexity during implementation.

The guiding principle is:

**Approved Design + Design System + Architecture + Content → Working Website → Specialized QA**
# 18. Agent 08 — Responsive QA

The **Responsive QA Agent** is the eighth specialized agent in the Agentic Website Factory.

Its purpose is to validate that the implemented website behaves correctly across the required viewport sizes and devices while remaining faithful to the approved UI/UX design, Design System, UX requirements, and responsive expectations.

The Responsive QA Agent focuses specifically on **responsive behavior, layout integrity, visual consistency, and usability across screen sizes**.

Its findings are used to route valid issues back to the Development stage for correction.

---

## 18.1 Objective

The primary objective of the Responsive QA Agent is to answer:

* Does the website work correctly across required screen sizes?
* Does the implementation remain consistent with the approved responsive design?
* Do layouts adapt correctly?
* Does navigation behave correctly on smaller screens?
* Does content remain readable and usable?
* Are components behaving correctly across viewport sizes?
* Are there overflow, clipping, spacing, or alignment problems?
* Are responsive breakpoints behaving as intended?
* Are mobile, tablet, and desktop experiences usable?

The objective is not merely to confirm that the website technically fits on a screen.

The objective is to verify that the website provides an appropriate experience across supported viewport sizes.

---

## 18.2 Primary Inputs

The Responsive QA Agent primarily receives:

* Working website implementation
* UI/UX Design artifacts
* Responsive design specifications
* Design System artifacts
* Frontend Architecture artifacts
* UX requirements
* Approved content
* Relevant design references
* Existing implementation notes
* Known development limitations

The primary workflow relationship is:

```text
04 — UI/UX DESIGN
        ↓
05 — DESIGN SYSTEM
        ↓
06 — FRONTEND ARCHITECTURE
        ↓
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
```

The QA Agent should validate the latest available implementation against the latest valid approved artifacts.

---

## 18.3 Core Responsibilities

The Responsive QA Agent is responsible for:

1. Testing the website across defined viewport sizes.
2. Validating responsive layouts.
3. Validating responsive navigation.
4. Checking typography behavior.
5. Checking spacing and alignment.
6. Checking image and media behavior.
7. Checking component transformations.
8. Identifying overflow and clipping issues.
9. Validating responsive interactions.
10. Comparing implementation against approved responsive design.
11. Recording responsive defects.
12. Prioritizing findings according to severity.
13. Producing the required Responsive QA artifacts.
14. Routing valid findings back to Development for rework.

---

## 18.4 Responsive QA Scope

Responsive QA should evaluate the complete website experience across relevant screen sizes.

The scope may include:

* Desktop
* Laptop
* Tablet
* Mobile
* Intermediate viewport sizes

The exact viewport matrix should be determined according to project requirements.

The QA process should not assume that testing only one desktop and one mobile size is sufficient.

---

## 18.5 Viewport Testing

The agent should test representative viewport sizes.

A project may define a matrix such as:

```text
Desktop
1440px
1280px

Tablet
1024px
768px

Mobile
430px
390px
375px
320px
```

The exact values may vary depending on the project.

The purpose is to identify responsive failures between predefined breakpoints as well as at common device widths.

---

## 18.6 Layout Validation

The agent should verify that layouts adapt correctly across viewport sizes.

This includes checking:

* Containers
* Grids
* Columns
* Sections
* Cards
* Forms
* Navigation
* Footer
* Content alignment
* Vertical spacing
* Horizontal spacing

The agent should identify situations where layouts become visually broken or unusable.

---

## 18.7 Horizontal Overflow

Horizontal overflow is an important responsive defect.

The agent should check for:

* Unexpected horizontal scrolling
* Elements extending outside the viewport
* Fixed-width components
* Oversized images
* Long text breaking layouts
* Tables exceeding viewport width
* Navigation overflow
* Components with inappropriate minimum widths

Where horizontal scrolling is intentionally required, it should not automatically be treated as a defect.

The expected behavior should be considered.

---

## 18.8 Typography Validation

Typography should remain usable across viewport sizes.

The agent should check:

* Heading sizes
* Body text sizes
* Line heights
* Text wrapping
* Text overflow
* Long headings
* Button labels
* Navigation labels
* Paragraph widths

The objective is to ensure that typography remains readable and visually appropriate.

---

## 18.9 Content Validation

Responsive QA should test realistic content rather than relying exclusively on idealized placeholder content.

The agent should look for:

* Text wrapping problems
* Unexpected content expansion
* Truncated content
* Overlapping elements
* Long labels
* Long service names
* Long button text
* Missing content caused by responsive rules

Responsive layouts should remain usable when real content is longer than expected.

---

## 18.10 Image and Media Validation

Images and other media should behave correctly across viewport sizes.

The agent should check:

* Image scaling
* Aspect ratio
* Cropping
* Object positioning
* Responsive sizing
* Loading behavior
* Image overflow
* Video behavior where applicable

Images should not unexpectedly distort or break the surrounding layout.

---

## 18.11 Navigation Validation

Responsive navigation should be specifically tested.

This may include:

```text
Desktop Navigation
        ↓
Tablet Navigation
        ↓
Mobile Navigation
```

The agent should verify:

* Menu visibility
* Menu opening and closing
* Mobile navigation behavior
* Touch usability
* Navigation item wrapping
* Dropdown behavior
* Menu overlays
* Menu scrolling where required

Navigation should remain usable across supported viewport sizes.

---

## 18.12 Component Responsiveness

Reusable components should be tested across the responsive range.

Examples include:

* Buttons
* Cards
* Forms
* Hero sections
* Testimonials
* Feature sections
* Navigation
* Modals
* Accordions
* Tables
* Galleries

The agent should verify that components transform according to the approved responsive rules.

---

## 18.13 Responsive Interaction Testing

Responsive QA should validate interactions that change across viewport sizes.

Examples include:

* Mobile menu
* Accordion
* Tabs
* Carousel
* Modal
* Form interactions
* Dropdowns
* Sticky elements

The agent should verify that interactions remain usable with different input methods where relevant.

---

## 18.14 Touch Usability

Where the website is intended for mobile or touch devices, the agent should consider:

* Interactive target sizes
* Spacing between controls
* Touch-friendly navigation
* Swipe interactions where applicable
* Accidental interaction risks

The objective is to ensure that the mobile interface is practically usable rather than simply visually scaled down.

---

## 18.15 Responsive Visual Comparison

Where approved design references are available, the implementation should be compared against them.

The comparison may evaluate:

* Layout
* Spacing
* Typography
* Component behavior
* Visual hierarchy
* Responsive transformations
* Navigation
* Content placement

The objective is not pixel-perfect comparison at every possible viewport.

The objective is to identify meaningful deviations from the approved responsive design.

---

## 18.16 Breakpoint Validation

The agent should test behavior around defined breakpoints.

For example:

```text
BEFORE BREAKPOINT
        ↓
BREAKPOINT
        ↓
AFTER BREAKPOINT
```

This helps identify issues that may not appear at standard device widths.

Examples include:

* Components jumping unexpectedly
* Navigation breaking
* Incorrect grid transitions
* Typography changing incorrectly
* Content becoming clipped

---

## 18.17 Accessibility-Aware Responsive Checks

Although dedicated Accessibility QA is handled by Agent 09, Responsive QA should identify responsive issues that affect accessibility or usability.

Examples include:

* Hidden content that becomes inaccessible
* Mobile controls that cannot be reached
* Focused elements moving unexpectedly
* Content becoming unreadable
* Interactive elements becoming too small
* Keyboard focus problems caused by responsive layout changes

These findings should be documented and routed appropriately.

---

## 18.18 SEO and Performance Awareness

Responsive QA may identify issues that have obvious SEO or performance implications.

Examples include:

* Mobile-specific content disappearing incorrectly
* Excessive mobile asset loading
* Oversized images
* Layout instability
* Responsive rendering failures

The Responsive QA Agent should identify the issue but should not replace the dedicated SEO & Performance QA stage.

---

## 18.19 Severity Classification

Responsive findings should be classified according to their impact.

A practical classification may be:

```text
CRITICAL
Prevents meaningful use of the website.

HIGH
Major responsive defect affecting important functionality or content.

MEDIUM
Noticeable responsive problem affecting usability or visual quality.

LOW
Minor visual inconsistency with limited user impact.
```

Severity should reflect actual user and business impact rather than the visual prominence of the defect alone.

---

## 18.20 QA Finding Structure

Each responsive QA finding should contain sufficient information for Development to reproduce and resolve the issue.

A finding may include:

```text
Issue ID
Severity
Page
Viewport
Component / Area
Description
Expected Behavior
Actual Behavior
Reproduction Steps
Evidence
Recommended Direction
Status
```

The exact structure should follow the project's existing QA artifact specification.

---

## 18.21 Evidence

Where practical, responsive findings should include evidence.

Evidence may include:

* Screenshots
* Screen recordings
* Browser information
* Viewport dimensions
* Reproduction steps
* Relevant implementation details

Evidence should make the issue understandable without requiring repeated investigation.

---

## 18.22 Machine-Readable QA Artifact

Where defined by the existing Responsive QA Agent specification, the agent should produce a machine-readable artifact.

For example:

```text
responsive-qa.json
```

The structured artifact may contain:

* Test results
* Viewports tested
* Findings
* Severity
* Page references
* Component references
* Status
* Rework requirements

Machine-readable output should remain consistent with the human-readable QA report.

---

## 18.23 Human-Readable QA Report

The Responsive QA Agent should also produce a human-readable report where required.

The report should summarize:

* Scope tested
* Viewports tested
* Pages tested
* Major findings
* Severity distribution
* Rework requirements
* Validation status
* Remaining issues

The report should be concise enough to support practical project decisions.

---

## 18.24 Pass / Fail Decision

The Responsive QA stage should determine whether the implementation is ready to proceed.

A conceptual outcome may be:

```text
PASS
   ↓
09 — ACCESSIBILITY QA
```

or:

```text
FAIL
   ↓
REWORK REQUIRED
   ↓
07 — DEVELOPMENT
   ↓
08 — RESPONSIVE QA
```

A stage should not be considered passed merely because some tests succeeded.

Blocking responsive issues must be resolved or explicitly accepted according to the project's approval rules.

---

## 18.25 QA Rework Loop

Responsive QA is part of a controlled rework loop.

The preferred process is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
FINDINGS
        ↓
REWORK REQUIRED
        ↓
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
```

Only affected areas should be re-tested where practical.

A complete responsive regression test should still be performed when changes are broad or high-risk.

---

## 18.26 Defect Ownership

The Responsive QA Agent identifies and documents defects.

The Development Agent is responsible for correcting implementation defects.

The process is:

```text
QA
 ↓
IDENTIFY DEFECT
 ↓
DOCUMENT DEFECT
 ↓
DEVELOPMENT
 ↓
FIX
 ↓
QA RE-VALIDATION
```

QA should not silently modify production implementation as part of the normal workflow.

---

## 18.27 Handling Design vs Implementation Differences

Not every difference between design and implementation is automatically a defect.

The QA Agent should consider:

* Approved design intent
* Responsive requirements
* Technical constraints
* Accessibility requirements
* User experience
* Project decisions

If a meaningful difference is intentional and documented, it should not be incorrectly reported as an implementation defect.

If the reason is unclear, the issue should be flagged for clarification.

---

## 18.28 Regression Considerations

A responsive fix can affect other viewport sizes.

For example:

```text
Mobile Fix
    ↓
Tablet Layout
    ↓
Desktop Layout
```

Therefore, fixes should be re-tested across affected viewport ranges.

The objective is to prevent one responsive correction from creating another responsive defect.

---

## 18.29 Primary Outputs

The Responsive QA Agent should produce the artifacts defined by its existing specification.

These may include:

* Responsive QA report
* Responsive test results
* Responsive findings
* Screenshots or evidence
* Machine-readable QA artifact
* Rework requirements
* Final responsive validation status

Where applicable:

```text
responsive-qa.json
```

should be maintained as the machine-readable source for responsive QA results.

---

## 18.30 Output Quality Check

Before the Responsive QA stage is considered complete, the outputs should be checked for:

* Required viewports tested
* Required pages tested
* Major responsive layouts validated
* Navigation validated
* Important components validated
* Overflow checked
* Typography checked
* Images and media checked
* Important interactions checked
* Findings documented clearly
* Severity assigned appropriately
* Evidence provided where useful
* Rework requirements clearly identified
* Final status recorded

---

## 18.31 Handoff to Agent 09

When Responsive QA passes, the primary downstream consumer is:

```text
09 — Accessibility QA Agent
```

The workflow becomes:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
RESPONSIVE QA PASS
        ↓
09 — ACCESSIBILITY QA
```

If responsive QA fails:

```text
08 — RESPONSIVE QA
        ↓
REWORK REQUIRED
        ↓
07 — DEVELOPMENT
```

---

## 18.32 Downstream Impact

Responsive defects may affect:

* Accessibility
* SEO
* Performance
* Production QA
* Final release readiness

For example:

```text
Responsive Defect
        ↓
Development Fix
        ↓
Accessibility Revalidation
        ↓
SEO / Performance Revalidation
        ↓
Production QA
```

The workflow should re-run only the affected validation stages where practical.

---

## 18.33 What the Responsive QA Agent Does Not Own

The Responsive QA Agent should not independently own:

* Business requirements
* UX strategy
* Content strategy
* Visual design
* Design-system definition
* Frontend architecture
* Source-code implementation
* Final accessibility validation
* Final SEO validation
* Final production QA
* Deployment approval

Its responsibility is to **validate responsive behavior and identify responsive defects**.

---

## 18.34 Completion Criteria

Agent 08 is considered complete when:

* Required viewport sizes have been tested.
* Required pages have been evaluated.
* Responsive layouts have been validated.
* Navigation has been tested across relevant screen sizes.
* Typography and content behavior have been checked.
* Images and media have been checked.
* Important responsive interactions have been tested.
* Overflow and clipping issues have been evaluated.
* Findings have been documented.
* Findings have been assigned appropriate severity.
* Required responsive defects have been resolved or explicitly accepted.
* Rework has been re-validated where required.
* The Responsive QA result has been recorded.
* The implementation is ready for Accessibility QA.

The workflow can then proceed to:

```text
09 — Accessibility QA Agent
```

---

## 18.35 Version 1 Principle

The Responsive QA Agent should remain focused on **proving that the website works across supported screen sizes and devices**.

It should not redesign the website or directly own implementation fixes.

The guiding principle is:

**Test the implemented experience across viewports → Identify responsive defects → Route rework → Re-test → Confirm responsive readiness**

# 19. Agent 09 — Accessibility QA

The **Accessibility QA Agent** is the ninth specialized agent in the Agentic Website Factory.

Its purpose is to evaluate the implemented website against relevant accessibility requirements and identify issues that may prevent users with different abilities, devices, or interaction methods from effectively using the website.

The Accessibility QA stage validates the **implemented website**, not merely the design or architecture documentation.

Its findings are used to drive corrective work in Development and, where necessary, upstream review.

## 19.1 Objective

The primary objective of the Accessibility QA Agent is to answer:

* Can users access and navigate the website effectively?
* Is the interface usable with keyboard interaction?
* Is the semantic structure appropriate?
* Are interactive elements accessible?
* Are forms understandable and usable?
* Are important states communicated appropriately?
* Are images and other media handled appropriately?
* Does the implementation provide a reasonable accessibility foundation?
* Which accessibility issues must be corrected before release?

The objective is to identify meaningful accessibility problems and provide actionable findings for remediation.

## 19.2 Primary Inputs

The Accessibility QA Agent primarily receives:

* Implemented website from `WEBSITE/`
* Approved UI/UX design artifacts
* Design System artifacts
* Frontend Architecture artifacts
* UX and Information Architecture artifacts
* Content implementation
* Existing development documentation
* Relevant accessibility requirements
* Previous QA findings where applicable
* Approved project decisions

The primary workflow relationship is:

```text
06 — FRONTEND ARCHITECTURE
        ↓
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
```

The Accessibility QA Agent should validate the latest available implementation.

## 19.3 Core Responsibilities

The Accessibility QA Agent is responsible for:

1. Evaluating semantic structure.
2. Evaluating keyboard accessibility.
3. Evaluating focus behavior.
4. Evaluating navigation accessibility.
5. Evaluating forms and form feedback.
6. Evaluating interactive components.
7. Evaluating images and alternative text.
8. Evaluating heading and content structure.
9. Evaluating color and visual accessibility where applicable.
10. Evaluating accessible states and feedback.
11. Identifying accessibility defects.
12. Classifying the severity and impact of findings.
13. Producing structured accessibility QA artifacts.
14. Supporting Development in resolving identified issues.
15. Re-validating corrected issues where required.

## 19.4 Accessibility QA Philosophy

Accessibility should be treated as a quality requirement throughout the factory rather than as a final checklist.

Accessibility considerations are introduced during:

```text
UX
 ↓
UI/UX DESIGN
 ↓
DESIGN SYSTEM
 ↓
FRONTEND ARCHITECTURE
 ↓
DEVELOPMENT
 ↓
ACCESSIBILITY QA
```

The Accessibility QA stage provides the formal validation layer.

The QA Agent should validate the actual implementation rather than assuming that accessibility requirements were correctly implemented because they were documented upstream.

## 19.5 Scope of Validation

The Accessibility QA Agent should evaluate the areas relevant to the project.

These may include:

* Semantic HTML
* Heading hierarchy
* Keyboard navigation
* Focus management
* Interactive controls
* Navigation
* Forms
* Labels
* Error messages
* Images
* Links
* Buttons
* Color contrast
* Text readability
* Responsive accessibility
* Dynamic content
* Status messages
* Modals and overlays
* Accessible states

The scope should be proportional to the actual website.

## 19.6 Semantic Structure

The agent should evaluate whether the implementation uses appropriate semantic structures.

Examples include:

* Appropriate headings
* Semantic landmarks
* Appropriate navigation elements
* Appropriate buttons and links
* Meaningful lists
* Form semantics
* Appropriate document structure

The objective is to determine whether the underlying structure communicates the intended meaning to users and assistive technologies.

## 19.7 Heading Hierarchy

The agent should review heading structure across important pages.

The validation should consider:

* Presence of an appropriate primary heading
* Logical heading progression
* Meaningful section headings
* Avoidance of heading misuse for purely visual styling

The heading structure should reflect the information hierarchy defined by UX and Content Strategy.

## 19.8 Keyboard Accessibility

The agent should verify that important website functionality can be accessed using keyboard interaction.

This may include:

* Navigation
* Links
* Buttons
* Forms
* Menus
* Accordions
* Tabs
* Modals
* Interactive controls

The agent should identify:

* Keyboard traps
* Inaccessible controls
* Unexpected focus behavior
* Missing keyboard interactions
* Incorrect interaction order

Keyboard accessibility should be evaluated against the actual implemented experience.

## 19.9 Focus Management

The agent should evaluate whether focus is visible and behaves appropriately.

Relevant considerations include:

* Visible focus indication
* Logical focus order
* Focus movement after opening interfaces
* Focus behavior in modals
* Focus behavior after closing interactive elements
* Avoiding unexpected focus loss

Focus behavior should support users navigating without a mouse.

## 19.10 Navigation Accessibility

The agent should evaluate whether the website navigation is accessible.

This may include:

* Primary navigation
* Mobile navigation
* Dropdown menus
* Menu controls
* Footer navigation
* Skip-navigation mechanisms where appropriate

The navigation should remain understandable and usable across supported interaction methods.

## 19.11 Interactive Elements

Interactive elements should be evaluated for appropriate semantics and behavior.

Examples include:

```text
Buttons
Links
Menus
Tabs
Accordions
Dialogs
Forms
Carousels
Custom Controls
```

The agent should identify cases where:

* A non-interactive element is incorrectly used as a control.
* A control lacks an accessible name.
* Keyboard interaction is missing.
* State information is not communicated.
* Interaction behavior is inconsistent.

The objective is reliable and understandable interaction.

## 19.12 Forms and Validation

Forms should receive particular attention because inaccessible forms can prevent users from completing important business actions.

The agent should evaluate:

* Field labels
* Required-field communication
* Input instructions
* Error identification
* Error messaging
* Validation feedback
* Keyboard interaction
* Focus behavior
* Success feedback
* Appropriate control semantics

For example:

```text
FORM
 ↓
USER INPUT
 ↓
VALIDATION
 ↓
ERROR / SUCCESS
 ↓
CLEAR USER FEEDBACK
```

Important form errors should be understandable and actionable.

## 19.13 Images and Alternative Text

The agent should review images and other visual content for appropriate accessibility treatment.

This may include:

* Meaningful alternative text
* Empty alternative text for decorative images where appropriate
* Avoiding unnecessary repetition
* Informative image descriptions where required

The correct treatment depends on the purpose of the image.

Decorative imagery should not create unnecessary noise for assistive-technology users.

## 19.14 Links and Buttons

The agent should evaluate whether links and buttons are used appropriately.

Examples:

```text
Link
→ Navigation to another location.

Button
→ Performs an action.
```

The agent should identify:

* Ambiguous link text
* Empty controls
* Missing accessible names
* Incorrect semantic usage
* Inconsistent interaction behavior

Controls should communicate their purpose clearly.

## 19.15 Color and Visual Accessibility

Where applicable, the agent should evaluate visual accessibility considerations.

This may include:

* Text contrast
* Interactive-state contrast
* Error-state visibility
* Success-state visibility
* Focus visibility
* Information conveyed only through color

The agent should not assume that color alone communicates meaning.

Where color is part of the design system, validation should consider the approved design tokens and actual rendered implementation.

## 19.16 Responsive Accessibility

Accessibility should also be considered across supported viewport sizes.

The agent should verify that accessibility does not degrade when the website changes layout.

Examples include:

* Mobile navigation
* Stacked forms
* Responsive controls
* Touch interactions
* Hidden or collapsed content
* Mobile menus
* Responsive dialogs

A website should remain usable across supported screen sizes and interaction methods.

## 19.17 Dynamic Content and State Changes

Where the website contains dynamic behavior, the agent should evaluate whether important state changes are communicated appropriately.

Examples include:

```text
Loading
Error
Success
Expanded
Collapsed
Selected
Disabled
Updated
```

Users should be able to understand meaningful state changes without relying exclusively on visual animation.

## 19.18 Accessibility Tools

The Accessibility QA Agent may use appropriate automated and manual validation tools.

These may include:

* Browser accessibility tools
* Automated accessibility scanners
* Lighthouse
* axe or similar tooling
* Keyboard-only testing
* Screen-reader testing where appropriate
* Manual inspection

Automated tools should support, not replace, manual accessibility evaluation.

No automated accessibility tool can identify every meaningful accessibility issue.

## 19.19 Manual Validation

Manual testing should be performed where automated checks are insufficient.

Important manual checks may include:

* Keyboard-only navigation
* Focus visibility
* Form interaction
* Menu interaction
* Dialog behavior
* Interactive component behavior
* Reading order
* User feedback
* Mobile interaction

The extent of manual testing should be proportional to project scope and risk.

## 19.20 Accessibility Findings

Each significant finding should be documented clearly.

A finding should ideally contain:

```text
Issue
Location
Description
Impact
Severity
Expected Behavior
Observed Behavior
Recommended Fix
Status
```

For example:

```text
Issue:
Mobile navigation button has no accessible name.

Impact:
Users relying on assistive technologies may not understand the purpose of the control.

Severity:
High

Recommended Fix:
Provide an accessible name that clearly identifies the navigation control.
```

Findings should be actionable rather than merely stating that something is "not accessible."

## 19.21 Severity Classification

Accessibility findings should be classified according to practical impact.

A suggested model is:

```text
CRITICAL
Prevents essential interaction or access.

HIGH
Significantly affects important functionality or user journeys.

MEDIUM
Creates meaningful usability or accessibility difficulty.

LOW
Minor issue with limited impact.

INFO
Observation or improvement recommendation.
```

The exact classification may be adapted to project requirements.

## 19.22 Accessibility QA Artifact

The Accessibility QA Agent should produce a structured QA artifact containing:

* Validation scope
* Tests performed
* Findings
* Severity
* Affected pages or components
* Recommended remediation
* Validation status
* Outstanding issues

Where the existing Agent 09 specification defines a specific filename or machine-readable format, that specification should be followed.

The artifact should provide enough information for Development to reproduce and resolve the issues.

## 19.23 Machine-Readable QA Results

Where practical, accessibility findings may also be represented in machine-readable form.

For example:

```text
accessibility-qa.json
```

A structured artifact may contain information such as:

```text
{
  "status": "rework_required",
  "issues": [
    {
      "severity": "high",
      "component": "Mobile Navigation",
      "issue": "Missing accessible name"
    }
  ]
}
```

The exact schema should follow the project's existing QA artifact definition.

Machine-readable output should remain consistent with the human-readable QA report.

## 19.24 Pass / Rework Decision

The Accessibility QA stage should produce a clear outcome.

A conceptual model is:

```text
ACCESSIBILITY QA
       ↓
   VALIDATION
       ↓
 ┌─────┴─────┐
 ↓           ↓
PASS      REWORK REQUIRED
             ↓
       DEVELOPMENT
             ↓
       RE-VALIDATION
```

The website should not be treated as fully QA-complete while unresolved release-blocking accessibility issues remain.

## 19.25 QA Rework Loop

When accessibility defects are identified, the Development Agent should correct the implementation.

The preferred workflow is:

```text
09 — ACCESSIBILITY QA
        ↓
ACCESSIBILITY FINDINGS
        ↓
07 — DEVELOPMENT
        ↓
CORRECTION
        ↓
09 — ACCESSIBILITY QA
        ↓
RE-VALIDATION
```

The entire factory should not automatically restart.

Only the affected implementation should be corrected and re-tested.

## 19.26 Upstream Design or Architecture Issues

Some accessibility findings may originate from upstream decisions rather than implementation mistakes.

Examples include:

* Insufficient contrast in approved design
* Inaccessible interaction pattern
* Inadequate component definition
* Structural UX problem
* Architecture limitation

In such cases, the QA Agent should identify the likely source.

The workflow may then become:

```text
ACCESSIBILITY FINDING
        ↓
IDENTIFY SOURCE
        ↓
DESIGN / SYSTEM / ARCHITECTURE REVIEW
        ↓
APPROVED CHANGE
        ↓
DEVELOPMENT
        ↓
ACCESSIBILITY QA
```

This preserves the distinction between implementation defects and upstream design decisions.

## 19.27 Relationship With Responsive QA

Accessibility QA follows Responsive QA in the standard workflow.

The relationship is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
```

However, accessibility findings may reveal responsive issues and responsive findings may reveal accessibility issues.

The workflow should therefore allow findings to be routed to the appropriate stage rather than enforcing an unnecessarily rigid sequence.

## 19.28 Relationship With SEO & Performance QA

Accessibility and SEO can overlap in areas such as:

* Semantic HTML
* Heading structure
* Link structure
* Page structure
* Image handling

However, the responsibilities remain distinct.

```text
ACCESSIBILITY QA
→ Can users access and use the interface effectively?

SEO & PERFORMANCE QA
→ Can the website be discovered efficiently and perform effectively?
```

Neither stage should silently replace the responsibility of the other.

## 19.29 What the Accessibility QA Agent Does Not Own

The Accessibility QA Agent should not independently own:

* Business requirements
* UX strategy
* Content strategy
* Visual design
* Design-system definition
* Frontend architecture
* Source-code implementation
* Formal responsive design
* SEO strategy
* Performance optimization
* Production deployment
* Final production approval

Its responsibility is to **validate accessibility and identify actionable accessibility issues**.

## 19.30 Primary Outputs

The Accessibility QA Agent should produce:

* Accessibility QA report
* Accessibility findings
* Severity classification
* Validation results
* Recommended remediation
* Re-validation results where applicable
* Machine-readable QA artifact where defined

The exact filenames should follow the existing Agent 09 specification.

## 19.31 Completion Criteria

Agent 09 is considered complete when:

* The implemented website has been evaluated for relevant accessibility requirements.
* Major semantic issues have been identified.
* Keyboard accessibility has been evaluated.
* Focus behavior has been evaluated.
* Navigation accessibility has been evaluated.
* Interactive components have been evaluated.
* Forms have been evaluated.
* Images and alternative text have been evaluated where applicable.
* Relevant visual accessibility issues have been evaluated.
* Dynamic states have been evaluated where applicable.
* Accessibility findings have been documented.
* Findings have been classified by severity.
* Required Development rework has been completed or clearly tracked.
* Re-validation has been performed where required.
* The accessibility QA artifact has been produced.
* No unresolved release-blocking accessibility issue remains.

The workflow can then proceed to:

```text
10 — SEO & Performance QA
```

## 19.32 Version 1 Principle

The Accessibility QA Agent should remain focused on **validating the real accessibility of the implemented website**.

Accessibility should not be treated as a checkbox or as an automated scanner score alone.

The guiding principle is:

**Implement with accessibility in mind → Validate real user access → Identify issues → Remediate → Re-validate**
# 20. Agent 10 — SEO & Performance QA

The **SEO & Performance QA Agent** is the tenth specialized agent in the Agentic Website Factory.

Its purpose is to validate the completed website from a search-engine optimization, technical discoverability, and performance perspective.

The agent verifies that the implementation satisfies the relevant SEO and performance requirements established earlier in the workflow.

This stage provides specialized validation before the website proceeds to **Agent 11 — Production QA & Release Readiness**.

---

## 20.1 Objective

The primary objective of the SEO & Performance QA Agent is to answer:

* Can search engines effectively understand and discover the website?
* Are important pages technically optimized for search?
* Is the website using appropriate metadata?
* Are URLs, headings, and page structure implemented correctly?
* Are technical SEO requirements satisfied?
* Does the website meet the defined performance expectations?
* Are images and assets optimized appropriately?
* Are there performance issues that could negatively affect user experience?
* Are there SEO or performance issues that could block production release?

The agent should provide an evidence-based assessment of the implemented website.

It should not redesign the website or independently change business, UX, content, or architectural decisions.

---

## 20.2 Primary Inputs

The SEO & Performance QA Agent primarily receives:

* Completed website implementation
* Business Discovery artifacts
* UX and Information Architecture artifacts
* Content Strategy artifacts
* UI/UX Design artifacts
* Design System artifacts
* Frontend Architecture artifacts
* Development outputs
* SEO requirements
* Performance requirements
* Approved project decisions
* Existing SEO information where applicable
* Previous QA findings where relevant

The primary workflow relationship is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
        ↓
10 — SEO & PERFORMANCE QA
```

The agent should use the latest valid implementation and project artifacts.

---

## 20.3 Core Responsibilities

The SEO & Performance QA Agent is responsible for:

1. Validating technical SEO implementation.
2. Validating page metadata.
3. Validating URL and routing behavior.
4. Validating heading and semantic structure where relevant to SEO.
5. Validating indexability requirements.
6. Validating sitemap and robots configuration where applicable.
7. Validating canonical configuration where applicable.
8. Validating structured data where required.
9. Evaluating website performance.
10. Identifying major performance bottlenecks.
11. Validating image and asset optimization.
12. Identifying SEO and performance risks.
13. Classifying findings according to severity.
14. Producing the required SEO and Performance QA artifacts.
15. Providing a clear recommendation for downstream production QA.

---

## 20.4 SEO and Performance as Validation

SEO and performance should not be treated as concerns that are introduced only at the end of development.

Relevant requirements should already have been considered during:

```text
CONTENT
   ↓
DESIGN
   ↓
DESIGN SYSTEM
   ↓
FRONTEND ARCHITECTURE
   ↓
DEVELOPMENT
```

Agent 10 validates whether those requirements have been correctly implemented.

The relationship is:

```text
SEO / PERFORMANCE REQUIREMENTS
          ↓
IMPLEMENTATION
          ↓
SEO & PERFORMANCE QA
```

---

## 20.5 Technical SEO Validation

The agent should validate technical SEO elements that are relevant to the project.

These may include:

* Page titles
* Meta descriptions
* Canonical URLs
* Robots directives
* XML sitemap
* Robots.txt
* URL structure
* Heading hierarchy
* Semantic HTML
* Internal linking
* Image alternative text
* Structured data
* Open Graph metadata
* Social sharing metadata
* Indexability
* Crawlability

Not every website requires every SEO feature.

The agent should validate only requirements relevant to the actual project.

---

## 20.6 Page Titles

The agent should verify that important pages have appropriate title metadata.

The validation should consider:

* Presence
* Uniqueness where appropriate
* Relevance to the page
* Alignment with the intended page purpose
* Absence of placeholder titles

Example:

```text
Home
→ Company Name | Primary Offering

Service Page
→ Commercial HVAC Services | Company Name
```

The agent should identify missing or clearly incorrect titles.

---

## 20.7 Meta Descriptions

Where applicable, the agent should verify that important pages contain appropriate meta descriptions.

The validation should consider:

* Presence
* Relevance
* Uniqueness where appropriate
* Alignment with page content
* Absence of placeholder content

The agent should not rewrite the entire content strategy during QA.

If a metadata problem originates from missing or incorrect content direction, it should be documented and routed to the responsible stage.

---

## 20.8 URL Structure

The agent should validate that website URLs are:

* Functional
* Consistent
* Understandable
* Stable
* Appropriate for the website structure

Examples of concerns may include:

* Broken routes
* Unexpected redirects
* Duplicate URL patterns
* Incorrect route names
* Unnecessary parameters
* Missing required pages

The implementation should reflect the approved information architecture.

---

## 20.9 Heading Structure

The agent should verify that page heading structure is implemented appropriately.

This may include:

* Appropriate primary heading
* Logical heading hierarchy
* Avoidance of unnecessary heading levels
* Alignment with page structure
* Meaningful heading content

Heading structure should support both accessibility and search-engine understanding.

The agent should not enforce arbitrary heading patterns when the actual content structure does not require them.

---

## 20.10 Semantic HTML

Where relevant, the agent should verify that the implementation uses meaningful semantic structures.

Examples include:

* Header
* Navigation
* Main
* Section
* Article
* Footer
* Form
* Button
* Appropriate heading elements

Semantic implementation should support:

```text
Accessibility
      +
SEO
      +
Maintainability
```

The agent should identify meaningful semantic problems rather than treating every implementation choice as an SEO failure.

---

## 20.11 Internal Linking

The agent should validate important internal navigation and linking structures.

This may include:

* Navigation links
* Footer links
* Contextual links
* Service-to-detail links
* Portfolio links
* CTA links
* Breadcrumbs where applicable

Important pages should be reachable through appropriate website pathways.

Broken internal links should be identified.

---

## 20.12 Image SEO

Where relevant, the agent should validate image implementation.

Checks may include:

* Appropriate alternative text
* Correct image references
* Missing images
* Image dimensions
* Responsive image behavior
* File size
* Appropriate formats
* Lazy loading where appropriate

Alternative text should be meaningful and appropriate to the purpose of the image.

Decorative images should not be given unnecessary descriptive text.

---

## 20.13 Robots and Indexability

Where applicable, the agent should verify:

* robots.txt
* Meta robots directives
* Indexability
* Noindex requirements
* Canonical configuration
* Crawl restrictions

The agent should ensure that important production pages are not accidentally blocked from indexing.

Development or staging restrictions should not unintentionally remain in the production configuration.

---

## 20.14 XML Sitemap

Where applicable, the agent should verify that the website's XML sitemap:

* Exists
* Is accessible
* Contains appropriate URLs
* Does not contain obviously invalid URLs
* Reflects the intended production website structure

The sitemap should not unnecessarily contain:

* Broken URLs
* Development URLs
* Redirecting URLs
* Non-indexable pages

The exact sitemap requirements depend on the project.

---

## 20.15 Canonical URLs

Where applicable, the agent should validate canonical configuration.

The purpose is to reduce ambiguity where multiple URLs could represent the same content.

The agent should identify:

* Missing canonical configuration where required
* Incorrect canonical targets
* Canonicals pointing to non-production URLs
* Obvious canonical conflicts

Canonical implementation should be consistent with the approved website structure.

---

## 20.16 Structured Data

Where structured data is required by the project, the agent should validate:

* Presence
* Appropriate schema type
* Correct implementation
* Alignment with visible page content
* Obvious syntax or configuration problems

Structured data should not be added merely for the sake of adding schema.

It should be used when there is a legitimate project or search-visibility reason.

---

## 20.17 Open Graph and Social Metadata

Where relevant, the agent should validate social sharing metadata.

This may include:

* Open Graph title
* Open Graph description
* Open Graph image
* Page URL
* Social sharing image availability

Where the project requires other social metadata, that should also be validated.

---

## 20.18 Performance Validation

The agent should evaluate the website's performance from a practical user-experience perspective.

Relevant areas may include:

* Page load behavior
* Asset loading
* Image performance
* Font loading
* JavaScript size
* CSS size
* Unnecessary dependencies
* Render-blocking resources
* Lazy loading
* Caching behavior where applicable
* Network requests
* Runtime performance

The agent should focus on meaningful performance issues rather than optimizing every implementation detail regardless of impact.

---

## 20.19 Core Performance Considerations

Where applicable, the agent should consider commonly used web performance indicators such as:

* Largest Contentful Paint
* Interaction to Next Paint
* Cumulative Layout Shift
* First Contentful Paint
* Total Blocking Time
* Overall page weight

The exact metrics and thresholds should be based on the project's requirements and testing environment.

The agent should document the testing conditions when performance measurements are reported.

---

## 20.20 Image Optimization

Images are often a significant contributor to website performance.

The agent should verify that images are appropriately optimized.

Possible checks include:

* Excessive file size
* Oversized images
* Appropriate image formats
* Responsive image handling
* Lazy loading
* Compression
* Unnecessary duplicate assets

Optimization should preserve the visual quality required by the approved design.

---

## 20.21 Font Performance

Where custom fonts are used, the agent should consider:

* Number of font files
* Font weights
* Font loading strategy
* Unnecessary font variants
* Loading behavior
* Fallback fonts

The objective is to prevent unnecessary font-loading overhead while maintaining the approved design.

---

## 20.22 JavaScript and Dependency Performance

The agent should identify unnecessary frontend performance overhead where applicable.

Potential concerns include:

* Excessive JavaScript
* Large third-party libraries
* Unused dependencies
* Heavy animation libraries
* Unnecessary client-side rendering
* Excessive network requests

The agent should distinguish between:

```text
Necessary Complexity
```

and:

```text
Unnecessary Complexity
```

A dependency should not be considered a problem simply because it exists.

---

## 20.23 Third-Party Resources

Third-party resources may affect performance.

Examples include:

* Analytics
* Chat widgets
* Maps
* Video embeds
* Marketing tools
* Social widgets
* External fonts
* External APIs

The agent should identify third-party resources that materially affect performance or reliability.

Where possible, the project should avoid unnecessary third-party dependencies.

---

## 20.24 Mobile Performance

Performance should be evaluated on mobile experiences where relevant.

The agent should consider:

* Mobile network conditions
* Mobile CPU constraints
* Image loading
* JavaScript execution
* Layout stability
* Font loading
* Interaction responsiveness

A website should not be considered performant merely because it performs well on a high-end desktop environment.

---

## 20.25 SEO and Performance Findings

Each significant finding should contain enough information for the responsible stage to understand and resolve the issue.

A finding may include:

```text
Finding ID
Category
Severity
Page / Component
Issue
Expected Behavior
Actual Behavior
Evidence
Recommended Resolution
Responsible Stage
Status
```

Example:

```text
Finding ID: SEO-004

Category:
Technical SEO

Severity:
MAJOR

Issue:
Production service pages are missing canonical URLs.

Responsible Stage:
Development

Status:
OPEN
```

---

## 20.26 Severity Classification

A practical severity model may be:

```text
BLOCKER
CRITICAL
MAJOR
MINOR
```

### BLOCKER

An issue that prevents the website from being safely released.

Examples:

* Production pages are accidentally blocked from indexing when indexing is required.
* Production build cannot load required SEO configuration.
* Critical performance failure makes the website unusable.

### CRITICAL

A serious SEO or performance problem affecting an important business requirement.

### MAJOR

A significant issue that should normally be fixed before release but may not independently block deployment.

### MINOR

A low-impact issue that does not materially affect the website's core SEO or performance objectives.

Severity should always reflect project context.

---

## 20.27 Performance Testing Conditions

Performance results should be interpreted according to the testing environment.

Where performance measurements are recorded, the report should identify relevant conditions such as:

* Device category
* Browser
* Network conditions
* Test environment
* Page tested
* Number of test runs where relevant

This prevents performance measurements from being interpreted without context.

---

## 20.28 SEO and Performance Regression

Changes made after Agent 10 may introduce new SEO or performance problems.

Therefore, if Development performs significant changes after this QA stage, the affected SEO and performance checks should be repeated.

The preferred flow is:

```text
DEVELOPMENT CHANGE
        ↓
IDENTIFY SEO / PERFORMANCE IMPACT
        ↓
RE-RUN AFFECTED TESTS
        ↓
UPDATE QA FINDINGS
```

The entire SEO test suite does not necessarily need to be repeated for every small change.

---

## 20.29 Primary Outputs

The SEO & Performance QA Agent should produce the artifacts defined by its existing Agent 10 specification.

These may include:

* SEO QA report
* Performance QA report
* Combined SEO and Performance QA report
* SEO findings
* Performance findings
* Recommendations
* Validation results
* Machine-readable QA artifact where applicable

The exact artifact filenames should follow the existing Agent 10 specification.

---

## 20.30 Machine-Readable QA Artifact

Where defined by the existing Agent 10 specification, the agent should produce a machine-readable QA artifact.

For example:

```text
seo-performance-qa.json
```

The structured artifact may represent:

* Test status
* SEO findings
* Performance findings
* Severity
* Affected pages
* Recommendations
* Resolution status
* Release impact

The machine-readable artifact should represent the same findings documented in the human-readable QA report.

---

## 20.31 QA Artifact Consistency

Human-readable and machine-readable QA artifacts should remain consistent.

For example:

```text
SEO & Performance QA Report
          +
seo-performance-qa.json
          ↓
Same QA Findings
Same Severity
Same Status
Same Release Impact
```

If a conflict exists between the two artifacts, the QA stage should resolve the discrepancy before handoff.

---

## 20.32 Output Quality Check

Before Agent 10 is considered complete, the outputs should be checked for:

* Required SEO checks completed
* Required performance checks completed
* Important pages evaluated
* Metadata validated
* Indexability validated where applicable
* Sitemap validated where applicable
* Robots configuration validated where applicable
* Canonical configuration validated where applicable
* Structured data validated where applicable
* Internal links evaluated
* Image optimization evaluated
* Performance bottlenecks identified
* Findings classified by severity
* Release-impacting issues clearly identified
* Required QA artifacts produced
* Machine-readable and human-readable artifacts consistent where both exist

---

## 20.33 Handoff to Agent 11

The primary downstream consumer is:

```text
11 — Production QA & Release Readiness Agent
```

The handoff is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
        ↓
10 — SEO & PERFORMANCE QA
        ↓
SEO / PERFORMANCE QA ARTIFACTS
        ↓
11 — PRODUCTION QA & RELEASE READINESS
```

Agent 11 uses the SEO and Performance QA outputs to determine whether:

* Important SEO issues remain.
* Performance issues remain.
* Any issue is release-blocking.
* Known risks require acceptance.
* Additional rework is required before production approval.

---

## 20.34 Rework Loop

If Agent 10 identifies issues that require development changes, the workflow should create a controlled rework loop.

For example:

```text
SEO / PERFORMANCE QA
        ↓
FINDING
        ↓
DEVELOPMENT REWORK
        ↓
AFFECTED VALIDATION
        ↓
SEO / PERFORMANCE QA
        ↓
UPDATED STATUS
```

The entire factory should not automatically restart.

Only affected work should be re-executed.

---

## 20.35 Example Rework Routing

A metadata issue may follow:

```text
SEO QA
   ↓
Missing Metadata
   ↓
Development
   ↓
SEO QA
```

An image-performance issue may follow:

```text
Performance QA
   ↓
Oversized Image
   ↓
Development / Asset Handling
   ↓
Performance QA
```

A sitemap issue may follow:

```text
SEO QA
   ↓
Invalid Sitemap
   ↓
Development
   ↓
SEO QA
```

A content-related SEO issue may require:

```text
SEO QA
   ↓
Missing / Incorrect Content
   ↓
Content Strategy
   ↓
Development
   ↓
SEO QA
```

The responsible stage should be determined according to the actual source of the problem.

---

## 20.36 Relationship With Development

Agent 10 validates the implementation produced by Agent 07.

The relationship is:

```text
FRONTEND ARCHITECTURE
        ↓
DEVELOPMENT
        ↓
IMPLEMENTED WEBSITE
        ↓
SEO & PERFORMANCE QA
```

Development remains responsible for implementing fixes.

Agent 10 remains responsible for validating those fixes.

---

## 20.37 Relationship With Accessibility QA

SEO and accessibility overlap in several areas, including:

* Semantic HTML
* Heading structure
* Image alternative text
* Navigation
* Page structure

However, the responsibilities remain distinct.

```text
09 — ACCESSIBILITY QA
        ↓
Accessibility Validation

10 — SEO & PERFORMANCE QA
        ↓
SEO + Performance Validation
```

A shared issue may therefore be identified by both agents from different perspectives.

The project should avoid duplicating ownership while allowing related findings to reference one another.

---

## 20.38 Relationship With Content Strategy

SEO requirements may reveal content problems.

For example:

```text
SEO QA
   ↓
Insufficient Page Content
   ↓
Content Strategy Review
   ↓
Content Update
   ↓
Development
   ↓
SEO QA
```

Agent 10 should identify the problem but should not independently redefine the complete content strategy.

---

## 20.39 What the SEO & Performance QA Agent Does Not Own

The SEO & Performance QA Agent should not independently own:

* Business discovery
* UX strategy
* Information architecture
* Content strategy
* Visual design
* Design-system definition
* Frontend architecture
* Feature development
* Major content creation
* Accessibility strategy
* Production deployment
* Final human approval

Its responsibility is to **validate SEO and performance quality of the implemented website**.

---

## 20.40 Completion Criteria

Agent 10 is considered complete when:

* Required SEO validation has been performed.
* Required performance validation has been performed.
* Important production pages have been evaluated.
* Major technical SEO requirements have been checked.
* Important performance risks have been identified.
* Findings have been classified by severity.
* Release-blocking issues have been identified where applicable.
* Required SEO and Performance QA artifacts have been produced.
* Machine-readable artifacts are consistent with human-readable findings where applicable.
* Findings are ready for downstream Production QA and Release Readiness.

The workflow can then proceed to:

```text
11 — Production QA & Release Readiness
```

---

## 20.41 Version 1 Principle

The SEO & Performance QA Agent should remain focused on **objective validation of search visibility, technical SEO, and website performance**.

It should not become a replacement for Content Strategy, Development, or Production QA.

The guiding principle is:

**Validate discoverability → Validate technical SEO → Validate performance → Identify risks → Route issues for resolution**
# 21. Agent 11 — Production QA & Release Readiness

The **Production QA & Release Readiness Agent** is the eleventh and final specialized QA agent in the Agentic Website Factory.

Its purpose is to perform the final validation of the completed website before production deployment.

The agent verifies that the implemented website is complete, consistent with the approved project requirements and design direction, technically ready for release, and free of known critical issues that would prevent production deployment.

This stage represents the final machine-assisted quality gate before **Final Human Deployment Approval**.

The Production QA Agent does not replace human approval.

Its responsibility is to establish whether the website is sufficiently ready for a human decision to deploy.

---

## 21.1 Objective

The primary objective of the Production QA & Release Readiness Agent is to answer:

* Is the website complete?
* Does the implementation satisfy the approved requirements?
* Does the implemented website match the approved UX and design direction?
* Are all required pages and functionality present?
* Are critical defects resolved?
* Are previous QA findings addressed?
* Is the website technically ready for production?
* Are required production configurations present?
* Are known risks documented?
* Is the website ready for final human deployment approval?

The goal is not simply to identify bugs.

The goal is to determine whether the website has reached a **release-ready state**.

---

## 21.2 Primary Inputs

The Production QA & Release Readiness Agent primarily receives:

* Completed website implementation
* Approved UI/UX design artifacts
* Design System artifacts
* Frontend Architecture artifacts
* Business Discovery artifacts where required
* UX and Information Architecture artifacts where required
* Content Strategy artifacts where required
* Responsive QA results
* Accessibility QA results
* SEO & Performance QA results
* Previous QA findings
* QA rework results
* Approved project decisions
* Human approval records
* Production configuration requirements
* Deployment requirements
* Release-related project information

The primary workflow relationship is:

```text
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
        ↓
10 — SEO & PERFORMANCE QA
        ↓
11 — PRODUCTION QA & RELEASE READINESS
```

The Production QA Agent may also reference earlier artifacts when validating traceability or resolving questions.

---

## 21.3 Core Responsibilities

The Production QA & Release Readiness Agent is responsible for:

1. Performing final end-to-end website validation.
2. Confirming required pages are implemented.
3. Confirming required functionality is implemented.
4. Verifying that major QA findings have been resolved.
5. Validating consistency with approved project artifacts.
6. Identifying release-blocking defects.
7. Identifying remaining non-blocking issues.
8. Reviewing production configuration readiness.
9. Reviewing critical user journeys.
10. Confirming that required QA stages have completed.
11. Assessing overall release readiness.
12. Producing the final production QA artifacts.
13. Providing a clear recommendation for or against release.
14. Preparing the project for final human deployment approval.

---

## 21.4 Production Readiness Philosophy

Production QA should not be treated as another isolated testing stage.

It is the final integration-level quality review of the complete website.

The relationship is:

```text
INDIVIDUAL QA
     ↓
FINDINGS
     ↓
REWORK
     ↓
RE-VALIDATION
     ↓
PRODUCTION QA
     ↓
RELEASE READINESS
```

The objective is to determine whether all important quality dimensions work together successfully.

A website should not be considered production-ready simply because individual QA agents have passed independently.

---

## 21.5 Requirement Verification

The agent should verify that the implemented website satisfies the major approved project requirements.

This may include:

* Required pages
* Required sections
* Required features
* Required forms
* Required calls to action
* Required integrations
* Required navigation
* Required content
* Required brand elements
* Required technical behavior
* Required deployment requirements

The agent should compare implementation against the approved project artifacts rather than relying only on the current website appearance.

---

## 21.6 Page Completeness

The agent should verify that all required pages identified during the project are present and functional.

The review may include:

```text
Required Page
     ↓
Implemented?
     ↓
Accessible?
     ↓
Functional?
     ↓
Content Complete?
     ↓
Design Consistent?
```

Missing or incomplete required pages should normally be treated as release-blocking issues unless explicitly approved as an intentional scope change.

---

## 21.7 Functional Completeness

The agent should verify important user-facing functionality.

Examples include:

* Navigation
* Forms
* Contact actions
* Buttons
* Links
* Interactive components
* Search where applicable
* Filters where applicable
* Modals
* Menus
* External integrations
* Required dynamic behavior

The agent should focus on functionality that is part of the approved project scope.

It should not classify intentionally excluded functionality as a defect.

---

## 21.8 Critical User Journeys

The Production QA Agent should validate the most important end-to-end user journeys.

Examples include:

```text
Home
 ↓
Service
 ↓
Service Detail
 ↓
Contact
 ↓
Inquiry Submission
```

or:

```text
Home
 ↓
Portfolio
 ↓
Project Detail
 ↓
Contact
```

The exact journeys depend on the project.

The purpose is to ensure that users can successfully complete the actions that matter most to the business.

---

## 21.9 Cross-Stage Consistency

The final QA review should verify consistency between major project artifacts and the implementation.

The agent should compare, where relevant:

```text
Business Requirements
        ↓
UX Structure
        ↓
Content Direction
        ↓
UI/UX Design
        ↓
Design System
        ↓
Frontend Architecture
        ↓
Implementation
```

The objective is to identify cases where the final website has drifted away from approved project decisions.

Examples include:

* Missing approved sections
* Different navigation structure
* Incorrect content hierarchy
* Inconsistent components
* Unapproved visual changes
* Missing required functionality
* Technical implementation that violates an approved constraint

---

## 21.10 Previous QA Findings

The Production QA Agent should review findings from the earlier QA stages.

These may include:

* Responsive QA findings
* Accessibility QA findings
* SEO findings
* Performance findings
* Development defects
* Human review findings
* Rework results

The agent should verify that release-relevant findings have been resolved or explicitly accepted.

A finding should not simply disappear because the project moved to the next stage.

---

## 21.11 QA Rework Verification

Where previous QA identified issues, the final QA stage should verify the resulting fixes.

The conceptual process is:

```text
QA FINDING
    ↓
REWORK
    ↓
UPDATED IMPLEMENTATION
    ↓
RE-TEST
    ↓
PASS / FAIL
```

If a fix introduces a new problem, the affected QA stage should be re-executed.

Production QA should therefore act as a final integration check rather than replacing the earlier specialized QA stages.

---

## 21.12 Release-Blocking Defects

The agent should classify defects according to their impact on production readiness.

A practical classification may include:

```text
CRITICAL
Blocks production release.

HIGH
Should normally be resolved before release.

MEDIUM
Should be resolved where practical but may not block release.

LOW
Minor issue that does not materially affect release readiness.
```

Examples of release-blocking conditions may include:

* Broken primary user journey
* Major page missing
* Critical functionality not working
* Serious accessibility failure affecting essential interaction
* Severe responsive failure
* Major security or configuration concern
* Production build failure
* Critical integration failure
* Significant content or business requirement mismatch

The exact release-blocking criteria should be adapted to the project.

---

## 21.13 Known Issues

Not every remaining issue necessarily prevents production release.

Where a known issue remains, the agent should document:

```text
Issue
Severity
Impact
Affected Area
Current Status
Release Blocking?
Recommended Action
```

A known issue should never be hidden simply because it is considered minor.

Transparency is important for release decisions.

---

## 21.14 Production Configuration Review

Where relevant, the agent should verify that production configuration requirements have been addressed.

This may include:

* Production environment configuration
* Environment variables
* API endpoints
* Domain configuration
* Build configuration
* Analytics configuration
* Form configuration
* Third-party integrations
* Sitemap
* Robots configuration
* Metadata
* Error handling
* Production asset configuration

Sensitive credentials should not be exposed in QA artifacts.

The QA Agent should verify configuration readiness without storing secrets in project documentation.

---

## 21.15 Build and Deployment Readiness

The agent should verify that the website can successfully reach the expected production-ready state.

Where applicable, this may include:

* Successful production build
* No critical build errors
* Required dependencies available
* Required assets present
* Expected routes available
* Production configuration valid
* Deployment package or output generated correctly

The exact checks depend on the technology stack.

---

## 21.16 Content Readiness

The final QA stage should verify that the website does not contain obvious development placeholders or incomplete content.

Examples include:

* Lorem ipsum
* Placeholder text
* Placeholder images
* Empty sections
* Temporary links
* Test data
* Development-only labels
* Unresolved content markers
* Missing required business information

Where content is intentionally marked as pending client input, that status should be explicitly documented.

---

## 21.17 Link and Navigation Validation

The agent should verify important internal and external links.

Checks may include:

* Internal routes
* Navigation links
* Footer links
* CTA links
* Contact links
* External links
* Social links where applicable
* Download links
* Form destinations

Broken links that affect important user journeys should normally be treated as release-blocking.

---

## 21.18 Forms and Conversion Actions

Where forms or conversion actions are part of the website, the agent should verify their complete flow.

For example:

```text
User Opens Form
      ↓
Enters Information
      ↓
Validation
      ↓
Submission
      ↓
Processing
      ↓
Success / Error Response
      ↓
Expected Business Destination
```

The review should verify that the form behaves as intended rather than simply checking that the form is visually present.

---

## 21.19 Analytics and Tracking

Where analytics or tracking requirements are part of the approved project scope, the agent should verify their production readiness.

This may include:

* Analytics configuration
* Required tracking events
* Conversion tracking
* Form tracking
* Important CTA tracking
* Tag configuration

The agent should validate only the tracking requirements defined for the project.

---

## 21.20 Security and Sensitive Configuration Awareness

Production QA should identify obvious release risks related to sensitive configuration.

The agent should check for issues such as:

* Exposed credentials
* API keys committed to source code
* Unsafe production configuration
* Debug settings unintentionally enabled
* Development-only endpoints
* Test credentials
* Sensitive information exposed in the client

The agent should not reproduce sensitive values in its output.

If a serious security concern is discovered, the release should be blocked until the issue is addressed or formally accepted by the appropriate authority.

---

## 21.21 Production QA Artifact

The Production QA Agent should produce a final production QA artifact.

The exact artifact filename should follow the existing Agent 11 specification.

The artifact should provide a structured summary of:

```text
Release Scope
Requirements Checked
Critical User Journeys
QA Status
Open Issues
Release-Blocking Issues
Production Configuration Status
Known Risks
Overall Readiness
Recommendation
```

Where appropriate, the artifact may also include machine-readable status information.

---

## 21.22 Release Readiness Status

The final status should clearly communicate whether the website is ready for deployment.

A practical status model is:

```text
NOT READY
      ↓
READY WITH REWORK
      ↓
READY FOR HUMAN APPROVAL
      ↓
APPROVED FOR DEPLOYMENT
```

The Production QA Agent itself should normally only determine:

```text
NOT READY
```

or:

```text
READY FOR HUMAN APPROVAL
```

The final **Approved for Deployment** decision belongs to the human approval process.

---

## 21.23 Machine-Readable Release Status

Where supported by the project implementation, the Production QA Agent may produce a machine-readable release status.

For example:

```json
{
  "status": "READY_FOR_HUMAN_APPROVAL",
  "release_blockers": 0,
  "critical_issues": 0,
  "high_issues": 0,
  "medium_issues": 2,
  "low_issues": 1,
  "human_approval_required": true
}
```

The exact schema should follow the project's established artifact conventions.

Machine-readable release status should remain consistent with the human-readable QA report.

---

## 21.24 Release Gate

Production QA establishes the final machine-assisted release gate.

The conceptual flow is:

```text
PRODUCTION QA
      ↓
RELEASE READINESS CHECK
      ↓
RELEASE BLOCKERS?
   ↙           ↘
 YES            NO
 ↓              ↓
REWORK      READY FOR HUMAN
                 ↓
        FINAL HUMAN APPROVAL
                 ↓
             DEPLOYMENT
```

The Production QA Agent must not bypass a release blocker simply because the project is near completion.

---

## 21.25 Final Human Deployment Approval

The Production QA Agent prepares the project for the final human decision.

The human approval should confirm that:

* Production QA has passed.
* No unacceptable release blockers remain.
* Known issues are understood.
* The final website is acceptable.
* The approved scope has been delivered.
* The person responsible for deployment authorizes production release.

The conceptual relationship is:

```text
AGENT 11
PRODUCTION QA
      ↓
RELEASE READY
      ↓
HUMAN DEPLOYMENT APPROVAL
      ↓
PRODUCTION
```

The final human approval is therefore separate from the automated or AI-assisted QA decision.

---

## 21.26 Handoff to Deployment

Once Production QA determines that the website is ready for human approval, the project moves to the deployment approval stage.

The handoff is:

```text
11 — PRODUCTION QA
        ↓
PRODUCTION QA ARTIFACT
        ↓
RELEASE READINESS STATUS
        ↓
FINAL HUMAN APPROVAL
        ↓
DEPLOYMENT
```

The Production QA Agent does not independently deploy the website unless a future workflow explicitly assigns deployment authority to an automated system.

---

## 21.27 Rework Loop

If production QA identifies a release-blocking issue, the workflow should return to the appropriate stage.

For example:

```text
PRODUCTION QA
      ↓
ISSUE IDENTIFIED
      ↓
IDENTIFY RESPONSIBLE STAGE
      ↓
REWORK
      ↓
AFFECTED QA
      ↓
PRODUCTION QA
```

Examples:

```text
Responsive Issue
      ↓
Development
      ↓
Responsive QA
      ↓
Production QA
```

or:

```text
SEO Issue
      ↓
Development / SEO-related Rework
      ↓
SEO & Performance QA
      ↓
Production QA
```

The workflow should avoid restarting unrelated stages.

---

## 21.28 Change Impact After Production QA

If a significant change is introduced after Production QA has passed, the release readiness status should be reconsidered.

The project should determine:

* Which artifact changed?
* Which implementation changed?
* Which user journey is affected?
* Which QA stage needs to be re-run?
* Whether Production QA must be repeated.

A significant change should invalidate only the affected validation where practical, but the final release decision must be based on the latest valid implementation.

---

## 21.29 Relationship With All Previous Agents

Agent 11 is the final validation stage and therefore has visibility across the complete workflow.

The relationship can be represented as:

```text
01 — BUSINESS DISCOVERY
          ↓
02 — UX / INFORMATION ARCHITECTURE
          ↓
03 — CONTENT STRATEGY
          ↓
04 — UI/UX DESIGN
          ↓
05 — DESIGN SYSTEM
          ↓
06 — FRONTEND ARCHITECTURE
          ↓
07 — DEVELOPMENT
          ↓
08 — RESPONSIVE QA
          ↓
09 — ACCESSIBILITY QA
          ↓
10 — SEO & PERFORMANCE QA
          ↓
11 — PRODUCTION QA
          ↓
FINAL HUMAN DEPLOYMENT APPROVAL
          ↓
PRODUCTION
```

This does not mean Agent 11 must re-perform every earlier agent's responsibility.

Instead, it verifies that the combined result is suitable for release.

---

## 21.30 What the Production QA Agent Does Not Own

The Production QA & Release Readiness Agent should not independently own:

* Business discovery
* UX strategy
* Content strategy
* Visual design
* Design-system definition
* Frontend architecture
* Primary development work
* Specialized responsive QA
* Specialized accessibility QA
* Specialized SEO validation
* Final human deployment approval
* Production deployment authorization

Its responsibility is to determine whether the completed website is ready to enter the final human release decision.

---

## 21.31 Output Quality Check

Before Agent 11 is considered complete, its output should be checked for:

* Complete release scope review
* Required pages verified
* Critical user journeys verified
* Important functionality verified
* Previous QA findings reviewed
* Release blockers identified
* Known issues documented
* Production configuration reviewed
* Build readiness reviewed
* Content completeness reviewed
* Important risks documented
* Release readiness clearly stated
* Human approval requirement clearly identified

The final QA artifact should provide enough information for a responsible human to make the deployment decision.

---

## 21.32 Completion Criteria

Agent 11 is considered complete when:

* The completed website has been reviewed against the approved project scope.
* Required pages and functionality have been validated.
* Critical user journeys have been validated.
* Previous QA findings have been reviewed.
* Release-blocking issues have been identified and resolved or explicitly escalated.
* Production configuration requirements have been reviewed.
* Build and deployment readiness has been assessed.
* Remaining known issues are documented.
* Final production QA artifacts are produced.
* Release readiness status is clearly established.
* The project is either returned for rework or marked **READY FOR HUMAN APPROVAL**.

The workflow can then proceed to:

```text
FINAL HUMAN DEPLOYMENT APPROVAL
```

followed by:

```text
PRODUCTION DEPLOYMENT
```

---

## 21.33 Version 1 Principle

The Production QA & Release Readiness Agent should remain focused on **final validation and release readiness**, not on replacing human responsibility for production deployment.

The guiding principle is:

**Validate the complete website → Identify release blockers → Confirm readiness → Hand control to the human release decision.**

The final production decision remains human-controlled.
# SECTION 22 — WORKFLOW EXECUTION MODES

## 22.1 Purpose

The Agentic Website Factory must support controlled execution of the 11-agent workflow under different project conditions.

The workflow must not assume that every agent always executes in exactly the same runtime pattern.

Some stages must execute sequentially.

Some activities may execute in parallel.

Some activities require human approval.

Some activities may require rework.

Some workflows may need to resume from a previously completed stage.

Section 22 defines the approved execution modes for the Agentic Website Factory.

The execution mode must preserve:

* Agent responsibilities
* Agent sequence
* Artifact contracts
* Source-of-truth rules
* Human approval gates
* QA rework loops
* Release gates
* Final deployment approval

Execution modes change how work is coordinated.

They do not change ownership of the agents.

---

# 22.2 Core Execution Principle

The Agentic Website Factory follows a controlled workflow rather than an unrestricted autonomous process.

The default execution model is:

```text
INPUT
  ↓
01 Business Discovery
  ↓
02 UX / Information Architecture
  ↓
03 Content Strategy
  ↓
04 UI/UX Design
  ↓
05 Design System
  ↓
06 Frontend Architecture
  ↓
07 Development
  ↓
08 Responsive QA
  ↓
09 Accessibility QA
  ↓
10 SEO / Performance QA
  ↓
11 Production QA
  ↓
Human Release Approval
  ↓
Human Deployment Approval
  ↓
PRODUCTION
```

The workflow may use controlled parallelism and rework loops where permitted.

No execution mode may bypass required quality gates.

---

# 22.3 Execution Modes

The Agentic Website Factory supports the following execution modes:

1. Sequential Execution
2. Parallel Execution
3. Conditional Execution
4. Human-Gated Execution
5. Rework Execution
6. Resume Execution
7. Controlled Restart

Each mode has a specific purpose.

---

# 22.4 Sequential Execution

Sequential execution is the default workflow mode.

An agent begins only after the required upstream artifacts are available and the stage is considered ready.

Example:

```text
Agent 01
   ↓
Agent 02
   ↓
Agent 03
   ↓
Agent 04
   ↓
Agent 05
   ↓
Agent 06
   ↓
Agent 07
```

The same principle applies to the QA chain:

```text
Agent 07
   ↓
Agent 08
   ↓
Agent 09
   ↓
Agent 10
   ↓
Agent 11
```

Sequential execution is required when downstream work depends directly on upstream decisions.

Examples:

* Agent 02 depends on Agent 01 business discovery.
* Agent 04 depends on approved UX and content direction.
* Agent 05 depends on the UI/UX design.
* Agent 06 depends on the approved design and design system.
* Agent 07 depends on the approved architecture.
* Agent 08 depends on the implemented website.
* Agent 09 depends on the implemented website.
* Agent 10 depends on the implemented website and prior QA.
* Agent 11 depends on the completed QA chain.

---

# 22.5 Parallel Execution

Parallel execution may be used when two or more activities are independent and do not modify the same source-of-truth artifact.

Parallel execution is an optimization mechanism.

It must not be used simply to make the workflow appear faster.

Examples of potentially parallel activities include:

```text
                    ┌── Content preparation
Business Discovery ─┤
                    └── Asset collection
```

or:

```text
Development
    │
    ├── Responsive validation
    │
    └── Automated accessibility checks
```

However, parallel activities must converge through a controlled synchronization point.

Example:

```text
                ┌── Responsive QA
Development ────┤
                └── Accessibility checks
                         ↓
                  Synchronization
                         ↓
                  Next QA Stage
```

Parallel execution must not create conflicting changes.

If two agents attempt to modify the same governed artifact, the activities must be serialized.

---

# 22.6 Approved Parallelism Rules

Parallel execution is permitted only when all of the following are true:

* The activities have clearly defined inputs.
* The activities have independent responsibilities.
* The activities do not overwrite each other's artifacts.
* The activities do not introduce conflicting decisions.
* The outputs can be merged deterministically.
* A synchronization point exists.
* Any human approval requirement is preserved.
* The resulting artifacts can be traced to their producing agent.

Parallel execution is not permitted when:

* One activity changes the input required by another.
* Two agents are making competing design decisions.
* Two agents modify the same source-of-truth artifact.
* The result requires unresolved human judgment.
* A downstream agent depends on an unresolved upstream decision.

When uncertain, use sequential execution.

---

# 22.7 Conditional Execution

Some workflow activities are conditional.

An agent or activity may be skipped when its defined purpose is not applicable to the project, provided that the workflow explicitly records the decision.

Example:

```text
Does the website require a complex form?

YES
 ↓
Implement form architecture

NO
 ↓
Skip complex form implementation
```

Conditional execution must never silently remove a required workflow stage.

The system must record:

* Condition evaluated
* Decision
* Reason
* Decision owner
* Date
* Impact

Example:

```text
Condition:
Complex form integration required?

Decision:
NO

Reason:
Website contains only a basic contact CTA.

Decision Owner:
Project workflow owner.

Impact:
No external form API integration required.
```

---

# 22.8 Human-Gated Execution

Certain decisions require human approval.

AI agents must not automatically approve their own work when a human approval gate has been defined.

Human approval may be required for:

* Business strategy
* Information architecture
* Content direction
* UI/UX design
* Design system
* Major architecture changes
* Release readiness
* Production deployment

The workflow must stop at a human approval gate until the required decision is recorded.

Example:

```text
Agent 04
   ↓
Design Output
   ↓
HUMAN DESIGN APPROVAL
   │
   ├── Approved → Agent 05
   │
   └── Changes Required
             ↓
        Agent 04 Rework
```

---

# 22.9 Human Approval States

Human approval decisions must use explicit states.

Approved states:

```text
APPROVED
```

```text
APPROVED_WITH_NOTES
```

Non-approved states:

```text
CHANGES_REQUESTED
```

```text
REJECTED
```

```text
BLOCKED
```

The workflow must not interpret an absent response as approval.

---

# 22.10 Rework Execution

Rework execution occurs when an agent or human reviewer identifies an issue requiring correction.

The workflow must return work to the smallest affected stage.

Example:

```text
Agent 08 Responsive QA
        ↓
Responsive defect
        ↓
Agent 07 Development
        ↓
Fix
        ↓
Agent 08 Revalidation
```

The entire factory must not restart unless the defect fundamentally invalidates earlier work.

---

# 22.11 Affected-Stage Rework Principle

The rework target must be determined by the origin of the problem.

Example:

```text
Business requirement problem
        ↓
Agent 01
```

```text
UX structure problem
        ↓
Agent 02
```

```text
Content problem
        ↓
Agent 03
```

```text
Visual design problem
        ↓
Agent 04
```

```text
Design token/component problem
        ↓
Agent 05
```

```text
Architecture problem
        ↓
Agent 06
```

```text
Implementation problem
        ↓
Agent 07
```

```text
Responsive implementation problem
        ↓
Agent 07
        ↓
Agent 08 revalidation
```

```text
Accessibility implementation problem
        ↓
Agent 07
        ↓
Agent 09 revalidation
```

```text
SEO/performance implementation problem
        ↓
Agent 07
        ↓
Agent 10 revalidation
```

```text
Production readiness problem
        ↓
Affected implementation/QA stage
        ↓
Agent 11 revalidation
```

---

# 22.12 Rework Loop Limits

Rework must be controlled.

Every rework cycle should record:

* Rework ID
* Source agent
* Receiving agent
* Issue ID
* Reason
* Required change
* Status
* Validation result

If the same issue repeatedly returns without resolution, the workflow must escalate the issue for human review.

The system must not enter an uncontrolled infinite rework loop.

---

# 22.13 Resume Execution

The factory must support resuming an interrupted project.

A workflow may be resumed when:

* A previous execution stopped.
* An agent failed.
* A human approval is pending.
* External information was unavailable.
* Development was paused.
* The project was temporarily archived.

When resuming, the workflow must inspect the existing project state before executing an agent again.

The system must determine:

```text
Completed
In Progress
Blocked
Needs Rework
Pending Approval
Not Started
```

The workflow should continue from the earliest incomplete or invalid stage.

---

# 22.14 Resume Validation

Before resuming execution, verify:

* Existing artifacts
* Artifact versions
* Approval status
* Decision records
* Known issues
* Rework status
* Agent completion status
* Project code state
* QA status

Do not assume that a previously completed stage remains valid if one of its governing inputs has changed.

---

# 22.15 Controlled Restart

A full workflow restart should be exceptional.

A restart may be required when:

* Business requirements fundamentally change.
* The project scope is replaced.
* The technology architecture is replaced.
* The approved design is abandoned.
* The existing implementation becomes unusable.
* A major upstream decision invalidates downstream work.

Before restarting, record:

```text
RESTART REASON
AFFECTED STAGES
INVALIDATED ARTIFACTS
PRESERVED ARTIFACTS
HUMAN DECISION
RESTART POINT
```

A restart must not delete historical project records.

Previous artifacts should remain available for traceability.

---

# 22.16 Artifact Synchronization

When multiple agents contribute to a project, artifacts must remain synchronized.

Each governed artifact should have:

* Artifact name
* Artifact type
* Producing agent
* Version
* Status
* Creation/update timestamp
* Approval status where applicable
* Dependencies

Example:

```text
Artifact:
design-system.tokens.json

Producer:
Agent 05

Status:
Approved

Version:
1.0.0
```

Downstream agents must use the approved version.

---

# 22.17 Source-of-Truth Enforcement

Every execution mode must respect the established source-of-truth hierarchy.

The workflow must not allow a downstream agent to silently override an upstream approved decision.

If a downstream implementation discovers a conflict:

```text
Detect Conflict
      ↓
Document Conflict
      ↓
Identify Affected Artifacts
      ↓
Determine Owner
      ↓
Human/Agent Decision
      ↓
Update Source of Truth
      ↓
Revalidate Downstream Work
```

---

# 22.18 Dependency-Aware Execution

Before executing an agent, the workflow should verify that its required dependencies are available.

Example:

```text
Agent 07 Development
        ↓
Requires:
Business brief
UX artifacts
Content artifacts
Design artifacts
Design system
Architecture
Machine-readable artifacts
        ↓
READY?
```

If required dependencies are missing:

```text
NOT READY
```

The agent must not proceed using guessed or fabricated information.

---

# 22.19 Execution Readiness

Each agent should have a readiness condition.

An agent is READY when:

* Required inputs exist.
* Required upstream stages are complete.
* Required approvals exist.
* No blocking dependency exists.
* Required decisions are resolved.

Example:

```text
AGENT 07

Inputs:
READY

Architecture:
APPROVED

Design:
APPROVED

Content:
READY

Dependencies:
READY

Execution:
READY
```

---

# 22.20 Execution Status

The workflow should maintain an execution status for each agent.

Allowed states:

```text
NOT_STARTED
```

```text
READY
```

```text
IN_PROGRESS
```

```text
WAITING_FOR_INPUT
```

```text
WAITING_FOR_APPROVAL
```

```text
BLOCKED
```

```text
REWORK_REQUIRED
```

```text
COMPLETED
```

```text
FAILED
```

The workflow controller should use these states to determine the next valid action.

---

# 22.21 Failure Handling

If an agent fails during execution:

1. Record the failure.
2. Preserve generated artifacts.
3. Identify the failure type.
4. Determine whether retry is safe.
5. Retry only when appropriate.
6. Escalate persistent failures.
7. Do not silently continue with incomplete output.

Failure categories may include:

```text
INPUT_FAILURE
```

```text
TOOL_FAILURE
```

```text
IMPLEMENTATION_FAILURE
```

```text
VALIDATION_FAILURE
```

```text
DEPENDENCY_FAILURE
```

```text
HUMAN_APPROVAL_FAILURE
```

---

# 22.22 Retry Rules

Retries must be controlled.

A retry is appropriate when the failure is:

* Temporary
* Tool-related
* Network-related
* Environment-related
* Recoverable

A retry is not sufficient when the failure is caused by:

* Invalid requirements
* Conflicting specifications
* Missing approval
* Incorrect architecture
* Fundamental implementation problems

Such issues require correction or escalation rather than repeated execution.

---

# 22.23 Execution Traceability

Every execution should be traceable.

The workflow should be able to determine:

```text
WHO
WHAT
WHEN
WHY
INPUT
OUTPUT
VERSION
DECISION
APPROVAL
REWORK
STATUS
```

This enables the project to be audited and resumed without reconstructing the workflow manually.

---

# 22.24 Execution Example

A normal project execution may look like:

```text
INPUT
  ↓
Agent 01
  ↓
Business Approval
  ↓
Agent 02
  ↓
Agent 03
  ↓
Design Approval
  ↓
Agent 04
  ↓
Agent 05
  ↓
Agent 06
  ↓
Agent 07
  ↓
Agent 08
  ↓
Agent 09
  ↓
Agent 10
  ↓
Agent 11
  ↓
Release Approval
  ↓
Deployment Approval
  ↓
PRODUCTION
```

A responsive defect may produce:

```text
Agent 08
   ↓
HIGH responsive issue
   ↓
Agent 07
   ↓
Fix
   ↓
Agent 08
   ↓
PASS
   ↓
Agent 09
```

An accessibility defect may produce:

```text
Agent 09
   ↓
HIGH accessibility issue
   ↓
Agent 07
   ↓
Fix
   ↓
Agent 09
   ↓
PASS
   ↓
Agent 10
```

---

# 22.25 Execution Rules Summary

The Agentic Website Factory follows these rules:

1. Sequential execution is the default.
2. Parallel execution is permitted only for independent activities.
3. Parallel activities must synchronize before dependent work continues.
4. Conditional execution must be explicitly recorded.
5. Human approval cannot be bypassed.
6. Rework must return to the smallest affected stage.
7. Rework must not create uncontrolled loops.
8. Interrupted projects must support resume execution.
9. Full restart should be exceptional.
10. Existing artifacts must be preserved for traceability.
11. Downstream agents must respect approved upstream decisions.
12. Missing dependencies must block execution.
13. Failed agents must not silently produce incomplete outputs.
14. Retries must be controlled.
15. Every significant execution decision must be traceable.
16. No agent may declare the entire website production-ready unless that responsibility is explicitly assigned to the workflow's final release process.
17. Final production deployment requires human approval.

---

# 22.26 Section Completion Criteria

Section 22 is complete when the Agentic Website Factory has clearly defined:

* Sequential execution
* Parallel execution
* Conditional execution
* Human-gated execution
* Rework execution
* Resume execution
* Controlled restart
* Dependency validation
* Execution readiness
* Execution states
* Failure handling
* Retry rules
* Artifact synchronization
* Source-of-truth enforcement
* Execution traceability
* QA rework behavior
* Human approval preservation

The execution model must remain compatible with the 11-agent architecture and MASTER_WORKFLOW.

---

# 22.27 Next Section

Section 23 will define the **Agent Dependency and Handoff Model**, including:

* Agent-to-agent dependencies
* Required inputs
* Produced outputs
* Dependency types
* Handoff conditions
* Handoff validation
* Blocked handoffs
* Upstream/downstream relationships
* Artifact-based handoffs
* Machine-readable handoff information
* Dependency visualization
# SECTION 23 — AGENT DEPENDENCY AND HANDOFF MODEL

## 23.1 Purpose

The Agentic Website Factory consists of 11 specialized agents.

Each agent performs a defined responsibility and produces artifacts required by downstream agents.

To maintain reliability, the workflow must explicitly define:

* Agent dependencies
* Required inputs
* Produced outputs
* Upstream relationships
* Downstream relationships
* Handoff conditions
* Handoff validation
* Dependency status
* Blocked handoffs
* Rework handoffs
* Human approval dependencies
* Machine-readable dependency information

The objective is to ensure that no agent begins work without the information required to perform its responsibility correctly.

---

# 23.2 Core Handoff Principle

An agent does not hand off work simply because it has finished executing.

A handoff occurs only when:

1. Required work is complete.
2. Required artifacts exist.
3. Required artifacts are valid.
4. Required dependencies are satisfied.
5. Required approvals exist.
6. Blocking issues are resolved or explicitly accepted.
7. The receiving agent can consume the outputs.

The basic model is:

```text
UPSTREAM AGENT
      ↓
CREATE ARTIFACTS
      ↓
VALIDATE ARTIFACTS
      ↓
CHECK DEPENDENCIES
      ↓
CHECK APPROVALS
      ↓
HANDOFF
      ↓
DOWNSTREAM AGENT
```

---

# 23.3 Agent Dependency Chain

The primary dependency chain is:

```text
01 Business Discovery
        ↓
02 UX / Information Architecture
        ↓
03 Content Strategy
        ↓
04 UI/UX Design
        ↓
05 Design System
        ↓
06 Frontend Architecture
        ↓
07 Development
        ↓
08 Responsive QA
        ↓
09 Accessibility QA
        ↓
10 SEO / Performance QA
        ↓
11 Production QA
```

The dependency chain represents the default execution order.

It does not prevent controlled parallel activities defined in Section 22.

---

# 23.4 Agent 01 — Business Discovery Dependencies

### Upstream

Agent 01 is the entry point of the agent workflow.

It receives:

* Client requirements
* Business information
* Existing website information
* Brand information
* Business documents
* Presentations
* Reference materials
* Client goals
* Target audience information
* Business constraints
* Available assets

### Produces

Agent 01 produces the approved business foundation.

Examples:

```text
business-brief.md
```

Additional artifacts defined by the Agent 01 specification must also be available.

### Downstream

Primary consumer:

```text
Agent 02 — UX / Information Architecture
```

Agent 03 may also consume relevant business discovery information.

### Handoff Condition

Agent 01 may hand off when:

* Business objectives are documented.
* Target audience is documented.
* Business offerings are understood.
* Conversion goals are documented.
* Important constraints are documented.
* Unknowns are identified.
* Required business decisions are recorded.
* Required artifacts exist.

---

# 23.5 Agent 02 — UX / Information Architecture Dependencies

### Upstream

Primary dependency:

```text
Agent 01
```

Agent 02 consumes the approved business foundation.

### Required Inputs

Examples:

```text
business-brief.md
```

and other Agent 01 outputs required by the UX specification.

Agent 02 may also receive approved client decisions.

### Produces

Examples:

```text
sitemap.md
page-architecture.md
user-flows.md
navigation.md
conversion-strategy.md
```

### Downstream

Primary consumers:

```text
Agent 03
Agent 04
Agent 06
```

### Handoff Condition

Agent 02 may hand off when:

* Sitemap is defined.
* Page architecture is defined.
* Navigation is defined.
* Important user flows are defined.
* Conversion paths are defined.
* UX decisions are documented.
* Open questions are resolved or recorded.

---

# 23.6 Agent 03 — Content Strategy Dependencies

### Upstream

Agent 03 primarily depends on:

```text
Agent 01
Agent 02
```

### Required Inputs

Examples:

```text
business-brief.md
sitemap.md
page-architecture.md
user-flows.md
conversion-strategy.md
```

### Produces

Examples:

```text
content-strategy.md
homepage-content.md
page-content.md
services-content.md
projects-content.md
trust-content.md
cta-strategy.md
content-components.md
```

### Downstream

Primary consumers:

```text
Agent 04
Agent 07
```

Content may also inform Agent 05 and Agent 06 where required.

### Handoff Condition

Agent 03 may hand off when:

* Required page content is defined.
* Content hierarchy is defined.
* CTA strategy is defined.
* Content components are defined.
* Business claims are traceable to approved information.
* Missing content is explicitly identified.

---

# 23.7 Agent 04 — UI/UX Design Dependencies

### Upstream

Agent 04 depends on:

```text
Agent 02
Agent 03
```

It also consumes approved business requirements.

### Required Inputs

Examples:

```text
sitemap.md
page-architecture.md
user-flows.md
navigation.md
content-strategy.md
homepage-content.md
page-content.md
```

and relevant business/brand assets.

### Produces

Examples:

```text
design-direction.md
ui-page-specifications.md
component-specifications.md
design-tokens.md
responsive-specification.md
interaction-specification.md
accessibility-specification.md
stitch-figma-specification.md
ai-developer-handoff.md
```

### Downstream

Primary consumers:

```text
Agent 05
Agent 06
Agent 07
```

### Human Gate

UI/UX design may require a formal human design approval gate.

The handoff must not proceed when the required design approval is:

```text
CHANGES_REQUESTED
REJECTED
BLOCKED
```

### Handoff Condition

Agent 04 may hand off when:

* Required page designs are defined.
* Component specifications are defined.
* Responsive behavior is defined.
* Interaction behavior is defined.
* Accessibility requirements are defined.
* Design handoff information is complete.
* Required human approval is obtained.

---

# 23.8 Agent 05 — Design System Dependencies

### Upstream

Agent 05 primarily depends on:

```text
Agent 04
```

### Required Inputs

Examples:

```text
design-direction.md
ui-page-specifications.md
component-specifications.md
design-tokens.md
responsive-specification.md
interaction-specification.md
accessibility-specification.md
```

### Produces

Examples:

```text
design-system-overview.md
design-system-tokens.md
component-library.md
component-contracts.md
responsive-system.md
accessibility-system.md
motion-system.md
figma-implementation-guide.md
stitch-implementation-guide.md
ai-studio-implementation-guide.md
claude-agent-implementation-guide.md
```

Machine-readable artifacts may include:

```text
design-system.tokens.json
design-system.components.json
```

### Downstream

Primary consumers:

```text
Agent 06
Agent 07
```

### Handoff Condition

Agent 05 may hand off when:

* Design tokens are defined.
* Component contracts are defined.
* Responsive rules are defined.
* Accessibility rules are defined.
* Motion rules are defined.
* Implementation guidance is available.
* Machine-readable artifacts are valid where required.

---

# 23.9 Agent 06 — Frontend Architecture Dependencies

### Upstream

Agent 06 depends on the approved:

```text
Agent 02 UX
Agent 04 UI/UX Design
Agent 05 Design System
```

It also considers content and business requirements.

### Required Inputs

Examples:

```text
sitemap.md
page-architecture.md
ui-page-specifications.md
component-specifications.md
design-system-overview.md
design-system-tokens.md
component-contracts.md
```

### Produces

Examples:

```text
frontend-architecture.md
technology-stack.md
project-structure.md
routing-architecture.md
page-component-map.md
component-architecture.md
data-architecture.md
responsive-architecture.md
asset-architecture.md
state-management.md
form-architecture.md
accessibility-architecture.md
seo-architecture.md
performance-architecture.md
testing-architecture.md
ai-development-contract.md
```

Machine-readable output:

```text
frontend-architecture.json
```

### Downstream

Primary consumer:

```text
Agent 07 — Development
```

### Handoff Condition

Agent 06 may hand off when:

* Technology stack is defined.
* Project structure is defined.
* Routing is defined.
* Component architecture is defined.
* Data architecture is defined.
* Asset architecture is defined.
* Form architecture is defined where applicable.
* Accessibility architecture is defined.
* SEO architecture is defined.
* Performance architecture is defined.
* Testing architecture is defined.
* AI development contract is defined.
* Required machine-readable architecture artifact is valid.

---

# 23.10 Agent 07 — Development Dependencies

### Upstream

Agent 07 depends on the combined approved foundation from Agents 01–06.

Primary implementation dependencies include:

```text
Agent 01 — Business
Agent 02 — UX
Agent 03 — Content
Agent 04 — Design
Agent 05 — Design System
Agent 06 — Architecture
```

### Required Inputs

Agent 07 must verify:

* Business requirements
* UX architecture
* Approved content
* UI/UX specifications
* Design system
* Design tokens
* Component contracts
* Frontend architecture
* Routing architecture
* Asset architecture
* Accessibility architecture
* SEO architecture
* Performance architecture
* Machine-readable artifacts

### Produces

Primary output:

```text
WEBSITE/
```

Development documentation includes:

```text
development-status.md
implementation-changelog.md
implementation-notes.md
development-qa.md
```

### Downstream

```text
Agent 08
Agent 09
Agent 10
Agent 11
```

### Handoff Condition

Agent 07 may hand off when:

* Website implementation exists.
* Required pages are implemented.
* Components are implemented.
* Content is implemented.
* Approved assets are implemented.
* Routes work.
* Responsive implementation exists.
* Approved interactions are implemented.
* Accessibility-aware implementation exists.
* SEO foundation exists.
* Performance foundations exist.
* Development validation is complete.
* Known issues are documented.
* Required outputs exist.

Agent 07 must not declare the website production-ready.

---

# 23.11 Agent 08 — Responsive QA Dependencies

### Upstream

Primary dependency:

```text
Agent 07
```

Agent 08 consumes the implemented website and relevant design specifications.

### Required Inputs

Examples:

```text
WEBSITE/
responsive-specification.md
responsive-system.md
ui-page-specifications.md
development-status.md
```

### Produces

Examples:

```text
responsive-qa-report.md
responsive-qa.json
```

along with the other artifacts defined by the Agent 08 specification.

### Downstream

Primary consumer:

```text
Agent 09
```

### Rework Dependency

If implementation defects are identified:

```text
Agent 08
   ↓
Finding
   ↓
Agent 07
   ↓
Fix
   ↓
Agent 08
```

### Handoff Condition

Agent 08 may hand off when:

* Required viewports are tested.
* Required pages are tested.
* Responsive defects are documented.
* Blocking responsive defects are resolved or explicitly accepted.
* Rework has been revalidated.
* Required QA artifacts exist.

---

# 23.12 Agent 09 — Accessibility QA Dependencies

### Upstream

Primary dependency:

```text
Agent 07
```

Agent 09 also consumes relevant findings from Agent 08.

### Required Inputs

Examples:

```text
WEBSITE/
accessibility-specification.md
accessibility-system.md
accessibility-architecture.md
development-status.md
responsive QA findings
```

### Produces

Examples:

```text
accessibility-fix-list.md
accessibility-qa-report.md
accessibility-qa.json
```

### Downstream

Primary consumer:

```text
Agent 10
```

### Rework Dependency

```text
Agent 09
   ↓
Accessibility Finding
   ↓
Agent 07
   ↓
Fix
   ↓
Agent 09
   ↓
Revalidation
```

If the issue originates in an upstream design or architecture decision, the workflow may route the issue to the affected upstream stage.

### Handoff Condition

Agent 09 may hand off when:

* Required accessibility checks are complete.
* Findings are documented.
* Blocking issues are resolved or explicitly accepted.
* Required remediation is complete.
* Revalidation is complete.
* Machine-readable QA artifact exists.

---

# 23.13 Agent 10 — SEO / Performance Dependencies

### Upstream

Primary dependencies:

```text
Agent 07
Agent 08
Agent 09
```

Agent 10 consumes the implemented website and relevant QA results.

### Required Inputs

Examples:

```text
WEBSITE/
seo-architecture.md
performance-architecture.md
responsive QA results
accessibility QA results
development status
```

### Produces

Machine-readable output:

```text
seo-performance-qa.json
```

Additional reports and fix lists are defined by the Agent 10 specification.

### Downstream

Primary consumer:

```text
Agent 11
```

### Rework Dependency

Implementation problems may return to Agent 07.

Example:

```text
Agent 10
   ↓
Performance Issue
   ↓
Agent 07
   ↓
Fix
   ↓
Agent 10
   ↓
Revalidation
```

### Handoff Condition

Agent 10 may hand off when:

* Required SEO checks are complete.
* Performance checks are complete.
* Findings are documented.
* Blocking issues are resolved or accepted.
* Required revalidation is complete.
* Machine-readable QA artifact is valid.

---

# 23.14 Agent 11 — Production QA Dependencies

### Upstream

Agent 11 depends on:

```text
Agent 07
Agent 08
Agent 09
Agent 10
```

### Required Inputs

Examples:

```text
WEBSITE/
development status
responsive QA results
accessibility QA results
SEO / performance QA results
approved design
approved architecture
release requirements
```

### Produces

Production readiness artifacts defined by Agent 11.

These may include:

```text
production-qa-report.md
production-qa.json
release-readiness.md
```

The exact canonical filenames must follow the Agent 11 specification.

### Downstream

```text
Human Release Approval
```

followed by:

```text
Human Deployment Approval
```

### Handoff Condition

Agent 11 may recommend release only when:

* Production QA is complete.
* Required routes are verified.
* Critical functionality is verified.
* QA blockers are resolved.
* Required release checks are complete.
* Production risks are documented.
* Release readiness is explicitly reported.

Agent 11 does not independently deploy the website unless deployment responsibility is explicitly assigned elsewhere.

---

# 23.15 Dependency Types

Dependencies are classified into five categories.

## 1. Data Dependency

A downstream agent requires information produced by an upstream agent.

Example:

```text
Agent 01
   ↓
business-brief.md
   ↓
Agent 02
```

## 2. Artifact Dependency

A downstream agent requires a specific artifact.

Example:

```text
Agent 05
   ↓
design-system.tokens.json
   ↓
Agent 07
```

## 3. Decision Dependency

A downstream agent requires a decision before continuing.

Example:

```text
Design Decision
      ↓
Human Approval
      ↓
Agent 05
```

## 4. Validation Dependency

A downstream agent requires an upstream validation result.

Example:

```text
Agent 08
      ↓
Responsive QA
      ↓
Agent 09
```

## 5. Rework Dependency

A downstream or upstream stage must be re-executed because a defect was identified.

Example:

```text
Agent 09
   ↓
Finding
   ↓
Agent 07
   ↓
Agent 09
```

---

# 23.16 Handoff Package

Each agent handoff should contain enough information for the receiving agent to continue without reconstructing the previous agent's work.

A handoff package should identify:

```text
SOURCE AGENT
TARGET AGENT
PROJECT
STATUS
INPUT ARTIFACTS
OUTPUT ARTIFACTS
ARTIFACT VERSIONS
DECISIONS
APPROVALS
KNOWN ISSUES
BLOCKERS
REWORK STATUS
NEXT ACTION
```

---

# 23.17 Handoff Validation

Before a handoff is accepted, the receiving stage should verify:

### Identity

* Correct source agent
* Correct target agent
* Correct project

### Completeness

* Required artifacts exist.
* Required fields exist.
* Required machine-readable artifacts are present.

### Validity

* Artifacts can be read.
* Artifacts are internally consistent.
* Versions are identifiable.

### Approval

* Required human approvals exist.
* No required approval is missing.

### Dependencies

* Required upstream dependencies are satisfied.
* No unresolved blocking dependency exists.

---

# 23.18 Handoff Status

A handoff may have one of the following statuses:

```text
PENDING
```

```text
READY
```

```text
ACCEPTED
```

```text
REJECTED
```

```text
BLOCKED
```

```text
REWORK_REQUIRED
```

```text
SUPERSEDED
```

A downstream agent must not treat:

```text
PENDING
BLOCKED
REJECTED
REWORK_REQUIRED
```

as a valid completed handoff.

---

# 23.19 Blocked Handoff

A handoff is BLOCKED when required information or approval is unavailable.

Examples:

```text
Missing required artifact
```

```text
Conflicting specifications
```

```text
Pending human approval
```

```text
Unresolved critical defect
```

```text
Invalid machine-readable artifact
```

```text
Missing required asset
```

```text
Missing required business decision
```

The receiving agent must not fabricate the missing information.

---

# 23.20 Handoff Rejection

A receiving agent may reject a handoff when:

* Required artifacts are missing.
* Artifacts are invalid.
* Inputs contradict approved decisions.
* Required approvals are absent.
* The upstream agent has not completed required work.
* Blocking issues remain unresolved.
* The handoff does not satisfy the agent's entry criteria.

The rejection must be documented.

Example:

```text
HANDOFF REJECTED

Source:
Agent 06

Target:
Agent 07

Reason:
frontend-architecture.json is missing.

Required Action:
Agent 06 must regenerate the required artifact.
```

---

# 23.21 Artifact Versioning During Handoffs

When an upstream artifact changes after a downstream stage has already executed, the workflow must determine whether downstream artifacts are still valid.

Example:

```text
Agent 05
   ↓
design-system.tokens.json v1.0
   ↓
Agent 06
   ↓
Agent 07
```

If Agent 05 changes the tokens:

```text
design-system.tokens.json v2.0
```

the workflow must evaluate the impact.

Potential result:

```text
Agent 06 → Revalidation
Agent 07 → Rework
Agent 08 → Revalidation
```

The workflow must not assume that downstream outputs remain valid after a governing input changes.

---

# 23.22 Dependency Invalidation

A downstream artifact becomes INVALID when a governing upstream decision or artifact changes in a way that affects it.

Example:

```text
UX change
   ↓
Page architecture changes
   ↓
Design affected
   ↓
Design system potentially affected
   ↓
Architecture affected
   ↓
Development affected
   ↓
QA affected
```

The workflow must identify the affected downstream stages rather than automatically restarting the entire factory.

---

# 23.23 Machine-Readable Dependency Model

Where practical, dependency information should be represented in machine-readable form.

Example:

```json
{
  "source_agent": "07",
  "target_agent": "08",
  "dependency_type": "artifact",
  "required_artifacts": [
    "WEBSITE/",
    "development-status.md"
  ],
  "handoff_status": "READY",
  "blocking_issues": []
}
```

The exact schema may evolve as the orchestration layer matures.

Machine-readable artifacts must remain consistent with the human-readable workflow documentation.

---

# 23.24 Agent Dependency Matrix

The primary dependency relationship is:

| Agent                    | Primary Upstream | Primary Downstream     |
| ------------------------ | ---------------- | ---------------------- |
| 01 Business Discovery    | Client/Input     | 02                     |
| 02 UX / IA               | 01               | 03, 04, 06             |
| 03 Content               | 01, 02           | 04, 07                 |
| 04 UI/UX Design          | 02, 03           | 05, 06, 07             |
| 05 Design System         | 04               | 06, 07                 |
| 06 Frontend Architecture | 02, 04, 05       | 07                     |
| 07 Development           | 01–06            | 08, 09, 10, 11         |
| 08 Responsive QA         | 07               | 09, 11                 |
| 09 Accessibility QA      | 07, 08           | 10, 11                 |
| 10 SEO / Performance QA  | 07, 08, 09       | 11                     |
| 11 Production QA         | 07–10            | Human Release Approval |

This matrix represents the primary workflow relationship.

Individual projects may contain additional dependencies.

---

# 23.25 Handoff Ownership

The producing agent is responsible for producing complete outputs.

The receiving agent is responsible for validating that the handoff is usable.

The workflow controller is responsible for determining whether execution may proceed.

Human reviewers are responsible for decisions explicitly assigned to human approval gates.

No agent may transfer responsibility for its own required deliverables to another agent without an explicit workflow rule.

---

# 23.26 Handoff and Human Approval

When human approval is required:

```text
Agent
 ↓
Artifact
 ↓
Validation
 ↓
Human Review
 ↓
Approval Decision
 ↓
Handoff
```

If the human requests changes:

```text
Human
 ↓
CHANGES_REQUESTED
 ↓
Affected Agent
 ↓
Rework
 ↓
Validation
 ↓
Human Review
```

Human approval must therefore be treated as a dependency, not merely a notification.

---

# 23.27 Handoff and QA

QA agents do not automatically modify implementation artifacts.

The standard QA relationship is:

```text
Implementation
      ↓
QA
      ↓
Finding
      ↓
Implementation Agent
      ↓
Fix
      ↓
QA Revalidation
```

This preserves separation between:

* Implementation
* Validation
* Approval

---

# 23.28 Handoff Traceability

Every important handoff should be traceable.

The project should be able to answer:

```text
Which agent produced this artifact?
Which version was used?
Who consumed it?
When was it handed off?
Was it approved?
Was it rejected?
Was it reworked?
Which downstream stages were affected?
```

This information is essential for debugging and project recovery.

---

# 23.29 No Silent Handoffs

An agent must never silently assume:

* Missing requirements
* Missing content
* Missing assets
* Missing design decisions
* Missing architecture
* Missing approvals
* Missing QA results

If information is missing, the agent must report:

```text
BLOCKED
```

or:

```text
INPUT_REQUIRED
```

rather than inventing information.

---

# 23.30 Handoff Completion Criteria

A handoff is COMPLETE when:

* Source agent has completed its required responsibility.
* Required outputs exist.
* Required artifacts are valid.
* Required approvals exist.
* Dependencies are satisfied.
* Blocking issues are resolved or explicitly accepted.
* Receiving agent can begin work.
* Handoff status is recorded.

---

# 23.31 Section Completion Criteria

Section 23 is complete when the Agentic Website Factory has clearly defined:

* Agent-to-agent dependencies
* Upstream relationships
* Downstream relationships
* Required inputs
* Produced outputs
* Dependency types
* Handoff packages
* Handoff validation
* Handoff states
* Blocked handoffs
* Rejected handoffs
* Artifact versioning
* Dependency invalidation
* QA rework handoffs
* Human approval dependencies
* Machine-readable dependency information
* Dependency matrix
* Handoff ownership
* Handoff traceability

The dependency and handoff model must remain compatible with:

* The 11-agent architecture
* Section 21 — Workflow Orchestration and Execution
* Section 22 — Workflow Execution Modes
* The actual agent specifications
* The actual project folder structure
* Canonical artifact filenames
* Human approval gates
* QA rework loops
* Final release and deployment controls

---

# 23.32 Next Section

Section 24 will define the **Artifact Contract and Data Exchange Model**, including:

* Artifact standards
* Artifact types
* Human-readable artifacts
* Machine-readable artifacts
* Required metadata
* Naming conventions
* Versioning
* Status
* Ownership
* Validation
* Artifact dependencies
* JSON contract principles
* Artifact immutability
* Artifact updates
* Artifact supersession
* Artifact traceability
* Agent consumption rules
# 24. Artifact Contract and Data Exchange Model

## 24.1 Purpose

The Agentic Website Factory relies on explicit artifacts to move information between stages.

Because Version 1 does not use a centralized database or complex event-driven orchestration, the project files themselves act as the official contracts between agents.

Section 24 defines the rules for how artifacts are created, formatted, updated, and consumed.

The objective is to ensure that data exchange remains reliable, predictable, and traceable whether the workflow is executed manually by a human or driven by an automated system.

---

## 24.2 Artifact as a Contract

An artifact is not merely a summary of work; it is a binding agreement within the workflow.

When an upstream agent produces an artifact and hands it off, it guarantees that the information within meets the requirements of its assigned stage.

When a downstream agent consumes that artifact, it must accept the information as the approved source of truth for its own work.

If a downstream agent cannot fulfill its duties based on the artifact provided, the artifact contract is broken, and the workflow must enter a blocked or rework state.

---

## 24.3 Artifact Types

Version 1 supports two primary types of artifacts, which are often used in tandem:

1. **Human-Readable Artifacts**
2. **Machine-Readable Artifacts**

Artifacts must not introduce proprietary formats that require specialized software to read, outside of standard design tool exports (for example, Figma files), which must still be accompanied by a standard artifact summary.

---

## 24.4 Human-Readable Artifacts

Human-readable artifacts form the primary record of project decisions, instructions, and context.

These artifacts must use **Markdown (`.md`)**.

They must be written clearly enough for a project manager, client, or developer to read, understand, and approve.

Markdown artifacts communicate the **why** and the **how** of project decisions.

---

## 24.5 Machine-Readable Artifacts

Machine-readable artifacts are used when structured data is required for technical downstream implementation.

These artifacts must use **JSON (`.json`)**.

Examples include:

* `design-system.tokens.json`
* `design-system.components.json`
* `frontend-architecture.json`
* `responsive-qa.json`
* `seo-performance-qa.json`

Machine-readable artifacts should only be introduced when they provide concrete downstream value, such as feeding design tokens directly into a frontend build system.

### The Consistency Rule

When both a Markdown and a JSON artifact exist for a single stage, they must not contradict each other.

---

## 24.6 Required Metadata

Every major Markdown artifact should begin with a standard metadata block at the top of the document.

This provides immediate context and traceability.

The required standard metadata format is:

```text
Artifact: [Name of the Artifact]
Producing Agent: [Agent Number and Name]
Project: [Client/Project Name]
Status: [Current Status]
Last Updated: [YYYY-MM-DD]
```

This ensures that any human or future automated system can instantly identify the file's origin and validity.

---

## 24.7 Naming Conventions

Artifacts must use predictable, standard filenames.

The naming rules are:

* Files must be entirely lowercase.
* Words must be separated by hyphens (`kebab-case`).
* Filenames must reflect the content.
* Filenames must align with the agent's specifications.

Examples:

```text
business-brief.md
ui-page-specifications.md
frontend-architecture.json
responsive-qa.json
```

Unpredictable naming conventions are strictly prohibited.

For example:

```text
Final_Design_V2_Updated.md
latest-final-final.md
new-version-copy.md
```

---

## 24.8 Versioning and Traceability

Version 1 relies on standard Git version control to maintain the history of artifact changes.

The factory does not require a proprietary or complex internal versioning system.

Traceability is maintained through:

* Git commit history.
* The `Last Updated` date in the artifact metadata block.
* The `DECISIONS/` directory for major project pivots and decisions.

---

## 24.9 Artifact Status

Artifact metadata must reflect a clear status.

Valid statuses include:

### `DRAFT`

The artifact is currently being worked on and is not ready for downstream use.

### `REVIEW_PENDING`

The artifact is complete but awaits human approval or upstream validation.

### `APPROVED`

The artifact is finalized and acts as the binding contract for downstream agents.

### `CHANGES_REQUESTED`

The artifact failed a review or QA check and requires rework.

### `SUPERSEDED`

The artifact is no longer the active source of truth, for example due to a major scope change or replacement artifact.

---

## 24.10 Artifact Ownership

The agent assigned to a specific factory stage is the sole owner of that stage's artifacts.

### The Rule of Ownership

For example:

> Agent 07 (Development) cannot modify `sitemap.md`.

Only Agent 02 (UX / Information Architecture) can modify `sitemap.md`.

If a downstream agent requires a change to an upstream artifact, the request must be routed back to the owning agent.

Downstream agents must not silently modify upstream artifacts.

---

## 24.11 Artifact Validation

Before an artifact is handed off, it must be validated by the producing agent.

Validation checks include:

* Is the metadata block present and correct?
* Are all required sections completed?
* Are there unresolved placeholder texts such as `TBD`?
* Are required dependencies available?
* Does the JSON artifact pass basic syntax validation?
* Does the artifact match the requirements of the producing agent?

Incomplete artifacts must not be marked as `APPROVED`.

---

## 24.12 Artifact Dependencies

Artifacts often depend on information contained in preceding artifacts.

If an upstream artifact changes its status from `APPROVED` to `CHANGES_REQUESTED`, all downstream artifacts that depend on it must be flagged for review.

This ensures downstream work remains aligned with the current source of truth.

---

## 24.13 JSON Contract Principles

Where JSON artifacts are used, they must remain strictly lean and predictable.

The rules for JSON artifacts are:

### Flat Structures

Avoid unnecessary deep nesting.

### No Duplicated Documentation

Do not include long paragraphs of explanatory text inside JSON files.

Explanations belong in the associated Markdown artifact.

### Strict Keys

Keys must remain consistent across projects so downstream automated systems can map them predictably.

### Valid JSON

JSON artifacts must be syntactically valid before handoff.

---

## 24.14 Artifact Immutability

Once an artifact is marked `APPROVED` and handed off to the next stage, it is considered locked.

Downstream agents must treat locked artifacts as immutable instructions.

They cannot be silently overridden during implementation.

If a downstream agent identifies an issue with an approved artifact, it must initiate the rework or escalation process rather than modifying the artifact directly.

---

## 24.15 Artifact Updates and Supersession

If a locked artifact must be changed due to:

* A QA failure
* A technical constraint
* A client scope change
* A business decision
* A missing dependency
* A discovered conflict

The workflow must follow the controlled supersession process.

### Controlled Supersession Process

1. The rework request is routed back to the owning agent.
2. The owning agent updates the artifact.
3. The metadata status is updated.
4. The `Last Updated` date is changed.
5. The updated artifact is reviewed and approved again where required.
6. Downstream agents relying on the old artifact are notified that their governing input has changed.
7. Affected downstream stages are re-executed or re-validated.

---

## 24.16 Agent Consumption Rules

When a downstream agent begins execution, it must strictly follow these consumption rules.

### Step 1 — Locate

Find the required upstream artifacts in the designated project folders.

### Step 2 — Verify

Check the metadata to confirm that the artifact is `APPROVED`.

### Step 3 — Consume

Use the information according to the artifact contract and source-of-truth hierarchy.

An agent must never silently "fix" or alter what it perceives as an error in an upstream artifact.

If an input is flawed, incomplete, contradictory, or missing, the downstream agent must:

1. Stop the affected work.
2. Document the issue.
3. Identify the affected artifact.
4. Identify the owning agent.
5. Flag the workflow for rework or escalation.

---

## 24.17 Section Completion Criteria

Section 24 is complete when the Agentic Website Factory has clearly defined:

* The role of artifacts as binding contracts.
* Formatting rules for Markdown and JSON.
* Required metadata and statuses.
* Predictable naming conventions.
* Strict ownership rules.
* Artifact immutability rules.
* Artifact validation requirements.
* Artifact dependency rules.
* The update and supersession process.
* How downstream agents consume artifacts safely.

---

## 24.18 Next Section

Section 25 defines the Human Approval Gates, including:

* The philosophy of human-in-the-loop validation.
* Required approval points.
* Approval states and decision recording.
* Escalation paths for blocked approvals.

---

# 25. Human Approval Gates

## 25.1 Purpose

The Agentic Website Factory is human-led and agent-assisted.

While the 11 specialized agents execute the heavy lifting of production, QA, and documentation, they do not have the authority to make final business or release decisions.

Section 25 defines the formal Human Approval Gates.

These gates act as circuit breakers in the workflow, ensuring that the project remains aligned with client expectations and business requirements before significant downstream effort is expended or a product is released to the public.

---

## 25.2 Philosophy of Human-in-the-Loop

Version 1 operates on a philosophy of meaningful intervention.

Humans should not be forced to approve every minor artifact, JSON file, or intermediate handoff.

Micromanagement defeats the purpose of an agentic factory.

Instead, human approval is reserved exclusively for major project milestones where subjective judgment, client sign-off, or critical business risk is involved.

The guiding principle is:

```text
Agents handle execution and validation
            ↓
Humans handle direction and authorization
```

---

## 25.3 The Required Approval Gates

To maintain a lean workflow, Version 1 mandates a minimum of two hard approval gates.

A project may not proceed past these points without explicit human authorization.

### Gate 1 — Design Approval

**Location in Workflow:**

After Agent 04 (UI/UX Design) and before Agent 05 (Design System).

**Purpose:**

To confirm that the proposed visual experience, page layouts, and interaction patterns meet the client's expectations and business goals.

**Why It Matters:**

Proceeding into design system tokenization, frontend architecture, and development without approved designs can lead to significant and costly rework if the client rejects the visual direction later.

---

### Gate 2 — Final Production Approval

**Location in Workflow:**

After Agent 11 (Production QA) and before actual deployment.

**Purpose:**

To authorize the release of the implemented website to the public.

**Why It Matters:**

AI agents can validate code, check accessibility, and verify responsive behavior, but only a human can accept the final business and operational risk and authorize a live deployment.

> A project manager may introduce additional gates, such as Business Brief Approval after Agent 01, but Design Approval and Final Production Approval are the mandatory minimum gates for Version 1.

---

## 25.4 Approval States

When a project reaches an approval gate, the human reviewer must record a clear decision using one of the following states.

### `APPROVED`

The work is accepted as is.

The workflow may proceed immediately to the next stage.

### `APPROVED_WITH_NOTES`

The work is accepted and the workflow may proceed, but minor adjustments or considerations are recorded for downstream agents.

### `CHANGES_REQUESTED`

The work is not accepted.

The workflow is paused and the artifact is returned to the responsible agent for rework based on the documented feedback.

### `REJECTED`

The work fundamentally misses the required outcome.

This may trigger a project reset to an earlier stage.

For example:

```text
Design Approval Rejected
        ↓
Return to Content Strategy
        ↓
Or
        ↓
Return to Business Discovery
```

### `BLOCKED`

The human reviewer cannot make a decision due to:

* Missing external information
* Pending client feedback
* An unresolved dependency
* An unresolved conflict

The workflow remains paused.

---

## 25.5 Decision Recording

Human approvals must not be given informally, for example through a verbal "looks good."

They must be explicitly recorded in the project file structure to maintain traceability.

Approvals should be stored in the dedicated `APPROVALS/` directory.

Example:

```text
APPROVALS/
└── design-approval.md
```

Example approval artifact:

```text
---
Gate: Design Approval
Reviewer: [Human Name/Role]
Date: [YYYY-MM-DD]
Status: APPROVED_WITH_NOTES
---

### Notes for Downstream

- The overall design is approved.
- Ensure the hero animation remains lightweight for mobile performance.
```

---

## 25.6 Managing Rework at Approval Gates

If a human reviewer issues a `CHANGES_REQUESTED` status, the workflow follows the established rework loop.

### Approval Rework Process

1. The human documents the specific issues required for approval.
2. The workflow routes the feedback back to the responsible agent.
3. The responsible agent processes the feedback.
4. The affected artifact is updated.
5. The `Last Updated` date is changed.
6. The artifact is submitted for review again.
7. Downstream agents remain paused until the required approval is achieved.

---

## 25.7 Escalation Paths

If a project becomes stuck at an approval gate, the workflow requires human escalation.

Examples include:

* Repeated `CHANGES_REQUESTED` cycles.
* Conflicting client feedback.
* Unclear requirements.
* An extended `BLOCKED` state.

Agents cannot force an approval.

If an approval loop repeats more than three times, a human project manager must intervene to:

* Resolve conflicting requirements.
* Clarify vague feedback.
* Redefine the project scope.
* Determine the appropriate stage for rework.

---

## 25.8 Section Completion Criteria

Section 25 is complete when the Agentic Website Factory has clearly defined:

* The philosophy of human-in-the-loop validation.
* The two mandatory approval gates.
* The standardized approval states.
* How and where to record human decisions.
* How approval-related rework is managed.
* How blocked or repeated approval loops are escalated.

---

## 25.9 Next Section

Section 26 defines Deployment Readiness, including:

* The transition from Code Complete to Ready for Deployment.
* Final environment configuration checks.
* The role of the human deployer in Version 1.
* Deployment execution and rollback requirements.

---

# 26. Deployment Readiness

## 26.1 Purpose

Section 26 defines the Deployment Readiness stage of the Agentic Website Factory.

Its purpose is to establish the exact conditions that must be met before a website is moved from a completed development state into a live production environment.

Deployment Readiness bridges the gap between Agent 11 (Production QA and Release Readiness) and the actual operational release of the website.

It ensures that the infrastructure, configuration, and business timing align with the completed technical implementation.

---

## 26.2 Deployment Philosophy

Version 1 of the Agentic Website Factory is strictly human-controlled at the deployment phase.

While agents write code, run QA, and generate deployment configuration artifacts, an AI agent must not autonomously push code to a live production domain without human authorization.

The guiding principle is:

```text
Agents prepare the release
        ↓
Humans authorize and execute the release
```

---

## 26.3 The "Ready for Deployment" State

A project is only considered `READY FOR DEPLOYMENT` when it has successfully cleared all required upstream gates.

Code completion by Agent 07 is not sufficient.

The required state before deployment can occur is:

```text
ALL REQUIRED AGENTS EXECUTED
        ↓
ALL REQUIRED QA STAGES PASSED
        ↓
OR ACCEPTED BLOCKERS FORMALLY DOCUMENTED
        ↓
AGENT 11 PRODUCES
"READY FOR HUMAN APPROVAL"
        ↓
FINAL HUMAN APPROVAL OBTAINED
        ↓
READY FOR DEPLOYMENT
```

If any of these conditions are unmet, the project is not ready for deployment.

---

## 26.4 Final Environment Configuration Checks

Before the human deployer executes the release, the production environment must be verified.

Deployment readiness includes confirming:

* Production domain name is correctly configured through DNS.
* SSL/TLS certificates are provisioned and active.
* Production environment variables are securely configured.
* Analytics and tracking codes are configured for production.
* Caching and CDN rules are appropriately configured.
* Development flags have been removed.
* Placeholder content has been removed.
* Test data has been removed.
* Production integrations are correctly configured.

The workflow must not store sensitive production credentials in plain text within project artifacts or source code.

---

## 26.5 The Role of the Human Deployer

The human deployer is responsible for the physical or triggered release of the website.

Their responsibilities include:

* Reviewing the final release readiness status produced by Agent 11.
* Confirming that Final Human Approval has been recorded.
* Applying required production environment variables.
* Executing the deployment action.
* Coordinating release timing with the client or business stakeholders.
* Confirming that rollback capability exists.

The human deployer accepts the operational responsibility of the final release.

---

## 26.6 Deployment Execution Methods

Version 1 does not mandate a single deployment technology.

However, the selected deployment method must be documented in the Frontend Architecture and project documentation.

Common deployment triggers include:

* Merging the approved codebase into the main or production Git branch.
* Approving a pending build on a hosting platform.
* Triggering a manual continuous deployment pipeline.
* Executing an approved release command.

The deployment mechanism must support the project's selected technology stack.

---

## 26.7 Rollback Planning

Deployment readiness requires a basic and documented understanding of how to undo a deployment if a critical production failure occurs.

For Version 1, this typically relies on standard modern hosting and Git capabilities.

The human deployer must ensure:

* The previous stable version is preserved or can be restored.
* Git history is clean enough to allow a quick revert.
* The deployment platform supports rollback where applicable.
* A critical production issue has a clear escalation path.

---

## 26.8 Post-Deployment Verification

Once deployment is executed, the release is not considered complete until basic post-deployment verification occurs on the live domain.

This includes:

* Verifying the live URL resolves correctly.
* Checking for redirect loops.
* Verifying SSL is active and secure.
* Testing at least one primary conversion action.
* Verifying critical assets load correctly.
* Checking for obvious layout failures.
* Checking for major console errors where applicable.

If post-deployment verification fails, the human deployer must initiate:

* A rollback, or
* An immediate hotfix process using the established QA and rework loops.

---

## 26.9 Workflow Completion

The Agentic Website Factory workflow is officially complete only when:

```text
FINAL HUMAN APPROVAL
        ↓
DEPLOYMENT EXECUTED
        ↓
POST-DEPLOYMENT VERIFICATION PASSED
        ↓
PROJECT MARKED COMPLETE
```

---

## 26.10 Section Completion Criteria

Section 26 is complete when the Agentic Website Factory has clearly defined:

* The difference between code completion and deployment readiness.
* The mandatory configuration checks before launch.
* The explicit operational role of the human deployer.
* Acceptable deployment execution methods.
* Rollback planning requirements.
* Post-deployment verification requirements.
* The criteria for absolute workflow completion.

---

# 27. Final Human Approval

## 27.1 Purpose

Section 27 defines the Final Human Approval stage of the Agentic Website Factory.

Its purpose is to provide the ultimate business and operational sign-off before a website is released to the public.

While Agent 11 determines whether a website is technically ready for release, only a human can accept the operational and business risk of actual deployment.

The Final Human Approval gate ensures that the project has successfully met client expectations and that all known risks are formally accepted.

---

## 27.2 The Approval Authority

Final approval cannot be granted by an AI agent.

The approval authority must be a designated human responsible for the project.

Depending on the organization, this may be:

* The Project Manager.
* The Technical Lead.
* The Client or Business Owner.
* The designated Deployment Manager.

The workflow must not allow automated scripts to bypass this authority in Version 1.

---

## 27.3 Prerequisites for Approval

The human approver should not be asked to review a project that is incomplete or failing QA.

Before the Final Human Approval gate can be opened, the following conditions must be met:

* All 11 agents have completed their required execution.
* Responsive QA has passed.
* Accessibility QA has passed.
* SEO and Performance QA has passed.
* Required Production QA checks have passed or approved exceptions are documented.
* Agent 11 has produced a status of `READY FOR HUMAN APPROVAL`.
* A formal Production QA artifact exists.
* The artifact is accessible to the human approver.
* The website is accessible in a staging or pre-production environment.

---

## 27.4 Review Scope

The human approver is not expected to re-run the detailed technical QA checks performed by the specialized agents.

The human review should focus on business readiness and high-level verification.

### Artifact Review

Review the Agent 11 Production QA report to understand the release status and any remaining non-blocking issues.

### Visual and Functional Confidence Check

Briefly interact with the staging website to confirm that:

* The overall look and feel meet expectations.
* Primary user journeys work.
* Important conversion actions function correctly.

For example:

```text
Homepage
    ↓
Primary CTA
    ↓
Contact Form
    ↓
Successful Submission
```

### Scope Verification

Confirm that the final product aligns with:

* Original business requirements.
* Approved content.
* Approved UX.
* Approved design.

### Risk Acceptance

Explicitly acknowledge any known and documented non-blocking issues that will be released into production.

---

## 27.5 Approval Outcomes

The human approver must issue a clear decision.

### `APPROVED FOR DEPLOYMENT`

The website is accepted.

The workflow proceeds to the deployment stage.

### `APPROVED WITH EXCEPTIONS`

The website is accepted for deployment, but specific non-blocking issues are documented for immediate post-launch resolution.

The workflow may proceed to deployment.

### `REJECTED / REWORK REQUIRED`

The human approver identifies a critical business, visual, functional, or scope failure.

The release is blocked.

The project is routed back to the responsible stage for correction.

---

## 27.6 Documenting the Decision

The final decision must be explicitly recorded in the project file structure.

It must be stored in the designated `APPROVALS/` directory.

Example:

```text
APPROVALS/
└── final-release-approval.md
```

Example artifact:

```text
---
Gate: Final Production Approval
Reviewer: [Human Name/Role]
Date: [YYYY-MM-DD]
Status: APPROVED FOR DEPLOYMENT
---

### Review Notes

- Agent 11 Production QA report reviewed.
- Staging environment verified.
- Known issue: slight layout shift on legacy mobile devices.
- Issue severity: Low.
- Risk accepted for production release.
- Authorized for immediate production deployment.
```

---

## 27.7 Handoff to Deployment

Once Final Human Approval is recorded as `APPROVED FOR DEPLOYMENT`, the workflow transitions to the final operational stage.

The conceptual flow is:

```text
AGENT 11
        ↓
READY FOR HUMAN APPROVAL
        ↓
HUMAN REVIEWER
        ↓
APPROVED FOR DEPLOYMENT
        ↓
HUMAN DEPLOYER EXECUTES RELEASE
        ↓
PRODUCTION
```

---

## 27.8 Handling Post-Approval Changes

If a significant change is made after Final Human Approval but before deployment, the approval is immediately invalidated.

Significant changes may include:

* Code changes.
* Configuration changes.
* Content changes.
* Integration changes.
* Dependency changes.

The project must return to Agent 11 for release re-verification.

A new Final Human Approval must then be recorded.

---

## 27.9 Section Completion Criteria

Section 27 is complete when the Agentic Website Factory has clearly defined:

* The absolute requirement for human authorization before deployment.
* The prerequisites required before human release review.
* The scope of human review.
* The valid approval outcomes.
* How approval outcomes route the workflow.
* The method for documenting final approval.
* The rules for invalidating approval after significant changes.

---

# 28. Version 1 Execution Model

## 28.1 Purpose

Section 28 defines the practical, day-to-day execution model for Version 1 of the Agentic Website Factory.

Because Version 1 intentionally avoids complex orchestration platforms, event-driven databases, and autonomous agent-to-agent communication, it requires a reliable manual execution method.

This section explains how a human Project Manager or Developer operates the factory using standard AI tools and a structured file system.

---

## 28.2 The Human as Orchestrator

In Version 1, the human operator acts as the workflow engine.

The human is responsible for:

* Creating the project folder structure.
* Managing project artifacts.
* Triggering the appropriate AI model with the correct context.
* Validating that the agent output meets stage requirements.
* Saving outputs as official project artifacts.
* Managing artifact statuses.
* Managing human approval gates.
* Routing rework between agents.

This keeps the process transparent, controllable, and easy to debug.

---

## 28.3 Tool Independence

The execution model is strictly tool-agnostic.

The agents defined in this factory are fundamentally roles and instruction sets, not locked-in software applications.

A human operator can execute an agent using:

### Chat Interfaces

* ChatGPT
* Claude
* Google AI Studio
* Gemini

### AI-Assisted IDEs

* Cursor
* Windsurf
* GitHub Copilot

### Design Tools with AI

* Figma
* Stitch

The factory defines:

* What must be done.
* What information must be consumed.
* What outputs must be produced.

The operator chooses the most appropriate tool for the specific agent stage.

---

## 28.4 Step-by-Step Execution Cycle

To execute a single stage of the factory, the operator follows this standard manual cycle.

### Step 1 — Preparation

The operator navigates to the current stage.

For example:

```text
03-content/
```

The operator reviews the required upstream artifacts.

For example:

```text
01-business-discovery/business-brief.md
02-ux/sitemap.md
02-ux/page-architecture.md
```

The operator confirms that required inputs are approved and ready for consumption.

---

### Step 2 — Context Assembly

The operator provides the required upstream artifacts and the relevant Agent Instruction Prompt to the selected AI tool.

For example:

```text
Agent Prompt:
03_Content_Strategy_Agent.md

Required Inputs:
business-brief.md
sitemap.md
page-architecture.md
```

---

### Step 3 — Execution

The operator instructs the AI to perform its assigned analysis and generate the required outputs.

If the AI:

* Asks clarifying questions.
* Detects missing inputs.
* Produces incomplete work.
* Detects conflicts.

The human operator manages the issue and ensures the stage follows the defined workflow.

---

### Step 4 — Artifact Extraction

Once the AI produces a satisfactory result, the operator saves the output into the appropriate project file.

For example:

```text
03-content/
└── content-strategy.md
```

---

### Step 5 — Validation and Handoff

The operator:

1. Validates the output.
2. Adds the required metadata.
3. Updates the artifact status.
4. Marks the artifact as `APPROVED` when appropriate.
5. Submits the artifact for human approval when an approval gate applies.
6. Proceeds to the next workflow stage once all dependencies are satisfied.

---

## 28.5 Project State Tracking

Because Version 1 does not use a central database, project state is tracked through:

* The file system.
* Artifact metadata.
* Git history.
* Approval artifacts.

For quick project visibility, the project team may optionally use a simple Kanban board.

Examples include:

* GitHub Projects.
* Trello.
* Jira.
* Notion.

The suggested workflow states are:

```text
BACKLOG
        ↓
01 — BUSINESS DISCOVERY
        ↓
02 — UX / IA
        ↓
03 — CONTENT STRATEGY
        ↓
04 — UI/UX DESIGN
        ↓
[GATE: DESIGN APPROVAL]
        ↓
05 — DESIGN SYSTEM
        ↓
06 — FRONTEND ARCHITECTURE
        ↓
07 — DEVELOPMENT
        ↓
08 — RESPONSIVE QA
        ↓
09 — ACCESSIBILITY QA
        ↓
10 — SEO / PERFORMANCE QA
        ↓
11 — PRODUCTION QA
        ↓
[GATE: FINAL APPROVAL]
        ↓
DEPLOYMENT
        ↓
DEPLOYED
```

The project board mirrors the actual state of the project artifacts.

The file system remains the source of truth.

---

## 28.6 Managing the Development Stage (Agent 07)

The Development stage is uniquely intensive.

While earlier stages such as Business Discovery, UX, and Content can often be executed in a standard chat interface, Agent 07 is generally best executed within an AI-assisted development environment.

### Recommended Execution Pattern

1. The operator opens the `WEBSITE/` directory in the selected development environment.
2. The operator provides the approved architecture, design system, content, UI specifications, and required development artifacts.
3. The AI development environment is instructed to implement the website step-by-step.
4. The operator validates each major implementation phase.
5. The local application is tested.
6. Code changes are committed to Git.
7. Development handoff artifacts are created.
8. The completed application proceeds to the QA stages.

The development process should follow the phase sequence defined by Agent 07.

---

## 28.7 Managing QA and Rework

When running QA Agents 08 through 11, the human operator acts as the bridge between the QA process and the development environment.

### QA Execution Pattern

1. The operator provides the implemented website or staging environment to the relevant QA agent.
2. The QA agent performs its assigned validation.
3. The QA agent produces findings and required artifacts.
4. If defects exist, the operator routes the findings to the responsible stage.
5. Development or another owning agent processes the required fixes.
6. The affected QA stage is executed again.
7. The QA artifact is updated to reflect the final status.

Example:

```text
DEVELOPMENT
        ↓
RESPONSIVE QA
        ↓
ISSUES FOUND
        ↓
DEVELOPMENT REWORK
        ↓
RESPONSIVE QA RE-TEST
        ↓
PASS
```

---

## 28.8 Handling Context Limits

AI context windows are large but not infinite.

The human operator must practice context discipline.

An agent should only receive the artifacts explicitly required for its stage.

Examples:

* Do not provide the entire `WEBSITE/` codebase to the Content Strategy Agent.
* Do not provide unrelated business artifacts to a Responsive QA Agent unless required for a specific rule.
* Do not overload an AI model with every project file when only a subset is relevant.

Keep context focused so the AI remains aligned with its specific responsibilities.

---

## 28.9 Section Completion Criteria

Section 28 is complete when the Agentic Website Factory has clearly defined:

* The manual role of the human operator as workflow orchestrator.
* The tool-agnostic nature of the agents.
* The standard five-step execution cycle.
* How project state is tracked without a database.
* Practical execution guidance for Development.
* Practical execution guidance for QA and rework.
* The importance of context discipline.

---

# 29. Future Automation Path

## 29.1 Purpose

Section 29 defines how the manual, human-orchestrated workflow of Version 1 can evolve into a programmatic and increasingly automated pipeline in future versions.

Version 1 is intentionally manual to establish:

* Process stability.
* Clear boundaries.
* Reliable artifacts.
* Predictable handoffs.

Once the factory reliably produces high-quality websites through manual execution, automation can be introduced without automating an unstable process.

---

## 29.2 The Automation Philosophy

The guiding principle for evolving the factory is:

```text
PROCESS STABILITY FIRST
        ↓
TARGETED AUTOMATION SECOND
```

Automation must not:

* Change the core responsibilities of the 11 agents.
* Remove artifact contracts.
* Bypass required QA.
* Bypass mandatory human approval gates.

Automation should primarily remove friction from:

* Moving artifacts.
* Tracking state.
* Triggering agents.
* Running repetitive QA checks.
* Processing structured outputs.

---

## 29.3 High-Value Automation Targets

When transitioning to Version 2, the factory should not attempt to build a massive monolithic orchestration engine immediately.

Automation should be introduced incrementally.

### 1. Automated State Tracking

A script can read the metadata of project artifacts and automatically generate:

* Project status dashboards.
* Workflow progress.
* Blocked stage alerts.
* Missing artifact alerts.

This reduces manual status tracking.

---

### 2. QA Rework Loops

Automation can improve the handoff between Development and QA.

For example:

```text
NEW BUILD DETECTED
        ↓
AUTOMATED QA EXECUTED
        ↓
STRUCTURED RESULTS GENERATED
        ↓
DEVELOPMENT REWORK REQUEST CREATED
        ↓
NEW BUILD
        ↓
QA RE-RUN
```

Structured tools may generate results that feed directly into the QA and development workflow.

---

### 3. Machine-Readable Artifact Parsing

Scripts can automatically transform structured artifacts into implementation-ready formats.

For example:

```text
design-system.tokens.json
        ↓
CSS VARIABLES
        ↓
APPLICATION DESIGN TOKENS
```

Or:

```text
design-system.tokens.json
        ↓
TAILWIND CONFIGURATION
```

The exact implementation depends on the selected frontend architecture.

---

### 4. CI/CD Integration

Future versions may integrate the Git repository with the selected hosting provider.

However, deployment automation must still respect the Final Human Approval gate.

Conceptually:

```text
ALL QA PASSED
        ↓
FINAL HUMAN APPROVAL RECORDED
        ↓
DEPLOYMENT PIPELINE ENABLED
        ↓
PRODUCTION DEPLOYMENT
```

---

## 29.4 Transitioning to API Orchestration

In Version 1, a human operator manually provides prompts and artifacts to AI tools.

In a future version, the workflow can shift toward API-driven orchestration.

A lightweight orchestrator may:

1. Monitor upstream artifact directories.
2. Detect newly approved artifacts.
3. Read the required agent instructions.
4. Assemble the required context.
5. Call the selected AI model through an API.
6. Validate the response format.
7. Save generated outputs into the appropriate project directories.
8. Update workflow state.

The orchestrator should enforce the existing workflow rather than replacing its core principles.

---

## 29.5 The Role of the Model Context Protocol (MCP)

As the factory evolves, the Model Context Protocol (MCP) may be introduced to standardize how agents access external project context and tools.

Potential future integrations may include:

* Project management systems.
* Design systems.
* File storage.
* Design tools.
* Internal documentation.
* Approved business data sources.

This can reduce manual context assembly while maintaining controlled access to external systems.

Any future MCP integration must continue to respect:

* Artifact ownership.
* Source-of-truth rules.
* Access boundaries.
* Human approval gates.

---

## 29.6 Immutable Human Gates

Regardless of how advanced future automation becomes, the two core Human Approval Gates must remain immutable:

1. **Design Approval**
2. **Final Production Approval**

An automated orchestrator must halt execution when these gates are reached.

The system must wait for verifiable human authorization before proceeding.

Potential future verification methods may include:

* An approved artifact in the `APPROVALS/` directory.
* A verified project management approval.
* A documented approval record.
* Another approved organizational authorization mechanism.

Automated deployment without required human sign-off violates the core principles of the Agentic Website Factory.

---

## 29.7 Section Completion Criteria

Section 29 is complete when the Agentic Website Factory has clearly defined:

* The philosophy of proving the manual process before automation.
* The highest-value workflow areas to automate first.
* How manual execution can transition toward API-driven orchestration.
* The potential role of MCP for controlled context retrieval.
* The requirement that Human Approval Gates remain mandatory and immutable.

---

# END OF MASTER_WORKFLOW.md

This concludes the Version 1 Lean Architecture for the Agentic Website Factory.

The workflow now defines:

* The 11 specialized agents.
* Agent responsibilities and boundaries.
* Workflow orchestration.
* Artifact contracts.
* Agent dependencies.
* Parallel execution where applicable.
* QA rework loops.
* Machine-readable artifacts.
* Release readiness.
* Human approval gates.
* Deployment readiness.
* Final human authorization.
* The Version 1 manual execution model.
* The future automation path.

The Agentic Website Factory Version 1 workflow is now ready for active project execution.
