# Verify the setup

Verify the claims made by the approved proposal. Begin with the smallest meaningful check and complete required project checks within the agreed scope.

## Match evidence to the claim

| Claim | Useful evidence | What it does not establish |
| --- | --- | --- |
| Navigation is usable | Resolve links; locate the relevant code and command from the guide | Runtime behavior or speed improvements |
| Commands are real | Inspect owning scripts/manifests; run a safe relevant command where authorized | That every environment supports them |
| A bug is fixed | Reproduce the issue; demonstrate changed behavior and run affected checks | Correctness for every possible input |
| Task state is recoverable | Resume using the saved record and verify current state | Successful recovery by every agent/runtime |
| A boundary is configured | Inspect the actual enforcing configuration | Complete resistance to bypass |
| A boundary is exercised | Observe rejection of a harmless approved out-of-scope action | Safety against every attack or destructive action |
| Reapplication preserves work | Repeat assessment on the same project state; inspect the proposed diff | Preservation across untested future changes |

For an existing behavioral check, confirm it can detect the relevant failure. Do not deliberately damage a real project to manufacture a red result. Use a pre-fix revision, existing reproducer or an approved isolated fixture.

Documentation-only changes normally need reference, syntax and consistency checks. They do not establish runtime compatibility.

## Use a representative task

Choose the task before changing the setup. It should expose the gap being fixed:
- navigation: find the correct implementation and existing check;
- loop: detect and repair a known bounded failure;
- continuity: recover after a session boundary;
- permissions: inspect enforcement or exercise a harmless permitted probe;
- reapplication: assess again and avoid redundant changes.

Record the initial state, commands, observed outputs and conclusion. Preserve evidence in the project's approved location; redact secrets and avoid publishing private material.

A simulated handoff is useful but must be labeled simulated. A real new-session recovery requires an actual session boundary and available authorization. Agent delegation is not implied by this playbook.

## Handle failures

Investigate before retrying. Distinguish a change-induced regression, pre-existing failure, environmental blocker and unknown cause using evidence.

Do not weaken a check, omit a required result, or fix unrelated failures to manufacture a clean report.

If an expensive check exceeds the agreed budget, report progress and reassess the remaining required checks. Stop optional expansion. Required checks that were not completed remain unverified.

## Handoff

Use [the acceptance-report template](../templates/acceptance-report.md) or the project's equivalent.

Separate:
- **Implemented:** the files/configuration were changed.
- **Verified:** a named capability was exercised or inspected with stated limits.
- **Unverified/blocked:** a required check or capability lacks evidence.
- **Not applicable:** a capability was unnecessary for this scope.

Report overall completion as **complete**, **partial** or **no changes needed**. Complete applies only when the approved scope and required checks are satisfied; it does not mean universal agent reliability.

Include the diff/revision, evidence, remaining limits and next action if anything required is unresolved. Do not claim measured performance improvements without a documented comparison.
