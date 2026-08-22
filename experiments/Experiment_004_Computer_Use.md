
# Experiment 004: AI Computer Use Reliability

## Overview

This experiment evaluates the reliability of AI agents when interacting with graphical computer environments to complete real-world development tasks.

Unlike direct API or command-line tool use, computer-use agents must interpret visual information, understand application state, select appropriate interface actions, and adapt when the interface changes unexpectedly.

The experiment focuses on AI interaction with complex creative and development software, including Blender, Roblox Studio, file-management environments, and other desktop applications.

---

## Research Question

How reliably can AI computer-use agents complete multi-step tasks in complex graphical software environments while maintaining accuracy, efficiency, project context, and appropriate error recovery?

---

## Hypothesis

AI computer-use agents are expected to perform well on clearly defined interface tasks but experience reduced reliability as workflows become longer, application states become more complex, or unexpected interface changes occur.

It is expected that agents capable of verifying application state after important actions will achieve higher overall task-completion rates.

---

## Objectives

This experiment evaluates whether an AI computer-use agent can:

- Correctly interpret application state
- Locate relevant interface elements
- Select appropriate actions
- Navigate complex applications
- Execute multi-step workflows
- Maintain awareness of the current task
- Detect unsuccessful actions
- Recover from errors
- Verify important changes
- Avoid unnecessary actions
- Preserve existing project data
- Complete tasks with limited human intervention

---

# Test Environments

Primary applications may include:

- Blender
- Roblox Studio
- Finder or file-management environments
- Development tools
- Other relevant desktop applications

Primary case-study projects:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon

---

# Experimental Conditions

Computer-use tasks will be divided into increasing levels of difficulty.

## Level 1: Basic Navigation

The agent performs a simple interface action.

Examples:

- Open an application
- Navigate to a known location
- Open a project
- Locate a visible interface control

### Purpose

Establish baseline computer-use reliability.

---

## Level 2: Application State Recognition

The agent must inspect the current application state before deciding what to do.

Examples:

- Determine which Blender project is currently open
- Identify the active Blender collection
- Determine whether Roblox Studio is in Edit or Play mode
- Recognise whether an operation has already been completed

### Evaluation

The agent should avoid acting on incorrect assumptions about the current state.

---

## Level 3: Multi-Step Workflow

The agent completes a sequence of related actions.

Example:

1. Open Blender.
2. Open the required project.
3. Navigate to the relevant scene or collection.
4. Inspect specified assets.
5. Perform an approved operation.
6. Verify the result.
7. Save the project.

This evaluates whether the agent can maintain task state across multiple interface interactions.

---

## Level 4: Unexpected Interface State

The agent encounters a situation that differs from the expected workflow.

Examples:

- Dialog box appears
- Application opens on a different workspace
- Object is not where expected
- Panel is closed
- Selection state differs
- File has already been modified

The agent should inspect the situation rather than blindly continuing with a predetermined action sequence.

---

## Level 5: Error Recovery

A controlled problem is introduced.

Examples:

- Wrong object selected
- Operation fails
- Application reports an error
- Incorrect menu is opened
- Expected asset cannot be found

The agent must:

1. Recognise the problem.
2. Determine the likely cause.
3. Avoid making the situation worse.
4. Select a recovery strategy.
5. Retry where appropriate.
6. Verify the final state.

---

## Level 6: Long-Horizon Computer Use

The agent performs a larger development task involving many actions.

Examples:

- Inspect multiple Blender assets
- Perform a structured asset-preparation workflow
- Complete a Roblox development task
- Review and modify several project components

This evaluates whether reliability decreases as the number of interactions increases.

---

# Test Procedure

Each test will follow a consistent procedure.

## Step 1: Define Initial State

Record:

- Application
- Project
- Relevant application state
- Expected starting conditions

Where possible, screenshots or structured state information may be retained for comparison.

---

## Step 2: Define Task

Document the exact objective before testing.

The task should describe the desired outcome without unnecessarily specifying every interface action.

This allows evaluation of the agent's ability to determine its own interaction strategy.

---

## Step 3: Define Expected Outcome

Document what successful completion should look like.

This may include:

- Required application state
- Required project changes
- Files created or modified
- Objects affected
- Behaviour that must remain unchanged

