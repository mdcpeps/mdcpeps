# CLAUDE.md

Working practices for agent sessions in this repo. They come from the course "AI Agents: The Most Valuable Skill You Can Learn in 2026", as summarized in a written summary (not the full transcript). Edit freely; keep this file short so it costs little context.

## Work the loop: observe, think, act

- Observe first: read the relevant files, tests and config before changing anything.
- Think: pick the next smallest step from the goal and what is still unknown.
- Act: make the change or run the command, then observe again to confirm it worked.
- Repeat until the goal is met, not until the first plausible answer.

## Define "done" before starting

- Restate the goal and what done looks like (acceptance criteria) before acting.
- If the goal is vague, pick the most objective reading, say so in one line, or ask when the answer changes the work.
- Stop only when those criteria are checked, and report the result against them.

## Keep context lean

- Read only what the task needs; prefer targeted reads over whole-file or whole-repo dumps.
- Put durable knowledge in markdown files in this repo, not in chat memory. This file is the global northstar and loads every session.
- Prefer objective, concrete statements over subjective ones when writing notes or docs.
- Keep a folder-scoped `CLAUDE.md` inside a subproject when it needs its own rules; it overrides this one for that folder.

## Skills: package what works

- After a workflow succeeds end to end, offer to package it as a skill under `.claude/skills/<name>/SKILL.md`.
- A skill has a name, a one-line description, step-by-step instructions, tool usage, output format rules and quality checks.
- Keep the description short; the full instructions load only when the skill is needed.
- Run the process first, then package it; refine the skill over later uses.

## Tools

- Use connected tools (MCP servers, browsers, scrapers) for the act step instead of guessing.
- Be careful with credential access (for example password managers); ask before using it.

## Be honest about blockers

- If a resource is unreachable (network policy, missing tool), say so plainly, state what was used instead, and do not invent the missing content.
- Label figures and claims that are someone's estimate rather than measured fact.
