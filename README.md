# Agent Stack

Give a coding agent a repository it can understand, checks it can run, and a reliable way to resume.

Agent Stack is a practical setup playbook for **existing coding repositories**. Point an agent at [APPLY.md](APPLY.md): it inspects your project, proposes the smallest useful improvements, applies approved changes, and reports evidence.

**Status:** initial documentation and templates. The [worked example](examples/worked-example/README.md) is a specification, not an executed demonstration. Runtime compatibility and productivity improvements have not been established.

## Start here

Open your target project in your coding agent and give it this instruction:

> Read https://github.com/Netkreatives/agent-stack/blob/main/APPLY.md and follow it for the repository currently open. Start with a read-only assessment. Respect this project's instructions and permissions, preserve existing work, and reuse its tooling. Propose exact changes and acceptance checks, then wait for approval before editing. Do not commit, push, deploy, install dependencies or change permissions without authorization covering that action.

For reproducible use, replace `main` in the link with a reviewed commit SHA. Keep the resulting assessment and approval together.

The agent should return:

1. An evidence-based assessment of existing capabilities and gaps.
2. A bounded proposal naming exact files, commands, permission needs and acceptance criteria.
3. After approval, an acceptance report distinguishing verified behavior from remaining uncertainty.

**No changes needed is a successful outcome.** Do not add a new instruction system on top of one that already works.

## The three layers

| Layer | What it supplies | Typical project improvement |
| --- | --- | --- |
| Harness | Environment: context, tools, saved state, permissions and traces | A short navigation guide pointing to real setup and testing instructions |
| Loop | Feedback: act, check, repair and stop | A focused verifier, actionable failures and a bounded retry policy |
| Graph | Coordination: separate jobs and explicit dependencies | Independent work with defined ownership and controlled handoffs |

Begin with a harness and one verification loop. Add orchestration only when a demonstrated need justifies it. Each layer needs observable evidence; a document describing a capability does not establish that it works.

## What gets assessed

- **Project navigation:** can an agent find the relevant code and commands without reading every document?
- **Task contract:** are the requested result, boundaries and completion evidence explicit?
- **Execution:** do documented commands exist, and can they actually run in the available environment?
- **Verification:** what does each check establish, and what remains outside its coverage?
- **Continuity:** can another session recover completed work, failed approaches and the next useful step?
- **Permissions:** which restrictions are guidance, and which are actually enforced?
- **Traceability:** can someone inspect the patch, checks and unresolved risks?
- **Coordination, if needed:** are ownership, dependencies and failure recovery explicit?

Use the statuses **verified**, **missing**, **unsupported**, **unverified** and **not needed**. No numerical readiness score.

## Read the playbooks

| File | Purpose |
| --- | --- |
| [APPLY.md](APPLY.md) | Entry point and application contract |
| [Assess](playbooks/assess.md) | Inspect existing capabilities and collect evidence |
| [Apply](playbooks/apply.md) | Make approved, minimal changes without overwriting conventions |
| [Verify](playbooks/verify.md) | Exercise the setup and explain the limits |
| [Task contract](templates/task-contract.md) | Define one task and its completion evidence |
| [Progress record](templates/progress.md) | Persist useful state across sessions |
| [Acceptance report](templates/acceptance-report.md) | Record results, commands and remaining limitations |
| [Worked-example specification](examples/worked-example/README.md) | Define future demonstrations and their pass conditions |

Templates are starting points. Adapt or omit them rather than creating empty paperwork. Use existing equivalents whenever possible.

## Boundaries

This repository does not grant permissions in your agent runtime. An `AGENTS.md` rule is guidance; a sandbox or independently enforced policy is a restriction. A Git worktree isolates changes but is not a security sandbox.

Do not weaken checks to obtain a passing result. Passing tests establish only the behavior they exercise. A second agent can share the first agent's assumptions, even in a separate context.

There is no installer, runtime or agent framework in this release. Support for a particular coding agent or stack must be demonstrated before it is advertised.

## Credits and sources

The harness / loop / graph framing was inspired by [Whitemon's article](https://x.com/0xWhitemon/status/2119430401701621865), with related writing by [IntuitMachine](https://x.com/IntuitMachine/status/2078419526354378975) and [leopardracer](https://x.com/leopardracer/status/2079491296557781155). Practical foundations include [Ryan Lopopolo's OpenAI article](https://openai.com/index/harness-engineering/) and [Anthropic Engineering's work on long-running agents](https://www.anthropic.com/research/effective-harnesses-for-long-running-agents).

See [SOURCES.md](SOURCES.md) for individual contributions, original links, and the distinction between source ideas and this repository's application procedure. Credit does not imply endorsement. Original articles and artwork are linked rather than reproduced.
