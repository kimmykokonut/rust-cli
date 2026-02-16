# Mini CLI with Rust

followed along [tutorial](https://www.youtube.com/watch?v=5UA9UWWAagc)

What?
Built mini-CLI: formatted ls command

Why?
learn/exposure:

- Rust
- Cargo crates
  - clap crate
  - owo-colors
  - strum
  - tabled
  - chrono
  - serde

How?
Setup:

1. clone gh repo
2. install rust if needed: brew install rust
3. install homebrew if needed

---

CLI examples:
arguments: Path
flags -h (help), -j (json)

`$ cargo run`

╭────────────┬──────┬────────┬─────────────────╮
│ Name │ Type │ Size B │ modified │
├────────────┼──────┼────────┼─────────────────┤
│ Cargo.toml │ File │ 262 │ Mon Feb 16 2026 │
│ target │ Dir │ 160 │ Sun Feb 15 2026 │
│ Cargo.lock │ File │ 13934 │ Mon Feb 16 2026 │
│ README.md │ File │ 134 │ Sun Feb 15 2026 │
│ .gitignore │ File │ 8 │ Sun Feb 15 2026 │
│ .git │ Dir │ 416 │ Mon Feb 16 2026 │
│ src │ Dir │ 96 │ Sun Feb 15 2026 │
╰────────────┴──────┴────────┴─────────────────╯
`$ cargo run -- src`

╭─────────┬──────┬────────┬─────────────────╮
│ Name │ Type │ Size B │ modified │
├─────────┼──────┼────────┼─────────────────┤
│ main.rs │ File │ 2566 │ Mon Feb 16 2026 │
╰─────────┴──────┴────────┴─────────────────╯

`$ cargo run -- -j`
// Shows JSON representation of data
[{"name":"Cargo.toml","e_type":"File","len_bytes":332,"modified":"Mon Feb 16 2026"},{"name":"target","e_type":"Dir","len_bytes":160,"modified":"Sun Feb 15 2026"},{"name":"Cargo.lock","e_type":"File","len_bytes":15521,"modified":"Mon Feb 16 2026"},{"name":"README.md","e_type":"File","len_bytes":1906,"modified":"Mon Feb 16 2026"},{"name":".gitignore","e_type":"File","len_bytes":8,"modified":"Sun Feb 15 2026"},{"name":".git","e_type":"Dir","len_bytes":416,"modified":"Mon Feb 16 2026"},{"name":"src","e_type":"Dir","len_bytes":96,"modified":"Sun Feb 15 2026"}]
