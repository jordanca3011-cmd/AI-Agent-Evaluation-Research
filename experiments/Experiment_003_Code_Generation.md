
# Experiment 003: AI Agent Code Generation and Debugging

## Overview

This experiment evaluates the ability of AI agents to generate, modify, debug, and maintain code during real-world software development workflows.

AI coding performance should not be measured only by whether generated code is syntactically valid. In practical development environments, code must also satisfy requirements, integrate with existing systems, preserve project constraints, handle errors, and remain understandable and maintainable.

This experiment therefore evaluates AI-generated code across several stages of the development process.

---

## Research Question

How effectively can AI agents generate, modify, debug, and integrate code within complex, existing software development projects?

---

## Hypothesis

AI agents are expected to perform well on isolated and clearly specified programming tasks but may experience reduced reliability when tasks require understanding existing architecture, maintaining project-specific constraints, coordinating multiple files, or debugging unexpected behaviour.

Agents with access to relevant project context and execution/testing tools are expected to perform better than agents relying only on task descriptions.

---

## Objectives

This experiment evaluates whether an AI agent can:

- Understand programming requirements
- Generate syntactically valid code
- Generate functionally correct code
- Follow project-specific conventions
- Modify existing code without introducing regressions
- Integrate new functionality into existing systems
- Identify and diagnose bugs
- Correct its own mistakes
- Interpret runtime errors
- Verify generated code
- Produce maintainable solutions
- Minimise unnecessary human intervention

---

## Test Environments

Testing may involve:

- Python
- Blender Python API
- Roblox Luau
- Development utilities
- Automation scripts
- Existing project codebases

Primary case-study environments include:

- BLACKSITE: Containment
- Forgefront: Weapons Factory Tycoon
- Kingdom Tycoon

---

# Experimental Conditions

Code-generation tasks will be divided into several levels.

## Level 1: Isolated Code Generation

The agent receives a clearly defined programming task with minimal external dependencies.

Example:

> Write a Python function that validates whether required asset names exist in a supplied list.

### Purpose

Establish baseline code-generation ability.

### Evaluation

- Syntax correctness
- Functional correctness
- Requirement adherence
- Code clarity

---

## Level 2: Project-Specific Code Generation

The agent must generate code while following existing project requirements.

Example:

> Create a Blender Python script that checks required creature collections without modifying existing scene data.

### Evaluation

- Understanding of requirements
- Correct API usage
- Preservation of project constraints
- Output accuracy

---

## Level 3: Existing Code Modification

The agent receives existing code and must implement a new requirement without breaking current behaviour.

### Evaluation

- Understanding of existing architecture
- Quality of modification
- Regression avoidance
- Scope control

The agent should modify only what is necessary to satisfy the requirement.

---

## Level 4: Debugging

The agent receives code containing one or more known defects.

Potential defects include:

- Syntax errors
- Runtime errors
- Incorrect API calls
- Logical errors
- Incorrect assumptions
- Integration problems

The agent must:

1. Identify the problem.
2. Explain the likely cause.
3. Produce an appropriate correction.
4. Test or verify the correction when tools are available.
5. Avoid introducing additional problems.

---

## Level 5: Multi-File Integration

The agent must implement functionality involving multiple components or files.

Examples:

- Adding a gameplay feature across multiple Roblox scripts
- Creating a Blender automation utility that reads project configuration
- Updating an existing system while maintaining compatibility with related components

### Evaluation

This tests whether the agent can reason about relationships between different parts of a codebase.

---

## Level 6: Iterative Development

The agent receives an initial requirement and later receives additional or changed requirements.

### Evaluation Questions

- Can the agent adapt existing code?
- Does it preserve previously working functionality?
- Does it unnecessarily rewrite working systems?
- Does it maintain earlier project constraints?

---

# Test Procedure

Each coding test will follow a standard process.

## Step 1: Define Requirements

Document:

