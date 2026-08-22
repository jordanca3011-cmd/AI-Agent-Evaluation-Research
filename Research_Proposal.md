# Research Proposal: Evaluating AI Agents in Long-Term Creative Software Development

## Abstract

AI systems are increasingly capable of generating code, using external tools, interacting with software applications, and assisting with complex development tasks. However, successful performance on isolated prompts does not necessarily demonstrate that an AI agent can function reliably as a long-term development collaborator.

This research proposes a practical evaluation framework for studying AI agents during extended software, creative, and game-development workflows.

The research focuses on four core capabilities:

1. Context retention
2. Tool use
3. Code generation and debugging
4. Computer use

Experiments will combine controlled tests with real-world development case studies involving Blender, Roblox Studio, Python, Luau, coding agents, and game-development workflows.

The objective is to measure not only whether an AI agent completes a task, but whether it maintains project requirements, selects and uses tools appropriately, verifies its work, recovers from errors, avoids regressions, preserves existing project state, and minimises the human intervention required.

A further objective is to investigate whether reliable AI development agents could improve game-development efficiency by reducing repetitive technical work, accelerating prototyping, assisting with testing and debugging, and enabling independent developers and smaller teams to create more ambitious interactive experiences while maintaining human creative direction.

The research aims to produce practical evidence about the strengths, limitations, and failure modes of AI agents operating in realistic development environments.

---

# 1. Introduction

AI-assisted software development has progressed from code completion and conversational programming toward systems capable of interacting with tools and completing multi-step tasks.

Modern AI agents may be capable of:

- Reading existing code
- Generating new code
- Executing development operations
- Using specialised tools
- Interacting with graphical applications
- Debugging errors
- Modifying project files
- Testing implementations
- Maintaining task context across multiple steps

These capabilities create the possibility of AI systems functioning as active development collaborators rather than passive conversational assistants.

However, real software and game development differs significantly from isolated benchmark tasks.

Long-term development projects contain:

- Existing architecture
- Previous decisions
- Changing requirements
- Large collections of files and assets
- Interconnected systems
- Application-specific constraints
- Unexpected errors
- Creative requirements
- Existing functionality that must be preserved

An AI agent may successfully complete a short programming task while still struggling to operate reliably across an extended development workflow.

This research investigates that gap.

---

# 2. Research Problem

Many AI evaluations focus on isolated tasks such as:

- Answering technical questions
- Generating individual functions
- Solving programming challenges
- Completing benchmark datasets
- Producing code from short specifications

These evaluations are useful but do not fully represent long-term human-AI development collaboration.

A development agent may need to:

1. Understand an existing project.
2. Retrieve relevant context.
3. Remember previous decisions.
4. Identify the current project state.
5. Select appropriate tools.
6. Make controlled modifications.
7. Execute or test its work.
8. Recognise failures.
9. Recover from errors.
10. Verify the final result.
11. Avoid damaging existing functionality.
12. Continue working across multiple development stages.

This creates additional questions about AI-agent reliability that cannot always be measured using isolated coding benchmarks.

---

# 3. Primary Research Question

> How effectively can AI agents support complex, long-term creative software development workflows while maintaining project context, executing multi-step tasks, using tools reliably, and recovering from errors?

---

# 4. Secondary Research Questions

## RQ1 — Context Retention

How reliably can AI agents retain and apply project-specific information across extended development workflows?

## RQ2 — Tool Use

How accurately can AI agents select, execute, interpret, and verify external development tools?

## RQ3 — Code Generation

How effectively can AI agents generate, modify, debug, integrate, and maintain code inside existing projects?

## RQ4 — Computer Use

How reliably can AI agents interact with graphical software environments to complete multi-step development tasks?

## RQ5 — Error Recovery

How effectively can agents identify and recover from failed actions, incorrect assumptions, runtime errors, and unexpected application states?

## RQ6 — Human Intervention

How much human assistance is required for AI agents to successfully complete realistic development tasks?

## RQ7 — Structured Project Context

Does providing structured project context improve AI-agent reliability compared with providing only immediate task instructions?

## RQ8 — Task Complexity

How does agent performance change as tasks increase in length, complexity, and number of required interactions?

## RQ9 — Game Development Efficiency

To what extent can AI-agent assistance reduce development time and repetitive workload in game-development workflows without reducing quality, reliability, or developer control?

---

# 5. Hypotheses

The research begins with several hypotheses.

## H1

AI agents will perform more reliably on isolated tasks than on long-horizon development workflows.

