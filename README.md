# AskShip

**Let your end users prompt for a change to your app — routed through your approval chain.**

AskShip is an open-source pattern (and reference implementation) for products that want to let end users request new components, options, or entries directly inside the product — where an AI agent drafts the change, and it only ships after your product manager and tech lead approve it.

## The idea

Most products have a few spots that are *designed to grow*: an insert menu, a picklist, a symbol library, a set of job titles. Today, when a user hits "the thing I need isn't here," that request goes into a feedback inbox and dies there.

AskShip turns that moment into a workflow:

```
User requests something  →  AI drafts it (mockup / data entry)
                          →  Guardrail check (safety, duplicates, fit)
                          →  PM reviews the request + the draft
                          →  Tech lead reviews the actual change
                          →  Ships, and the user gets notified
```

You define **which parts of your product are extensible**, **who the approvers are**, and **what the guardrails are**. AskShip handles the orchestration.

## Repos

| Repo | What it is |
|---|---|
| [`workflow`](https://github.com/askship/workflow) | The n8n workflow template — webhook intake, AI drafting, Slack approval gates, and the PR/merge step |
| [`askship-widget`](https://github.com/askship/askship-widget) | The embeddable front-end widget — the "Request new X" button + form your app drops in |

## Status

Early / experimental. This started as a pattern for a floor-plan diagramming app's "insert component" menu and a job-board picklist, and is being generalized from there. Expect rough edges — contributions and issues welcome.

## Why this exists

Existing AI-prototyping tools (Aha! Builder, Builder.io Fusion, Alloy) let a *PM or developer* turn a prompt into a prototype or PR. AskShip is for the other direction: letting the *end user* be the one who prompts, with the same rigor of human review before anything reaches production.

## License

MIT, unless a repo says otherwise.

## Contact

Open an issue on either repo, or start a discussion here at the org level.
