# Agentic Website Factory – Master Workflow

## Version

1.0.0

---

# 1. Purpose

The Agentic Website Factory is a structured workflow for transforming client requirements, business information, presentations, brand assets, and reference materials into a production-ready website.

The factory uses 11 specialized AI agents.

Each agent is responsible for a specific stage of the website creation process.

The workflow ensures that:

* Each agent receives the correct inputs.
* Each agent produces defined outputs.
* Outputs are passed to the correct next agent.
* Human approval is used at important decision points.
* Quality assurance issues follow a controlled rework process.
* The final website is tested before deployment.

The core principle of the Agentic Website Factory is:

> Agents create artifacts. Approved artifacts become inputs for the next agent.

---

# 2. Master Workflow

```text
CLIENT INPUT
      │
      ▼
01 BUSINESS DISCOVERY
      │
      ▼
BUSINESS REVIEW & APPROVAL
      │
      ▼
02 UX & INFORMATION ARCHITECTURE
      │
      ▼
UX REVIEW & APPROVAL
      │
      ▼
03 CONTENT STRATEGY
      │
      ▼
CONTENT REVIEW & APPROVAL
      │
      ▼
04 UI/UX DESIGN
      │
      ▼
05 DESIGN SYSTEM
      │
      ▼
DESIGN REVIEW & APPROVAL
      │
      ▼
06 FRONTEND ARCHITECTURE
      │
      ▼
TECHNICAL REVIEW
      │
      ▼
07 DEVELOPMENT
      │
      ▼
08 RESPONSIVE QA
      │
      ▼
09 ACCESSIBILITY QA
      │
      ▼
10 SEO & PERFORMANCE
      │
      ▼
REWORK IF REQUIRED
      │
      ▼
11 PRODUCTION QA
      │
      ▼
FINAL HUMAN APPROVAL
      │
      ▼
GITHUB
      │
      ▼
CLOUDFLARE DEPLOYMENT
      │
      ▼
LIVE WEBSITE
```

---

# 3. Agent Sequence

The factory contains the following 11 specialized agents.

| Stage | Agent                               | Primary Responsibility                                            |
| ----- | ----------------------------------- | ----------------------------------------------------------------- |
| 01    | Business Discovery Agent            | Understand the business, audience, goals and website requirements |
| 02    | UX & Information Architecture Agent | Define sitemap, navigation, user journeys and page structure      |
| 03    | Content Strategy Agent              | Create messaging hierarchy and website content                    |
| 04    | UI/UX Design Agent                  | Define visual direction, page layouts and design requirements     |
| 05    | Design System Agent                 | Create reusable design tokens and component guidelines            |
| 06    | Frontend Architect Agent            | Define the technical and frontend architecture                    |
| 07    | Development Agent                   | Build the website                                                 |
| 08    | Responsive QA Agent                 | Test responsiveness across devices                                |
| 09    | Accessibility QA Agent              | Test accessibility and usability requirements                     |
| 10    | SEO & Performance Agent             | Review SEO and website performance                                |
| 11    | Production QA Agent                 | Perform final production readiness testing                        |

---

# 4. Project Start

Every client website project must begin with a structured project workspace.

Recommended project structure:

```text
ClientName-Website/
│
├── INPUT/
│   ├── client-brief.md
│   ├── client-documents/
│   ├── presentations/
│   ├── brand-assets/
│   ├── images/
│   └── reference-websites.md
│
├── OUTPUT/
│   ├── 01-business-discovery/
│   ├── 02-ux-information-architecture/
│   ├── 03-content-strategy/
│   ├── 04-ui-ux-design/
│   ├── 05-design-system/
│   ├── 06-frontend-architecture/
│   ├── 08-responsive-qa/
│   ├── 09-accessibility-qa/
│   ├── 10-seo-performance/
│   └── 11-production-qa/
│
├── APPROVALS/
│
├── DECISIONS/
│
└── WEBSITE/
```

The INPUT folder is the source of truth for client-provided information.

The OUTPUT folder contains the artifacts created by the agents.

The APPROVALS folder stores human approval decisions.

The DECISIONS folder records important business, design and technical decisions.

The WEBSITE folder contains the final website source code.

---

# 5. Stage 01 – Business Discovery

## Agent

01_Business_Discovery_Agent

## Inputs

The Business Discovery Agent receives:

* Client brief
* Client presentation
* Business documents
* Existing website information
* Brand assets
* Target audience information
* Reference websites
* Client goals

## Responsibilities

The agent identifies:

* Business model
* Business goals
* Target audience
* Customer problems
* Core services
* Unique selling propositions
* Brand positioning
* Website objectives
* Primary conversion goals
* Secondary conversion goals
* Assumptions and risks

## Outputs

The Business Discovery Agent should produce:

