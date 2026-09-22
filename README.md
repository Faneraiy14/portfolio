# Projects

*[Українською](README.uk.md)*

A map of what I've built — [github.com/Faneraiy14](https://github.com/Faneraiy14).
Grouped by what they actually are, not by when I made them.

## Nyxilum — my own programming language

A bytecode compiler + stack VM built from scratch, with its own standard
library and package manager. Self-hosted — its own interpreter is written
in the language itself.

- **[NyxilumLang](https://github.com/Faneraiy14/NyxilumLang)** — the language: compiler, VM, 166 built-in functions (math, strings, HTTP + WebSocket server, 2D graphics, GUI, concurrency, an embedded DB, OS process control, zip/regex). Also compiles straight to native x86 (no VM at all) — real modules of a hobby OS kernel are written in it, compiled this way, and boot in QEMU.
- **[NyxilumDb](https://github.com/Faneraiy14/NyxilumDb)** — the embedded key-value database NyxilumLang's `dbOpen()` runs on, with WAL durability.
- **[NyxilumNode](https://github.com/Faneraiy14/NyxilumNode)** — the standalone runtime (`nx file.nx`), plus a package manager (`nx install owner/repo`). Ships as a ready `.exe` — no .NET install needed.
- **[NyxilumMcp](https://github.com/Faneraiy14/NyxilumMcp)** — an MCP server so an AI assistant can compile, run, lint, and REPL-eval `.nx` code directly, sandboxed.
- **[nyxilum-assert](https://github.com/Faneraiy14/nyxilum-assert)** — an assertion library for testing NyxilumLang code.

## Built with Nyxilum

Real applications, not toy demos — each running entirely on NyxilumLang's
own standard library, no external dependencies.

- **[nyxilum-chat](https://github.com/Faneraiy14/nyxilum-chat)** — a live group chat: real one-to-many WebSocket broadcast.
- **[nyxilum-control-center](https://github.com/Faneraiy14/nyxilum-control-center)** — a live system monitor: web dashboard, WebSocket push, ping, history export to zip.
- **[nyxilum-paste](https://github.com/Faneraiy14/nyxilum-paste)** — a Pastebin-style snippet-sharing service.

## NyxOS — a custom operating system

A kernel from scratch in C + assembly, with no Linux/BSD or any
existing kernel underneath — not for practicality, but to control
every level of the system personally, starting from the first byte
after the bootloader. Interrupts, a physical memory manager and
paging, its own filesystem (NyxFS), Ring 3 (userspace) with a
preemptive scheduler, a graphical VESA/GOP mode with a window manager
and desktop, networking (PCI/RTL8139/lwIP — DHCP/DNS/TCP/HTTP), its
own package format and package manager, a minimal browser, user
accounts, a real-disk GPT installer, and USB (UHCI) with its first
real HID mouse.

- **[NyxOS-releases](https://github.com/Faneraiy14/NyxOS-releases)** — ready-to-download ISO; source code lives in a separate private repo.

## FL Launcher

A Minecraft launcher I actively develop and ship to real users.

- **[fl-launcher](https://github.com/Faneraiy14/fl-launcher)** — the release channel (auto-updating `.exe`); source lives in a separate private repo.
- **[fl-bridge](https://github.com/Faneraiy14/fl-bridge)** — releases of `FLBridge.jar`, the mod loader FL Launcher downloads and updates automatically.

## NyxilumCMS

A general-purpose content management system, built from scratch — PHP + MySQL, no framework.

- **[NyxilumCMS](https://github.com/Faneraiy14/NyxilumCMS)** — content of any type, categories, menu, media, roles (admin/editor) with TOTP two-factor login, scheduled publishing, SEO/Open Graph tags, sitemap.xml + RSS, full export/import, and a from-scratch web installer. A companion MCP server gives an AI assistant direct database access (kept private).

## MCP servers

Tools that let an AI assistant do something real instead of just talking
about it.

- **[wordpress-mcp](https://github.com/Faneraiy14/wordpress-mcp)** — an MCP server for WordPress (site health, posts, plugins), built on the official `modelcontextprotocol/php-sdk`.
- **[minecraft-rcon-mcp](https://github.com/Faneraiy14/minecraft-rcon-mcp)** — lets an AI control a live Minecraft server over RCON (players, chat, teleport, weather, and more).
- **[workspace-status-mcp](https://github.com/Faneraiy14/workspace-status-mcp)** — five tools for working across dozens of repos at once: a git+CI status snapshot, which `Architecture/<repo>.txt` docs are missing or stale, release drift between a source repo and the one that tags releases from it, and a batched GitHub PR status check (state, CI, review decision, top-level vs. inline comment counts).
- **[ci-watch-mcp](https://github.com/Faneraiy14/ci-watch-mcp)** — waits for a GitHub Actions run to finish and reports the result, so an AI doesn't have to poll.

*(NyxilumMcp is listed above, under Nyxilum — it's an MCP server too.)*

## Dev tools

- **[anylint](https://github.com/Faneraiy14/anylint)** — a cross-language static analyzer: one core, plugin providers per language (PHP, NyxilumLang, JS/TS + 15 more via tree-sitter) — the same rules catch the same bugs everywhere.
- **[anylint-vscode](https://github.com/Faneraiy14/anylint-vscode)** — the VS Code extension: inline diagnostics and quick fixes from anylint.
- **[envcheck](https://github.com/Faneraiy14/envcheck)** — a CLI that diffs `.env` against `.env.example` (missing/empty/extra keys).
- **[secretscan](https://github.com/Faneraiy14/secretscan)** — a CLI that scans for accidentally committed secrets (API keys, tokens, private keys).

## Just for fun

- **[CursorNinja](https://github.com/Faneraiy14/CursorNinja)** — a Fruit Ninja clone played with the mouse cursor. Python + tkinter, zero dependencies.
- **[DesktopCat](https://github.com/Faneraiy14/DesktopCat)** — a cat that sits on your desktop, taps along to your keystrokes, and falls asleep when you stop. Python + tkinter, zero dependencies.
- **[tap-site](https://github.com/Faneraiy14/tap-site)** — a clicker game with a separate TypeScript backend and frontend.

## Security research

- **[obriycipher](https://github.com/Faneraiy14/obriycipher)** — a hand-rolled block cipher pulled out of a messenger app, honestly labeled as unsafe for real use (see its `SECURITY.md`).

## Contributions to other projects

- **[cyklokoalicia/OpenSourceBikeShare](https://github.com/cyklokoalicia/OpenSourceBikeShare)** — a real, live bike-sharing system in Bratislava. 9 merged PRs: introduced PHPStan static analysis (level 4) and fixed all 82 errors it found, then a string of real bugs found via code review and CI investigation — a `TypeError` crash on legacy credit-history rows, a coupon-generator bug that could silently issue fewer codes than requested (or collide on a `UNIQUE` column), missing `ext-intl` that broke ICU translations, and a Symfony security-patch regression that broke password-change sessions.
- **[modelcontextprotocol/php-sdk](https://github.com/modelcontextprotocol/php-sdk)** — the official PHP SDK for MCP. One merged PR (variadic tool parameters).
- **[sveneld/mailqueue](https://github.com/sveneld/mailqueue)** — a framework-agnostic mail queue package for PHP (Symfony/Yii2 adapters, retry-friendly delivery). 2 open PRs: raised PHPStan static analysis from level 8 to level 9, added CC/BCC recipient support across `EmailMessage` and every real transport.

## Code quality

Every PHP project below runs static analysis and an automated test
suite in CI on every push — not just "it works on my machine."

| Project | PHPStan | Tests |
|---|---|---|
| [NyxilumCMS](https://github.com/Faneraiy14/NyxilumCMS) | level 6 | PHPUnit, hits a real disposable MySQL DB |
| [wordpress-mcp](https://github.com/Faneraiy14/wordpress-mcp) | max | PHPUnit |
| [anylint](https://github.com/Faneraiy14/anylint) | max | PHPUnit, 106 tests (incl. a 15-language tree-sitter matrix) |
| [secretscan](https://github.com/Faneraiy14/secretscan) | max | PHPUnit, 27 tests |
| [envcheck](https://github.com/Faneraiy14/envcheck) | max | PHPUnit, 14 tests |

(PHPStan level is how strict the type-checking is — `max` catches
everything short of custom rule extensions; picked per-project at the
highest level where every finding is real, not a false positive from
a stub PHPStan can't see past.)
