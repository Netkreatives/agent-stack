# Apply an approved setup

Start from the accepted proposal. Keep its paths, behavior and acceptance criteria stable unless new evidence requires a material change.

## Preserve the project

Recheck the target root and working-tree status before edits. Read affected files and immediate dependencies. Preserve unrelated changes and active sessions.

Extend existing instructions and documentation instead of adding competing sources of truth. If the project already has a task ledger or handoff format, use it.

Do not create a parallel toolchain, replace lockfiles or introduce a package manager for this procedure.

## Make navigation useful

Keep the project's entry file short and task-oriented. Point to deeper existing sources for architecture, commands, testing and sensitive boundaries.

Every path and command must exist or be explicitly identified as proposed/unavailable. Do not invent setup commands. Record prerequisite services or environment dependencies without copying secrets.

If different agents require different entry filenames, use a documented canonical source and thin pointers where supported. Do not advertise compatibility you have not tested.

## Define completion and feedback

Use the task-contract template or a project equivalent for tasks that need it. Match verification to the claim: links for documentation, behavioral checks for logic, integration or device evidence where required.

Use existing checks first. Add a regression test only when it captures a meaningful failure. Do not introduce tests that merely assert your template text or mirror the implementation.

Failures should tell the next attempt:
- what was expected;
- what actually happened;
- where the evidence is;
- what was already tried;
- what new evidence supports a different next step.

Set a proportionate time/retry/spend budget. Repeated unchanged failure is a reassessment signal, not a universal two-attempt rule. Stop repeating the same approach without new evidence. Never convert exhausted budget into a passing result.

## Preserve recoverable state

For sustained work, record the current objective, completed work, relevant decisions, failed approaches and next action in the project's existing durable location.

State is task-specific. Keep credentials, personal data and sensitive logs out of it. Do not silently add local progress records to Git; follow project policy and the user's publication authority.

A recovery record must distinguish observations from assumptions and completed work from intended work. Include paths or revision identifiers that let the next session check whether recorded evidence is still current.

## Enforce boundaries honestly

Use existing runtime permissions and external controls. Setup documentation cannot change those controls by itself.

If enforcement requires new runtime configuration, infrastructure, credentials or a permission change, include the exact change and consequences in a separately approved proposal unless already covered. Never expand privileges just to get checks to run.

Keep model-written instructions separate from the authority that approves external side effects.

## Introduce orchestration only when justified

If approved:
- Assign bounded jobs, owned paths and required inputs/outputs.
- Preserve other workers' edits; coordinate shared integration.
- Separate genuinely independent context where useful.
- Use deterministic code for mechanical joins, counting or validation.
- Preserve accepted outputs and rerun only affected work. Revalidate downstream outputs when changed inputs invalidate them.
- Bound retries and aggregate resource use.
- Keep permission gates at the authorized side effects.

Do not spawn workers merely because the article describes graphs.

## Repeat application safely

On a later run:
1. Inspect the current files and previous acceptance evidence.
2. Identify what changed or invalidated earlier evidence.
3. Reuse relevant passing evidence.
4. Propose only justified differences.
5. Preserve user edits and avoid duplicate instructions.

Do not apply blind replacements or append a fresh copy of the same section. If provenance is useful, add a small source/revision note in the affected document rather than a new tracking system.

Finish with a review of the intended diff and the verification playbook.
