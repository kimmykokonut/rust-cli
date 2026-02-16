# Mini CLI with Rust: `ls` command made pretty

followed [YouTube tutorial](https://www.youtube.com/watch?v=5UA9UWWAagc)

## Tech Stack

- **Rust** - Language
- **Cargo** - Package manager
- **clap** - Command-line argument parsing
- **owo-colors** - Colored terminal output
- **strum** - Enum utilities (Display derive)
- **tabled** - Pretty table formatting
- **chrono** - DateTime handling
- **serde** - Serialization/JSON support

## What?

A mini Rust CLI that recreates `ls` with pretty formatting and useful features.

## Why?

Learning project to get hands-on with Rust and useful crates like CLI arg parsing, color output, and JSON serialization.

## How?

### Setup:

Prerequisites:

- macOS with Homebrew (or skip if Rust already installed)

Steps:

1. Install Rust if needed: `brew install rust`
2. Clone this repo: `git clone <https://github.com/kimmykokonut/rust-cli.git>`
3. Navigate to project: `cd rust-cli`
4. Run it: `cargo run`

Or with a path argument:
`cargo run -- src`

---

## Usage

**Arguments:**

- `<PATH>` - Directory path to list (optional, defaults to current directory)

**Flags:**

- `-h, --help` - Show help message
- `-j, --json` - Output as JSON instead of table

**Examples:**

`$ cargo run`

| Name       | Type | Size B | Modified        |
| ---------- | ---- | ------ | --------------- |
| Cargo.toml | File | 262    | Mon Feb 16 2026 |
| target     | Dir  | 160    | Sun Feb 15 2026 |
| Cargo.lock | File | 13934  | Mon Feb 16 2026 |
| README.md  | File | 134    | Sun Feb 15 2026 |
| .gitignore | File | 8      | Sun Feb 15 2026 |
| .git       | Dir  | 416    | Mon Feb 16 2026 |
| src        | Dir  | 96     | Sun Feb 15 2026 |

`$ cargo run -- src`

| Name | Type | Size B | Modified |
| ---- | ---- | ------ | -------- |

│ main.rs │ File │ 2566 │ Mon Feb 16 2026 │

`$ cargo run -- -j`
[
{"name":"Cargo.toml","e_type":"File","len_bytes":332,"modified":"Mon Feb 16 2026"},
{"name":"target","e_type":"Dir","len_bytes":160,"modified":"Sun Feb 15 2026"},
{"name":"Cargo.lock","e_type":"File","len_bytes":15521,"modified":"Mon Feb 16 2026"},
{"name":"README.md","e_type":"File","len_bytes":1906,"modified":"Mon Feb 16 2026"},
{"name":".gitignore","e_type":"File","len_bytes":8,"modified":"Sun Feb 15 2026"},
{"name":".git","e_type":"Dir","len_bytes":416,"modified":"Mon Feb 16 2026"},
{"name":"src","e_type":"Dir","len_bytes":96,"modified":"Sun Feb 15 2026"}
]

## Features

- 🎨 Colored output with `owo-colors`
- 📊 Table formatting with `tabled`
- 📋 JSON output support with `serde`
- 🕐 File modification times with `chrono`
