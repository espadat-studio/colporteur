<p align="center">
  <h1 align="center"><a href="https://colporteur.espadat.com">Colporteur</a></h1>
</p>
<p align="center">
  <a href="https://crates.io/crates/colporteur">
    <img src="https://img.shields.io/crates/v/colporteur" alt="Crates.io">
  </a>
</p>

> Read your newsletters in your feed reader, not your inbox.

Colporteur turns newsletters into Atom feeds from the mailbox you already have. It reads the senders you list over IMAP, strips tracking pixels and scripts, and writes Atom files any feed reader can subscribe to. You don't need a forwarding address, and nobody else reads your mail. A colporteur was the pedlar who carried pamphlets from door to door.

## Features

- **IMAP native** -- connects directly to any IMAP mailbox, no forwarding rules needed
- **HTML sanitization** -- strips tracking pixels, scripts, and styles while preserving content
- **Atom feeds** -- generates standard Atom XML consumable by any feed reader
- **Multi-account** -- pull newsletters from multiple IMAP accounts into separate feeds
- **Dry-run mode** -- preview what would be fetched before writing anything
- **JSON output** -- machine-readable output for scripting and automation

## Quick Start

Install colporteur from a [pre-compiled binary](https://github.com/espadat-studio/colporteur/releases/latest) or via cargo:

```bash
cargo install colporteur
```

Generate a sample config:

```bash
colporteur init
```

Edit `~/.config/colporteur/config.toml` with your IMAP accounts and feeds, then:

```bash
colporteur test    # verify IMAP connection
colporteur fetch   # fetch and generate feeds
colporteur list    # show feed sync state
```

## Documentation

Full documentation available at [colporteur.espadat.com](https://colporteur.espadat.com):

- [Installation](https://colporteur.espadat.com/getting-started/installation/) - Detailed setup guide
- [Quick Start](https://colporteur.espadat.com/getting-started/quick-start/) - Step-by-step walkthrough
- [CLI Reference](https://colporteur.espadat.com/cli-reference/) - All commands documented
- [Configuration](https://colporteur.espadat.com/configuration/) - Config file format and options
- [How It Works](https://colporteur.espadat.com/how-it-works/email-processing/) - Email processing pipeline

## Requirements

- An IMAP-accessible email account with newsletters

## Develop

`./setup` installs mise and the git hooks, `mise run` lists the tasks. Tooling and configuration: [the development page](https://colporteur.espadat.com/development/).

## Community

- [Documentation](https://colporteur.espadat.com)
- [Report Issues](https://github.com/espadat-studio/colporteur/issues)
