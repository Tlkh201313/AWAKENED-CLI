<p align="center">
  <a href="https://github.com/Tlkh201313/AWAKENED-CLI">
    <img src="https://img.shields.io/badge/⚡-Awakening_CLI-gold?style=for-the-badge" alt="Awakening CLI">
  </a>
</p>

<p align="center"><strong>Awakening CLI</strong> — AI coding agent (OpenCode fork)</p>

<p align="center">
  <a href="https://github.com/Tlkh201313/AWAKENED-CLI/releases"><img alt="Release" src="https://img.shields.io/github/v/release/Tlkh201313/AWAKENED-CLI?style=flat-square" /></a>
  <a href="https://github.com/Tlkh201313/AWAKENED-CLI/actions/workflows/test.yml"><img alt="Build status" src="https://img.shields.io/github/actions/workflow/status/Tlkh201313/AWAKENED-CLI/test.yml?style=flat-square&branch=dev" /></a>
  <a href="https://github.com/anomalyco/opencode"><img alt="Upstream" src="https://img.shields.io/badge/upstream-OpenCode-blue?style=flat-square" /></a>
</p>



> **Awakening CLI** is an independent fork of [OpenCode](https://github.com/anomalyco/opencode). It ships the **Awakened** agent runtime with capability packs, design auto-routing, memory, and a terminal + web UI. This repository is maintained at [Tlkh201313/AWAKENED-CLI](https://github.com/Tlkh201313/AWAKENED-CLI).

---

## Installation

Requires [Bun](https://bun.sh) 1.3+.

```bash
git clone https://github.com/Tlkh201313/AWAKENED-CLI.git
cd AWAKENED-CLI
bun install
bun run --cwd packages/awakened build
bun link
awakened
```

### From release binaries

Download the latest from [GitHub Releases](https://github.com/Tlkh201313/AWAKENED-CLI/releases).

```bash
./install --version 1.0.0
```

The install script places the binary in `~/.awakened/bin` and adds it to `$PATH`.

```bash
# Custom install directory
AWAKENED_INSTALL_DIR=$HOME/.local/bin ./install --version 1.0.0
```

## Quick start

```bash
awakened          # terminal UI
awakened serve      # local server + web app
awakened --version  # should print 1.0.0
```

Configuration lives in `.awakened/` (project) or `~/.awakened/` (global). See [AGENTS.md](./AGENTS.md) for contributor conventions.

## Agents

Switch agents with `Tab` in the TUI:

- **build** — full-access development agent (default)
- **plan** — read-only analysis and exploration

Use `@general` for complex multi-step searches. Capability packs (e.g. **awakened-design**) activate automatically and appear as `using <pack-id>` in the UI.

## Desktop app (beta)

Desktop builds are published on [Releases](https://github.com/Tlkh201313/AWAKENED-CLI/releases) when available:

| Platform              | Artifact                           |
| --------------------- | ---------------------------------- |
| macOS (Apple Silicon) | `awakened-desktop-mac-arm64.dmg`   |
| macOS (Intel)         | `awakened-desktop-mac-x64.dmg`     |
| Windows               | `awakened-desktop-windows-x64.exe` |
| Linux                 | `.deb`, `.rpm`, or `.AppImage`     |

## Documentation

- [CONTRIBUTING.md](./CONTRIBUTING.md) — dev setup and PR guidelines
- [SECURITY.md](./SECURITY.md) — threat model and reporting
- [AGENTS.md](./AGENTS.md) — coding standards for this repo
- Upstream reference: [OpenCode docs](https://opencode.ai/docs)

## Contributing

Contributions welcome on this fork. Read [CONTRIBUTING.md](./CONTRIBUTING.md) first. For upstream OpenCode changes, consider contributing to [anomalyco/opencode](https://github.com/anomalyco/opencode) as well.

## License

MIT — see [LICENSE](./LICENSE). Based on OpenCode; see upstream for original copyright.
