# Project initialisation

For the AI: follow this procedure only when the owner asks to retain or initialise their project. Reading it does not authorise implementation, commits or publication. `START.md` remains the entry point; this procedure is needed only for initialisation or completing missing setup.

All paths below are relative to the project root. If the folder is not a Git repository or Git access is unavailable, disclose that limitation and continue only the file work supported by available access. Do not claim Git checks succeeded or require the owner to run technical commands just to explore an idea.

```
Initialise this project using membrAIn.

1. Inspect repository and Git state.
2. Read local Git identity with `git config user.name` and `git config user.email`.
   - Determine whether identity appears configured and privacy-safe.
   - Continue initialisation even if identity is missing or appears unsafe.
   - Do not copy Git name or email into project files, README project content, archived origin or chat logs in full.
   - If name or email is missing, record a concise warning in the response.
   - If email appears personal rather than privacy-safe, record a concise warning without echoing the full value.
   - Do not commit or push during initialisation.
   - If a commit is later requested, pause until Git identity is privacy-safe or explicitly approved by the maintainer.
3. Read `START.md` and `memory/agreements.md`, including Starting and evolving a project. Use the owner's idea and decisions from the conversation plus any existing idea notes; do not require manual template edits. Ask only about missing information needed for the next step.
4. Confirm whether the project is already initialised (`memory/intent.md` and `memory/now.md` present with real content). If memory is partial, preserve approved content and complete only genuinely missing steps; do not recreate existing files blindly.

If already initialised:
- Do not overwrite project memory blindly.
- Report current state from canonical memory.
- Complete only genuinely missing initialisation steps.
- Preserve existing approved project memory.

If not initialised:
5. Interpret the rough intent without inventing decisions. If neither the conversation nor existing notes contain a real idea, ask for it before creating memory. Do not require implementation or delivery choices for an exploratory project.
6. Create:
   - `memory/intent.md`
   - `memory/now.md`
   - `evidence/origin/YYYY-MM-DD-origin.md` (archive the user's own words from the supplied idea and any existing idea notes in START.md; exclude assistant prose and instructional template text; redact accidental PII or local-system information and note any redaction)
7. Replace `START.md` with the initialised-project entry point below, preserving its routing instructions. It remains the single starting point for every AI.
8. Update the repository-root `README.md` with only:
   - project name
   - one-line stable description
   - links to `memory/intent.md` and `memory/now.md`
   Do not add lifecycle state, active slice details, version history, deployment status or Git identity to the README.
9. Record material uncertainties explicitly, without a checklist of irrelevant future choices. Record confirmed working arrangements in the Project choices section of memory/agreements.md; do not add an empty section.
10. Propose one small, useful next step. Further exploration is valid; initialisation does not authorise implementation.
11. Do not create architecture docs, deployment docs, roadmaps, `memory/decisions/`, specialist docs, work files, generated context or identity configuration files unless the rough intent and existing repository already genuinely require them.
12. Scan intended changes for PII, local-system information, secrets and private values.
13. Do not commit or push unless explicitly asked.
14. Return:
    - interpreted purpose
    - uncertainties
    - proposed next step (exploration or an implementation slice for agreement)
    - Git identity status (configured / missing / may be privacy-unsafe) without printing unsafe values in full
    - exact files changed
    - next prompt to begin work

### Output contracts

**memory/intent.md** headings: Purpose; Audience and value; Principles; Non-goals; Assumptions and uncertainties. Synthesise intent — do not copy verbatim. No current status, active tasks, invented architecture, deployment or Git identity.

**memory/now.md** headings: Purpose; Lifecycle; What exists now; Active focus; Active slice; Blockers; Uncertainties; Next safe action; Last meaningful update; Pointers. Purpose is one line. Use `none` where meaningful. List only real artefacts. No fictional infrastructure. Pointers only to files that exist. Roughly one screen.

**START.md** after initialisation:

# Start here

This project is initialised. Tell your AI what you want to explore or work on; it handles the project files where access permits.

For the AI: read `memory/agreements.md` and `memory/now.md`, then `memory/intent.md` when purpose or scope matters. Inspect relevant repository and Git state; follow only task-relevant pointers. Reuse agreed project choices, ask only about missing decisions needed next, and do not restart onboarding. Disclose access or editing limitations rather than claiming unverified or unsaved work.

Current project memory:

- [Product intent](memory/intent.md)
- [Current project truth](memory/now.md)

The original project idea is archived under `evidence/origin/`.
```
