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
- 🔄 **Backup-friendly**: DB lives at `~/.crank.db` — copy it, version it, `rsync` it to Mars

---

## 🚀 Quick Start

```bash
# Install (requires Rust 1.70+)
cargo install --git https://github.com/Mohammad-Ali-Rauf/crank

# Verify install
crank version  # should print something like "crank v0.1.0"

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

# Unleash personalized hell (requires ~/.crank/roasts.txt)
crank roast --russian-mode
```

---

## 🧪 Philosophy

- **No WCA dogma** — this is **your** training log  
- **No GUIs**, no web, no cloud — if it can’t run over SSH, it’s useless  
- **Roasts are opt-in** — customize your pain via `~/.crank/roasts.txt`  
- **Speed > polish** — but not at the cost of correctness  

---

## 🔧 Roast Customization

Create `~/.crank/roasts.txt` — one savage line per row:

```txt
Your lookahead is sponsored by buffering wheel.
Is that a solve or a cry for help?
Your BLD memo failed. Again. We’re used to it now.
OH? More like "Oh no."
```

Then run:
```bash
crank roast --russian-mode
```

> 🚨 **Warning**: These lines are **evaluated as raw strings** — no escapes, no mercy.

---

## 🗃️ Backup & Portability

Your data lives **only** in `~/.crank.db`.  
To back up:
```bash
cp ~/.crank.db ~/backups/crank-$(date -I).db
```

To migrate to another machine:  
1. Install `crank`  
2. Copy your old `~/.crank.db` into place  
3. Resume getting roasted exactly where you left off  

**No cloud. No sync. Just files.** Like God intended.

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
- Self-delete if you dare whisper “CFOP” near it  

- **DO NOT USE if you are sensitive to verbal insults**  

**It’s not a bug — it’s a feature.**

> 💀 Made for cubers who `strace` their timers and believe `/bin/bash` is a lifestyle.  
