# First run

This page covers what you do after NxtOS opens for the first time. Steps for the desktop app and the terminal are shown side by side.

## What you need before the first session

NxtOS does not include a coding agent. It runs the ones you already use. Before you can chat, one agent has to be set up and signed in. See [Engines](engines.md).

## Open a workspace

A workspace is the folder NxtOS works in. Everything the agent can read or write is inside it.

| Desktop | Terminal |
| --- | --- |
| Choose a folder with Add project in the sidebar. Or open Settings > Workspace and type the full path under Switch workspace. | Run `nxtos` from a terminal opened in the folder. The workspace is the current directory. Pass `--workspace <dir>` to use another. |

Switching workspace in the desktop app closes any running conversations. NxtOS asks first.

## Set up and sign in to an agent

| Desktop | Terminal |
| --- | --- |
| Open Settings > Agents. Each agent shows a status such as Not installed, Not signed in or Connected. Use the Set up and Sign in buttons, then Use. | `/engine` lists the installed agents. `/engine install <id>` sets one up. `/engine login <id>` signs in. `/engine <id>` switches to it. |

Sign-in happens with the agent's own account. NxtOS does not ask for your agent password or API key itself, unless you bind a key under Settings > Trust.

## Start a session

| Desktop | Terminal |
| --- | --- |
| Type in the message box and send. | Type a message at the prompt. Bare words after the command also work as a one-shot prompt, as in `nxtos fix the bug`. |

In the terminal, `/help` lists every command. `/new` starts a fresh session. `Ctrl-C` stops a turn. `Ctrl-D` leaves.

## Get the terminal command

The `nxtos` command ships with the app but is not on your PATH until you add it.

1. Open Settings > General.
2. Find the Terminal command row.
3. Choose Install Terminal Command.

The row says where the link was made. If that folder is not on your PATH yet, it says so. Add the folder to your shell profile, then open a new terminal window. Choose Remove on the same row to undo it.

The terminal and the app need to be the same version. If they differ by a patch version, the terminal warns and carries on. If they differ by a major or minor version, it refuses and names both versions. `--allow-version-mismatch` overrides that. Updating the app fixes it. See [Updates](updates.md).

## Check that things are healthy

In the terminal, `/doctor` prints a readiness report: versions, workspace, policy, security and logs. `/doctor --copy` copies a diagnostics bundle you can attach to a [bug report](feedback.md).

## What a fresh machine shows

<!-- UNVERIFIED: the first-launch screen, any welcome or setup wizard, and the order of agent set-up prompts on a machine with no agents installed were not observed. This page describes the settings that exist in the shipped code, not a captured first-launch walkthrough. -->

Expect an empty workspace and no agent in use until you set one up. Add screenshots here after a clean-machine run.
