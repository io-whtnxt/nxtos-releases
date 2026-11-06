# Feedback

Use these when something breaks, when you have a question, or when you have an idea. Each opens a form on this repository's GitHub issues.

## Report a problem

| Desktop | Terminal |
| --- | --- |
| Help > Report a Problem. Or Settings > General > Feedback > Report a problem. | `/feedback` |

Both open a prefilled issue in your browser. If no browser opens, the terminal prints the link instead.

The form arrives with two fields already filled in:

- Your NxtOS version.
- Your macOS version and chip, for example `macOS 14.5 (arm64)`.

Nothing else is sent. NxtOS does not add your workspace, username, paths, model or engine to the link.

The page is public. Leave out API keys, passwords and anything private before you submit.

## Ask a question or suggest an idea

Settings > General > Feedback also has Ask a question and Suggest an idea. In the terminal, `/feedback` lists those two links under the problem report.

## What to include

- What you did, what you expected, and what happened instead.
- Whether it happens in the desktop app, the terminal, or both.
- The agent you were using.

For startup or update problems, add diagnostics:

| Desktop | Terminal |
| --- | --- |
| Help > Copy Diagnostics. Help > Reveal Logs opens the logs folder. | `/doctor --copy` copies the bundle and saves a copy beside the logs. |

Skim the diagnostics before you paste them into a public issue.

## If the link does not open

If the backend has not started, the desktop menu cannot fill in your versions. It tells you to use Report a problem in Settings once the app is up. You can also open a new issue from the repository's Issues tab and type the versions yourself. Find them under NxtOS > About NxtOS, or with `/about` in the terminal.