## H2

Providing structured project context will reduce requirement violations, repeated work, and incorrect assumptions.

## H3

Agents with access to appropriate execution and inspection tools will achieve higher verified task-completion rates than agents relying only on conversational reasoning.

## H4

Agents that perform explicit verification will produce more reliable outcomes than agents that assume successful execution.

## H5

Error-recovery capability will be an important differentiator between AI-agent systems.

## H6

Human intervention requirements will increase as task complexity and workflow length increase.

## H7

AI assistance may reduce development time for some game-development tasks, but correction and verification costs may reduce or eliminate these gains when agent reliability is poor.

These hypotheses will be evaluated against experimental evidence and should not be treated as predetermined conclusions.

---

# 6. Research Approach

The project uses a mixed practical evaluation approach combining:

- Controlled experiments
- Repeatable test suites
- Real-world development case studies

Controlled experiments provide more consistent conditions for comparison.

Real-world case studies expose agents to the complexity and uncertainty found in genuine development projects.

Using both approaches allows the research to investigate controlled capability differences while also examining whether those capabilities remain reliable in practical workflows.

---

# 7. Controlled Experiments

The initial experimental programme contains four major experiments.

## Experiment 001 — Context Retention

Evaluates whether AI agents maintain:

- Project requirements
- Previous decisions
- Naming conventions
- Technical constraints
- Current development state
- Completed work

Reference:

`experiments/Experiment_001_Context_Retention.md`

---

## Experiment 002 — Tool Use

Evaluates:

- Tool selection
- Tool execution
- Tool-result interpretation
- Verification
- Failure detection
- Error recovery

Reference:

`experiments/Experiment_002_Tool_Use.md`

---

## Experiment 003 — Code Generation

Evaluates:

- Requirement understanding
- Code generation
- Existing-code modification
- Debugging
- Multi-file integration
- Regression avoidance
- Verification

Reference:

`experiments/Experiment_003_Code_Generation.md`

---

## Experiment 004 — Computer Use

Evaluates AI interaction with graphical development applications.

Measurements may include:

- Visual-state understanding
- Navigation accuracy
- Action accuracy
- Repeated actions
- Error recovery
- Verification
- Efficiency
- Project safety

Reference:

`experiments/Experiment_004_Computer_Use.md`

---

# 8. Test Suites

Three repeatable environment-specific test suites support the experiments.

## Blender Test Suite

`experiments/blender-tests.md`

Evaluates:

- Scene understanding
- Object identification
- Collection structure
- Blender Python
- Materials
- Asset organisation
- Error recovery
- Constraint following
- Computer use
- Long-horizon Blender workflows

## Coding Agent Test Suite

`experiments/coding-agent-tests.md`

Evaluates:

- Code generation
- Existing-code understanding
- Targeted modification
- Multi-file development
- Debugging
- Testing
- Tool use
- Context retention
- Regression avoidance
- Long-horizon development

## Roblox Test Suite

`experiments/roblox-tests.md`

Evaluates:

- Roblox project understanding
- Luau generation
- Roblox API usage
- Client-server reasoning
- Multiplayer systems
- Gameplay implementation
- Debugging
- Playtesting
- Roblox Studio computer use

---

# 9. Real-World Case Studies

Controlled benchmarks alone may not capture the complexity of real development.

The research therefore includes ongoing development projects as case studies.

## BLACKSITE: Containment

A complex Roblox and Blender development project involving:

- Large 3D environments
- Creature assets
- Asset pipelines
- Gameplay systems
- Project-specific constraints
- Long-term project context
- Blender-to-Roblox workflows

This case study is particularly useful for evaluating long-horizon context retention, complex tool use, project safety, and cross-application development.

Reference:

`Case_Studies/BLACKSITE.md`

---

## Forgefront: Weapons Factory Tycoon

A Roblox development project containing interconnected systems involving:

- Factory production
- Economy
- Combat
- Capture objectives
- Vehicles
- Progression
- Rebirth systems

This case study can be used to evaluate systems reasoning, Luau development, gameplay integration, balancing, and regression avoidance.

Reference:

`Case_Studies/Forgefront.md`

---

## Kingdom Tycoon

A stylised fantasy Roblox and Blender project involving:

- 3D asset collections
- Environment development
- Modular assets
- Material consistency
- Visual design
- Blender-to-Roblox workflows

This case study can be used to evaluate creative workflows, asset organisation, Blender automation, project consistency, and human-AI creative collaboration.

Reference:

`Case_Studies/Kingdom_Tycoon.md`