```text
01-business-discovery/
├── business-brief.md
├── target-audience.md
├── brand-positioning.md
├── conversion-goals.md
└── assumptions-and-risks.md
```

## Next Stage

02 UX & Information Architecture Agent

---

# 6. Human Approval Gate – Business Strategy

Before the UX stage begins, the following should be reviewed:

* Business Brief
* Target Audience
* Brand Positioning
* Conversion Goals

Possible status:

```text
APPROVED
CHANGES REQUIRED
BLOCKED
```

Only approved business direction should proceed to the next stage.

---

# 7. Stage 02 – UX & Information Architecture

## Agent

02_UX_Information_Architecture_Agent

## Inputs

The agent receives approved outputs from:

```text
01-business-discovery/
```

## Responsibilities

The agent defines:

* Sitemap
* Navigation
* Page hierarchy
* User journeys
* Conversion flows
* Page objectives
* Content hierarchy

## Outputs

```text
02-ux-information-architecture/
├── sitemap.md
├── navigation-structure.md
├── user-flows.md
└── page-requirements.md
```

## Next Stage

03 Content Strategy Agent

---

# 8. Stage 03 – Content Strategy

## Agent

03_Content_Strategy_Agent

## Inputs

```text
01-business-discovery/
02-ux-information-architecture/
```

## Responsibilities

The agent creates:

* Messaging strategy
* Headlines
* Supporting copy
* Website content
* CTA strategy
* Trust-building content
* Content hierarchy

## Outputs

```text
03-content-strategy/
├── messaging-framework.md
├── website-content.md
├── cta-strategy.md
└── content-inventory.md
```

## Next Stage

04 UI/UX Design Agent

---

# 9. Stage 04 – UI/UX Design

## Agent

04_UI_UX_Design_Agent

## Inputs

```text
01-business-discovery/
02-ux-information-architecture/
03-content-strategy/
```

## Responsibilities

The agent defines:

* Visual direction
* Website style
* Page layouts
* Section hierarchy
* Component requirements
* Image requirements
* Interaction requirements

The output may be used with design tools such as:

* Stitch
* Figma
* Gemini
* Other AI design tools

## Outputs

```text
04-ui-ux-design/
├── design-brief.md
├── visual-direction.md
├── page-layouts.md
├── component-specification.md
└── design-tool-prompts.md
```

## Next Stage

05 Design System Agent

---

# 10. Stage 05 – Design System

## Agent

05_Design_System_Agent

## Inputs

```text
04-ui-ux-design/
```

## Responsibilities

The agent defines:

* Color system
* Typography
* Spacing
* Layout rules
* Design tokens
* Component styles
* Interaction guidelines

## Outputs

```text
05-design-system/
├── design-tokens.md
├── colors.md
├── typography.md
├── spacing.md
├── components.md
└── interaction-guidelines.md
```

## Next Stage

06 Frontend Architect Agent

---

# 11. Human Approval Gate – Design

Before technical implementation begins, the following should be reviewed:

* Visual Direction
* Page Layouts
* Component Specification
* Design System

Possible status:

```text
APPROVED
CHANGES REQUIRED
BLOCKED
```

---

# 12. Stage 06 – Frontend Architecture

## Agent

06_Frontend_Architect_Agent

## Inputs

```text
02-ux-information-architecture/
04-ui-ux-design/
05-design-system/
```

## Responsibilities

The agent defines:

* Technology stack
* Project structure
* Component architecture
* Routing
* Asset strategy
* Responsive strategy
* Performance strategy
* Implementation plan

## Outputs

```text
06-frontend-architecture/
├── technical-architecture.md
├── technology-stack.md
├── project-structure.md
├── component-architecture.md
└── implementation-plan.md
```

## Next Stage

07 Development Agent

---

# 13. Stage 07 – Development

## Agent

07_Development_Agent

## Inputs

The Development Agent receives approved outputs from:

```text
03-content-strategy/
04-ui-ux-design/
05-design-system/
06-frontend-architecture/
```

## Responsibilities

The agent:

* Builds the website
* Creates reusable components
* Implements responsive layouts
* Uses the approved design system
* Implements website content
* Maintains clean project structure
* Avoids unnecessary dependencies

## Development Sequence

```text
1. Project setup
2. Global styles
3. Design tokens
4. Layout structure
5. Navigation
6. Hero section
7. Core sections
8. Reusable components
9. Additional pages
10. Forms and interactions
11. Final integration
```

## Output

The final source code is stored in:

```text
WEBSITE/
```

---

# 14. Stage 08 – Responsive QA

## Agent

08_Responsive_QA_Agent

## Responsibilities

The agent tests:

* Mobile layouts
* Tablet layouts
* Desktop layouts
* Navigation behavior
* Layout overflow
* Typography scaling
* Image responsiveness
* Touch interactions

