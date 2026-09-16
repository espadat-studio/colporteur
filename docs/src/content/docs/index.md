---
title: Colporteur
description: Turn email newsletters into Atom feeds straight from your IMAP inbox. Strips trackers, needs no forwarding address or third-party service.
---

> Read your newsletters in your feed reader, not your inbox.

Colporteur turns newsletters into Atom feeds from the mailbox you already have. It reads the senders you list over IMAP, strips tracking pixels and scripts, and writes Atom files any feed reader can subscribe to. You don't need a forwarding address, and nobody else reads your mail. A colporteur was the pedlar who carried pamphlets from door to door.

## Features

- **IMAP fetching** — connects to any IMAP server over TLS
- **Atom feed generation** — produces standard Atom XML consumable by any feed reader
- **HTML sanitization** — strips tracking pixels, scripts, and unsafe markup via allowlist
- **Incremental sync** — tracks last-seen UID per sender, only fetches new emails
- **UIDVALIDITY handling** — detects mailbox resets and re-syncs automatically
- **Multi-account** — configure multiple IMAP accounts and map feeds across them
- **Multi-sender feeds** — aggregate multiple senders into a single feed
- **Dry-run mode** — preview what would be fetched without writing anything
- **JSON output** — machine-readable output for scripting (`--json`)
- **Atomic writes** — feed files and state are written atomically (write-to-tmp then rename)

## Quick Start

```bash
cargo install colporteur
```

Create a config file at `~/.config/colporteur/config.toml`:

```toml
output_dir = "/var/lib/colporteur/feeds"

[accounts.mail]
server = "imap.example.com"
username = "newsletters@example.com"
password = "your-password" # or "!pass show email/imap" for a password manager

[feeds.weekly-digest]
title = "Weekly Digest"
account = "mail"
senders = ["digest@newsletter.com"]
```

Fetch:

```bash
colporteur fetch
```

The generated feed will be at `/var/lib/colporteur/feeds/weekly-digest.xml`.

See [Installation](/getting-started/installation/) and [Quick Start](/getting-started/quick-start/) for detailed setup instructions.
