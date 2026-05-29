# AGENTS.md

> This is the root operating manual for your second brain, for AI coding agents that read `AGENTS.md` (such as OpenAI Codex CLI). It is the Codex-side twin of `CLAUDE.md`: same brain, same content, read by a different agent. Your agent reads this file at the start of every session in this folder. It tells the agent who you are, what matters to you, and where to find more detail.
>
> The `{{placeholders}}` below are filled in automatically when you run the `second-brain` skill. You can edit anything by hand afterwards, but the skill is the easier way: edit `second-brain-intake.md` and re-run.

---

## Who this brain belongs to

**{{name}}**, {{role_one_liner}}.

Working pattern: {{working_pattern}}.

---

## What the business does

{{business_one_liner}}

Full description: [[context/about-business.md|about-business]].

---

## What I sell

See [[context/services.md|services]] for the full list. The short version: {{services_short}}.

---

## Who I serve

See [[context/icp.md|icp]] for the full ideal-client picture. The short version: {{icp_short}}.

---

## What matters right now

The next 90 days, in order:

{{priorities_list}}

Full detail in [[context/priorities.md|priorities]].

---

## Voice and never-assume

- Voice register and writing samples: [[references/voice.md|voice]]. Match this.
- Things your agent must never assume or get wrong: [[context/never-assume.md|never-assume]]. Read this before drafting anything client-facing.

---

## Files in this brain

Populated context (read these to understand the business):

{{populated_context_files}}

Populated references:

{{populated_reference_files}}

Two more folders stand ready for the capture-and-synthesis method: `raw/` and `wiki/`. See the section below.

---

## Capturing source material and synthesis

Two folders run on a different discipline from the rest of your brain. This is the method the bootcamp calls the Karpathy track.

**`raw/` is for captured moments, and it is never edited.** Meeting transcripts, voice notes, articles worth keeping, observations. Once something lands in `raw/`, leave it alone: it is a record of what was said or seen at the time. If you later find an error in it, write a new note and link the two rather than changing the original. Name files `YYYY-MM-DD-source-slug.md`. Full rule in [[raw/README.md|raw]].

**`wiki/` is for synthesis, and it can be rewritten any time.** When you pull together what you have learned about a client, a topic, or a problem across several raw captures, that is a wiki file. Unlike raw, wiki is meant to be regenerated as your understanding shifts. Each wiki file lists the raw sources it draws from, so it can be rebuilt. Full rule in [[wiki/README.md|wiki]].

The short version: raw is what happened, wiki is what you make of it. Raw never changes; wiki always can.

---

## How to use this brain

- Ask questions in plain language. Your agent will use the files above to ground its answers in your actual business.
- To update the brain, edit `second-brain-intake.md` and re-run the `second-brain` skill. Previous file versions back up to `archives/`.
- To hire an AI employee, run the `hire` skill. The employee leans on this brain.

---

## How AI employees work

When the user addresses any AI employee by name in this project (for example "Hi Cleo", "Cleo, can you draft this for me?", "Cassandra, what should I focus on?"), do the following before responding:

1. Look in the `employees/` folder for a file matching that name (slugify the name: lowercase, hyphens replace spaces, strip punctuation). So "Cleo" maps to `employees/cleo.md`, "Cassandra Reid" maps to `employees/cassandra-reid.md`.
2. If a matching file exists, read it in full. The file is written in second-person ("You are…", "You do…"). Adopt that identity from this point in the chat and respond as that employee.
3. Stay in that employee's voice and authority for every subsequent response in the chat, until the user addresses a different employee by name. Switching employees is just switching names.
4. If no matching file exists, treat the name as a regular conversational reference rather than an employee invocation.

The employee's persona, voice, responsibilities, and boundaries come from their file. Their knowledge base is everything in `context/` and `references/`. Ground every answer in those files, not in generic assumptions.

Multiple employees can coexist in this project. Each `employees/<name>.md` file is a separate hire. One brain, many employees. The brain is the shared substrate; the employee is the lens on top.

---

*This brain was built with the `second-brain` skill from the [Build Your Second Brain with Claude](https://github.com/tabithawinter-jpg/second-brain) bootcamp kit. It is taught in Claude Code; this `AGENTS.md` file is included so the same brain runs under Codex CLI too.*
