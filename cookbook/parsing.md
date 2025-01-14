---
title: Parsing
---

# Parsing

Nu offers the ability to do some basic parsing.

How to parse an arbitrary pattern from a string of text into a multi-column table.

```shell
> cargo search shells --limit 10 | lines | parse "{crate_name} = {version} #{description}" | str trim
```

Output

```
───┬──────────────┬─────────────────┬────────────────────────────────────────────────────────────────────────────────
 # │  crate_name  │     version     │                                  description
───┼──────────────┼─────────────────┼────────────────────────────────────────────────────────────────────────────────
 0 │ shells       │ "0.2.0"         │ Sugar-coating for invoking shell commands directly from Rust.
 1 │ pyc-shell    │ "0.3.0"         │ Pyc is a simple CLI application, which allows you to perform shell commands in
   │              │                 │ cyrillic and other a…
 2 │ ion-shell    │ "0.0.0"         │ The Ion Shell
 3 │ sheldon      │ "0.6.6"         │ Fast, configurable, shell plugin manager.
 4 │ nu           │ "0.44.0"        │ A new type of shell
 5 │ git-gamble   │ "2.3.0"         │ blend TCR + TDD to make sure to develop the right thing, babystep by babystep
 6 │ martin       │ "1.0.0-alpha.0" │ Blazing fast and lightweight PostGIS vector tiles server
 7 │ fnm          │ "1.29.2"        │ Fast and simple Node.js version manager
 8 │ remote_shell │ "2.0.0"         │ remote shell written by rust.
 9 │ sauce        │ "0.6.6"         │ A tool for managing directory-specific state.
───┴──────────────┴─────────────────┴────────────────────────────────────────────────────────────────────────────────
```
