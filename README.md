# Skills: from issue to PR

Agent skills that take a piece of work from an issue to a pull request someone else can review.

They are small and composable, and they run your repo's own commands instead of owning your process. They work with GitHub Issues, Linear, Jira, markdown issues kept in the repo, or no tracker at all.

## Install

### Claude Code

```text
/plugin marketplace add maricarmendev/skills
/plugin install maricarmendev-skills@maricarmendev
```

### Any other agent

```bash
npx skills@latest add maricarmendev/skills
```

skills.sh copies the files into your project, so updates are manual (`npx skills update`).

## Skills

Work in progress. These are the skills planned for the first release:

| Skill | What it does |
| --- | --- |
| `setup` | Reads the repo (tracker, stack, the commands CI runs, services, database, per-worktree environment) and writes the repo profile the other skills use. |
| `read-issue` | Reads an issue from any supported tracker and numbers its acceptance criteria `AC-1`, `AC-2`, and so on. |
| `ground` | Questions you round by round, with a recommendation on each question, until you and the agent understand the issue the same way. Records agreed terms in a glossary and lasting decisions as ADRs. |
| `lanes` | Tells you which of your issues can move in parallel today without colliding at merge time, and why the rest cannot. |
| `review-diff` | Reviews the diff against the rules the repo already has. |
| `test-plan` | Writes a manual test plan and its seed data from the acceptance criteria. |

## License

[MIT](./LICENSE)
