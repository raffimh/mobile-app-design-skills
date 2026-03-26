---
name: mobile-app-design
description: Build or refine mobile app UI/UX to production quality (not generic AI-looking output). Use this whenever the user asks to design/redesign mobile screens, flows, app UI, onboarding, checkout, chat, dashboards, component specs, or .pen-based artifacts for mobile apps.
---

# Mobile App Design — Production Skill

This skill produces mobile app designs that are implementation-ready, accessible, performant, and clearly non-generic.

## 0) Context Gathering Protocol (Required)

Do not design until required context is confirmed.

Required context:
- target audience
- top user jobs/use cases
- brand personality/tone

Also collect mobile-specific context:
- platform scope (`ios`, `android`, `both`)
- usage context (one-hand, field usage, low connectivity, etc.)
- success KPI for the flow

Rules:
- Do not infer audience/tone from code alone.
- Ask up to 3 clarification questions if critical context is missing.
- If unanswered, continue with explicit `Assumptions`.

## 1) Trigger Rules

Use this skill when the user requests any of the following:
- new mobile app screens/flows
- mobile UI redesign or UI improvements
- fixes for visual hierarchy, spacing, consistency, or UX states
- design outputs for engineering handoff (`.pen`, design specs, tokens, state maps)

Do not use this skill when:
- the task is purely backend/API/database
- the task is copywriting-only without UI changes
- the task is logic bugfixing without visual/interaction changes

## 2) Input Contract

Before designing, collect these minimum inputs:
1. `product_domain`
2. `target_user` + `user_goal` (JTBD)
3. `primary_flow`
4. `platform` (`ios`, `android`, `both`)
5. `screen_scope`
6. `design_constraints` (brand/system constraints)
7. `success_metric`
8. `device_scope` (small/standard/large phones)
9. `state_requirements` (offline/permissions/slow network if applicable)

If anything is missing:
- ask **up to 3 clarification questions**
- if still unanswered, continue with explicit `Assumptions`

Use template: `templates/input-contract.md`.

## 3) Mode Selection

Pick one mode:
- `greenfield` → design from scratch
- `feature-extension` → add new screens/flows
- `redesign` → improve existing screens/flows
- `system-aligned` → strict compliance with existing design system

If `system-aligned`, prefer DS components first and document any custom exceptions.

## 4) Process (Stage-Gated)

Follow this order. Do not skip stages.

### Stage A — Discover
- understand product context + constraints
- identify existing design system/components
- define **3 domain anchors** (required domain-specific elements)
- define mobile constraints (safe area, reachability, keyboard, connectivity)

Output:
- context summary
- mode
- assumptions
- domain anchors

### Stage B — Structure
- create screen map + flow map
- each screen must have 1 primary action
- define key components per screen
- ensure no dead-end state transitions

Output:
- screen list and purpose
- navigation between screens
- reusable vs custom components

### Stage C — Visual System
- define tokens: color, typography, spacing, radius, elevation
- use consistent spacing grid (base 4/8)
- define explicit typography hierarchy
- define platform-appropriate iconography and navigation patterns
- select style direction from `references/style-library.md`:
  - one **General Style** (required)
  - one **BI/Analytics Dashboard Style** (required only when dashboard/analytics is in scope)

Output:
- design tokens
- component styling rules
- interaction density rules
- selected style(s) + why they fit the product context

### Stage D — States & Recovery
- every screen must include at least: `success`, `loading`, `empty`, `error`
- add `offline/permission denied` when relevant
- every error state must include a recovery path
- add `network-degraded` and `keyboard-visible` when relevant
- include behavior for dynamic text scaling

Output:
- state matrix per screen
- feedback behavior (toast, inline error, disabled/loading button)

### Stage E — Validation
- score quality with a 0-100 rubric
- run quality gates P0/P1/P2
- if any P0 fails, revise before final output

Output:
- score + rationale
- pass/fail checklist
- tradeoff log (max 5 points)

