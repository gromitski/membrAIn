# membrAIn

[Version 3.0](https://github.com/gromitski/membrAIn/releases/tag/v3.0)

**A shared memory for you and your AI.**

membrAIn gives different AIs the same project memory, so you can switch tools, work with several assistants or return later without re-explaining your idea, decisions and progress each time.

It directs each AI to a small set of current notes and the extra detail relevant to its task. This helps avoid repeatedly reading whole projects or long chat histories, reducing unnecessary context and potentially saving AI credits.

Start with a rough idea and let this small foundation of plain-text files grow only as needed. You describe what you want; your AI helps organise the files.

## Get started

1. **Get your own copy.** [Download membrAIn](https://github.com/gromitski/membrAIn/archive/refs/heads/main.zip) and unzip it, or clone this repository if you use Git.
2. **Give your AI access.** Open the folder in your AI tool. If you are using a chat app, attach [`START.md`](START.md) first; the AI will ask for any other files it needs.
3. **Paste this into the conversation:**

```
Inspect START.md and follow its instructions. Report back to me when you're ready to begin.
```

Then describe your idea. It can be as simple as “I'd like to make something that helps me plan my meals.” You do not need a finished plan or any files edited in advance.

When you want to keep your progress, ask the AI to save the project memory. With file-editing access, it prepares the files for you to review.

## What the memory files do

[`START.md`](START.md) is always the way in. It tells the AI where to look next.

| File | What it remembers |
| --- | --- |
| `memory/agreements.md` | How you want to work: responsibilities, permissions and shared rules. |
| `memory/intent.md` | What you are making, who it is for and what matters. |
| `memory/now.md` | Where things stand and the next useful step. |

The agreements come with membrAIn and can adapt as your project expands. The AI creates the intent and current-state files when you ask it to retain the project, and updates them as things change. Other documents are added only when useful.

## Q&A

**Do I need to know how to code?**
No coding is needed to explore an idea. Tell the AI what you want in ordinary language and ask it to explain anything unfamiliar.

**Which AI can I use?**
ChatGPT, Claude, Gemini, Codex, Cursor or another assistant that can read the files. An AI without editing access can prepare content, but cannot save it into your project; use a tool with file access to apply it.

**Can I just brainstorm?**
Yes. You can explore for as long as useful. Tools, roles and delivery choices come up only when they affect what you want to do next.

**How do I make sure my progress is saved?**

During brainstorming, ask “Please save this idea as project memory” when you want to keep it. Once the project is underway, the AI should keep relevant documentation current as part of its work.

Before finishing a session, “Please update the project memory and tell me which files changed” is a useful final check. The AI needs editing access to save files; committing or uploading changes to GitHub follows your agreed permissions.

**How do I return later or change AI tools?**
Give the AI the latest project files and use the same starting prompt. Keep the memory up to date so it has something reliable to resume from.

**Will it build or publish things without asking?**
You agree the work first. Commits, pushes and publishing need your explicit permission, either for the task or within a scope you have already authorised.

**Does it guarantee the AI remembers everything?**
No. The files give it a shared reference; the AI still needs to read and maintain them. Review important decisions and correct mistakes.

**Can I add it to an existing project?**
Yes. Ask your AI to inspect both projects and propose how to adopt membrAIn while preserving your existing files and workflow.

**Will it use fewer AI credits?**
It can help by directing the AI to relevant files instead of loading everything into each chat. Actual usage depends on your tool and task; membrAIn cannot control what the tool automatically includes.

**Is it free?**
membrAIn is free to use and adapt under the [MIT License](LICENSE). Your chosen AI service may have its own charges.
