# scoop-bucket

[![Tests](https://github.com/vshylov/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/vshylov/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/vshylov/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/vshylov/scoop-bucket/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket for **[mindfork](https://mindfork.io)** — a
terminal AI chat written in Rust: local models via llama.cpp, or OpenAI,
Anthropic, Gemini, Grok and OpenRouter in the cloud, with persistent memory,
notes, RAG and tools.

## Install

```pwsh
scoop bucket add mindfork https://github.com/vshylov/scoop-bucket
scoop install mindfork/mindfork
```

Then run `mindfork` in any terminal — or `mindfork demo` to look around with
sample chats and a scripted engine, no model and no key needed.

## What it installs

- The release's portable Windows build
  (`mindfork-rs-vX.Y.Z-x86_64-windows.zip`), its hash checked against the
  release's own `sha256sums.txt`.
- A `defaults.json` beside the binary that says `{ "mode": "system" }`: your
  chats, notes and settings live in `%APPDATA%\mindfork-rs\data`, so an update
  or a `scoop uninstall` leaves them where they are — the location the Windows
  installer recommends too. What the file can say instead is in
  [install.md §2.1](https://github.com/vshylov/mindfork-rs/blob/main/docs/install.md#21-installation-defaults-defaultsjson).
- `mindfork` on your `PATH`, and a Start menu shortcut.

## Updates

[Excavator](.github/workflows/excavator.yml) looks for a new release every four
hours and commits the manifest for it, its hash taken from that release's
`sha256sums.txt`; `scoop update mindfork` then installs it.

## Where to report what

A problem with the app — [mindfork-rs issues](https://github.com/vshylov/mindfork-rs/issues).
A problem with installing it through Scoop — [this repository's issues](https://github.com/vshylov/scoop-bucket/issues).

The manifests are in the public domain ([LICENSE](LICENSE), the Unlicense);
mindfork itself is MIT.
