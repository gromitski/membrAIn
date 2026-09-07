# Working agreements

Universal rules for humans and agents working on this project. Canonical vendor-neutral guidance lives here — not in Cursor rules alone.

## Repository truth

- Inspect current repository state before claims about files, branches, configuration or behaviour. Claim inspection, reading or verification only when relevant access succeeded in this session; remembered state is not inspection.
- Current repository evidence overrides remembered assumptions or chat history.
- Record uncertainty honestly. Use states such as unknown, assumed, proposed, investigating, accepted, rejected, superseded or deferred.
- Do not invent architecture, deployment, product decisions or infrastructure that does not exist in the repository.
- Disclose required access failures before repository-dependent work; never silently substitute conversation memory.
- Distinguish user-provided reports, screenshots and pasted changes from independently verified repository evidence.
- For delivered-work claims, prefer current pushed evidence on the agreed branch, then directly observed implementation or runtime, agent reports, supplied artefacts and recalled conversation. Match evidence to the claim: a commit alone proves neither deployment nor runtime behaviour.
- Verify claimed commits and pushes against the repository before accepting work as delivered.
- Classify visuals and documents as current implementation, design/reference or historical evidence. Prototypes neither prove implementation nor authorise scope.

## Repository identity

- Do not include personal identity in repository content unless it is deliberately public and relevant to the project.
- Use neutral role language by default, such as the maintainer, the project owner or the user.
- Do not write Git commit email addresses into documentation.
- Prefer a privacy-safe no-reply address for public repositories where the Git host supports one.
- Do not commit unnecessary personally identifiable information.
- Do not include private or unnecessary real names, personal emails, private addresses, telephone numbers, family details or private employment information.
- Do not include local usernames, filesystem paths, device names, hardware specifications, hostnames, private IP addresses or private service URLs.
- Redact logs and diagnostics before committing them.
- Private repositories are not exempt from privacy discipline.

## Secrets and security

- Never commit secrets, credentials or real environment values.
- Use ignored local configuration, secret stores and safe example files.
- Validate untrusted input, use least privilege where relevant, and consider privacy and retention when processing user data. Security must be proportionate, never optional.

## Git identity and authority

- Do not commit, push, merge, tag, release, deploy, rewrite history or perform destructive Git operations unless explicitly authorised for that task.
- An explicitly granted project-specific standing permission covers a task only within its recorded actions, scope, target branches/environments and exclusions. Do not infer it from a tool choice, implementation approval or example workflow; absent or unclear permission requires explicit authorisation before the affected action.
- Inspect branch and working-tree state first.
- Use the maintainer's configured privacy-safe Git identity for commits.
- Warn if configured identity appears to expose a personal email; never print unsafe identity values in full or commit with an unreviewed privacy-unsafe identity.
- Use descriptive commit messages.
- Inspect the complete commit subject, body, trailers, author and committer metadata after every commit and every amend, before the first push.
- Do not add Cursor, cursoragent, ChatGPT, Claude, Copilot, Gemini, Grok, OpenAI or another AI identity as author, committer or co-author.
- Do not add AI attribution in a commit subject, body or trailer, including `Co-authored-by`, `Generated-by`, `Authored-by`, `Assisted-by` or equivalent declarations.
- Ordinary technical references to AI tools in commit prose are allowed when they describe the project rather than claim authorship.
- Do not expose PII through commit metadata.
- In every fresh clone, run `node scripts/no-ai-attribution.mjs install` before the first commit or push, then run `node scripts/no-ai-attribution.mjs self-test`.
- Run `node scripts/no-ai-attribution.mjs commit HEAD` after every commit or amend. Failure is a hard stop before push, never a harmless warning.
- If an editor or agent automatically adds attribution, do not push it. Recreate or amend the commit with clean human authorship metadata and verify it again.

## Branch and file hygiene

- After work lands on the intended branch, remove its local and remote task branches only after verifying the merged state and establishing required deletion authority. Do not use stale branches as an archive.
- Promptly flag stale, superseded or contradictory files for review; do not silently leave them as active guidance.
- Do not delete a file merely because it is old. Distinguish active truth, useful historical evidence and genuinely obsolete material, and obtain any required authority before removal.
- Preserve useful history in designated evidence; branches do not replace maintained documentation or evidence.

## Scope and implementation

