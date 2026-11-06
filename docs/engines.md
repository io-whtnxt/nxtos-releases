# Engines

NxtOS runs coding agents you bring. It talks to them over the Agent Client Protocol (ACP), a common wire format many coding tools speak. NxtOS calls an agent an engine in some places and an agent in others. They are the same thing.

## Built-in engines

NxtOS 0.5.1 includes setup for four:

- Claude Code
- Codex
- OpenCode
- pi

You keep the subscription or key you already have for each. Any other ACP agent can be added with a `nxtos/engines.json` file in your workspace. The README in the NxtOS source describes the format. This page covers the four above.

## Set up an agent

| Desktop | Terminal |
| --- | --- |
| Settings > Agents. Choose Set up, then Sign in, then Use. | `/engine install <id>`, `/engine login <id>`, then `/engine <id>`. |

Status labels in Settings > Agents include Connected, Not installed, Installing, Not signed in, Waiting for sign-in, Missing requirement, Needs your OK and Failed.

## Is the agent safe to start?

NxtOS tests each agent by starting it on your Mac with every action denied, then watching whether it changes anything. The result is one of three badges. The Settings > Safety page and `/safety` show them.

| Badge | Meaning |
| --- | --- |
| Asks first | The agent sent every file change, command and fetch to NxtOS and changed nothing. Your answers in NxtOS are the only way it can act. |
| Acts without asking | It still changed things. Your answers in NxtOS do not reach it, and NxtOS cannot see or stop what it does. |
| Not checked | NxtOS has not tested it, so it cannot say either way. |

NxtOS will not start an agent that acts without asking, or one it has not tested, until you accept it. Accepting is a decision for one folder only.

## Accepted and not accepted

- Not accepted: the agent shows Review and use. NxtOS refuses to start it. Choosing Review and use shows the exact command it runs and a plain statement of what the test found.
- Accepted: you confirmed that dialog. The agent starts. It shows Stop using, which takes the acceptance back.

An accepted agent that acts without asking still acts without asking. Accepting records your choice. It does not make the agent safer. The acceptance does not carry to other folders, and it stops applying if a later check finds something different.

In the terminal:

- `/engine review <id>` shows what the agent runs and what was measured.
- `/engine accept <id>` accepts it for this workspace, after you confirm. `--yes` skips the question.
- `/engine probe <id>` runs the check again.
- `/safety stop <agent>` stops using an agent you accepted.

## Approvals while the agent works

Every session has a permission mode. There are three:

| Mode | What it does |
| --- | --- |
| Ask | Ask before anything the policy leaves to you. |
| Accept edits | File edits run without asking. Commands and fetches still ask. |
| Allow all | Everything the policy allows runs without asking. |

Moving to Allow all always needs an explicit yes.

| Desktop | Terminal |
| --- | --- |
| The permission chip in the chat shows and changes the mode. | `/mode` shows the mode. `/mode ask`, `/mode edits` or `/mode all` changes it. Shift+Tab cycles modes in the composer. |

## Plan mode

Plan mode is read-only. Every change is refused, even ones you saved. The agent plans, and you decide how it goes on.

| Desktop | Terminal |
| --- | --- |
| Turn on plan mode from the permission chip. | `/plan` toggles plan mode. |

When the plan is ready you are offered these options. The text is the same idea in both places.

| Desktop | Terminal |
| --- | --- |
| Approve and continue: Ask | Approve, and ask before each action |
| Approve and continue: Accept edits | Approve, and let edits run without asking |
| Approve and continue: Allow all (asks you to confirm with Allow all and continue) | Approve, and let everything the policy allows run |
| Approve and start fresh | Approve, and start a fresh session from the task ledger |
| Keep planning | Keep planning |

Nothing changes until you choose. Esc, or an empty Enter in the terminal, keeps planning. "Start fresh" begins a new conversation from the task ledger rather than the old transcript.

<!-- UNVERIFIED: how plan mode is switched on from the permission chip (control name and placement) was not confirmed against the rendered app -->