---

# 10. Evaluation Framework

Agent performance is evaluated using:

`methodology/evaluation-framework.md`

and:

`Data/evaluation_metrics.md`

Core metrics include:

| Metric | Purpose |
|---|---|
| Task Completion | Was the requested objective achieved? |
| Requirement Understanding | Did the agent understand the task? |
| Accuracy | Were outputs and actions correct? |
| Context Retention | Were relevant previous requirements maintained? |
| Tool Use | Were tools selected and operated correctly? |
| Error Recovery | Could the agent recover after failure? |
| Verification | Did the agent confirm that its work succeeded? |
| Efficiency | Was unnecessary work avoided? |
| Project Integration | Did the result integrate with existing systems? |
| Regression Avoidance | Was existing functionality preserved? |
| Project Safety | Were unintended changes avoided? |

Applicable metrics use a 0–4 scale.

Metrics that do not apply to a specific experiment are recorded as `N/A`.

---

# 11. Human Intervention

Human intervention is recorded separately.

| Level | Description |
|---|---|
| 0 | No intervention |
| 1 | Minor clarification |
| 2 | Occasional correction |
| 3 | Significant guidance |
| 4 | Human effectively completes the task |

Lower intervention represents greater agent autonomy.

The reason for intervention should also be recorded because the numeric level alone may not explain why assistance was necessary.

---

# 12. Verification

A central principle of the research is that AI self-reported success is not sufficient evidence of task completion.

Where practical, results should be independently verified using:

- Automated tests
- Runtime execution
- Git comparison
- File inspection
- Blender scene inspection
- Roblox Studio playtesting
- Application-state inspection
- Human review

This allows the research to distinguish between:

> The agent reported that the task succeeded.

and:

> The final project state independently demonstrated that the task succeeded.

---

# 13. Failure Analysis

Agent failures are treated as research evidence rather than discarded results.

Failure categories include:

- Requirement failure
- Context failure
- Reasoning failure
- Tool-selection failure
- Tool-execution failure
- Code failure
- Integration failure
- Verification failure
- Recovery failure
- Regression
- Safety/scope failure
- Efficiency failure

Failures may also be classified by severity.

Repeated failure patterns may become targets for additional controlled experiments.

---

# 14. Comparative Testing

Where practical, equivalent tasks will be performed using different:

- AI models
- Agent systems
- Context configurations
- Tool configurations

For example:

## Condition A — Minimal Context

The agent receives only the immediate task and essential information.

## Condition B — Structured Context

The agent additionally receives relevant:

- Project overview
- Architecture
- Previous decisions
- Constraints
- Naming conventions
- Current project state

Performance can then be compared.

---

# 15. Data Collection

Each experimental run should record where applicable:

- Experiment ID
- Test ID
- Trial ID
- Date
- AI system
- Model
- Agent mode
- Software version
- Available tools
- Project context supplied
- Starting state
- Task
- Constraints
- Expected result
- Actual result
- Verification method
- Metric scores
- Tool calls
- Failed tool calls
- Interface actions
- Incorrect actions
- Debugging attempts
- Regressions
- Human interventions
- Completion time
- Failure classification

---

# 16. Data Analysis

Initial analysis will primarily use descriptive statistics.

Potential measurements include:

## Task Completion Rate

```text
Completed Tasks / Total Tasks
AI agents may eventually provide a new form of development assistance where an AI system can help perform practical development work while a human developer remains responsible for creative direction and important decisions.

This research aims to investigate how close current AI systems are to supporting this type of workflow reliably.

---

## Improving Development Efficiency

A reliable AI development agent could reduce the amount of time developers spend on repetitive or technical tasks.

Potential examples include:

- Generating boilerplate code
- Finding bugs
- Running tests
- Inspecting project structure
- Organising assets
- Preparing 3D assets
- Checking naming conventions
- Identifying missing components
- Performing repetitive Blender operations
- Creating or modifying gameplay scripts
- Testing gameplay systems
- Documenting project changes

Instead of replacing the developer, the AI agent could act as an additional development tool.

For example, a developer might describe a gameplay feature and allow an AI agent to inspect the existing project, identify the relevant systems, implement an initial version, run tests, identify problems, and present the result for human review.

A workflow could potentially become:

```text
Developer Idea
      ↓
AI Project Analysis
      ↓
Implementation Plan
      ↓
Code / Asset Work
      ↓
Automated Testing
      ↓
AI Verification
      ↓
Human Review
      ↓
Iteration
