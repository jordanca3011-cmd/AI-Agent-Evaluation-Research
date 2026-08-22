
# Roblox AI Agent Test Suite

## Overview

This document defines a repeatable test suite for evaluating AI agents during Roblox development workflows.

The purpose of the test suite is to measure how effectively AI systems can understand Roblox project structure, generate and modify Luau code, interact with Roblox Studio, debug gameplay systems, preserve existing functionality, and verify their work.

The same tests can be repeated across different AI models and agent systems to support consistent comparison.

---

# Test Environment

## Software

Primary environment:

- Roblox Studio

Programming language:

- Luau

Additional tools may include:

- Computer-use systems
- Code execution tools
- File-management tools
- Git/version-control workflows
- Roblox Studio plugins
- External development tools

---

# Case Study Projects

Testing may use:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon
- Controlled Roblox test projects

Controlled projects should be preferred for experiments that could introduce destructive changes.

---

# General Test Rules

For every test:

1. Record the initial project state.
2. Define the task before execution.
3. Define the expected result.
4. Record the AI system/model.
5. Allow the agent to attempt the task.
6. Record significant actions and errors.
7. Test the implementation.
8. Verify the final Studio/project state.
9. Record human intervention.
10. Score the result.

An agent claiming that a feature works is not considered sufficient verification.

---

# Test Categories

The Roblox test suite evaluates:

1. Project Understanding
2. Instance Hierarchy Understanding
3. Luau Generation
4. Existing Script Understanding
5. Script Modification
6. Gameplay System Implementation
7. Debugging
8. Client-Server Reasoning
9. Multiplayer Behaviour
10. Constraint Following
11. Regression Avoidance
12. Roblox Studio Tool Use
13. Context Retention
14. Long-Horizon Development

---

# Test R001: Project Structure Understanding

## Objective

Determine whether the AI agent can understand an unfamiliar Roblox project.

## Task

Inspect a controlled Roblox project and identify:

- Major systems
- Important services
- Relevant scripts
- Key folders
- Remote communication systems
- Likely gameplay architecture

## Expected Behaviour

The agent should inspect available project information before making conclusions.

It should distinguish observed project structure from assumptions.

## Failure Conditions

Examples:

- Inventing scripts that do not exist
- Incorrectly describing hierarchy
- Missing important systems
- Modifying the project when asked only to inspect it

## Result

- [ ] Not tested
- [ ] Pass
- [ ] Partial
- [ ] Fail

### Observations

-

---

# Test R002: Instance Hierarchy Understanding

## Objective

Evaluate whether the agent understands Roblox's instance hierarchy.

## Task

Locate specified instances and report:

- Parent
- Children
- Relevant properties
- Scripts
- Connections to other systems

## Expected Behaviour

The agent should accurately navigate structures such as:

- Workspace
- ReplicatedStorage
- ServerScriptService
- ServerStorage
- StarterPlayer
- StarterGui

## Measurements

- Instances requested:
- Correctly located:
- Incorrect locations:
- Missing instances correctly identified:

## Result

-

---

# Test R003: Basic Luau Generation

## Objective

Establish baseline Roblox coding ability.

## Task

Generate a small self-contained Luau component from a clear specification.

## Expected Behaviour

Code should:

- Use valid Luau
- Use appropriate Roblox APIs
- Follow the stated requirements
- Avoid unnecessary complexity

## Measurements

- Syntax valid:
- First attempt functional:
- Corrections required:
- Runtime errors:

## Result

-

---

# Test R004: Roblox API Usage

## Objective

Evaluate whether the agent correctly uses Roblox-specific APIs.

## Evaluation Areas

Examples:

- Services
- Events
- Instances
- Attributes
- RemoteEvents
- RemoteFunctions
- Data structures
- Player lifecycle
- Character lifecycle

## Failure Conditions

Examples:

- Non-existent APIs
- Deprecated approaches without justification
- Incorrect service usage
- Incorrect assumptions about execution context

## Result

-

---

# Test R005: Existing Script Understanding

## Objective

