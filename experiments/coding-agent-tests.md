
# Coding Agent Test Suite

## Overview

This document defines a repeatable test suite for evaluating AI coding agents during real-world software development tasks.

The purpose of this test suite is to measure whether coding agents can move beyond isolated code generation and reliably understand requirements, inspect existing codebases, implement changes, debug failures, use development tools, verify their work, and preserve existing functionality.

The same tests can be repeated across different models and agent systems to support consistent comparison.

---

# Test Environments

Testing may include:

- Python
- Blender Python (`bpy`)
- Roblox Luau
- Git repositories
- Terminal environments
- Existing project codebases
- Automated test environments

Primary case-study projects may include:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon

Controlled test repositories should also be used where appropriate.

---

# General Test Rules

For every test:

1. Record the initial project state.
2. Define the task before execution.
3. Define the expected result.
4. Record the AI system and model.
5. Allow the agent to attempt the task.
6. Record significant tool actions and failures.
7. Run available tests or verification.
8. Compare the final state against requirements.
9. Record human intervention.
10. Score the result.

An agent claiming that code works is not considered sufficient verification.

---

# Test Categories

The coding-agent test suite evaluates:

1. Requirement Understanding
2. Isolated Code Generation
3. Existing Code Understanding
4. Code Modification
5. Debugging
6. Multi-File Changes
7. Tool Use
8. Test Generation
9. Regression Avoidance
10. Context Retention
11. Error Recovery
12. Long-Horizon Development

---

# Test C001: Requirement Understanding

## Objective

Determine whether the coding agent correctly understands a technical request before implementing it.

## Task

Provide a development requirement containing:

- Required behaviour
- Technical constraints
- Existing functionality that must remain unchanged
- Explicit restrictions

The agent should explain or demonstrate an implementation consistent with those requirements.

## Measurements

- Requirements provided:
- Requirements correctly followed:
- Requirements missed:
- Incorrect assumptions:
- Clarifications required:

## Result

- [ ] Not tested
- [ ] Pass
- [ ] Partial
- [ ] Fail

---

# Test C002: Isolated Code Generation

## Objective

Evaluate baseline code-generation ability.

## Task

Generate a self-contained function or script from a clear specification.

Example:

> Write a Python function that validates a list of required asset names and returns any missing entries.

## Expected Behaviour

The generated code should:

- Be syntactically valid
- Produce the expected output
- Handle expected edge cases
- Avoid unnecessary complexity

## Measurements

- First attempt valid:
- First attempt functional:
- Corrections required:
- Tests passed:
- Tests failed:

## Result

-

---

# Test C003: Existing Codebase Understanding

## Objective

Evaluate whether the agent can understand an unfamiliar codebase before making changes.

## Task

Inspect a controlled repository and report:

- Major components
- Relevant files
- Important dependencies
- Likely location for implementing a specified feature

## Expected Behaviour

The agent should inspect available code rather than inventing architecture.

## Failure Conditions

Examples:

- References files that do not exist
- Misidentifies important components
- Begins modifying code without sufficient inspection
- Makes unsupported assumptions about architecture

## Result

-

---

# Test C004: Targeted Code Modification

## Objective

Determine whether an agent can modify existing code while keeping changes within scope.

## Task

Implement one defined feature in an existing project.

## Expected Behaviour

The agent should:

1. Inspect relevant code.
2. Identify the appropriate modification location.
3. Make the smallest reasonable change.
4. Preserve unrelated functionality.
5. Test the implementation.

## Measurements

- Files inspected:
- Files modified:
- Unnecessary files modified:
- Tests passed:
- Regressions introduced:

## Result

-

---

# Test C005: Bug Diagnosis

## Objective

Evaluate whether the agent can correctly identify the cause of a software defect.

## Setup

Provide code containing a known bug.

Possible categories:

- Syntax error
- Runtime error
- Logic error
- Incorrect API usage
- State-management problem
- Integration failure

## Expected Behaviour

The agent should:

1. Reproduce or inspect the failure.
2. Analyse available evidence.
3. Identify the likely root cause.
4. Avoid unrelated modifications.

## Measurements

- Correct root cause identified:
- Incorrect diagnoses:
- Attempts required:
- Human hints required:

## Result

-

---

# Test C006: Bug Repair

## Objective

Evaluate whether the agent can successfully repair a known defect.

## Expected Behaviour

The agent should:

1. Identify the cause.
2. Implement a targeted correction.
3. Execute relevant tests.
4. Confirm the original failure is resolved.
5. Check for regressions.

## Measurements

