# Install NxtOS

NxtOS is a Mac app with a terminal command that ships inside it. This page gets the app onto your Mac.

## Requirements

- A Mac with Apple silicon. Intel Macs are not supported.
- macOS 13.3 or later.
- At least one coding agent of your own, signed in with the account you already have. See [Engines](engines.md).

## Download

1. Open the [Releases](../../../releases) page of this repository.
2. Download the latest `NxtOS-<version>.dmg`.
3. Open the downloaded disk image.
4. Drag NxtOS to the Applications folder.
5. Eject the disk image.

The same builds are mirrored at <https://downloads.whtnxt.io/>.

## First launch and Gatekeeper

NxtOS is signed with a Developer ID and notarized by Apple, so macOS can check it before it opens.

1. Open NxtOS from Applications.
2. macOS may ask you to confirm that you want to open an app downloaded from the internet. Choose Open.
3. NxtOS starts its background service and opens a window.

You should not need to open System Settings or right-click the app. If macOS says it cannot verify the app, do not work around it. Download the disk image again from Releases and [report the problem](feedback.md).

## If the first launch is slow

NxtOS starts a small local service when it opens. If nothing usable appears after about ten seconds, a dialog offers a way forward. These are the button labels in 0.5.1:

- Keep waiting
- Check for Updates
- Retry
- Connect to another computer

A start that is only slow offers Keep waiting and Check for Updates. A start that failed offers Retry and Connect to another computer.

## Verify the download (optional)

The disk image's SHA-256 is in the release feed. It proves the file arrived intact. It does not prove who built it. The check that does is described in the [README](../README.md#what-nxtos-checks-before-it-installs-anything).

## Next

[First run](first-run.md).
