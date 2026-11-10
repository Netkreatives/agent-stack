# Assess the current setup

Start read-only. The goal is to identify the smallest consequential gap, not generate a large report.

## Inspect the project

Read the root instructions, relevant nested instructions, package/build manifests, lockfiles, existing CI and immediate task documentation. Expand only where evidence requires it.

Find the actual commands for setup, running, formatting, testing and building. A command in a README is a candidate, not proof. Check it against the owning manifest or script.

Do not run installers, migrations, release scripts, writes to external services or expensive suites during an assessment. Even a test command may access production services, update snapshots or incur costs; inspect its relevant entry point before executing it.

Use a safe, inexpensive existing check when authorized and useful. Otherwise mark execution unverified and propose it as validation.

## Record capabilities

Use this table, shortened to the relevant rows:

| Capability | Existing mechanism | Status | Evidence and limits | Smallest useful next step |
| --- | --- | --- | --- | --- |
| Project navigation | | | | |
| Task completion contract | | | | |
| Execution tools and commands | | | | |
| Meaningful verification | | | | |
| Session recovery | | | | |
| Permission enforcement | | | | |
| Execution trace and handoff | | | | |
| Coordination, if needed | | | | |

Statuses:
- **Verified:** exercised or directly inspected at the level of the specific claim. State which.
- **Missing:** required for the intended use and absent.
- **Unsupported:** the available runtime/environment cannot supply it.
- **Unverified:** possibly present, but evidence is insufficient or the check was not run.
- **Not needed:** unnecessary for the current workflow; explain briefly.

Do not combine these into a score. A good navigation file cannot compensate for a missing verifier.

## Questions that matter

### Harness
Can the agent locate the code and commands? Are tool inputs, failures and side effects understandable? Is useful task state recoverable? Are credentials handled through established tooling?

### Loop
What observable result would demonstrate completion? Can the check reject an incorrect result? Does failure feedback identify expected versus observed behavior? What limits time, retries or spend, and when should the approach be reassessed?

A reproducing regression test is appropriate for a behavioral bug when feasible. Do not require a failing test for every documentation, exploration or setup task.

### Permissions
For each important boundary, identify the enforcing mechanism and what is actually restricted. Written instructions, runtime prompts, filesystem restrictions and externally controlled credentials provide different guarantees. Do not call a worktree a sandbox.

Do not test a boundary by attempting destructive or unauthorized actions. Use configuration inspection or a harmless approved probe. Configuration inspection establishes configured intent, not complete bypass resistance.

### Coordination
Start with one agent. Suggest multiple workers only if the task needs independent specialties, useful parallel work, different access or isolated failure recovery.

For every proposed dependency, ask whether the next job truly needs the previous output. Separate workers need explicit ownership and a controlled handoff. A separate context alone does not guarantee independent judgment.

## Deliver the proposal

Summarize:
1. What already works and should stay.
2. The first gap worth fixing and its practical consequence.
3. Exact proposed changes, acceptance checks, estimated validation cost and permission needs.

If nothing consequential is missing, recommend no changes. Do not create template files merely to show activity.