- Task objective
- Technical requirements
- Existing constraints
- Expected behaviour

---

## Step 2: Record Baseline

Where applicable, record the state of the existing code before AI modification.

This may include:

- Existing tests
- Current behaviour
- Known bugs
- Relevant files

---

## Step 3: Generate or Modify Code

The AI agent attempts the assigned task.

Record:

- Initial solution
- Significant reasoning or approach changes where observable
- Files modified
- Number of iterations

---

## Step 4: Execute or Test

Where possible, generated code should be executed or tested.

Potential methods include:

- Automated tests
- Runtime execution
- Blender execution
- Roblox Studio testing
- Manual verification

---

## Step 5: Debug

If the implementation fails, the AI agent should be given relevant error information and allowed to attempt recovery.

Record each correction attempt.

---

## Step 6: Final Verification

The final implementation is compared against the original requirements.

---

# Evaluation Metrics

## 1. Requirement Understanding

Measures whether the AI correctly understands what needs to be implemented.

| Score | Description |
|---|---|
| 0 | Fundamentally misunderstands task |
| 1 | Major requirements missed |
| 2 | Partially understands requirements |
| 3 | Minor misunderstandings |
| 4 | Correctly understands requirements |

---

## 2. Syntax Correctness

Measures whether generated code is syntactically valid.

| Score | Description |
|---|---|
| 0 | Code cannot execute |
| 1 | Multiple major syntax problems |
| 2 | Requires several corrections |
| 3 | Minor syntax correction required |
| 4 | Syntactically correct |

---

## 3. Functional Correctness

Measures whether the implementation behaves as required.

| Score | Description |
|---|---|
| 0 | Does not work |
| 1 | Major functionality incorrect |
| 2 | Partially functional |
| 3 | Mostly correct with minor issues |
| 4 | Fully satisfies expected behaviour |

---

## 4. Project Integration

Measures whether generated code works correctly with the existing project.

Evaluation includes:

- Existing architecture
- Dependencies
- Naming conventions
- Existing functionality
- Project-specific constraints

| Score | Description |
|---|---|
| 0 | Breaks or cannot integrate with project |
| 1 | Major integration problems |
| 2 | Significant adjustments required |
| 3 | Minor integration changes required |
| 4 | Integrates correctly |

---

## 5. Debugging Ability

Measures whether the agent can diagnose and resolve problems.

| Score | Description |
|---|---|
| 0 | Cannot diagnose failure |
| 1 | Incorrect diagnosis or fix |
| 2 | Requires substantial assistance |
| 3 | Resolves problem with minor assistance |
| 4 | Independently diagnoses and resolves issue |

---

## 6. Regression Avoidance

Measures whether existing functionality remains intact.

| Score | Description |
|---|---|
| 0 | Major existing functionality broken |
| 1 | Multiple regressions introduced |
| 2 | Significant regression requiring correction |
| 3 | Minor unintended effect |
| 4 | No observed regression |

---

## 7. Code Quality

Evaluation includes:

- Readability
- Structure
- Maintainability
- Appropriate comments
- Avoidance of unnecessary complexity

| Score | Description |
|---|---|
| 0 | Unusable or extremely poor code |
| 1 | Difficult to understand or maintain |
| 2 | Acceptable but requires improvement |
| 3 | Good quality |
| 4 | Clear and maintainable |

---

## 8. Verification Behaviour

Measures whether the agent checks that its implementation actually works.

| Score | Description |
|---|---|
| 0 | No verification |
| 1 | Assumes success |
| 2 | Limited verification |
| 3 | Appropriate testing |
| 4 | Thorough verification against requirements |

---

# Human Intervention

Human intervention will be recorded separately.

| Level | Description |
|---|---|
| 0 | No human intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant developer guidance |
| 4 | Human effectively completes/fixes task |

Lower intervention represents greater agent autonomy.

---

# Additional Quantitative Measurements

