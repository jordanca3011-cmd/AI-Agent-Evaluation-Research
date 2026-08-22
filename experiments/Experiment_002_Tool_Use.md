
# Experiment 002: AI Agent Tool Use Reliability

## Overview

This experiment evaluates how effectively AI agents select, use, and verify tools while completing complex software development tasks.

Modern AI agents can interact with external tools such as code execution environments, terminals, file systems, development applications, and computer-control systems. Successful agent behaviour therefore depends not only on reasoning ability, but also on selecting the correct tool, providing valid instructions, interpreting results, and recovering when an action fails.

This experiment focuses on real-world development workflows involving Blender, Roblox Studio, Python, file management, and computer-use tools.

---

## Research Question

How reliably can AI agents select and use appropriate tools to complete multi-step tasks in complex software development environments?

---

## Hypothesis

AI agents will generally perform well when the required tool and task are clearly defined, but reliability will decrease as tasks require longer sequences of tool interactions, interpretation of changing application state, and recovery from unexpected errors.

It is expected that verification after tool execution will be an important factor in overall task reliability.

---

## Objectives

The experiment will evaluate whether an AI agent can:

- Select an appropriate tool for a task
- Generate valid tool instructions
- Execute tools in the correct sequence
- Interpret returned information accurately
- Verify whether an action succeeded
- Detect unexpected results
- Recover from tool failures
- Avoid unnecessary or inappropriate tool calls
- Maintain project constraints while using tools
- Complete multi-step workflows with limited human intervention

---

## Test Environments

Testing may be conducted using:

- Blender
- Roblox Studio
- Python
- Terminal/command-line environments
- File-system tools
- Computer-use tools
- Development and debugging tools

The primary case-study projects are:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon

---

## Experimental Conditions

Tool-use tasks will be divided into several levels of complexity.

### Level 1: Single Tool Action

The agent performs one clearly defined action.

Examples:

- Inspect a Blender object
- Read a project file
- Execute a Python script
- Retrieve an application state

Purpose:

Establish baseline tool-use reliability.

---

### Level 2: Tool Selection

The agent receives a goal but is not explicitly told which available tool to use.

Example:

> Determine which creatures in a Blender project are missing required assets.

The agent must decide whether to inspect project data, query Blender, read documentation, or use another available tool.

Evaluation focuses on whether the most appropriate tool is selected.

---

### Level 3: Multi-Step Tool Workflow

The agent must perform several related operations.

Example workflow:

1. Inspect the current Blender scene.
2. Identify the relevant collections.
3. Determine whether required objects exist.
4. Perform an approved modification.
5. Verify the modification.
6. Save the project.

This tests whether the agent can maintain state across multiple tool interactions.

---

### Level 4: Tool Failure and Recovery

A controlled failure or unexpected result is introduced.

Examples:

- Invalid command
- Missing object
- Incorrect object name
- Script execution error
- Unexpected application state

The agent must:

1. Recognise that the action failed.
2. Interpret the error.
3. Determine an alternative approach.
4. Retry safely.
5. Verify the final result.

---

### Level 5: Cross-Tool Workflow

The agent must coordinate multiple tools.

Example:

1. Inspect project documentation.
2. Query Blender project state.
3. Generate or modify Python code.
4. Execute the code.
5. Inspect the resulting scene.
6. Record the result.

This evaluates whether the agent can transfer information correctly between different tools.

---

## Test Procedure

Each test will follow the same general procedure.

### Step 1: Define the Task

A specific development objective is provided to the agent.

The expected result is documented before testing begins.

### Step 2: Record Available Tools

The tools available to the agent are recorded.

This allows analysis of whether the agent selected an appropriate tool.

### Step 3: Execute the Task

The agent attempts to complete the objective.

All significant tool actions and errors are recorded where practical.

### Step 4: Verify the Result

The final state is checked against the expected result.

### Step 5: Score Performance

Performance is scored using the project's evaluation metrics.

---

## Data Collection

For each test, the following information will be recorded:

- AI system/model tested
- Date
- Task
- Available tools
- Tool selected
- Number of tool calls
- Successful tool calls
- Failed tool calls
- Incorrect tool selections
- Recovery attempts
- Human interventions
- Final task outcome
- Time required
- Observed failure modes

---

## Tool Selection Accuracy

This metric measures whether the agent chooses an appropriate tool.

| Score | Description |
|---|---|
| 0 | Unable to select a usable tool |
| 1 | Selects an inappropriate tool and requires human correction |
| 2 | Eventually selects an appropriate tool after unnecessary attempts |
| 3 | Selects an appropriate tool with minor inefficiency |
| 4 | Selects the most appropriate tool immediately |

---

## Tool Execution Accuracy

This metric measures whether the agent uses the selected tool correctly.

| Score | Description |
|---|---|
| 0 | Tool execution completely fails |
| 1 | Major errors prevent successful execution |
| 2 | Execution works after significant correction |
| 3 | Successful with minor corrections |
| 4 | Correct execution without intervention |

---