Determine whether an AI agent can understand existing Luau before modifying it.

## Task

Inspect a specified script and explain:

- Its purpose
- Important functions
- Dependencies
- Events
- Data flow
- Relevant external systems

## Expected Behaviour

The agent should understand the script before proposing changes.

## Result

-

---

# Test R006: Targeted Script Modification

## Objective

Evaluate whether the agent can safely modify existing gameplay code.

## Task

Implement one defined change to an existing script.

## Expected Behaviour

The agent should:

1. Inspect existing implementation.
2. Identify the appropriate modification.
3. Make a targeted change.
4. Preserve unrelated functionality.
5. Test the result.

## Measurements

- Scripts inspected:
- Scripts modified:
- Unnecessary modifications:
- Runtime errors:
- Regressions:

## Result

-

---

# Test R007: Gameplay Feature Implementation

## Objective

Evaluate whether an AI agent can implement a complete gameplay feature.

## Example Tasks

- Capture point
- Upgrade system
- Factory machine
- Interaction system
- Player reward system
- Simple NPC behaviour

## Expected Behaviour

The agent should:

1. Understand the feature requirements.
2. Identify required project components.
3. Implement appropriate code.
4. Integrate with existing systems.
5. Test the feature.
6. Verify expected behaviour.

## Result

-

---

# Test R008: Client-Server Architecture

## Objective

Evaluate whether the agent understands Roblox client-server separation.

## Task

Implement or analyse functionality requiring communication between client and server.

## Evaluation

The agent should correctly determine:

- What runs on the client
- What runs on the server
- What data must cross the boundary
- Where validation should occur

## Failure Conditions

Examples:

- Trusting client-provided values unnecessarily
- Putting server-authoritative behaviour entirely on the client
- Incorrect RemoteEvent direction
- Exposing server-only logic unnecessarily

## Result

-

---

# Test R009: Remote Communication

## Objective

Evaluate correct use of Roblox remote communication.

## Task

Create or inspect a controlled RemoteEvent or RemoteFunction workflow.

## Evaluation

- Correct location
- Correct direction
- Correct arguments
- Appropriate validation
- Correct event handling

## Result

-

---

# Test R010: Server Authority

## Objective

Evaluate whether the agent preserves server authority for important gameplay systems.

## Example Systems

- Currency
- Rewards
- Damage
- Progression
- Purchases
- Capture objectives

## Expected Behaviour

The agent should avoid trusting the client for authoritative game state.

## Result

-

---

# Test R011: Multiplayer Reasoning

## Objective

Evaluate whether generated systems behave correctly with multiple players.

## Task

Implement or analyse a system involving multiple simulated players.

## Evaluation

Check for:

- Player-specific state
- Shared state
- Ownership
- Race conditions
- Incorrect global state
- Cleanup after players leave

## Result

-

---

# Test R012: Luau Error Diagnosis

## Objective

Evaluate whether the agent can interpret Roblox runtime errors.

## Setup

Provide a controlled script containing a known error.

Potential errors:

- Nil access
- Incorrect property
- Missing instance
- Invalid argument
- Event connection issue
- Execution-context problem

## Expected Behaviour

The agent should:

1. Interpret the error.
2. Locate relevant code.
3. Identify likely root cause.
4. Produce a targeted correction.

## Result

-

---

# Test R013: Debugging and Repair

## Objective

Determine whether the AI can repair a broken Roblox gameplay feature.

## Procedure

1. Run the feature.
2. Observe failure.
3. Provide available debugging information.
4. Allow agent investigation.
5. Implement correction.
6. Retest.
7. Verify behaviour.

## Measurements

- Diagnosis attempts:
- Repair attempts:
- Successful repair:
- New errors introduced:
- Human intervention:

## Result

-

---

# Test R014: Failed Approach Recovery

## Objective

Evaluate whether an agent can adapt after its first solution fails.

## Expected Behaviour

The agent should:

- Recognise failure
- Inspect evidence
- Avoid repeatedly using the same failed solution
- Change its approach
- Retest
- Verify

## Result

-

---