- Repair successful:
- Attempts:
- New errors introduced:
- Tests passed:
- Human intervention:

## Result

-

---

# Test C007: Multi-File Feature

## Objective

Evaluate coding performance when a feature requires coordinated changes across multiple files.

## Task

Implement a feature involving multiple project components.

## Expected Behaviour

The agent should understand dependencies between components and make consistent changes.

## Measurements

- Required files identified:
- Correct files modified:
- Missing changes:
- Unnecessary modifications:
- Integration success:

## Result

-

---

# Test C008: Test Generation

## Objective

Evaluate whether the agent can create useful tests for existing functionality.

## Task

Given an existing function or system, generate appropriate tests.

## Evaluation

Tests should:

- Cover normal behaviour
- Include meaningful edge cases
- Detect incorrect behaviour
- Avoid testing implementation details unnecessarily

## Measurements

- Tests generated:
- Valid tests:
- Useful failures detected:
- False assumptions:

## Result

-

---

# Test C009: Test-Driven Repair

## Objective

Evaluate whether the coding agent can use failing tests as evidence during debugging.

## Setup

Provide:

- Existing code
- Automated tests
- At least one failing test

## Expected Behaviour

The agent should:

1. Run or inspect tests.
2. Identify relevant failure information.
3. Determine the cause.
4. Modify the implementation.
5. Rerun tests.
6. Verify that the suite passes.

## Result

-

---

# Test C010: Constraint Following

## Objective

Determine whether the coding agent follows explicit restrictions.

## Example Constraints

- Do not modify specified files.
- Do not change public interfaces.
- Do not add dependencies.
- Preserve backwards compatibility.
- Do not rewrite unrelated code.

## Measurements

- Constraints supplied:
- Constraints followed:
- Constraints violated:
- Severity:

## Result

-

---

# Test C011: Regression Avoidance

## Objective

Determine whether existing functionality remains intact after an AI-generated change.

## Procedure

1. Run baseline tests.
2. Allow agent modification.
3. Run the same tests again.
4. Compare results.

## Measurements

- Baseline tests passed:
- Final tests passed:
- New failures:
- Existing functionality affected:

## Result

-

---

# Test C012: Tool Selection

## Objective

Evaluate whether the coding agent selects appropriate development tools.

Potential tools include:

- File search
- Code search
- Terminal
- Test runner
- Git
- Static analysis
- Application-specific tools

## Expected Behaviour

The agent should select tools appropriate to the current problem rather than relying entirely on assumptions.

## Measurements

- Tool calls:
- Appropriate tool selections:
- Unnecessary calls:
- Failed calls:

## Result

-

---

# Test C013: Error Interpretation

## Objective

Evaluate whether the agent correctly interprets compiler, runtime, or application errors.

## Task

Provide an authentic error produced during execution.

## Expected Behaviour

The agent should distinguish between:

- Root cause
- Secondary symptoms
- Unrelated warnings

## Result

-

---

# Test C014: Failed Approach Recovery

## Objective

Determine whether an agent adapts after its initial implementation fails.

## Expected Behaviour

The agent should:

1. Recognise failure.
2. Inspect new evidence.
3. Avoid repeatedly applying the same unsuccessful solution.
4. Develop an alternative.
5. Verify the alternative.

## Measurements

- Failed attempts:
- Repeated failed strategies:
- Successful recovery:
- Human intervention:

## Result

-

---

# Test C015: Project Context Retention

## Objective

Evaluate whether the coding agent maintains project-specific requirements during development.

## Context May Include

- Naming conventions
- Architecture decisions
- Technical restrictions
- Previous changes
- Current project stage

## Evaluation

Measure:

- Forgotten requirements
- Contradictions
- Incorrect assumptions
- Repeated work
- Context restoration required

## Result

-

---

# Test C016: Context vs No Context

## Objective

Measure whether structured project context improves coding-agent performance.

## Condition A: Minimal Context

Provide only the immediate programming task.

## Condition B: Structured Context

Provide:

- Project overview
- Relevant architecture
- Constraints
- Naming conventions
- Relevant previous decisions
- Immediate task

## Compare

- Completion rate
- Code correctness
- Regression rate
- Human intervention
- Number of attempts
- Completion time

## Result

-

---

# Test C017: Long-Horizon Development

## Objective

Evaluate coding-agent performance across a larger development workflow.

## Example Workflow

1. Inspect repository.
2. Understand requirements.
3. Identify relevant components.
4. Implement feature.
5. Run tests.
6. Diagnose failures.
7. Correct implementation.
8. Rerun tests.
9. Check for regressions.
10. Review changes.
11. Produce final report.

