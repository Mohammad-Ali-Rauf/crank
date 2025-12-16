# crank ⚙️

> *"Your lookahead is still buffering..."*

`crank` is a **CLI-first**, **Rust-powered** speedcubing tracker for **Roux**, **OH**, and **BLD** nerds (like me) who refuse to touch a GUI.

Built for **Linux**. Single static binary. **Zero runtime deps** (SQLite bundled).

---

## ✨ Features

- ⚡ **Blazing fast** — Rust + SQLite = solves logged in **nanoseconds**
- 🧊 **Method-aware**: track `roux`, `oh`, `bld` separately with tailored stats
- 📊 **Real metrics**: PB, avg5, avg12, consistency (stdev%), fuck-up ratio, BLD success rate
- 🎲 **Built-in scrambler**: method-optimized, no network, no bloat
- 🎯 **Goal tracking**: `crank goal roux pb 11.5` → it watches. It judges.
- 💥 **Roast mode**: optional motivational abuse (`crank roast`)
- 🗃️ **Single binary, single DB** (`~/.crank.db`) — your entire cubing life in 2 files

---

## 🚀 Quick Start

```bash
# Build (requires Rust 1.70+)
cargo install --git https://github.com/Mohammad-Ali-Rauf/crank

# Log a Roux solve
crank add 12.34 --roux

# Add a successful BLD attempt
crank add 45.6 --bld --success

# Check stats
crank stats roux

# Get scrambled
crank scramble oh

# Need "encouragement"?
crank roast
```

---

## 🧪 Philosophy

- **No WCA dogma** — this is **your** training log
- **No GUIs**, no web, no cloud — if it can’t run over SSH, it’s useless
- **Roasts are opt-in** (and easily customizable via `~/.crank/roasts.txt`)
- **Speed > polish** — but not at the cost of correctness

---

## 🛠️ Build from Source

```bash
git clone https://github.com/Mohammad-Ali-Rauf/crank.git
cd crank
cargo install --path .
```

> ℹ️ Public roast lines are **tame**. Enable `--russian-mode` to load your personal humiliation list (store in `~/.crank/roasts.txt`, not tracked).

---

## 🤡 Disclaimer

This tool may:
- Tell you your OH is pathetic
- Remind you that your BLD memo failed *again*
- Refuse to validate your life choices

- **DO NOT USE if you are sensitive to verbal insults**

**It’s not a bug — it’s a feature.**

> 💀 Made for cubers who `strace` their timers and believe `/bin/bash` is a lifestyle.
