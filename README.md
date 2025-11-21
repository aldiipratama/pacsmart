# 🍒 Pacsmart

> **The Ultimate Arcade Wrapper for Arch Linux Package Managers.**
>
> Transform your boring `pacman`, `yay`, or `paru` output into an engaging, gamified, and pixel-perfect arcade experience.

-----

## 🎮 What is Pacsmart?

**Pacsmart** is not just a wrapper; it's a visual overhaul for your Arch Linux terminal. It intelligently wraps around your existing helper (`paru`, `yay`, or vanilla `pacman`) to provide:

  * **Gamification:** An RPG-style ranking system based on your installed packages ("Loot").
  * **Smart Batching:** Automatically separates Official Repo and AUR packages for safer, sequential installation.
  * **Visual Feedback:** Replaces standard loading bars with "Waka-Waka" Pacman animations.
  * **Automation:** Built-in Garbage Collector (`-C`) and Lockfile Remover (`--unlock`).
  * **Zero Config:** Automatically detects your installed helper.

**Professional Note:** Under the hood, Pacsmart passes **all** flags directly to the backend. If a command works in `pacman` or `yay`, it works in Pacsmart.

-----

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🍒 **Arcade UI** | High-contrast, pixel-perfect terminal UI with headers and icons. |
| 🏆 **Rank System** | Level up from *Beginner* to *Legendary* as you install more packages. |
| ⚔️ **Universal Wrapper** | Supports `-S`, `-Rns`, `-Qdt`, and *every* other standard flag. |
| 🧹 **Auto-Clean** | dedicated `-C` flag to detect and remove orphan packages easily. |
| 🚑 **Medic Mode** | Fix `db.lck` errors instantly with `--unlock`. |
| 🛡️ **Safety First** | Sudo keep-alive mechanism prevents password prompt timeouts/blank screens. |
| ⏩ **Speedrun** | Skip animations with `--fast` for quick operations. |

-----

## 📸 Visual Preview

```bash
  .--.   PACSMART v19.0
 / _.-'  (The Perfect Hybrid)
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

## 🕹️ Usage Guide

Pacsmart uses a **"Hybrid Passthrough"** system. It has its own special flags, but also accepts everything else.

### 🍒 Main Quests (Basic Usage)

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
| `pacsmart --fast` | **Speedrun:** Disable animations for faster execution. |
| `pacsmart --simulate` | **Demo:** Show package info without installing. |

### 📖 Universal Compatibility

Do you need to use specific flags like `--overwrite` or `--asdeps`? Just type them\!

```bash
# Example: Force overwrite a file
pacsmart -Syu --overwrite "*"

# Example: Install as dependency
pacsmart -S --asdeps libsomething
```

-----

## 🏆 Ranking System

Your rank is determined by the number of packages installed (`Loot`) tracked in `~/pkg-installed.txt`.

  * **Beginner:** 0 - 50 pkgs
  * **Ricer:** 50 - 200 pkgs
  * **Veteran:** 200 - 500 pkgs
  * **Arch Wizard:** 500 - 1000 pkgs
  * **LEGENDARY:** 1000+ pkgs

-----

## 🤝 Contributing

Feel free to fork, open issues, or submit PRs. Whether it's adding new "Skins", optimizing the code, or fixing bugs.

1.  Fork it
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## ❤️ Credits & Inspiration

This project stands on the shoulders of giants. While the Arcade/RPG concept is original to Pacsmart, it is heavily inspired by:

* **[Arch Linux Pacman](https://wiki.archlinux.org/title/Pacman):** Specifically the legendary `ILoveCandy` Easter egg configuration that inspired the "Waka-Waka" visual theme.
* **[Yay](https://github.com/Jguer/yay) & [Paru](https://github.com/Morganamilo/paru):** The powerful AUR helpers that serve as the backend engines for this wrapper.
* **The Ricing Community:** For proving that terminal tools don't have to be boring.

-----

## Support

For support, email paldi0013@gmail.com.
