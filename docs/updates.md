# Updates

NxtOS updates itself. You can check by hand, or let it check on launch.

For what NxtOS verifies before it replaces itself, see the [README](../README.md#what-nxtos-checks-before-it-installs-anything). That covers the Apple notarization check, the pinned team identifier and the refusal to install an older version. This page does not repeat it.

## Check for an update

There are two ways in the desktop app.

- Settings > General > Updates. The Version row shows what you run. The Status row has a Check now button.
- NxtOS menu > Check for Updates...

The menu item also works when the main window has not opened. The dialog shown when launch is slow offers Check for Updates too.

## Install an update

When a newer version is found, the Status row shows Update available and a Download update button. The steps are:

1. Download update. The row shows Downloading, then Verifying. Verifying takes about half a minute. Do not quit NxtOS during it, because that cancels the update.
2. Ready to install. Choose Restart and install.
3. NxtOS restarts on the new version.

A What changed link on the row opens the release notes.

If an update fails, the row shows Failed and a Copy diagnostics button. Paste that into a [bug report](feedback.md).

If the row says Waiting, a conversation is running. NxtOS waits until none is.

## Automatic checks and installs

Two settings sit under Updates in Settings > General:

- Check for updates automatically. When on, NxtOS looks for a new version each time it starts.
- When an update is found. Choose Ask me before installing, or Install automatically.

With Install automatically, NxtOS downloads in the background, waits until no conversation is running, then restarts itself. It retries about every minute while a conversation is running. With Ask me before installing it downloads but leaves the install to you.

A check you run by hand works whatever these say. When automatic checking is off, nothing is contacted at launch.

## Updates in the terminal

The terminal command does not update itself. It is a link to the app, so updating the app updates it. See [First run](first-run.md) for what happens when the two versions differ.

## Updating by hand

Download the new `.dmg` from [Releases](../../../releases) and drag NxtOS over the old copy in Applications.
