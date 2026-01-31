<p align="center">
  <img src="https://gal.run/logo.svg" alt="GAL" width="120">
</p>

<h1 align="center">GAL - Governance Agentic Layer</h1>

<p align="center">
  <strong>Enterprise governance for AI coding agents</strong>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@scheduler-systems/gal"><img src="https://img.shields.io/npm/v/@scheduler-systems/gal.svg" alt="npm version"></a>
  <a href="https://github.com/Scheduler-Systems/gal.run/blob/main/LICENSE"><img src="https://img.shields.io/npm/l/@scheduler-systems/gal.svg" alt="license"></a>
</p>

---

GAL enables organizations to centrally manage and distribute AI coding agent configurations to developers. Your CISO defines approved settings, and developers sync them with a single command.

## Supported Agents

| Agent | Config Files | Status |
|-------|--------------|--------|
| Claude Code | `.claude/`, `CLAUDE.md` | ✅ Supported |
| Cursor | `.cursor/`, `.cursorrules` | ✅ Supported |
| Windsurf | `.windsurfrules` | ✅ Supported |
| GitHub Copilot | `.github/copilot-instructions.md` | ✅ Supported |
| Cline | `.clinerules`, `.cline/` | ✅ Supported |
| Aider | `.aider*` | ✅ Supported |
| Amazon Q | `.amazonq/` | 🔜 Coming Soon |

## Installation

### npm (Recommended)

```bash
npm install -g @scheduler-systems/gal
```

### curl (macOS/Linux)

```bash
curl -fsSL https://gal.run/install.sh | bash
```

### PowerShell (Windows)

```powershell
irm https://gal.run/install.ps1 | iex
```

## Prerequisites

- **Node.js** 18.0 or higher
- **npm** 8.0 or higher
- A GAL organization account (sign up at [gal.run](https://gal.run))

## Quick Start

1. **Authenticate with GitHub**
   ```bash
   gal auth login
   ```

2. **Sync your organization's approved configuration**
   ```bash
   gal sync --pull
   ```

3. **Verify configuration applied**
   ```bash
   gal sync --status
   ```

That's it! Your AI coding agents are now configured with your organization's approved settings.

## Commands

| Command | Description |
|---------|-------------|
| `gal auth login` | Authenticate with GitHub |
| `gal auth logout` | Sign out |
| `gal sync --pull` | Download approved configuration |
| `gal sync --status` | Check sync status |
| `gal --help` | Show all commands |

## Documentation

- [Getting Started Guide](https://docs.gal.run/getting-started)
- [Configuration Reference](https://docs.gal.run/configuration)
- [Admin Guide](https://docs.gal.run/admin)
- [FAQ](https://docs.gal.run/faq)

## How It Works

```
┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
│   GAL Console   │      │    GAL API      │      │   Developer     │
│  (CISO/AI Lead) │─────>│   (Cloud)       │<─────│   (CLI)         │
└─────────────────┘      └─────────────────┘      └─────────────────┘
      │                          │                        │
      │ 1. Set approved          │                        │
      │    configurations        │                        │
      │                          │                        │
      │                          │ 2. gal sync --pull     │
      │                          │<───────────────────────│
      │                          │                        │
      │                          │ 3. Return approved     │
      │                          │    configs             │
      │                          │───────────────────────>│
      │                          │                        │
      │                          │                 4. Apply to
      │                          │                    agent configs
```

## Support

- **Issues**: [GitHub Issues](https://github.com/Scheduler-Systems/gal.run/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Scheduler-Systems/gal.run/discussions)
- **Email**: support@scheduler-systems.com

## Security

Found a security issue? Please report it privately. See [SECURITY.md](./SECURITY.md) for our security policy.

## License

MIT - see [LICENSE](./LICENSE) for details.

---

<p align="center">
  Built by <a href="https://scheduler-systems.com">Scheduler Systems</a>
</p>