## Measurements

- Steps completed:
- Failed steps:
- Tool calls:
- Debugging attempts:
- Context errors:
- Human interventions:
- Tests passed:
- Final outcome:

## Result

-

---

# Test C018: Blender Python Integration

## Objective

Evaluate coding-agent performance when generating code for Blender.

## Task

Create or modify a Blender Python script that performs a controlled development operation.

## Evaluation

- Correct `bpy` usage
- Scene safety
- Error handling
- Requirement adherence
- Successful execution
- Verification

## Result

-

---

# Test C019: Roblox Luau Integration

## Objective

Evaluate coding-agent performance with Roblox development.

## Task

Create or modify a controlled Roblox gameplay component using Luau.

## Evaluation

- Valid Luau
- Correct Roblox API usage
- Integration quality
- Existing-system preservation
- Runtime behaviour
- Verification

## Result

-

---

# Test C020: Self-Review

## Objective

Determine whether an agent can identify problems in its own implementation before final submission.

## Procedure

After implementation but before revealing test results, instruct the agent to review its own changes.

Record whether it identifies:

- Bugs
- Missing requirements
- Edge cases
- Unnecessary changes
- Potential regressions

## Result

-

---

# Standard Scoring

Each applicable test should record:

| Metric | Score |
|---|---|
| Requirement Understanding | /4 |
| Functional Correctness | /4 |
| Code Quality | /4 |
| Project Integration | /4 |
| Tool Use | /4 |
| Debugging | /4 |
| Verification | /4 |
| Regression Avoidance | /4 |
| Context Retention | /4 |

Maximum score:

**36 points**

Metrics that do not apply to a particular test should be recorded as `N/A`.

---

# Human Intervention

Record separately:

| Level | Description |
|---|---|
| 0 | No intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant guidance |
| 4 | Human effectively completes the task |

Lower intervention represents greater agent autonomy.

---

# Quantitative Measurements

Where possible, record:

- Files inspected
- Files modified
- Lines changed
- Tool calls
- Failed tool calls
- Execution attempts
- Debugging attempts
- Tests passed
- Tests failed
- Regressions introduced
- Human interventions
- Time to first working solution
- Time to verified solution

---

# Test Run Template

Copy this section for every actual coding-agent test.

## Test Run

### Test ID

C___

### Date

YYYY-MM-DD

### AI System

-

### Model

-

### Agent/Mode

-

### Programming Language

-

### Repository/Project

-

### Starting Commit

-

### Task

-

### Constraints

-

### Expected Result

-

### Agent Approach

-

### Actual Result

-

### Files Modified

-

### Verification Performed

-

### Automated Test Results

Tests passed:

Tests failed:

### Quantitative Results

- Tool calls:
- Failed calls:
- Implementation attempts:
- Debugging attempts:
- Human interventions:
- Completion time:

### Scores

| Metric | Score |
|---|---|
| Requirement Understanding | /4 |
| Functional Correctness | /4 |
| Code Quality | /4 |
| Project Integration | /4 |
| Tool Use | /4 |
| Debugging | /4 |
| Verification | /4 |
| Regression Avoidance | /4 |
| Context Retention | /4 |

### Human Intervention Level

/4

### Successful Behaviours

-

### Failure Cases

-

### Unexpected Behaviour

-

### Final Outcome

- [ ] Pass
- [ ] Partial
- [ ] Fail

### Notes

-

---

# Model Comparison

Results from repeated tests can be summarised here.

| Test | AI System | Model | Score | Tests Passed | Human Intervention | Outcome |
|---|---|---|---:|---:|---:|---|
| C001 | TBD | TBD | TBD | TBD | TBD | TBD |
| C002 | TBD | TBD | TBD | TBD | TBD | TBD |
| C003 | TBD | TBD | TBD | TBD | TBD | TBD |

---

# Research Questions Supported

Results from this test suite may help answer:

- How reliable are coding agents on real development tasks?
- Does performance decrease as codebase complexity increases?
- How effectively can agents debug their own mistakes?
- Does tool access improve coding reliability?
- Does structured project context improve performance?
- How often do AI-generated changes introduce regressions?
- How much human intervention is required?
- How effectively do coding agents verify their own work?
- How do different AI models compare under identical conditions?

---

# Research Goal

The goal of this test suite is to produce repeatable evidence about AI coding-agent performance in realistic software development environments.

The research focuses not only on whether an agent can generate code, but whether it can function as a reliable development collaborator capable of understanding existing systems, making controlled changes, debugging failures, verifying results, and maintaining project requirements over time.
