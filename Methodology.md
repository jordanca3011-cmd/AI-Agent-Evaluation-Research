
# Methodology

## Overview

This document describes the methodology used in the AI Agent Evaluation Research project.

The research investigates how effectively AI agents can support complex, long-term software and creative development workflows.

The methodology combines controlled experiments with real-world case studies to evaluate AI performance across:

- Context retention
- Tool use
- Code generation
- Computer use
- Error recovery
- Verification
- Project integration
- Human-AI collaboration
- Long-horizon task execution

The research focuses primarily on development environments including Blender, Roblox Studio, Python, Luau, and coding-agent workflows.

---

# Research Question

The primary research question is:

> How effectively can AI agents support complex, long-term creative software development workflows while maintaining project context, executing multi-step tasks, using tools reliably, and recovering from errors?

---

# Secondary Research Questions

The research also investigates:

1. How reliably can AI agents retain project-specific information over extended workflows?

2. How accurately can agents select and operate external tools?

3. How effectively can coding agents generate, modify, debug, and maintain software?

4. How reliably can computer-use agents operate complex graphical applications?

5. Does structured project context improve agent performance?

6. Does access to specialised tools improve task completion compared with text-only assistance?

7. How frequently do agents require human intervention?

8. What are the most common causes of AI agent failure?

9. How effectively can agents detect and recover from their own mistakes?

10. Does agent performance decrease as task length and complexity increase?

---

# Research Approach

The project uses a mixed evaluation approach consisting of:

## Controlled Experiments

Controlled tasks are designed with known starting conditions and expected outcomes.

These experiments allow more consistent comparison between AI systems.

Examples include:

- Debugging deliberately broken code
- Locating known Blender objects
- Modifying controlled Roblox systems
- Recovering from intentionally introduced errors
- Following predefined project constraints

---

## Real-World Case Studies

AI agents are also evaluated during genuine development work.

Current case studies include:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon

These projects provide realistic environments containing:

- Existing project history
- Evolving requirements
- Large asset structures
- Interconnected systems
- Technical constraints
- Creative requirements

Controlled experiments provide repeatability, while case studies provide ecological validity and expose failure modes that may not appear in artificial benchmarks.

---

# AI Systems

Different AI systems may be evaluated over the duration of the research.

For every test, the following should be recorded where available:

- Provider
- Model
- Model/version identifier
- Date
- Agent mode
- Available tools
- Relevant configuration

Because hosted AI systems may change over time, the test date should always be preserved.

Results should not assume that a model tested at one point in time remains identical indefinitely.

---

# Experimental Variables

## Independent Variables

Depending on the experiment, independent variables may include:

- AI model
- Agent system
- Amount of project context
- Available tools
- Task complexity
- Computer-use availability
- Memory availability
- Error information provided

---

## Dependent Variables

Measured outcomes may include:

- Task completion
- Accuracy
- Context retention
- Tool-use success
- Code correctness
- Verification behaviour
- Error recovery
- Efficiency
- Regression rate
- Human intervention
- Completion time

---

## Controlled Variables

When comparing AI systems, the following should remain consistent where practical:

- Task instructions
- Starting project state
- Expected outcome
- Available project information
- Software version
- Test environment
- Verification procedure
- Evaluation criteria

Any important differences should be documented.

---

# Experimental Procedure

Each experiment should follow a standard procedure.

## Step 1: Select Capability

Identify the AI capability being evaluated.

Examples:

- Context retention
- Tool use
- Coding
- Computer use

---

## Step 2: Define Task

Define a specific objective.

The task should include enough information to establish what successful completion means.

Avoid changing the task after the experiment begins unless adaptation itself is being tested.

---

## Step 3: Define Success Criteria

Before testing, record:

- Expected outcome
- Required behaviours
- Constraints
- Prohibited actions
- Verification method

This reduces the risk of changing evaluation criteria after observing results.

---

## Step 4: Record Starting State

Record the initial project state where relevant.

Possible methods include:

- Git commit/hash
- Duplicate project file
- Scene statistics
- Roblox hierarchy
- Existing automated test results
- Screenshots
- File inventory