# Test R015: Constraint Following

## Objective

Determine whether the AI respects explicit Roblox project constraints.

## Example Constraints

- Do not rename existing instances.
- Do not modify unrelated scripts.
- Do not change the map.
- Preserve existing RemoteEvents.
- Do not change existing public module interfaces.
- Do not delete existing assets.

## Measurements

- Constraints provided:
- Constraints followed:
- Constraints violated:
- Severity:

## Result

-

---

# Test R016: Regression Avoidance

## Objective

Determine whether existing gameplay remains functional after an AI-generated modification.

## Procedure

### Before Modification

Record baseline behaviour.

### After Modification

Repeat the same tests.

## Measurements

- Baseline tests passed:
- Final tests passed:
- New failures:
- Existing systems affected:

## Result

-

---

# Test R017: Roblox Studio Navigation

## Objective

Evaluate an AI computer-use agent interacting with Roblox Studio.

Only applicable when the evaluated system has computer-use capabilities.

## Task

Navigate Studio to locate specified project components.

## Measurements

- Interface actions:
- Incorrect actions:
- Navigation errors:
- Repeated actions:
- Human interventions:

## Result

-

---

# Test R018: Studio Modification

## Objective

Evaluate whether an AI computer-use agent can safely modify a Roblox Studio project.

## Example Task

Perform a controlled modification to a test instance.

## Expected Behaviour

The agent should:

1. Confirm the correct project.
2. Locate the correct instance.
3. Perform only the requested modification.
4. Verify the change.
5. Preserve unrelated content.

## Result

-

---

# Test R019: Playtest Verification

## Objective

Evaluate whether an agent verifies gameplay through Roblox Studio testing rather than assuming code is correct.

## Task

After implementing a controlled feature, the agent should perform an appropriate test.

## Expected Behaviour

The agent should:

1. Enter an appropriate test mode.
2. Trigger the feature.
3. Observe behaviour.
4. Inspect relevant errors/output.
5. Determine whether requirements were satisfied.

## Result

-

---

# Test R020: Context Retention

## Objective

Evaluate whether the agent remembers project-specific Roblox requirements.

## Context May Include

- Architecture
- Naming conventions
- Gameplay rules
- Economy values
- Existing systems
- Previous decisions
- Current development stage

## Measurements

- Forgotten requirements:
- Contradictions:
- Repeated work:
- Incorrect assumptions:
- Context restoration required:

## Result

-

---

# Test R021: Context vs No Context

## Objective

Measure whether structured project context improves Roblox development performance.

## Condition A: Minimal Context

Provide only the immediate task.

## Condition B: Structured Context

Provide:

- Project overview
- Architecture
- Gameplay rules
- Relevant existing systems
- Naming conventions
- Previous decisions
- Current task

## Compare

- Task completion
- Code correctness
- Regressions
- Human intervention
- Attempts
- Completion time

## Result

-

---

# Test R022: Game Systems Reasoning

## Objective

Evaluate whether the agent understands interactions between multiple gameplay systems.

## Example

A progression change may affect:

- Income
- Upgrade prices
- Combat rewards
- Rebirth progression
- Player pacing

## Task

Ask the agent to analyse or modify one system while considering its effects on related systems.

## Evaluation

- Dependencies identified
- Side effects identified
- Incorrect assumptions
- Balance implications
- Implementation quality

## Result

-

---

# Test R023: Economy Reasoning

## Objective

Evaluate AI assistance with game-economy design.

## Task

Analyse or modify a controlled progression system.

## Measurements

- Existing progression understood:
- Mathematical consistency:
- Progression consequences identified:
- Unintended exploits identified:
- Human corrections required:

## Result

-

---

# Test R024: Project Safety

## Objective

Determine whether the AI can operate without damaging unrelated project content.

## Evaluation

Check whether the agent:

- Avoids deletion of unrelated instances
- Avoids unnecessary restructuring
- Preserves scripts
- Preserves assets
- Respects project boundaries

## Result

-

---

# Test R025: Long-Horizon Roblox Development

## Objective

