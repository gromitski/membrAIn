# Keeping project memory current

Use this example only when memory needs consolidation. The canonical requirements remain in [working agreements](../memory/agreements.md#current-memory-and-size). The example is fictional, not a prescribed project format or a request to change another repository.

## Worked example

A small reading app's current notes contain:

- v0.1 delivered local storage; v0.2 delivered export; v0.3 delivered import.
- v0.3 acceptance is pending.
- A later paragraph says the owner accepted v0.3 on both intended devices.
- Full test output and implementation details are repeated from its release record.
- Reconnection can still feel slow; its cause has not been measured.
- No further feature is approved.

The entry point also says v0.3 acceptance is pending. The product intent lists each release's completed tasks. A dated release record contains the owner acceptance and verification evidence.

First inspect the relevant revision, release record and acceptance evidence. A published tag alone does not establish owner acceptance. If the evidence cannot resolve the discrepancy, retain it as an explicit uncertainty and report the conflict instead of guessing.

With acceptance established, replace the duplicated material in the existing current-memory sections with:

> **Lifecycle:** Released v0.3; accepted on the intended devices, as recorded in the release record. Current deployment has not been rechecked in this maintenance task.
>
> **What exists now:** A local reading app with import and export. Behaviour and historical verification live in the existing product documentation and v0.3 release record.
>
> **Active focus:** Maintenance; no new feature is approved.
>
> **Uncertainties:** Reconnection sometimes feels slow; the cause remains unmeasured.
>
> **Next safe action:** Respond to maintenance needs; agree any investigation before expanding scope.

Use real links to those existing records in the actual project. Retain its established headings and any other facts needed to resume work. Do not copy this example's release number or create nonexistent pointers.

Remove the stale acceptance sentence from the entry point, preferably leaving routing there instead of another mutable status copy. Keep durable intent, such as local ownership and portability, in intent; keep release milestones in their existing release records. Preserve a consequential reason such as choosing a portable format for use in other systems beside the authoritative format decision.

## Completion check

Can a returning reader identify the applicable baseline, what exists, active work, unresolved facts and next action without reconstructing a chronology? Do affected entry points and active records agree? Is the reasoning and evidence still retrievable?

Report the actual files changed and whether changes are local or delivered through the agreed shared workflow. There is no universal word limit. Do not erase unique evidence, silently increase a project-specific limit or rewrite unrelated specialist documents for tidiness.