---

## Step 5: Record Experimental Configuration

Record:

- AI system
- Model
- Agent mode
- Available tools
- Software versions
- Project context supplied
- Test difficulty

---

## Step 6: Execute Experiment

Allow the AI agent to attempt the task.

Where practical, record:

- Tool calls
- Commands
- Code modifications
- Interface actions
- Errors
- Recovery attempts
- Requests for assistance

The evaluator should avoid unnecessary intervention unless intervention is required for safety or continuation.

---

## Step 7: Human Intervention

If human assistance is required, record:

- Why intervention occurred
- What information or action was provided
- Whether the task could have continued without assistance

Human intervention is treated as experimental data.

---

## Step 8: Verify Result

The final result should be independently checked.

Possible verification methods include:

- Automated tests
- Runtime execution
- Blender scene inspection
- Roblox Studio playtesting
- File comparison
- Git diff
- Application state inspection
- Manual review

The agent's own statement that the task succeeded is not considered sufficient evidence.

---

## Step 9: Score Result

Apply relevant metrics from:

`evaluation_metrics.md`

and:

`evaluation-framework.md`

Metrics that do not apply should be recorded as:

`N/A`

---

## Step 10: Classify Failures

Failures should be assigned appropriate categories.

Examples:

- Requirement failure
- Context failure
- Reasoning failure
- Tool selection failure
- Tool execution failure
- Code failure
- Integration failure
- Verification failure
- Recovery failure
- Regression
- Safety/scope failure
- Efficiency failure

Multiple categories may apply.

---

## Step 11: Record Findings

Record:

- Successful behaviours
- Failures
- Unexpected behaviour
- Human intervention
- Quantitative measurements
- Possible explanations
- Follow-up experiments

---

# Test Difficulty

Experiments may be classified using five difficulty levels.

## Level 1 — Basic

A single clearly defined task with minimal dependencies.

Example:

Generate a small standalone function.

---

## Level 2 — Intermediate

Requires multiple steps or limited project understanding.

Example:

Inspect a Blender collection and report missing objects.

---

## Level 3 — Complex

Requires interaction with several project components.

Example:

Modify an existing Roblox gameplay feature and verify integration.

---

## Level 4 — Long-Horizon

Requires sustained execution across many steps.

Example:

Inspect a project, implement a feature, test it, debug failures, and verify the final result.

---

## Level 5 — Open-Ended

Requires significant planning, adaptation, and decision-making within broad constraints.

Example:

Complete a larger development objective where the agent must determine its own workflow.

---

# Repeated Testing

Controlled tests should be repeated where practical.

A single successful run should not be treated as sufficient evidence of reliable behaviour.

For important comparisons:

- Run multiple trials
- Preserve failed trials
- Use equivalent starting conditions
- Avoid selecting only successful runs
- Record variation between attempts

Where resources allow, at least three repetitions of important controlled tests are desirable for exploratory comparison.

Larger sample sizes should be used where practical before making stronger statistical claims.

---

# Context Retention Methodology

Context retention experiments compare agent performance under different information conditions.

## Condition A: Minimal Context

The agent receives only the immediate task and essential information.

## Condition B: Structured Context

The agent additionally receives relevant:

- Project overview
- Architecture
- Previous decisions
- Naming conventions
- Constraints
- Current project state

Performance can then be compared using:

- Accuracy
- Task completion
- Context violations
- Human intervention
- Efficiency
- Regression rate

---

# Tool-Use Methodology

Tool-use experiments evaluate:

1. Tool selection
2. Tool execution
3. Result interpretation
4. Verification
5. Error recovery

Agents may be tested with different levels of tool access.

Example:

### Condition A

Text reasoning only.

### Condition B

Code execution tools.

### Condition C

Application-specific tools.

### Condition D

Visual computer use.

The purpose is to investigate how tool access changes reliability and autonomy.

---

# Coding-Agent Methodology

Coding-agent experiments may include:

- Standalone code generation
- Existing codebase understanding
- Targeted modification
- Multi-file implementation
- Debugging
- Test generation
- Regression testing
- Long-term maintenance

Generated code should be executed whenever practical.

Evaluation should distinguish:

- Syntactic correctness
- Functional correctness
- Integration quality
- Maintainability
- Verification behaviour

---

# Computer-Use Methodology

Computer-use experiments evaluate AI interaction with graphical applications.

Measurements may include:

- Visual state understanding
- Navigation accuracy
- Action accuracy
- Total interface actions
- Incorrect actions
- Repeated actions
- Recovery attempts
- Completion time
- Human intervention

Computer-use experiments should independently verify the final application state.

---

# Blender Methodology

Blender experiments may evaluate:

- Scene understanding
- Collection inspection
- Object identification
- Python automation
- Material workflows
- Asset organisation
- Scene modification
- Constraint following
- Project preservation
- Computer use

Where modifications are potentially destructive, experiments should use duplicate or controlled `.blend` files.

---

# Roblox Methodology

Roblox experiments may evaluate:

- Project structure understanding
- Luau generation
- Existing script modification
- Client-server reasoning
- Remote communication
- Multiplayer behaviour
- Gameplay systems
- Debugging
- Playtesting
- Studio computer use

Gameplay implementations should be tested in Roblox Studio where practical rather than evaluated solely from code appearance.

---

# Human Intervention Measurement

Human intervention is recorded using the following scale:

| Level | Description |
|---|---|
| 0 | No intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant guidance |
| 4 | Human effectively completes the task |

Human intervention should also be described qualitatively.

Example:

> Agent required the evaluator to identify the correct Blender collection after repeatedly selecting the wrong asset.

This provides more information than the numeric score alone.

---

# Quantitative Data Collection

Where practical, record:

- Total tasks
- Tasks passed
- Tasks partially completed
- Tasks failed
- Tool calls
- Failed tool calls
- Interface actions
- Incorrect actions
- Code execution attempts
- Debugging attempts
- Tests passed
- Tests failed
- Regressions
- Context errors
- Human interventions
- Time to first working result
- Time to verified result

---

# Qualitative Data Collection

Qualitative observations may include:

- Repeated failure patterns
- Unexpected successful strategies
- Incorrect assumptions
- Hallucinated project state
- Poor recovery behaviour
- Effective self-correction
- Useful planning strategies
- Verification behaviour

Qualitative findings should be clearly distinguished from quantitative measurements.

---

# Failure Analysis

Failures are treated as an important research output rather than discarded experiments.

For each significant failure, record:

1. What the agent attempted
2. What actually happened
3. Expected behaviour
4. Failure category
5. Failure severity
6. Whether the agent detected the problem
7. Whether recovery succeeded
8. Human intervention required

Repeated failure patterns may then be identified across models and environments.

---

# Model Comparison

When comparing models, use equivalent experimental conditions where possible.

A comparison may include:

| Metric | Model A | Model B |
|---|---:|---:|
| Completion Rate | TBD | TBD |
| Accuracy | TBD | TBD |
| Context Retention | TBD | TBD |
| Tool Use | TBD | TBD |
| Error Recovery | TBD | TBD |
| Human Intervention | TBD | TBD |
| Completion Time | TBD | TBD |

Raw results should be retained alongside summary statistics.

---

# Avoiding Evaluation Bias

Several practices are used to reduce evaluator bias.

## Predefine Success

Expected outcomes should be recorded before execution.

## Preserve Failures

Failed experiments should not be removed simply because they reduce performance scores.

## Consistent Scoring

The same scoring criteria should be used across comparable experiments.

## Separate Observation from Interpretation

Example:

Observation:

> Agent attempted the same failing command three times.

Interpretation:

> The agent may have difficulty adapting its strategy after tool failure.

These should not be treated as the same type of evidence.

## Avoid Model Favouritism

Where possible, equivalent tasks and evaluation criteria should be applied across models.

---

# Data Analysis

Initial research will primarily use descriptive analysis.

Possible measurements include:

## Completion Rate

```text
Completed Tasks / Total Tasks
