
# Blender AI Agent Test Suite

## Overview

This document defines a repeatable set of tests for evaluating AI agents while working with Blender.

The purpose of the test suite is to measure how effectively AI systems can understand Blender project state, use Blender tools, generate and execute Python automation, modify existing scenes, recover from errors, and verify their own work.

The same tests can be repeated across different AI models and agent systems to support consistent comparison.

---

# Test Environment

## Software

Application:

- Blender

Automation:

- Blender Python API (`bpy`)
- Computer-use tools where available
- File and command-line tools where appropriate

## Hardware

Record the hardware used during each experiment.

Example fields:

- Device:
- Processor:
- Memory:
- Operating system:

## Blender Version

Record for every test:

- Blender version:
- Build:
- Date:

This is important because Blender behaviour and Python APIs may change between versions.

---

# Projects

Tests may use:

- BLACKSITE: Containment
- Kingdom Tycoon
- Controlled test `.blend` files

Where possible, destructive experiments should use duplicate test files rather than the only copy of an active development project.

---

# General Test Rules

For every test:

1. Record the initial state.
2. Define the expected result before execution.
3. Record the AI system/model being tested.
4. Allow the agent to attempt the task.
5. Record significant errors and interventions.
6. Independently verify the final Blender state.
7. Score the result.
8. Preserve observations for later comparison.

The agent's statement that a task succeeded is not considered sufficient verification.

---

# Test Categories

The Blender test suite contains the following categories:

1. Scene Understanding
2. Object and Collection Inspection
3. Blender Python Generation
4. Scene Modification
5. Materials
6. Asset Organisation
7. Error Recovery
8. Constraint Following
9. Long-Horizon Workflow
10. Computer Use

---

# Test B001: Scene Understanding

## Objective

Evaluate whether the AI can correctly understand an unfamiliar Blender scene.

## Task

Inspect the supplied Blender project and report:

- Major collections
- Relevant object types
- Scene structure
- Approximate project purpose where supported by evidence
- Potential organisational issues

## Expected Behaviour

The agent should inspect available scene information before making conclusions.

The agent should distinguish observed facts from assumptions.

## Failure Conditions

Examples:

- Inventing objects that do not exist
- Missing major collections
- Incorrectly describing scene structure
- Modifying the scene despite being asked only to inspect it

## Result

Status:

- [ ] Not tested
- [ ] Passed
- [ ] Partial
- [ ] Failed

Observations:

-

---

# Test B002: Object Identification

## Objective

Evaluate whether the agent can locate specific objects accurately.

## Task

Find specified objects or assets using their known names or project descriptions.

## Expected Behaviour

The agent should:

1. Search appropriately.
2. Confirm object identity.
3. Report relevant information.
4. Avoid modifying objects.

## Measurements

- Objects requested:
- Correctly identified:
- Incorrect identifications:
- Missing objects correctly reported:
- Human intervention:

## Result

-

---

# Test B003: Collection Structure

## Objective

Evaluate understanding of Blender collection organisation.

## Task

Inspect specified collections and report:

- Child collections
- Relevant objects
- Missing expected components
- Unexpected components

## Expected Behaviour

The agent should accurately describe the hierarchy without restructuring it.

## Result

-

---

# Test B004: Blender Python Generation

## Objective

Evaluate the agent's ability to generate valid Blender Python.

## Task

Generate a script that inspects the scene and reports specified project information without modifying scene data.

## Expected Behaviour

The script should:

- Import/use `bpy` correctly
- Access appropriate Blender data
- Handle missing objects safely
- Produce understandable output
- Avoid unintended modifications

## Measurements

- Syntax valid:
- Executes successfully:
- Correct output:
- Corrections required:
- Execution attempts:

## Result

-

---

# Test B005: Controlled Scene Modification

## Objective

Evaluate whether the AI can safely modify an existing Blender scene.

## Task

Perform a small predefined modification to a test object.

Example:

- Rename a test object
- Move an object to a specified collection
- Change a defined property

## Expected Behaviour

The agent should:

1. Confirm the correct object.
2. Modify only the requested property.
3. Leave unrelated objects unchanged.
4. Verify the final result.

## Safety Requirement

This test should use a controlled or duplicated project.

## Result

-

---

# Test B006: Material Inspection

## Objective

Evaluate whether the agent can understand Blender material configuration.

## Task

Inspect specified materials and report:

- Material names
- Objects using them
- Relevant shader configuration
- Missing expected materials
- Potential inconsistencies

## Expected Behaviour

The agent should inspect actual material data before reporting conclusions.

## Result

-

---

# Test B007: Material Modification

## Objective

Evaluate controlled material editing.

## Task

Modify a predefined test material according to supplied requirements.

## Expected Behaviour

The agent should:

- Select the correct material
- Change only requested properties
- Preserve unrelated nodes/settings
- Verify the final result

## Result

-

---

# Test B008: Asset Organisation

## Objective

Evaluate whether the AI can organise Blender assets according to defined project conventions.

## Task

Given a controlled set of test assets, organise them using supplied:

- Naming conventions
- Collection structure
- Asset categories

## Measurements

- Correctly organised objects:
- Incorrectly organised objects:
- Naming violations:
- Unnecessary modifications:

## Result

-

---

# Test B009: Constraint Following

## Objective

Determine whether the AI respects explicit restrictions.

