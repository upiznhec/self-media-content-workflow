# Contributing

Thank you for improving these self-media Skills.

This repository is an English edition of [yanhua1010/self-media-content-workflow](https://github.com/yanhua1010/self-media-content-workflow). Changes that also apply to the original are better proposed there.

## Before you start

For new platforms, changes to the status flow, publishing capabilities or how data is measured, open an issue first to explain the scenario, the expected output and the safety boundaries. Small copy fixes and typos can go straight to a pull request.

## Development rules

- Each Skill has one clear job.
- `SKILL.md` keeps the core process; detailed platform rules go in `references/`.
- Copyable templates go in `assets/`.
- Do not tie the Skills to a single tool vendor.
- Do not add real credentials, cookies, tokens, user data or private links.
- Do not write temporary platform limits as permanent rules.
- Behavior changes must state the human approval points, failure paths and fallbacks.

## Validation

```bash
python3 scripts/validate.py
```

If you change complex behavior, run a forward test with a real scenario that does not contain the expected answer, and record the result in the pull request.

## Pull requests

Explain:

- What changed
- Why it changed
- The effect on users or developers
- Whether the safety boundaries changed
- Which checks and tests you ran

Use conventional commits, for example:

```text
feat(self-media-short-video): add interview storyboard pattern
fix(self-media-platform-copywriting): prevent unsupported metric claims
docs(project): clarify project-local installation
```
