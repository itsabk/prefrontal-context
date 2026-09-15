# Prefrontal Context

**Project context that stays with the repository.**

v0.4.0 — the five-file core. No install, no account, no AI provider. Copy the files into a repo and agents maintain them across sessions.

Site: [prefrontal.dev](https://prefrontal.dev)

## The five files

| File | Owns | Maintained by |
| --- | --- | --- |
| `AGENTS.md` | Rules for agents, including the memory rules | Owner (agents propose, never materially edit) |
| `MEMORY.md` | Current project context | Agents (Direction section records the owner's words) |
| `WORK.md` | Execution context: active and planned work | Agents |
| `DECISIONS.md` | Decisions that currently stand | Agents |
| `OPEN.md` | Unresolved questions | Agents |

Git-managed files hold canonical project knowledge. A developer can switch coding agents without moving project truth into a proprietary memory service. Different agents may behave differently — this does not promise identical execution or automatic compliance.

## Install

1. Copy `AGENTS.md`, `MEMORY.md`, `DECISIONS.md`, `WORK.md`, and `OPEN.md` into the repository root. If the repo already has an `AGENTS.md`, merge this template's harness sections into it instead of overwriting — keep your existing rules.
2. `CLAUDE.md` is a one-line loader (`@AGENTS.md`) for platforms that don't read `AGENTS.md` natively. Keep it only if you need it; if a `CLAUDE.md` already exists, append the `@AGENTS.md` line rather than replacing the file. For any platform whose agent-instruction surface differs, create its equivalent one-line loader pointing at `AGENTS.md`.
3. Fill `MEMORY.md`'s Direction section with what you actually want, in your own words. Then ask an agent to inspect the repository and fill State, Architecture, Conventions, and How-to-verify from verified facts only. The italic prompts inside the template files are placeholders — replace them with real content. Plain-prose notes (like the Agent line in `AGENTS.md`) are standing rules — keep them.
4. If the repo already has memory-like files (notes, roadmaps, progress logs), fold anything still current into the five files and delete or archive the rest. Keep genuinely useful project documents — specs, plans, design docs, contracts — as project documents, and reference them from the memory files. Don't leave parallel sources of truth.

You do not need this README in the target repository. Agents never read it.

## Operating

- Agents read `AGENTS.md`, `MEMORY.md`, `DECISIONS.md`, and `OPEN.md` at session start (plus `WORK.md` when continuing or planning work), then maintain the files as they work; the rules in `AGENTS.md` govern exactly how.
- Your surface is `MEMORY.md`'s Direction section, any conventions you state there, and `AGENTS.md`'s Project rules section — review those occasionally. Let agents maintain everything else.
- To change direction or rules, say so in conversation; agents record it. They won't edit owner-governed material unilaterally.
- History is git. Nothing needs running; nothing regenerates; there is nothing to operate.

## Remove

Delete the five files (and `CLAUDE.md` if it only points at `AGENTS.md`). Nothing was installed elsewhere.

## License

MIT. See `LICENSE`.