- Make the smallest useful, testable change.
- Investigate before risky, broad or ambiguous implementation.
- Avoid unrelated refactors; refactor while context is fresh when it directly supports active work.
- Prefer clear, maintainable code over cleverness; remove dead code and avoid unnecessary duplication.
- Do not introduce speculative abstractions merely because a project may grow.
- Do not introduce a new architecture layer, broad refactor or substantial test harness unless there is a reproducible failure or measured problem, evidence that focused existing mechanisms are inadequate, a plain-language cost-benefit explanation and explicit approval.
- After two materially failed or substantially corrected attempts in the same area, stop. Summarise the evidence, reassess the approach and obtain agreement before issuing another implementation attempt.
- Before substantial feature or version work, establish the intended delivery depth — for example MVP, prototype or complete build — and scale scope and verification accordingly.
- Keep release and hardening work focused on proving and publishing the agreed change. Do not introduce speculative product architecture, broad refactors or unrelated test infrastructure during release preparation without explicit approval.

## Human collaboration and delivery

- The maintainer or project owner owns product decisions, priorities, scope, trade-offs, creative direction, product and experience acceptance, and authorisation. Support these decisions without burying them in procedure. Agree each implementation slice before starting; choosing a tool or agent grants no unscoped build, Git or deployment permission.
- Define technical direction, implementation and review responsibilities in the project's working agreements. One person or agent may hold multiple roles; the foundation mandates no tool, model or division of roles.
- Respect agreed roles; do not silently take over another. The project owner may change roles at any point: follow and record revised responsibilities for future sessions.
- A tool or model preference does not prove what is configured or running. Verify relevant configuration before claims; distinguish preference from observation.
- Before significant technical work or substantial implementation, explain in plain English the problem, user-visible effect, proposed approach and rationale, relevant alternatives, assumptions, material risks, likely effort or cost, and expected result. Explain necessary jargon so the owner can challenge the approach.
- When tool access permits, the coding agent owns implementation mechanics: repository inspection, terminal commands, builds, linting, type checks, automated tests, diagnostics and diff review. Do not offload long technical command sequences to the maintainer by default.
- Treat money, tokens, time, attention and enthusiasm as real project constraints. Flag broad repository scans, large generated test suites, multi-agent reviews or other potentially expensive work before starting them, and explain the cheaper focused alternative.
- Keep workflow lightweight: process must materially improve understanding or reduce risk, without duplicated rules or ceremony.
- Prefer a steady rhythm: product decision, bounded slice, complete implementation prompt where needed, agent-owned technical verification, concise outcome review, limited human acceptance and then documentation or release work.

### Starting and evolving a project

- Use the owner's request and existing decisions. Ask one short question only when an unresolved choice affects the next step; do not repeat settled questions or present a setup questionnaire. If the owner is unsure, explain a proportionate recommendation and obtain agreement before recording a decision.
- Take the owner's idea from the conversation or existing notes; never require them to edit a template. During brainstorming, explore and reflect back the idea. Require no tool, role, branch or deployment choices, and do not initialise files or start implementation merely because the idea is detailed. When asked to retain or initialise it, follow the initialisation procedure in `docs/initialisation.md` and prepare the files yourself where access permits; more exploration remains a valid next step.
- Before implementation, settle missing choices needed for the agreed slice: intended depth, preferred tools if any, and technical direction, implementation and review responsibilities. Ask about tools, then their roles, only if unresolved. One agent can hold multiple roles; tool names establish neither roles nor authority.
- When the next step requires sharing or publishing work, first agree where the owner will review the result (local, preview or development), the checks and delivery steps before acceptance, and whether commit/push permission is per task or explicitly granted for a defined scope. Assume no branch, pull-request policy, hosting service or need to publish; apply the Git authority rules.
- Record confirmed arrangements in a concise **Project choices** section here, adding it only when needed. Current work belongs in `memory/now.md` when present. Create no empty choice fields, questionnaire file, speculative documents or duplicated universal rules.
- Reuse choices in later sessions. Settle changes with the owner and update the same record, revisiting only affected choices. The owner can revise arrangements at any point; changing a tool or environment does not silently expand permissions.

### Coding-agent prompt format

- When asked for a prompt for any coding agent, the entire response must be exactly one uninterrupted fenced Markdown block containing the complete, untruncated prompt, directly copyable as-is without reconstruction from other messages or artefacts.
- Do not add commentary before or after the block. Do not include a language identifier, ID or other fence metadata. Do not use nested code fences; use indentation or inline code for examples inside the prompt.
- Include relevant repository, branch and current project context; objective and plain-English outcome; agreed technical approach; explicit scope and exclusions; likely files or areas; applicable architectural and quality constraints; proportionate verification; authorised Git or delivery actions; and expected report back. Do not invent missing decisions or authority.

### Review, acceptance and delivery

