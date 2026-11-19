# Atlas Kit Downloads

Prebuilt pieces for the Atlas Kit, so setup downloads them instead of compiling for an hour. You don't need to grab anything here by hand. The setup app does it.

## What's here

Each release has:

- `matrix-rustpush-linux-x86_64.tar.gz`: the iMessage bridge the bots talk through, built for Ubuntu 24.04 on WSL. The setup app checks its sha256 before it uses it.
- `bridge-source-patches.tar.gz`: the exact commits and patches it was built from.

## Where it comes from

The bridge isn't my code. It's [jasonlaguidice/imessage](https://github.com/jasonlaguidice/imessage) and [OpenBubbles/rustpush](https://github.com/OpenBubbles/rustpush) with my patches on top. It's AGPL-3.0, so the source for every binary here is in the same release: `SOURCE.md` inside the tarball says which commits, and the patches are right next to it. Clone those commits, apply the patches, run `make build` and you get the same thing.

## Heads up

It signs in to Apple's iMessage servers as a Mac. Apple doesn't support that. Use a spare Apple ID, go slow on logins, and know that Apple can block the account or the Mac it's posing as.