## Outputs

```text
08-responsive-qa/
├── responsive-report.md
└── responsive-issues.md
```

---

# 15. Stage 09 – Accessibility QA

## Agent

09_Accessibility_QA_Agent

## Responsibilities

The agent reviews:

* Semantic HTML
* Heading hierarchy
* Keyboard navigation
* Focus states
* Color contrast
* Alternative text
* Form labels
* ARIA usage

## Outputs

```text
09-accessibility-qa/
├── accessibility-report.md
└── accessibility-issues.md
```

---

# 16. Stage 10 – SEO & Performance

## Agent

10_SEO_Performance_Agent

## Responsibilities

### SEO

The agent reviews:

* Page titles
* Meta descriptions
* Heading hierarchy
* Semantic structure
* Image optimization
* Structured data requirements

### Performance

The agent reviews:

* Image sizes
* JavaScript usage
* CSS efficiency
* Loading strategy
* Performance bottlenecks

## Outputs

```text
10-seo-performance/
├── seo-report.md
├── performance-report.md
└── optimization-tasks.md
```

---

# 17. QA Rework Loop

QA agents identify problems.

QA agents should not independently change the business strategy or design direction.

Issues should follow this process:

```text
QA ISSUE
   │
   ▼
ISSUE CLASSIFICATION
   │
   ├── Development Issue
   │        │
   │        ▼
   │   Development Agent
   │
   ├── Design Issue
   │        │
   │        ▼
   │   UI/UX Design Agent
   │
   └── Requirement Issue
            │
            ▼
       Human Decision
```

After changes:

```text
FIX
 ↓
RETEST
 ↓
PASS / FAIL
```

---

# 18. Stage 11 – Production QA

## Agent

11_Production_QA_Agent

## Responsibilities

The Production QA Agent performs the final review.

The review includes:

### Functional Testing

* Navigation
* Links
* Forms
* CTAs

### Visual Testing

* Layout consistency
* Missing assets
* Broken components

### Responsive Testing

* Mobile
* Tablet
* Desktop

### Accessibility

* Critical accessibility issues resolved

### SEO

* Metadata complete

### Performance

* Major performance issues resolved

## Outputs

```text
11-production-qa/
├── production-readiness-report.md
└── release-checklist.md
```

---

# 19. Final Human Approval

The final production decision must be reviewed by a human.

Possible status:

```text
APPROVED FOR DEPLOYMENT
CHANGES REQUIRED
NOT APPROVED
```

---

# 20. Deployment Workflow

The website can proceed to deployment only when:

```text
Production QA = PASSED
        +
Human Approval = APPROVED
        +
GitHub Repository = UPDATED
```

Deployment process:

```text
LOCAL DEVELOPMENT
        │
        ▼
GITHUB
        │
        ▼
PREVIEW DEPLOYMENT
        │
        ▼
FINAL VALIDATION
        │
        ▼
PRODUCTION DEPLOYMENT
        │
        ▼
LIVE WEBSITE
```

---

# 21. Tool Mapping

The Agentic Website Factory may use different tools at different stages.

| Stage                 | Possible Tools                        |
| --------------------- | ------------------------------------- |
| Business Discovery    | ChatGPT / Claude / Gemini             |
| UX & IA               | ChatGPT / Claude / Gemini             |
| Content Strategy      | ChatGPT / Claude / Gemini             |
| UI/UX Design          | Stitch / Figma / Gemini               |
| Design System         | Stitch / Figma / AI Tools             |
| Frontend Architecture | ChatGPT / Claude / Gemini             |
| Development           | AI Studio / Claude / Cursor / VS Code |
| QA                    | Browser Testing / AI Agents           |
| Version Control       | GitHub                                |
| Deployment            | Cloudflare                            |

The tool may change over time.

The workflow and artifact structure should remain independent of a specific AI tool.

---

# 22. Core Factory Principle

The Agentic Website Factory operates using the following principle:

> Client inputs become structured business artifacts.
> Business artifacts become UX artifacts.
> UX artifacts become content and design artifacts.
> Approved design artifacts become technical architecture.
> Technical architecture becomes implementation.
> Implementation passes through quality assurance.
> Approved implementation becomes a production website.

The goal is not simply to generate websites.

The goal is to create a repeatable, controlled and scalable website production system.

---

# 23. Definition of Done

A project is considered complete only when:

* Business requirements are documented.
* Target audience is defined.
* Business goals are approved.
* UX architecture is complete.
* Website content is complete.
* Design direction is approved.
* Design system is documented.
* Frontend architecture is defined.
* Website development is complete.
* Responsive QA is completed.
* Accessibility QA is completed.
* SEO and performance reviews are completed.
* Production QA passes.
* Final human approval is received.
* The website is deployed successfully.

---

# End of Master Workflow