Where possible, record:

- Number of generated code attempts
- Number of failed executions
- Number of debugging attempts
- Number of human corrections
- Number of files modified
- Number of regressions
- Time to first working solution
- Total time to verified solution
- Automated tests passed
- Automated tests failed

---

# Overall Evaluation

Each test will record:

| Metric | Score |
|---|---|
| Requirement Understanding | /4 |
| Syntax Correctness | /4 |
| Functional Correctness | /4 |
| Project Integration | /4 |
| Debugging Ability | /4 |
| Regression Avoidance | /4 |
| Code Quality | /4 |
| Verification Behaviour | /4 |

Maximum qualitative score:

**32 points**

Human intervention and quantitative measurements will be recorded separately.

---

# Example Test 1: Blender Python

## Task

Generate a Blender Python script that inspects specified collections and reports missing required objects without modifying the scene.

## Expected Behaviour

The agent should:

1. Correctly use the Blender Python API.
2. Locate the specified collections.
3. Inspect required objects.
4. Report missing components.
5. Avoid modifying project data.
6. Handle missing collections safely.

## Actual Result

To be completed after testing.

## Scores

| Metric | Score |
|---|---|
| Requirement Understanding | /4 |
| Syntax Correctness | /4 |
| Functional Correctness | /4 |
| Project Integration | /4 |
| Debugging Ability | /4 |
| Regression Avoidance | /4 |
| Code Quality | /4 |
| Verification Behaviour | /4 |

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

# Example Test 2: Roblox Luau

## Task

Generate or modify a Roblox gameplay script while preserving existing project functionality.

## Expected Behaviour

The agent should:

- Understand the requested gameplay behaviour
- Produce valid Luau
- Integrate with existing systems
- Avoid unnecessary changes
- Test or verify the implementation where possible

## Actual Result

To be completed after testing.

---

# Example Test 3: Debugging

## Task

Provide the AI agent with code containing a known runtime or logic error.

## Expected Behaviour

The agent should:

1. Analyse the code.
2. Identify the likely cause.
3. Produce a targeted correction.
4. Avoid rewriting unrelated components.
5. Execute or test the correction.
6. Confirm that the original problem is resolved.

## Actual Result

To be completed after testing.

---

# Expected Results

It is expected that:

- AI agents will perform better on isolated coding tasks than on complex project integration tasks.
- Clear technical requirements will improve code-generation accuracy.
- Access to execution and testing tools will improve final reliability.
- Debugging performance will vary depending on the quality of available error information.
- Multi-file tasks will require greater context awareness.
- Verification behaviour will strongly affect final implementation reliability.
- Some agents may produce plausible-looking code without sufficiently verifying that it works.

These are hypotheses and will be evaluated against observed results.

---

# Analysis

Analysis will examine:

- Code-generation success rate
- First-attempt success rate
- Debugging success rate
- Frequency of regressions
- Human intervention requirements
- Relationship between task complexity and performance
- Relationship between tool access and code quality
- Differences between AI systems or models

Particular attention will be given to cases where generated code appears technically plausible but fails during real execution.

---

# Limitations

Potential limitations include:

- Different programming languages have different levels of model training coverage.
- Blender and Roblox APIs may change over time.
- Project complexity varies between experiments.
- Some bugs may be substantially harder than others.
- Human judgement is required when evaluating maintainability.
- Results from game-development workflows may not generalise to all software engineering domains.

These limitations will be documented when interpreting results.

---

# Conclusion

To be completed after testing.

The final conclusion will summarise how effectively AI agents generate, integrate, debug, and maintain code during real-world development workflows.

---

# Future Extensions

Future experiments may investigate:

- Model-to-model coding comparisons
- AI-generated code with and without execution tools
- Long-term codebase maintenance
- Autonomous debugging
- Test generation
- Security and robustness of generated code
- Large multi-file codebases
- Effects of project memory on coding performance
