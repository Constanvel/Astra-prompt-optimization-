```md
# Astra Prompt Optimizer

> A prompt optimization tool designed to transform rough instructions into clear, structured, and effective prompts for Astra.

## Overview

**Astra Prompt Optimizer** is a tool focused on improving prompts before they are sent to Astra.

Instead of simply making prompts longer, the optimizer analyzes the user's original intent and rewrites the prompt so Astra can understand the task more accurately.

The goal is simple:

> **Better instructions → better Astra output.**

---

## Why This Project?

Prompts are often written quickly and may contain:

- Vague instructions
- Missing context
- Unclear requirements
- Repetitive wording
- Undefined constraints
- No expected output format

For example:

```text
make my game boss harder and better
```

This works, but it leaves many decisions unclear.

Astra Prompt Optimizer can turn it into something more actionable:

```text
Improve the existing boss fight while preserving the current gameplay system.

Goals:
- Increase the overall difficulty.
- Make attack patterns more challenging but still readable.
- Add more attack pattern variations.
- Avoid unfair or unavoidable damage.
- Gradually increase difficulty throughout the fight.

Implementation:
- Reuse the existing gameplay systems where possible.
- Do not rewrite working systems unnecessarily.
- Keep the code organized and maintainable.
```

The optimized version gives Astra much clearer direction while preserving the user's original request.

---

## Main Goal

This project aims to act as a:

> **Prompt compiler for Astra**

It converts human instructions into prompts that are:

- Clear
- Structured
- Specific
- Efficient
- Context-aware
- Easy for Astra to execute

The goal is **not to generate the longest possible prompt**.

The goal is to generate the **most useful prompt with the least unnecessary complexity**.

---

## How It Works

The optimizer follows a simple process:

```text
Raw User Prompt
       ↓
Intent Analysis
       ↓
Context Detection
       ↓
Missing Information Detection
       ↓
Prompt Restructuring
       ↓
Constraint Optimization
       ↓
Astra-Optimized Prompt
```

The optimizer should determine:

1. What the user wants to achieve
2. What information is already provided
3. Which instructions are unclear
4. What additional detail would improve the task
5. What should remain unchanged
6. What constraints should be added
7. What output format would work best

---

## Core Optimization Principles

### 1. Preserve User Intent

The optimized prompt should never change the user's actual objective.

It may clarify or expand the request, but it should not introduce unrelated features or requirements.

---

### 2. Improve Specificity

Vague instructions should become actionable.

Example:

```text
make the UI better
```

Becomes:

```text
Improve the UI hierarchy, spacing, readability, and visual consistency while preserving the existing layout and functionality.
```

---

### 3. Add Structure When Needed

Complex requests should be organized into clear sections such as:

```text
Task
Context
Goals
Requirements
Behavior
Constraints
Implementation Notes
Expected Result
```

Simple prompts should remain simple.

---

### 4. Prevent Unnecessary Changes

For coding tasks, the optimizer may add instructions such as:

```text
- Inspect the existing implementation first.
- Preserve working functionality.
- Reuse the current project structure.
- Avoid unnecessary dependencies.
- Do not rewrite working components without a clear reason.
```

---

### 5. Avoid Prompt Bloat

A better prompt is not automatically a longer prompt.

The amount of detail should scale with the complexity of the task.

Simple requests should stay concise.

Complex coding or implementation tasks may require more structure and detail.

---

## Optimization Levels

The application may support multiple optimization levels.

### Light

Small improvements to wording and clarity.

Best for simple requests.

### Balanced

Improves clarity, structure, specificity, constraints, and expected output.

This should be the default mode.

### Detailed

Transforms the user's request into a more complete implementation specification.

Best for:

- Coding tasks
- Debugging
- Large features
- UI/UX work
- Game development
- Refactoring
- Complex implementation tasks

---

## Optimization Modes

The optimizer may support different modes depending on the user's task.

Planned modes include:

- General
- Coding
- Debugging
- UI/UX
- Game Development
- Feature Implementation
- Refactoring
- Research

Each mode can use different prompt structures and optimization strategies.

---

## Example

### Input

```text
make the enemy attacks harder and less repetitive
```

### Optimized Output

```text
Improve the existing enemy attack system to make combat more difficult and less repetitive.

Goals:
- Increase attack variety.
- Prevent the enemy from repeatedly using the same pattern.
- Introduce multiple attack sequences.
- Make pattern selection feel dynamic.
- Gradually increase difficulty during the fight.

Gameplay Constraints:
- Attacks should remain readable.
- Avoid unavoidable or unfair damage.
- Preserve the current movement and collision systems.
- Do not remove existing working mechanics.

Implementation:
- Reuse the current attack system where possible.
- Add controlled variation instead of completely random behavior.
- Keep the implementation maintainable and easy to modify later.
```

---

## Coding Prompt Optimization

For programming-related prompts, the optimizer should consider:

### Context

What project, file, system, or feature is being modified?

### Goal

What exactly should change?

### Existing Behavior

What currently happens?

### Desired Behavior

What should happen instead?

### Constraints

Examples:

```text
- Preserve the existing architecture.
- Reuse existing components.
- Avoid unnecessary refactoring.
- Maintain current functionality.
- Avoid unnecessary dependencies.
```

### Code Quality

When appropriate:

```text
- Keep the code readable.
- Avoid duplicated logic.
- Handle edge cases.
- Keep the implementation maintainable.
- Do not introduce regressions.
```

---

## Astra-Oriented Prompt Structure

For larger requests, optimized prompts may follow this structure:

```text
Task

Context

Goals

Requirements

Behavior

Constraints

Implementation Notes

Expected Result
```

However, not every prompt needs every section.

The optimizer should prioritize:

> **Clarity over template consistency.**

---

## Prompt Quality Check

Before returning an optimized prompt, the system should verify that it clearly answers:

1. What needs to be done?
2. What is the main objective?
3. What should remain unchanged?
4. What behavior is expected?
5. What constraints exist?
6. What counts as a successful result?
7. Are all instructions actually necessary?

If an important detail is missing, the optimizer should improve the prompt before returning it.

---

## Planned Features

- Prompt rewriting
- Automatic intent detection
- Prompt complexity detection
- Astra-oriented prompt formatting
- Optimization level selection
- Task-specific optimization modes
- Original vs optimized prompt comparison
- Copy optimized prompt button
- Prompt quality analysis
- Optional explanation of improvements

Future versions may also include:

- Prompt history
- Custom optimization presets
- Model-specific optimization profiles
- Prompt scoring
- Prompt templates
- Local prompt storage
- User-created optimization rules
- Multiple output variants

---

## Design Philosophy

The optimizer should not simply add more words.

It should make the prompt:

- Easier to understand
- Easier to execute
- Less ambiguous
- More structured
- More useful for Astra

The optimizer should always preserve the user's original goal.

---

## Project Status

🚧 **Currently in development**

The prompt optimization system, Astra-specific behavior, and optimization strategies are still being researched, tested, and improved.

---

## Project Philosophy

Astra Prompt Optimizer follows one main principle:

> **Maximum instruction quality with minimum unnecessary complexity.**

A good prompt should help Astra:

- Understand the task faster
- Make fewer incorrect assumptions
- Preserve existing work when necessary
- Follow requirements more accurately
- Produce results closer to what the user actually wants

---

## Contributing

Ideas, improvements, prompt examples, and optimization strategies are welcome.

If you discover a prompt structure that consistently produces better Astra results, feel free to open an issue or contribute to the project.

---

## License

License information will be added as the project develops.
```