---

## Step 4: Execute

Allow the AI computer-use agent to attempt the task.

Record significant actions where practical.

---

## Step 5: Verify

Compare the final application/project state with the expected outcome.

Verification should not rely solely on the agent claiming that the task succeeded.

---

## Step 6: Score

Evaluate performance using the metrics defined below.

---

# Evaluation Metrics

## 1. Visual State Understanding

Measures whether the agent correctly interprets what is visible on screen.

| Score | Description |
|---|---|
| 0 | Fundamentally misunderstands application state |
| 1 | Major visual/state errors |
| 2 | Partially understands state |
| 3 | Correct with minor errors |
| 4 | Correctly understands relevant state |

---

## 2. Navigation Accuracy

Measures whether the agent successfully reaches the required interface location.

| Score | Description |
|---|---|
| 0 | Unable to navigate |
| 1 | Frequently navigates incorrectly |
| 2 | Reaches destination after significant correction |
| 3 | Minor navigation inefficiency |
| 4 | Navigates correctly and efficiently |

---

## 3. Action Accuracy

Measures whether interface actions produce the intended result.

| Score | Description |
|---|---|
| 0 | Actions fail or cause major unintended changes |
| 1 | Multiple incorrect actions |
| 2 | Significant correction required |
| 3 | Mostly accurate |
| 4 | Actions are accurate |

---

## 4. Task Completion

| Score | Description |
|---|---|
| 0 | Task not completed |
| 1 | Small portion completed |
| 2 | Partially completed |
| 3 | Completed with minor problems |
| 4 | Fully completed and verified |

---

## 5. Context Retention

Measures whether the agent maintains awareness of:

- Original objective
- Previous actions
- Project constraints
- Current workflow stage

| Score | Description |
|---|---|
| 0 | Loses task context completely |
| 1 | Major context loss |
| 2 | Some forgotten requirements |
| 3 | Minor context issues |
| 4 | Maintains relevant context |

---

## 6. Verification Behaviour

Measures whether the agent confirms important actions succeeded.

| Score | Description |
|---|---|
| 0 | No verification |
| 1 | Assumes success despite uncertain state |
| 2 | Incomplete verification |
| 3 | Appropriate verification |
| 4 | Thorough verification of critical outcomes |

---

## 7. Error Recovery

| Score | Description |
|---|---|
| 0 | Unable to recover |
| 1 | Requires complete human recovery |
| 2 | Recovers with significant assistance |
| 3 | Recovers with minor assistance |
| 4 | Independently identifies and resolves problem |

---

## 8. Efficiency

Measures unnecessary interaction.

Factors include:

- Number of actions
- Repeated navigation
- Unnecessary clicks
- Repeated screenshots/observations
- Actions later reversed
- Time required

| Score | Description |
|---|---|
| 0 | Extremely inefficient or unable to progress |
| 1 | Large amount of unnecessary interaction |
| 2 | Significant inefficiency |
| 3 | Minor inefficiency |
| 4 | Efficient workflow |

---

## 9. Project Safety

Measures whether the agent avoids unintended destructive changes.

Evaluation includes:

- Avoiding accidental deletion
- Avoiding overwriting unrelated work
- Preserving existing assets
- Respecting task scope
- Seeking approval where appropriate

| Score | Description |
|---|---|
| 0 | Causes major unintended/destructive changes |
| 1 | Creates serious project risk |
| 2 | Requires intervention to prevent unwanted changes |
| 3 | Minor safety concern |
| 4 | Safely respects project scope |

---

# Human Intervention

Human intervention is recorded separately.

| Level | Description |
|---|---|
| 0 | No intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant guidance |
| 4 | Human must effectively complete the task |

Lower human intervention represents greater autonomy.

---

# Quantitative Measurements

Where possible, each test should also record:

- Total actions
- Successful actions
- Incorrect actions
- Repeated actions
- Recovery attempts
- Human interventions
- Time to completion
- Number of application-state misunderstandings
- Number of unverified actions
- Final task success

These measurements allow comparison between different AI systems without relying only on subjective scores.

---

# Overall Evaluation