- The agreed reviewer must inspect actual implementation and relevant verification evidence, not just a completion report. For delivery through a shared repository, inspect the delivered commit and diff on the expected branch.
- Before technical acceptance, review scope, unrelated changes, correctness, architectural fit, applicable accessibility, security, privacy, performance and cost, verification results and documentation accuracy.
- Establish facts directly where evidence permits rather than asking the owner. Explain defects and make or request focused corrections within agreed roles and authority; avoid broadly rewriting a mostly correct implementation.
- Ask the owner only for short acceptance checks genuinely requiring human judgement, visual judgement, usability/product preference, physical devices, private access, real-world behaviour or product decisions. State the action, expected result and failure criteria.
- Keep automated verification and human acceptance distinct: automation proves repeatable technical behaviour; human checks confirm product judgement and real-world experience.
- Follow documented delivery, distinguishing automatic and manual steps. After successful automatic deployment, do not request redundant manual deployment. Report the delivered revision after an authorised push; distinguish pushed work from verified deployment.
- Review and delivery requirements grant no commit, push, merge, deployment or release authority; follow **Git identity and authority** and the project's agreed workflow.

## Accessibility and usability

- User interfaces should aim for WCAG AA. Apply semantic structure, keyboard access, visible focus, accessible names, readable contrast and usable error handling from the start; accessibility is not a later bolt-on.
- Usability includes responsive, speedy performance. Avoid unnecessary dependencies and payload; measure performance before complex optimisation.
- Review the agreed user problem and outcome first. Technical explanations and qualifications should support a useful product/interface experience without overwhelming it; preserve accuracy and honest uncertainty.

## Data separation

- Keep maintained data and content separate from presentation and executable logic where practical. JSON, YAML, Markdown, text files, APIs or databases may suit. Do not hard-code significant maintainable data into UI or business logic without good reason.

## Testing and verification

- Every implementation should have repeatable verification proportionate to changed behaviour and risk. Add automated tests where valuable; prefer focused checks, existing infrastructure and build, lint, type, accessibility or manual checks, with small integration checks where useful.
- Do not create large suites or exhaustive test matrices for ceremony, add frameworks without evidence, build infrastructure for hypothetical needs or substantially expand scope merely for coverage. Do not turn feature, maintenance or defect work into a test-infrastructure programme without concrete risk and explicit approval. Before expanding testing mechanisms, explain the concrete gap and cost; obtain the approval required by the preceding rule and **Scope and implementation**, including its evidence conditions for substantial harnesses.
- Do not leave the project in a state where testing would later require a structural rebuild.
- Run available checks and report exact commands or checks and results; never claim an unrun check passed. The agreed reviewer should challenge testing disproportionate to the change and risk.

## Documentation and memory

- Keep canonical memory concise, with one authoritative home per durable fact. Keep historical evidence retrievable outside normal context; do not create permanent files for trivial tasks or decisions.
- Keep meaningful documentation aligned with the work, review its accuracy and deliver it to the agreed shared source of truth through the authorised workflow. Local edits alone do not update shared documentation.
- Report pending documentation delivery, including missing authority or required steps. Minor spelling or formatting corrections need no heavyweight review.
- Do not rewrite specialist documents during unrelated implementation unless the documented behaviour changed.
- Store lengthy investigations as dated reports in an appropriate evidence or audit location; keep chat summaries concise. For risky or ambiguous work, report findings before implementation; investigation does not grant implementation permission.

### Current memory and size

- `memory/now.md`, when present, holds only current facts needed to resume work, not a diary, release log, duplicate of roadmaps, architecture or agreements, or investigation dump.
- Keep historical detail in authoritative documentation, evidence or Git history; link relevant material rather than duplicate it in current memory.
- When current memory exceeds an agreed size guideline or stops being a concise snapshot, flag growth and propose consolidation or moving detail to its proper home. Discuss necessary expansion with the owner; never silently raise limits or discard useful information. The foundation sets no fixed limit or checking tool.

### Memory impact and completion

- Before completing meaningful implementation or documentation, assess changes to current state, active/next work, completion status, plans, delivered baseline, roles/workflow, behaviour/contracts, architecture, limitations and specialist-document pointers.
- When meaningful reality changes, update authoritative memory/documentation in the same bounded work or an immediately following documentation change before another feature. Reuse existing documents when sufficient.
- If no memory update is needed, report `Memory impact: no update required` with a short reason.
- Follow the project's agreed application/package versioning policy; keep relevant version declarations and current memory consistent. Documentation-only edits need no artificial application-version bump.
- The agreed reviewer must check current memory and any active roadmap against delivered reality. Materially stale current documentation leaves implementation incomplete.

## Specialist guidance

Deeper project-specific guidance may appear under `specialist/` only when a real need exists. Follow relevant specialist guidance when it exists and when current project truth points to it for the active task.
