
# Research Observations

## Overview

This document records observations made during the AI Agent Evaluation Research project.

Observations may include successful behaviours, failures, unexpected behaviour, recurring patterns, and other information noticed during experimental trials.

Observations recorded here are not automatically considered research findings.

A finding should only be reported in `Findings.md` when sufficient evidence supports the conclusion.

The purpose of this document is therefore to preserve potentially important behaviours without prematurely drawing conclusions.

---

# Observation Principles

When recording observations:

- Record what actually happened.
- Separate observation from interpretation.
- Avoid changing observations after later results are known.
- Record failures as well as successes.
- Include the relevant experiment and trial.
- Include the AI system/model where known.
- Link to supporting evidence where possible.
- Clearly identify speculation or possible explanations.
- Do not treat a single observation as evidence of general model behaviour.

---

# Observation vs Interpretation

It is important to distinguish between what happened and why it may have happened.

## Example

### Observation

> The agent executed the same unsuccessful tool action three times despite receiving an error after each attempt.

### Interpretation

> This may indicate difficulty adapting tool-use strategy after repeated failure.

The observation is evidence.

The interpretation is a possible explanation that requires additional testing.

---

# Observation Status

Observations may use the following status labels.

## Single Observation

Observed once.

## Repeated Observation

Observed in multiple trials.

## Candidate Pattern

Observed often enough to justify targeted testing.

## Supported Finding

Sufficient evidence has been collected and the result has been summarised in `Findings.md`.

---

# Observation Categories

Observations may be classified using the following categories:

- Context retention
- Requirement understanding
- Reasoning
- Tool selection
- Tool execution
- Code generation
- Debugging
- Computer use
- Verification
- Error recovery
- Efficiency
- Regression avoidance
- Project safety
- Human intervention
- Game-development efficiency
- Unexpected behaviour

Multiple categories may apply to one observation.

---

# Observation Record Template

Copy this section for each significant observation.

---

## Observation ID

OBS-___

### Date

YYYY-MM-DD

### Experiment

-

### Test

-

### Trial

-

### AI System

-

### Model

-

### Agent/Mode

-

### Environment

-

### Project

-

### Category

-

### Status

Single Observation

### Task Context

Briefly describe what the agent was attempting to do.

-

### Observation

Describe exactly what happened.

-

### Expected Behaviour

Describe what should have happened.

-

### Actual Behaviour

Describe what the agent actually did.

-

### Evidence

Examples:

- Tool output
- Runtime error
- Test result
- Git diff
- Screenshot
- Blender state
- Roblox Studio output
- Trial record

-

### Human Intervention

Level: /4

Description:

-

### Immediate Outcome

- [ ] Successful
- [ ] Partially successful
- [ ] Failed
- [ ] No effect on final result

### Interpretation

Possible explanation:

-

This interpretation is provisional and should not be treated as a confirmed finding without additional evidence.

### Follow-Up Test

-

### Related Observations

-

---

# Context Retention Observations

This section records behaviours involving project memory and previous decisions.

Potential observations include:

- Correct recall of previous decisions
- Forgotten constraints
- Contradictions
- Repeated completed work
- Confusion between projects
- Successful use of structured project context

## Recorded Observations

None recorded yet.

---

# Tool-Use Observations

This section records behaviours involving tool selection and execution.

Potential observations include:

- Correct tool selection
- Incorrect tool selection
- Failed tool calls
- Repeated failed actions
- Successful recovery
- Incorrect interpretation of tool output
- Failure to verify tool results

## Recorded Observations

None recorded yet.

---

# Code-Generation Observations

Potential observations include:

- Correct first-attempt code
- Syntax errors
- Runtime errors
- Incorrect APIs
- Unnecessary rewrites
- Effective debugging
- Regression introduction
- Successful self-correction

## Recorded Observations

None recorded yet.

---

# Computer-Use Observations

Potential observations include:

- Correct visual-state interpretation
- Incorrect UI-state assumptions
- Navigation errors
- Incorrect clicks
- Repeated actions
- Successful adaptation
- Failure to notice unsuccessful actions
- Successful verification

## Recorded Observations

None recorded yet.

---

# Blender Observations

Potential observations include:

- Scene-understanding accuracy
- Collection navigation
- Object identification
- Blender Python behaviour
- Material handling
- Asset organisation
- Project safety
- Long-horizon workflow behaviour

## Recorded Observations

None recorded yet.

---

# Roblox Observations

Potential observations include:

- Project hierarchy understanding
- Luau accuracy
- Client-server reasoning
- Remote communication
- Gameplay implementation
- Multiplayer reasoning
- Debugging
- Playtest verification

## Recorded Observations

None recorded yet.

---

# Human Intervention Observations

Record situations where the human evaluator needed to assist the agent.

Potential reasons include:

- Agent became stuck
- Agent requested clarification
- Incorrect project state
- Repeated failed actions
- Safety intervention
- Incorrect code
- Context restoration
- Tool failure

## Recorded Observations

None recorded yet.

---

# Verification Observations

This section is particularly important.

Record cases where:

- The agent correctly verified its work
- The agent failed to verify
- The agent claimed success without evidence
- Independent verification contradicted the agent
- Verification detected a previously unnoticed problem

## Recorded Observations

None recorded yet.

---

# Error-Recovery Observations

Record how agents behave after encountering failures.

Potential behaviours include:

- Correct diagnosis
- Successful alternative strategy
- Repeated unsuccessful strategy
- Incorrect diagnosis
- Recovery requiring human intervention
- Independent recovery

## Recorded Observations

None recorded yet.

---

# Efficiency Observations

Record behaviour that affects development efficiency.

Examples:

- Unnecessary tool calls
- Repeated inspection
- Excessive code rewriting
- Efficient batch operations
- Time saved through automation
- Time lost correcting AI-generated work

## Recorded Observations

None recorded yet.

---

# Game-Development Impact Observations

This section records observations relating specifically to whether AI assistance improves game-development workflows.

Potential observations include:

- Reduced implementation time
- Faster prototyping
- Faster debugging
- Faster asset preparation
- Reduced repetitive work
- Increased correction time
- Increased testing requirements
- Ability to attempt more complex tasks
- Improved iteration speed

## Recorded Observations

None recorded yet.

---

# Positive Agent Behaviours

Research should record successful behaviour as carefully as failures.

Examples may include:

- Correctly identifies project state before acting
- Remembers an earlier constraint
- Selects an appropriate tool
- Detects its own error
- Recovers without assistance
- Verifies implementation
- Avoids unnecessary modification
- Completes a complex workflow autonomously

## Recorded Observations

None recorded yet.

---

# Unexpected Behaviours

Record behaviours that were not predicted by the experiment design.

These may later become useful research questions.

## Recorded Observations

None recorded yet.

---

# Candidate Patterns

Observations that appear repeatedly should be listed here.

| Pattern ID | Description | Observations | Status |
|---|---|---:|---|
| P001 | TBD | 0 | Not established |

A candidate pattern should not automatically be treated as a finding.

Additional controlled testing may be required.

---

# Observations Promoted to Findings

When sufficient evidence supports an observation, record its transition here.

| Observation/Pattern | Finding | Evidence | Date |
|---|---|---|---|
| TBD | TBD | TBD | TBD |

The resulting finding should also be documented in:

`Findings.md`

---

# Example Observation

The following is an example only and is not research data.

## Observation ID

EXAMPLE-OBS-001

### Experiment

Experiment 002 — Tool Use

### Test

Controlled Tool Failure

### Trial

Example only

### Category

Tool Use / Error Recovery

### Task Context

The agent was asked to inspect a development project using an available tool.

### Observation

The first tool call failed because the returned data used a different structure than the agent expected.

### Expected Behaviour

The agent should inspect the error, modify its approach, and retry.

### Actual Behaviour

The agent recognised the error and changed the command before attempting the operation again.

### Human Intervention

Level: 0

### Immediate Outcome

Successful.

### Interpretation

This behaviour may indicate effective recovery from structured tool errors.

Additional trials would be required before treating this as a general capability.

---

# Observation Summary

This section should be periodically updated.

## Total Observations

0

## By Category

| Category | Observations |
|---|---:|
| Context Retention | 0 |
| Tool Use | 0 |
| Code Generation | 0 |
| Computer Use | 0 |
| Blender | 0 |
| Roblox | 0 |
| Verification | 0 |
| Error Recovery | 0 |
| Efficiency | 0 |
| Human Intervention | 0 |
| Game Development | 0 |

---

# Research Notes

General research notes that do not yet justify a formal observation may be recorded here.

-

---

# Relationship to Findings

The intended evidence flow for the project is:

```text
Experiment
    ↓
Trial
    ↓
Raw Evidence
    ↓
Observation
    ↓
Repeated Observation
    ↓
Candidate Pattern
    ↓
Finding
    ↓
Final Conclusion
