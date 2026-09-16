# Set up Prefrontal Context with your agent

This is the prompt to paste into your coding agent, in the repository you want it set up in. It creates the five files, fills them from what the agent can verify, and asks you only for the parts that are yours to decide. It merges rather than overwrites, so an existing `AGENTS.md` keeps its rules.

Works with any agent that can read and edit files. Nothing else is required: no install, no account, no provider.

Copy the block below. If your agent can fetch a URL instead, hand it `https://prefrontal.dev/setup.txt`.

```text
Set up Prefrontal Context in this repository: five markdown files that keep project
memory between agent sessions. Work only in this repository.

The files and what each owns:
  AGENTS.md    - rules an agent must follow here, including how to maintain the
                 other four files. Owner-governed.
  MEMORY.md    - the project as it stands: direction (owner-governed), state,
                 architecture, conventions and quirks, how to verify.
  WORK.md      - what is being worked on now and what comes next.
  DECISIONS.md - decisions that currently stand, and why.
  OPEN.md      - questions nobody has settled yet.

Templates: https://github.com/itsabk/prefrontal-context (or the copies already in
this repository, if they are there). Keep their rules; do not invent replacements.

1. Create the five files at the repository root. If AGENTS.md already exists, merge
   these rules into it and keep every rule that is already there. If CLAUDE.md
   exists, append the line `@AGENTS.md`; if the platform you run on reads a
   different instruction file, add the equivalent one-line loader pointing at
   AGENTS.md.

2. MEMORY.md's Direction section and AGENTS.md's Project rules are mine to write,
   not yours. Ask me for my words before you fill them: at most three questions,
   in one message, then wait for my answer. Record what I say in my words.

3. Fill every other section from what you actually verify in this repository, and
   say how you know - the command, the test, or the file you read. Replace each
   italic placeholder prompt with real content. Rename, merge or drop sections that
   do not fit this project, but leave no section holding only its own prompt.

4. If this repository already has notes, roadmaps, progress logs or handoff files,
   fold what is still current into the five files and list the rest for me to
   delete or archive. Keep real project documents - specs, plans, design docs,
   contracts - as documents, and reference them from MEMORY.md instead of copying
   them in. Leave one home per fact.

5. Never invent a fact. Anything you cannot verify goes in OPEN.md as a question.
   If something you find contradicts a recorded decision, tell me rather than
   editing the decision yourself.

6. From now on, read these files before non-trivial work and keep them current in
   the same piece of work: record what changed, prune what is stale or false, and
   use git for history instead of keeping old text in the files.

7. When the setup is done, report: the files you wrote, the facts you verified with
   the commands you ran, what you need from me, and anything you deliberately left
   out.

Do not add indexes, sync scripts, hooks or other machinery for these files unless I
ask for it.
```
