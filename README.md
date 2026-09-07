# NxtOS releases

Signed and notarized NxtOS builds, and the update feed the app reads.

The source lives in `io-whtnxt/nxtos` and is private. Only release artefacts
are here.

## The feed

`updates.json` is served by GitHub Pages at
<https://io-whtnxt.github.io/nxtos-releases/updates.json> and is what a
running NxtOS checks. It names one release: the newest.

## What NxtOS checks before it installs anything

Being in this repository is not what makes a download trustworthy, and neither
is the `sha256` below — both arrive from the same place, so the digest proves
only that the file arrived intact.

Before NxtOS replaces itself it mounts the disk image and requires that macOS
assess the app inside as **Notarized Developer ID** for team **HNLP5Y62W7**,
with a stapled ticket. Apple notarizes everybody's software, so "notarized"
alone would only mean Apple has seen it; the team identifier is the part that
means we built it, and it is pinned in the app rather than read from this feed.

An update is also refused unless its version is strictly greater than the one
running, so a feed that rolls back cannot roll an installation back with it.

## Installing by hand

Download the `.dmg` from [Releases](../../releases), open it, and drag NxtOS
to Applications. The same builds are mirrored at
<https://downloads.whtnxt.io/>.
