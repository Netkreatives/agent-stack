# Sources and acknowledgments

Agent Stack translates published ideas into a project-assessment and application procedure. The harness / loop / graph framing and many underlying practices come from the writers below. We do not claim to have invented them.

Reviewed for this initial edition on 2026-11-10. Links identify the original publications. X article text and images were inspected through a third-party mirror because direct X fetching was blocked; that access path is not an independent verification of every factual claim in the articles.

## Core inspiration

### Whitemon (@0xWhitemon)
[Harness, Loop, Graph: The 3 Layers That Decide If Your AI Agent Works](https://x.com/0xWhitemon/status/2119430401701621865) — November 8, 2026.

Credit: the organizing distinction between environment, verification feedback and work coordination; the contract/map/tools/memory/walls/traces checklist; practical failure diagnosis.

Agent Stack adapts this into assessment, approval, application and acceptance playbooks. It does not reproduce the article or its artwork.

### IntuitMachine (@IntuitMachine)
[From Loop Engineering to Graph Engineering?](https://x.com/IntuitMachine/status/2078419526354378975)

Credit: loops can optimize the wrong metric, conflict with each other or drift away from reality. Coordinated systems still need independent observations, explicit authority and protected constraints.

[Loop Engineering and The Missing Compiler](https://x.com/IntuitMachine/status/2068808668393451770)

Credit: choose a verifier appropriate to the level of the claim; distinguish useful checks from repeated self-assurance, and recognize the limits of automated judgment.

The compiler analogy is a metaphor. Compilation does not prove arbitrary program behavior, and tests/review do not provide complete correctness guarantees.

### leopardracer (@leopardracer)
[From Loop Engineering to Graph Engineering](https://x.com/leopardracer/status/2079491296557781155)

Credit: nodes, routing and shared state; when separate roles and failure isolation help; explicit warnings that a single loop is often enough.

### Ryan Lopopolo / OpenAI
[Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/) — February 11, 2026.

Credit: repository knowledge as the system of record, concise navigation with deeper documentation, mechanically enforced constraints, and improving the environment when agents struggle.

This is experience from a particular environment, not a guarantee of the same outcome elsewhere.

### Anthropic Engineering
[Effective harnesses for long-running agents](https://www.anthropic.com/research/effective-harnesses-for-long-running-agents) — November 26, 2025.

Credit: incremental progress across context windows, environment initialization, durable progress records and checks that help a new session recover the actual work state.

## Contributors cited through the original article

These are supporting perspectives and product announcements, not independently established performance guarantees:

| Contributor | Original source | Contribution acknowledged |
| --- | --- | --- |
| Andrej Karpathy (@karpathy) | [Programming's expanding agent-tooling layer](https://x.com/karpathy/status/2004607146781278521) | The growing set of concepts and tools surrounding model use |
| Mitchell Hashimoto (@mitchellh) | [Generic agent harnesses and CLI/MCP](https://x.com/mitchellh/status/2077788454860316915) | The value of general-purpose harnesses with existing tools and context |
| Boris Cherny (@bcherny) | [Long-running agent tips](https://x.com/bcherny/status/2063792263067754658) | Giving agents ways to verify work end to end |
| Boris Cherny (@bcherny) | [The /loop announcement](https://x.com/bcherny/status/2030193932404150413) | A concrete recurring-task feature; not a portable verification-loop specification |
| Peter Steinberger (@steipete) | [Loops or graphs?](https://x.com/steipete/status/2078277297791189132) | The question that prompted the cited coordination discussion |
| Santiago (@svpino) | [Graph engineering response](https://x.com/svpino/status/2078516761318584774) | Participation in the loop-versus-graph discussion |
| Rohit (@rohit4verse) | [Four-image explanation](https://x.com/rohit4verse/status/2078776077745623498) | Coordinated loops and the need for real-world anchors |
| Rohit (@rohit4verse) | [Separate review and failure isolation](https://x.com/rohit4verse/status/2079945989511905549) | Separating production from review and limiting failure propagation |
| Anthropic (@claudeai) | [Managed Agents announcement](https://x.com/claudeai/status/2041927687460024721) | An example of a managed harness product |

Product features and availability change. Consult the provider's current documentation before relying on any named command or service. These posts are not runtime support commitments by Agent Stack.

## Technical references

- [LangGraph overview — LangChain](https://docs.langchain.com/oss/python/langgraph/overview): a concrete stateful orchestration framework.
- [Agent Development Kit — Google](https://adk.dev/): a concrete agent development and workflow toolkit.

These illustrate existing implementations of coordination patterns. Agent Stack currently integrates with neither and requires neither.

## Related material not verified here

[QPT video linked by IntuitMachine](https://www.youtube.com/watch?v=53Y3SYR5vTU) could not be retrieved during the source review. It is listed for completeness, not presented as a reviewed foundation.

## What this repository contributes

The assessment-to-approval-to-application procedure, evidence statuses, reusable report templates, reapplication requirements and demonstration acceptance specification are Agent Stack's synthesis of these ideas for existing coding repositories.

Important qualifications in this synthesis:
- Existing sufficient setups should be preserved.
- Guidance and enforced permissions are different.
- A worktree is not a security sandbox.
- Passing checks provide bounded evidence.
- Separate reviewers may share blind spots.
- Retry policies should respond to evidence and task constraints rather than a universal attempt count.
- Runtime compatibility and improvements require demonstrations.

## Attribution and reuse

Original articles, posts and artwork remain attributable to their respective authors. They are linked, not bundled. Acknowledgment does not imply endorsement or permission to redistribute third-party material.

When adding borrowed text, code or artwork, record the author, exact source and applicable reuse terms. Obtain permission where needed. Keep third-party terms distinct from any future license selected for this repository's original material.
