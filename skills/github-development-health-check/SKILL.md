# GitHub Development Health Check

## Purpose

Audit a GitHub repository as a real software project and determine what should be improved next.

The goal is not to maximize GitHub activity or achievements. The goal is to build something real, maintain it well, document it, test it, review it, release it, and make collaboration possible. GitHub achievements are a byproduct of healthy development.

## Invocation

Primary command:

`check <repository>`

Examples:

- `check daikiito-dk/Ghost-Protocol`
- `check daikiito-dk/trustyon`
- `check https://github.com/owner/repository`

Modes:

- `check repo` — full audit
- `check github` — GitHub workflow audit
- `check engineering` — technical quality audit
- `check portfolio` — portfolio value audit
- `check achievement` — natural achievement opportunities
- `check release` — release readiness audit

If a repository name is supplied without an owner, identify the repository when possible rather than immediately asking the user to repeat it.

## Core Philosophy

1. **Product First** — product value comes before GitHub activity.
2. **Real Development** — issues, commits, branches, PRs, reviews, and releases should represent genuine work.
3. **Evidence Based** — judge from observable repository evidence; do not invent missing facts.
4. **Complete Development Loop** — prefer Idea → Issue → Branch → Implementation → Test → PR → CI → Review → Fix → Merge → Release → Documentation.
5. **Next Action** — every audit should end with concrete next steps.

Golden rule:

> Never optimize GitHub activity at the expense of product quality.

Japanese principle:

> GitHub実績のために開発するのではなく、良い開発をした結果としてGitHub実績が積み上がる状態を作る。

## Inspection Areas

Inspect the repository using available GitHub data and repository files.

### Repository

Check:

- public/private status
- archived status
- default branch
- description
- README
- license
- repository structure
- language/technology stack
- deployment/demo links

### Development History

Check:

- recent commits
- commit quality and scope
- branch usage
- open and closed issues
- pull requests
- PR descriptions
- reviews
- CI checks
- merge history
- releases/tags
- development continuity

Do not reward commit volume by itself. Prefer meaningful, scoped changes.

### Engineering Quality

Evaluate:

- architecture
- code quality
- maintainability
- tests
- CI
- build reliability
- linting/formatting
- error handling
- security
- performance
- concurrency
- state management
- reliability/recovery
- observability where relevant
- documentation for developers

Adapt the audit to the technology. For Go, explicitly consider goroutines, mutexes, channels, context handling, error propagation, race detection, package design, and integration testing when relevant.

### GitHub Workflow

Evaluate whether the project naturally follows:

`Issue → Branch → Implementation → Test → PR → CI → Review → Fix → Merge → Release`

Check:

- issue-driven development
- branch naming and scope
- PR quality
- CI quality
- meaningful code review
- fixes after review
- merge discipline
- release practice

A PR should normally communicate:

- summary
- motivation
- changes
- testing
- related issue

### Collaboration

Check whether a newcomer could realistically contribute.

Look for:

- CONTRIBUTING.md
- CODE_OF_CONDUCT.md
- SECURITY.md
- issue templates
- pull request template
- useful labels
- good first issue candidates
- help wanted issues
- Discussions when appropriate
- external contributions
- clear setup instructions

### Product Quality

Evaluate:

- clear purpose
- target user/value
- working core functionality
- UX
- live demo where appropriate
- screenshots/GIF/video where appropriate
- README clarity
- roadmap
- current project maturity

### Portfolio Value

Evaluate whether the repository communicates a strong technical story:

- what was built
- why it matters
- technical challenges
- engineering decisions
- evidence of quality
- public demo/release
- development history
- visuals

## Score

Use a 100-point score:

- Product Quality — 25
- Engineering Quality — 25
- GitHub Workflow — 20
- Collaboration — 15
- Portfolio Value — 15

Do not force irrelevant criteria. If a criterion is genuinely not applicable, mark it `⚪ Not Applicable` and explain the adjustment.

## Status

Use:

- 🟢 **Healthy** — strong and progressing
- 🟡 **Needs Improvement** — usable but with meaningful gaps
- 🔴 **Critical** — broken, unsafe, or severely incomplete
- ⚪ **Not Applicable** — criterion does not reasonably apply

## Achievement Opportunity Audit