## Result Interpretation

This metric measures whether the agent correctly understands information returned by tools.

Examples include:

- Understanding an error message
- Correctly interpreting Blender scene information
- Recognising whether a script succeeded
- Understanding application state

| Score | Description |
|---|---|
| 0 | Completely misinterprets result |
| 1 | Major misunderstanding |
| 2 | Partially correct interpretation |
| 3 | Correct with minor issues |
| 4 | Correct interpretation |

---

## Verification Behaviour

This metric measures whether the agent confirms that its actions produced the intended result.

| Score | Description |
|---|---|
| 0 | Performs no verification |
| 1 | Assumes success despite uncertain state |
| 2 | Performs incomplete verification |
| 3 | Performs adequate verification |
| 4 | Performs thorough and appropriate verification |

---

## Error Recovery

This metric measures the agent's response when a tool action fails.

| Score | Description |
|---|---|
| 0 | Cannot recover |
| 1 | Requires complete human intervention |
| 2 | Recovers after significant assistance |
| 3 | Recovers with minor assistance |
| 4 | Independently diagnoses and resolves the failure |

---

## Tool Efficiency

This metric evaluates unnecessary actions.

Measurements may include:

- Total tool calls
- Redundant tool calls
- Failed calls
- Repeated inspections
- Unnecessary application interactions

An efficient agent should complete the task using an appropriate number of actions without sacrificing verification or safety.

---

## Human Intervention

Human intervention will be recorded using the following scale:

| Level | Description |
|---|---|
| 0 | No intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant guidance |
| 4 | Human must effectively complete the task |

Lower scores represent greater autonomy for this metric.

---

## Overall Evaluation

Each experiment will record:

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Tool Selection | /4 |
| Tool Execution | /4 |
| Result Interpretation | /4 |
| Verification | /4 |
| Error Recovery | /4 |
| Context Retention | /4 |
| Reliability | /4 |
| Efficiency | /4 |

Human intervention will be recorded separately because lower intervention represents better autonomous performance.

---

## Example Test: Blender Scene Inspection

### Task

Inspect a Blender project and determine whether specified creature assets contain all required components.

### Expected Behaviour

The agent should:

1. Select an appropriate Blender inspection tool.
2. Inspect the relevant scene data.
3. Identify the required objects or collections.
4. Compare the observed state against project requirements.
5. Report missing or incorrect components.
6. Avoid modifying the project unnecessarily.

### Result

To be completed after testing.

### Scores

| Metric | Score |
|---|---|
| Task Completion | /4 |
| Tool Selection | /4 |
| Tool Execution | /4 |
| Result Interpretation | /4 |
| Verification | /4 |
| Error Recovery | /4 |
| Context Retention | /4 |
| Reliability | /4 |
| Efficiency | /4 |

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

## Example Test: Tool Failure Recovery

### Task

Complete a development operation where the initial tool action produces an error.

### Expected Behaviour

The agent should:

1. Recognise the failure.
2. Read and interpret the error.
3. Avoid repeatedly executing the same failing action.
4. Determine the likely cause.
5. Modify its approach.
6. Retry the task.
7. Verify successful completion.

### Result

To be completed after testing.

---

## Expected Results

It is expected that:

- Single-tool tasks will have higher success rates than multi-tool workflows.
- Tool-selection errors will increase when several similar tools are available.
- Longer workflows will create more opportunities for state-tracking errors.
- Agents that explicitly verify actions will have higher final task success rates.
- Error recovery will be a major differentiator between more and less capable agents.
- Tool reliability may depend on the quality and structure of information returned to the agent.
- Human intervention requirements are expected to increase as workflow complexity increases.

These are hypotheses and will be compared against observed results rather than treated as conclusions.

---

## Analysis

After sufficient tests have been completed, analysis will examine:

- Tool selection success rate
- Tool execution success rate
- Relationship between tool-call count and task success
- Common causes of tool failures
- Frequency of unnecessary actions
- Verification behaviour
- Error recovery performance
- Human intervention requirements
- Differences between AI systems or models

Particular attention will be given to situations where an agent reports successful completion even though the underlying tool result indicates failure.

---

## Limitations

Potential limitations include:

- Different tools provide different amounts of feedback.
- Application updates may change tool behaviour.
- Some creative tasks do not have a single objectively correct outcome.
- Human judgement may be required when evaluating visual results.
- Tool availability may differ between AI systems.
- Results from Blender and Roblox workflows may not generalise to every software environment.

These limitations will be documented when interpreting results.

---

## Conclusion

To be completed after testing.

The final conclusion will summarise how reliably AI agents can select, execute, interpret, verify, and recover from tool interactions during complex development workflows.

---

## Future Extensions

Future experiments may investigate:

- Different models using identical tools
- Computer-use agents versus direct API/tool integrations
- Long-duration autonomous workflows
- Tool-use performance with external project memory
- Recovery from multiple consecutive failures
- Effects of tool documentation quality
- Cross-application workflows
- Human approval and safety mechanisms