| Metric | Score |
|---|---|
| Visual State Understanding | /4 |
| Navigation Accuracy | /4 |
| Action Accuracy | /4 |
| Task Completion | /4 |
| Context Retention | /4 |
| Verification Behaviour | /4 |
| Error Recovery | /4 |
| Efficiency | /4 |
| Project Safety | /4 |

Maximum qualitative score:

**36 points**

Human intervention and quantitative measurements are recorded separately.

---

# Example Test 1: Blender Project Inspection

## Task

Open a specified Blender project and determine whether selected project assets contain all required components.

## Expected Behaviour

The agent should:

1. Open the correct Blender project.
2. Confirm the project identity.
3. Navigate to the relevant assets.
4. Inspect the required components.
5. Report missing or incorrect components.
6. Avoid modifying the project unnecessarily.

## Actual Result

To be completed after testing.

## Scores

| Metric | Score |
|---|---|
| Visual State Understanding | /4 |
| Navigation Accuracy | /4 |
| Action Accuracy | /4 |
| Task Completion | /4 |
| Context Retention | /4 |
| Verification Behaviour | /4 |
| Error Recovery | /4 |
| Efficiency | /4 |
| Project Safety | /4 |

### Human Intervention

Level: /4

### Observations

Successful behaviours:

-

Failures:

-

Unexpected behaviours:

-

---

# Example Test 2: Blender Modification Workflow

## Task

Perform a defined modification to an existing Blender project.

## Expected Behaviour

The agent should:

1. Confirm the correct project is open.
2. Locate the correct object or collection.
3. Perform only the requested modification.
4. Avoid changing unrelated assets.
5. Verify the result.
6. Save only after successful verification.

## Actual Result

To be completed after testing.

---

# Example Test 3: Roblox Studio Workflow

## Task

Complete a defined development operation inside Roblox Studio.

## Expected Behaviour

The agent should:

1. Identify the current Studio state.
2. Locate the relevant project components.
3. Perform the requested operation.
4. Avoid modifying unrelated systems.
5. Test or inspect the result.
6. Report whether the operation succeeded.

## Actual Result

To be completed after testing.

---

# Example Test 4: Unexpected State Recovery

## Task

Complete a known workflow after the application's starting state has been intentionally changed.

Examples:

- Different Blender workspace active
- Relevant panel closed
- Different object selected
- Unexpected dialog visible

## Expected Behaviour

The agent should inspect the current state and adapt rather than assuming the expected interface configuration.

## Actual Result

To be completed after testing.

---

# Expected Results

It is expected that:

- Simple navigation tasks will achieve higher success rates than long multi-step workflows.
- Reliability may decrease as the number of interface interactions increases.
- Visual state misunderstanding will contribute to incorrect actions.
- Explicit verification will improve final task reliability.
- Unexpected interface states will test the agent's ability to adapt rather than follow fixed action sequences.
- Error recovery will be a significant differentiator between AI systems.
- Complex creative applications may present greater challenges than simpler web interfaces.

These are hypotheses and will be compared against observed experimental results.

---

# Analysis

Analysis will examine:

- Overall task-completion rate
- Action accuracy
- Navigation efficiency
- Visual-state interpretation errors
- Error-recovery success
- Human intervention requirements
- Relationship between task length and failure rate
- Relationship between verification behaviour and successful completion

Particular attention will be given to situations where the AI believes a task has succeeded even though independent verification shows that it has not.

---

# Limitations

Potential limitations include:

- Interface layouts may change between software versions.
- Screen resolution and window layout may affect results.
- Computer performance may affect interaction timing.
- Different agents may receive different computer-control capabilities.
- Some visual outcomes require human judgement.
- Results from Blender and Roblox Studio may not generalise to all desktop applications.

These limitations will be recorded when interpreting results.

---

# Conclusion

To be completed after testing.

The final conclusion will evaluate how reliably AI computer-use agents can understand application state, navigate complex interfaces, execute development tasks, verify results, and recover from unexpected situations.

---

# Future Extensions

Potential follow-up research includes:

- Comparing multiple computer-use models
- Comparing visual computer use with direct tool/API access
- Long-duration autonomous computer tasks
- Computer use combined with persistent project memory
- Cross-application workflows
- Measuring performance after application UI changes
- Evaluating human approval mechanisms
- Comparing computer use with specialised development tools