Achievements and GitHub activity should emerge naturally from useful development.

Audit opportunities around:

- meaningful pull requests
- meaningful code reviews
- issue-driven development
- releases
- documentation
- discussions
- external contributions
- community-friendly issues

Use:

- 🟢 High opportunity
- 🟡 Medium opportunity
- ⚪ Not applicable

Never create artificial issues, commits, PRs, reviews, discussions, or releases solely to obtain achievements.

## Anti-Farming Detection

Flag suspicious or low-value activity when evidence supports it:

`⚠ Achievement Farming Risk`

Potential signals:

- meaningless issue volume
- meaningless commit volume
- self-review padding
- achievement-only changes
- README noise
- trivial PRs created only for activity
- artificial contribution patterns

Do not accuse the developer without evidence. Explain the observed signal and why it may reduce project quality.

## Repository Maturity

Classify the project:

- Level 0 — Idea
- Level 1 — Prototype
- Level 2 — Working Project
- Level 3 — Structured Project
- Level 4 — Production Candidate
- Level 5 — Open Source Project
- Level 6 — Mature Product

State both current level and a realistic next target.

## Project-Type Specialization

### Web App

Consider:

- UX
- accessibility
- performance
- security
- responsive behavior
- deployment
- browser compatibility

### Game

Consider:

- gameplay loop
- UX
- performance
- state management
- multiplayer/realtime behavior
- save/recovery
- edge cases
- playability
- demo/release quality

### Backend

Consider:

- architecture
- API design
- concurrency
- testing
- observability
- security
- failure recovery

### Library

Consider:

- API design
- compatibility
- versioning
- tests
- documentation
- examples

### AI Project

Consider:

- evaluation
- reproducibility
- model abstraction
- prompt management
- safety
- cost
- latency
- failure handling

## Next Action Engine

The most important output is what to do next.

Determine the highest-value next actions from the repository's actual state.

Priority order:

1. Broken functionality
2. Security/data integrity
3. CI/test failures
4. Missing core functionality
5. Reliability/recovery
6. Testing
7. Documentation
8. Collaboration
9. Portfolio presentation
10. Achievement opportunities

Examples:

- Code exists but tests are missing → add meaningful tests.
- Tests and CI exist but review is missing → perform a meaningful code review.
- Feature is complete, tests are green, and PR is ready → complete review and merge.
- Feature is merged and stable → prepare a release.
- Release exists but collaboration is weak → improve contribution docs and create genuine starter issues.

Always provide a **Top 3 Next Actions** list.

## Autonomous Development Mode

If the user says:

- `go`
- `gogo`
- `continue`
- `続けて`

use the latest health-check state to continue development.

Preferred loop:

`Health Check → Issue → Branch → Implement → Test → CI → PR → Review → Fix → Merge → Release`

Reuse existing issues/branches/PRs when appropriate instead of creating duplicates.

Do not perform destructive operations, expose secrets/credentials, make irreversible changes, or deploy to production without explicit authorization.

## Standard Output

Return a concise but evidence-based report in this structure:

```text
# GitHub Development Health Check
Repository: owner/repository
Overall Score: XX / 100
Status: 🟢 HEALTHY
Maturity: Level X — Name

## Score
1. Product Quality XX/25
2. Engineering Quality XX/25
3. GitHub Workflow XX/20
4. Collaboration XX/15
5. Portfolio Value XX/15

## What Is Working
- ...
- ...
- ...

## Risks / Gaps
- ...
- ...
- ...

## Achievement Opportunities
🟢 Pull Request activity
🟢 Code review activity
🟡 Community contribution
⚪ Other opportunities where not applicable

## Top 3 Next Actions
1. ...
2. ...
3. ...

## Portfolio Verdict
...

## Recommended Positioning
"..."
```

Support the report with concrete repository evidence whenever available. Distinguish observed facts from recommendations.

## Quality Bar

A strong result should:

- identify the project's actual maturity
- recognize meaningful engineering work
- find the most important missing pieces
- avoid rewarding activity for activity's sake
- identify natural GitHub achievement opportunities
- provide actionable next steps
- preserve the project's product goals

The skill succeeds when it helps the developer make the **next best engineering decision**, not when it produces the highest score.