Use output template: `templates/output-structure.md`.

## 5) Production Baselines (Non-Negotiable)

### Touch target
- iOS: minimum 44x44pt
- Android: minimum 48x48dp

### Accessibility
- normal text contrast minimum 4.5:1
- component/focus contrast minimum 3:1
- focus state must be clearly visible
- logical screen-reader order must be preserved

### Consistency
- avoid random spacing values (e.g. 13px, 17px, 21px)
- all screens must use the same token system

### Platform conventions
- iOS and Android must follow native interaction patterns when platform-specific

### Safe area & keyboard
- keep tappable controls out of notch/home-indicator conflict zones
- avoid keyboard overlap in forms and composer areas

### Device adaptation
- define behavior for small, standard, and large phones
- preserve task completion in portrait-first layout

### Performance baseline
- transitions should feel smooth at 60fps target
- avoid heavy visual effects that degrade scrolling and input responsiveness

## 6) Anti-Generic Guardrails

Avoid these generic patterns unless explicitly requested:
- default nav without domain context (random Home/Search/Profile/Settings)
- generic metric dashboard with no relation to user goals
- contextless generic placeholder copy

Required:
- each screen includes >=2 domain-specific elements
- each key decision includes concise rationale
- do not add out-of-scope features without user approval
- do not ship "template defaults" as final direction

Detailed anti-pattern list: `references/anti-generic-patterns.md`.

## 6.1) Design Direction Requirement

Before producing final output, commit to an explicit design direction:
- purpose
- tone/style direction
- differentiation point (what makes this interface memorable)

Direction must be intentional and consistent with user context.

Style selection must reference `references/style-library.md` and include rationale.

## 7) Quality Gates

### P0 (must pass before final)
- 100% of requirements mapped to UI
- every screen has complete states (success/loading/empty/error)
- no dead-end flows
- baseline accessibility requirements met
- safe area + keyboard-safe interactions verified
- platform conventions respected for selected platform

### P1
- token consistency across screens
- high design system reuse (target >=80% in system-aligned mode)
- clear, action-oriented microcopy
- degraded network/offline behavior defined where relevant
- list/content performance risks documented

### P2
- smooth, meaningful micro-interactions
- visual polish (rhythm, balance, detail)
- additional edge cases handled

### Scoring Rubric (0-100)
- Design system consistency: 25
- UX/usability and flow clarity: 25
- Engineering feasibility/performance: 25
- Visual polish/non-genericity: 25

Use checklist: `templates/quality-gates.md`.

## 7.1) AI Slop Test (Mandatory)

Before finalizing, run this check:
- If this output looks like a generic template from another domain, revise.
- If differentiation depends only on colors/gradients, revise.
- If content can be swapped with another product without UX changes, revise.

## 8) Required Output Format

Always return output in this order:
1. `Context & Assumptions`
2. `Flow & Screen Map`
3. `Visual System`
4. `Platform Patterns`
5. `State Matrix`
6. `Validation Score + Gates`
7. `Implementation Handoff`

Each section must include:
- `Decision`
- `Rationale`
- `Constraints`
- `Implementation Notes`

## 9) Engineering Handoff Rules

When the user asks for implementation-ready output:
- include tokens that can be translated to code
- specify reusable components and key props
- provide testable acceptance criteria
- mark technical risks (if any)
- specify platform-specific behavior (iOS vs Android) when needed
- include accessibility props and state behavior requirements

## 9.1) Platform-Specific Patterns

### iOS
- use iOS-native navigation and gesture expectations
- maintain clear back navigation and reachable primary actions

### Android
- use Material-style navigation/feedback patterns when requested
- ensure back behavior is predictable and consistent

## 10) Failure Handling

If requirements conflict:
1. prioritize P0 (usability + accessibility + flow completion)
2. explain tradeoff briefly
3. ask the user to choose option A/B if business impact is significant
