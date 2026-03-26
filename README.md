# mobile-app-design

mobile-app-design is an agent skill for designing mobile apps with production standards in mind. It is built for people who want better results than generic AI UI output and need a workflow that stays useful in real product work.

The skill detects design intent from natural prompts, fills in obvious context when possible, and only asks a small number of follow-up questions when the missing details would materially change the result.

## What this skill does

mobile-app-design helps an agent turn a simple request such as “I want to build a fitness mobile app” into a structured design process with clear outputs for product, design, and engineering.

It covers context gathering, flow design, visual system definition, mobile states, platform patterns, quality gates, and implementation handoff.

It also includes a style library with general mobile styles and BI or analytics dashboard styles so the design direction is chosen intentionally instead of falling back to a generic template.

## Why this skill is useful

Most design prompts fail for the same reason. They are too open ended, too generic, or too eager to jump into screens before the product context is clear.

This skill solves that by giving the agent a disciplined path.

First, it detects the likely domain and product goal from the user prompt.

Second, it asks only the minimum number of questions needed when the request is still too ambiguous.

Third, it applies production constraints that matter on mobile, including safe areas, touch targets, keyboard handling, performance, accessibility, and platform-specific behavior.

Fourth, it checks the result against anti-generic rules so the output does not look like a recycled AI template.

## Core strengths

1. Intent detection from simple prompts.

2. Minimal clarification flow instead of a long interview.

3. Stage-based design process from discovery to engineering handoff.

4. Mobile-specific guardrails for iOS, Android, and cross-platform work.

5. Built-in style selection for stronger art direction.

6. Explicit quality gates before final output.

7. Better support for real product states such as loading, empty, error, offline, degraded network, keyboard visible, and permission flows.

## How it works

The skill follows a fixed process.

Step 1 is context gathering. The agent identifies the user, use case, tone, platform scope, and product goal.

Step 2 is structure. The agent maps screens, actions, and transitions.

Step 3 is visual direction. The agent selects a general style and, when relevant, a dashboard style.

Step 4 is state coverage. The agent defines success, loading, empty, error, offline, and recovery behavior.

Step 5 is validation. The agent applies quality gates and checks for generic output.

Step 6 is handoff. The result is shaped so engineering can implement it.

## Installation

Install the skill from GitHub with:

```bash
npx skills add raffimh/mobile-app-design-skills
```

If your skill runner supports installing from a local path, you can also add it from your cloned repository after download.

## Repository

The publish target for this skill is:

```text
https://github.com/raffimh/mobile-app-design-skills.git
```

## Usage

You can invoke the skill with direct product prompts.

Example 1

```text
I want to create a fitness mobile app for beginners who want guided home workouts.
```

Expected behavior:

The agent should detect a greenfield mobile app request, identify fitness as the domain, infer likely goals such as workout discovery and progress tracking, then ask only a small number of useful questions if critical details are still missing.

Example 2

```text
Design a mobile app for personal finance with a strong focus on budgeting and weekly spending insights.
```

Expected behavior:

The agent should define the domain, choose a fitting mobile style direction, structure the primary flow, include trust-oriented patterns, and return screens and states that are implementation-ready.

Example 3

```text
I need a mobile analytics dashboard for warehouse operations. Keep it readable on smaller phones.
```

Expected behavior:

The agent should recognize that dashboard styles are required, choose an analytics pattern such as Data-Dense Dashboard or Real-Time Monitoring, adapt it to mobile constraints, and include performance and scanability considerations.

Example 4

```text
Redesign our chat mobile app so it feels less generic and more trustworthy for parents tracking their children’s school transport.
```

Expected behavior:

The agent should preserve the mobile domain, avoid generic chat templates, and anchor the design to the actual trust, safety, and monitoring use case.

## Output shape

The skill is designed to return work in a stable structure.

Context and assumptions.

Flow and screen map.

Visual system.

Platform patterns.

State matrix.

Validation score and quality gates.

Implementation handoff.

## Included references

The skill package includes:

A main skill definition.

Input, output, and quality gate templates.

An anti-generic pattern reference.

A style library that includes general styles and BI or analytics dashboard styles.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