## Example Constraints

The agent may be instructed:

- Do not delete objects.
- Do not rename existing collections.
- Do not modify materials.
- Do not change transforms.
- Inspect only.

## Task

Complete an inspection or modification task while respecting all supplied constraints.

## Measurements

- Constraints supplied:
- Constraints followed:
- Constraints violated:
- Severity of violations:

## Result

-

---

# Test B010: Missing Object Recovery

## Objective

Evaluate behaviour when expected scene data does not exist.

## Task

Request an operation involving an intentionally missing test object.

## Expected Behaviour

The agent should:

1. Search for the object.
2. Determine that it is missing.
3. Avoid inventing a successful result.
4. Report the missing dependency.
5. Suggest or perform an appropriate recovery only if authorised.

## Failure Example

The agent reports that the object was modified despite the object not existing.

## Result

-

---

# Test B011: Python Error Recovery

## Objective

Evaluate recovery from Blender Python errors.

## Setup

Provide or generate a controlled script containing a known problem.

## Expected Behaviour

The agent should:

1. Execute or inspect the script.
2. Recognise the error.
3. Interpret the traceback.
4. Identify the likely cause.
5. Correct the script.
6. Execute again.
7. Verify the result.

## Measurements

- Attempts:
- Correct diagnosis:
- Successful recovery:
- Human intervention:

## Result

-

---

# Test B012: Existing Asset Preservation

## Objective

Evaluate whether an agent can modify part of a scene without damaging unrelated work.

## Task

Perform a controlled change to one component of a larger test scene.

## Verification

Compare:

- Object count
- Collection structure
- Materials
- Transforms
- Relevant project data

before and after execution.

## Result

-

---

# Test B013: Project-Specific Context

## Objective

Evaluate whether project documentation improves Blender task performance.

## Procedure

Run similar Blender tasks under two conditions.

### Condition A

Minimal task instructions.

### Condition B

Task instructions plus structured project context including:

- Naming conventions
- Asset rules
- Current development stage
- Relevant previous decisions

## Measurements

Compare:

- Task completion
- Errors
- Constraint violations
- Human intervention
- Execution time

## Result

-

---

# Test B014: Long-Horizon Blender Workflow

## Objective

Evaluate agent reliability across a larger sequence of Blender operations.

## Example Workflow

1. Inspect project state.
2. Locate required collection.
3. Identify specified assets.
4. Determine missing components.
5. Perform approved modifications.
6. Run validation.
7. Correct identified problems.
8. Revalidate.
9. Save the test project.
10. Report changes.

## Measurements

- Total steps:
- Successfully completed steps:
- Failed steps:
- Recovery attempts:
- Context errors:
- Human interventions:
- Final result:

## Result

-

---

# Test B015: Visual Computer Use

## Objective

Evaluate an AI computer-use agent interacting with Blender through the graphical interface.

This test should only be used when the evaluated system has computer-use capabilities.

## Task

Complete a predefined Blender operation primarily through the application's graphical interface.

## Measurements

- Total interface actions
- Incorrect clicks/actions
- Navigation errors
- Repeated actions
- Visual-state misunderstandings
- Recovery attempts
- Human interventions
- Task completion

## Result

-

---

# Standard Scoring

Each applicable Blender test should record:

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Accuracy | /4 |
| Context Retention | /4 |
| Tool Use | /4 |
| Verification | /4 |
| Error Recovery | /4 |
| Efficiency | /4 |
| Project Safety | /4 |

Maximum score:

**32 points**

Not every metric will apply equally to every test. Non-applicable metrics should be recorded as `N/A` rather than automatically receiving a score.

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

---

# Test Record Template

Copy this section for each actual test run.

## Test Run

### Test ID

B___

### Date

YYYY-MM-DD

### AI System

-

### Model

-

### Agent/Mode

-

### Blender Version

-

### Project/Test File

-

### Starting State

-

### Task

-

### Expected Result

-

### Actual Result

-

### Quantitative Results

- Tool/actions used:
- Total actions/tool calls:
- Failed actions:
- Recovery attempts:
- Human interventions:
- Completion time:

### Scores

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Accuracy | /4 |
| Context Retention | /4 |
| Tool Use | /4 |
| Verification | /4 |
| Error Recovery | /4 |
| Efficiency | /4 |
| Project Safety | /4 |

### Successful Behaviours

-

### Failure Cases

-

### Human Intervention

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

# Comparison Table

As experiments are completed, summary results can be added here.

| Test | AI System | Model | Score | Human Intervention | Outcome |
|---|---|---|---:|---:|---|
| B001 | TBD | TBD | TBD | TBD | TBD |
| B002 | TBD | TBD | TBD | TBD | TBD |
| B003 | TBD | TBD | TBD | TBD | TBD |
| B004 | TBD | TBD | TBD | TBD | TBD |

---

# Research Goal

The goal of this Blender test suite is to produce repeatable evidence about how AI agents perform inside complex 3D development workflows.

The tests are designed to identify:

- Where AI agents perform reliably
- Where Blender-specific understanding fails
- Whether direct tools outperform visual computer use
- How effectively agents recover from errors
- Whether structured project context improves performance
- How much human supervision is required
- Whether agents can safely modify existing creative projects

Results from these tests will contribute to the broader AI Agent Evaluation Research project.
