# 🍒 Pacsmart

> **The Ultimate Arcade Wrapper for Arch Linux Package Managers.**
>
> Transform your boring `pacman`, `yay`, or `paru` output into an engaging, gamified, and pixel-perfect arcade experience.

<div align="center">

[![MIT License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

[![Security](https://img.shields.io/badge/Security-orange?style=for-the-badge)](./SECURITY.md)
[![Contributing](https://img.shields.io/badge/Contributing-blue?style=for-the-badge)](./CONTRIBUTING.md)
[![Code Of Conduct](https://img.shields.io/badge/Code_of_Conduct-purple?style=for-the-badge)](./CODE_OF_CONDUCT.md)

</div>

-----

## 🎮 What is Pacsmart?

**Pacsmart** is not just a wrapper; it's a visual overhaul for your Arch Linux terminal. It intelligently wraps around your existing helper (`paru`, `yay`, or vanilla `pacman`) to provide:

  * **Gamification:** An RPG-style ranking system based on your installed packages ("Loot").
  * **Visual Feedback:** Replaces standard loading bars with "Waka-Waka" Pacman animations.
  * **Automation:** Built-in Garbage Collector (`-C`) and Lockfile Remover (`--unlock`).
  * **Safety First:** Sudo keep-alive mechanism prevents password prompt timeouts.

**Professional Note:** Under the hood, Pacsmart passes **all** flags directly to the backend. If a command works in `pacman` or `yay`, it works in Pacsmart.

-----

## 📸 Visual Preview

```text
  .--.   PACSMART v1.0
 / _.-'  (Initial Release)
 \  '-.  Automated & Informative
  '--'   

┌── PLAYER PROFILE ──────────────────────────────┐
│  User      : aldi                              │
│  System    : Arch Linux                        │
│  Engine    : paru                              │
├── STATS ───────────────────────────────────────┤
│  Rank      : ARCH WIZARD                       │
│  Loot      : 520 / 1000                        │
└────────────────────────────────────────────────┘

>>> MISSION START: EATING (REPO) >>>
[sudo] password for aldi: 
ᗧ C • • • • • • • ᗣ
```

-----

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🍒 **Arcade UI** | High-contrast, pixel-perfect terminal UI with headers and icons. |
| 🏆 **Rank System** | Level up from *Beginner* to *Legendary* as you install more packages. |
| ⚔️ **Universal Wrapper** | Supports `-S`, `-Rns`, `-Qdt`, and *every* other standard flag. |
| 🧹 **Auto-Clean** | dedicated `-C` flag to detect and remove orphan packages easily. |
| 🚑 **Medic Mode** | Fix `db.lck` errors instantly with `--unlock`. |
| ⏩ **Speedrun** | Skip animations with `--fast` for quick operations. |

-----

## 🚀 Installation Guide

Pacsmart is a standalone Bash script. You don't need to compile anything.

### Prerequisites

Ensure you have **Arch Linux** (or derivative) and at least one of these installed:

  * `pacman` (Default)
  * `yay` (Recommended)
  * `paru` (Recommended)

### Method 1: Quick Install (Recommended)

Copy and paste this block into your terminal to download and install automatically:

```bash
# 1. Download the script
curl -O https://raw.githubusercontent.com/aldiipratama/pacsmart/main/pacsmart

# 2. Give it execute permission
chmod +x pacsmart

# 3. Move to your binary path (Requires Sudo)
sudo mv pacsmart /usr/local/bin/

# 4. Verify installation
pacsmart --version
```

### Method 2: Manual / Git Clone

If you want to inspect the code or contribute:

```bash
git clone https://github.com/aldiipratama/pacsmart.git
cd pacsmart
chmod +x pacsmart
sudo cp pacsmart /usr/local/bin/
```

-----

### ⚡ Setup Aliases (The Pro Move)

To get the full "Arcade Experience", replace your standard commands with Pacsmart aliases.

Add the following lines to your shell configuration file (usually `~/.bashrc` or `~/.zshrc`):

```bash
# ~/.zshrc or ~/.bashrc

# Option A: Safety First (Use 'pac' keyword)
alias pac="pacsmart"

# Option B: Full Replacement (Override 'pacman')
# WARNING: This replaces the standard pacman command visually
alias pacman="pacsmart"
alias yay="pacsmart --use=yay"
alias paru="pacsmart --use=paru"
```

**Apply changes:**

```bash
source ~/.bashrc
# or
source ~/.zshrc
```

Now, just type `pac -S neovim` and enjoy the show\! 🍒

-----

### 🗑️ Uninstallation

If you want to remove Pacsmart (but why would you?):

```bash
sudo rm /usr/local/bin/pacsmart
rm ~/pkg-installed.txt  # Removes your high score/rank data
```

-----

## 🕹️ Usage Guide

Pacsmart uses a **"Hybrid Passthrough"** system. It has its own special flags, but also accepts everything else.

### 🍒 Main Quests

| Command | Action |
| :--- | :--- |
| `pacsmart -S <pkg>` | Install package (Auto-detects Repo/AUR). |
| `pacsmart -Syu` | Full System Upgrade (Level Up). |
| `pacsmart -Rns <pkg>` | Remove package + dependencies (Clean Uninstall). |

### ⚙️ Automation & Specials

| Command | Action |
| :--- | :--- |
| `pacsmart -C` | **Garbage Collector:** Find & remove orphans automatically. |
| `pacsmart --unlock` | **Medic:** Removes `/var/lib/pacman/db.lck` if stuck. |
| `pacsmart --fast` | **Speedrun:** Disable animations. |
| `pacsmart --simulate` | **Demo:** Show package info without installing. |

-----

## 🤝 Community & Contribution

We welcome "Player 2" to join the development\!

  * **Want to contribute code?** Read our [Contributing Guide](https://www.google.com/search?q=./CONTRIBUTING.md).
  * **Found a glitch/bug?** Create an issue using our [Issue Templates](https://www.google.com/search?q=.github/ISSUE_TEMPLATE/).
  * **Found a security exploit?** Please read our [Security Policy](https://www.google.com/search?q=./SECURITY.md) before posting publicly.
  * **Our Rules:** Play nice\! Read our [Code of Conduct](https://www.google.com/search?q=./CODE_OF_CONDUCT.md).

-----

## ❤️ Credits & Inspiration

This project stands on the shoulders of giants.

  * **[Arch Linux Pacman](https://wiki.archlinux.org/title/Pacman):** Specifically the legendary `ILoveCandy` config.
  * **[Yay](https://github.com/Jguer/yay) & [Paru](https://github.com/Morganamilo/paru):** The powerful AUR helpers backend.

-----

Made with ❤️ and ☕ by [Muhamad Rinaldi Agus Pratama](https://github.com/aldiipratama)