Evaluate agent reliability across a complete development workflow.

## Example Workflow

1. Inspect project.
2. Understand requirements.
3. Locate relevant systems.
4. Plan implementation.
5. Modify or create code.
6. Integrate feature.
7. Run playtest.
8. Diagnose problems.
9. Correct implementation.
10. Retest.
11. Check regressions.
12. Verify final project state.
13. Report changes.

## Measurements

- Steps completed:
- Failed steps:
- Tool calls/actions:
- Debugging attempts:
- Context errors:
- Regressions:
- Human interventions:
- Completion time:

## Result

-

---

# Standard Scoring

Each applicable Roblox test should record:

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Requirement Understanding | /4 |
| Roblox/Luau Accuracy | /4 |
| Project Integration | /4 |
| Tool Use | /4 |
| Debugging | /4 |
| Context Retention | /4 |
| Verification | /4 |
| Regression Avoidance | /4 |
| Project Safety | /4 |

Maximum score:

**40 points**

Metrics that do not apply should be recorded as `N/A`.

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

- Scripts inspected
- Scripts modified
- Instances modified
- Tool calls
- Computer-use actions
- Failed actions
- Runtime errors
- Debugging attempts
- Playtests
- Regressions
- Human interventions
- Time to first working implementation
- Time to verified implementation

---

# Test Run Template

Copy this section for every actual Roblox test.

## Test Run

### Test ID

R___

### Date

YYYY-MM-DD

### AI System

-

### Model

-

### Agent/Mode

-

### Roblox Studio Version

-

### Project

-

### Starting Project State

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

### Scripts Modified

-

### Instances Modified

-

### Playtest Performed

- [ ] Yes
- [ ] No

### Runtime/Output Errors

-

### Quantitative Results

- Tool calls:
- Computer-use actions:
- Failed actions:
- Implementation attempts:
- Debugging attempts:
- Human interventions:
- Completion time:

### Scores

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Requirement Understanding | /4 |
| Roblox/Luau Accuracy | /4 |
| Project Integration | /4 |
| Tool Use | /4 |
| Debugging | /4 |
| Context Retention | /4 |
| Verification | /4 |
| Regression Avoidance | /4 |
| Project Safety | /4 |

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

As tests are completed, results can be summarised here.

| Test | AI System | Model | Score | Human Intervention | Outcome |
|---|---|---|---:|---:|---|
| R001 | TBD | TBD | TBD | TBD | TBD |
| R002 | TBD | TBD | TBD | TBD | TBD |
| R003 | TBD | TBD | TBD | TBD | TBD |

---

# Case Study Applications

## BLACKSITE: Containment

Useful for evaluating:

- Large project context
- Blender-to-Roblox workflows
- Creature systems
- Facility systems
- Complex project constraints
- Long-term agent collaboration

## Forgefront: Weapons Factory Tycoon

Useful for evaluating:

- Gameplay systems
- Economy reasoning
- Progression
- Multiplayer mechanics
- Luau implementation
- Iterative balancing

## Kingdom Tycoon

Useful for evaluating:

- Asset integration
- World organisation
- Creative development
- Blender-to-Roblox workflows
- Style and project consistency

---

# Research Questions Supported

Results from this test suite may help answer:

- How reliably can AI agents develop Roblox experiences?
- How accurately do AI agents understand Luau and Roblox APIs?
- Can AI agents reason correctly about client-server architecture?
- How effectively can agents debug Roblox gameplay?
- Can agents safely modify existing projects?
- How much human intervention is required?
- Does structured project context improve performance?
- Does performance decline during long development workflows?
- How effectively do agents verify their work through playtesting?
- How do different AI models compare under equivalent Roblox tasks?

---

# Research Goal

The goal of this test suite is to produce repeatable evidence about AI agent performance during real-world Roblox development.

The research evaluates not only whether an AI can generate Luau code, but whether it can understand an existing Roblox project, reason about multiplayer architecture, safely modify gameplay systems, debug failures, verify behaviour through testing, preserve existing functionality, and collaborate effectively with a human developer over extended development workflows.
