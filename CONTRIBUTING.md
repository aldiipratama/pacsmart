# 🎮 Join the Dev Guild (Contributing Guide)

Thank you for your interest in becoming **Player 2** in the development of Pacsmart!

Pacsmart is an Open Source project, and we greatly appreciate every “Loot” (contribution) you bring, whether it's bug fixes (glitches), new features (DLC), or simply typo corrections in the documentation.

Here's a guide to help your contributions merge smoothly.

## 🛠️ Setup Gear (Preparation)

1.  **Fork this Repository:** Click the `Fork` button in the top right corner.
2.  **Clone to Local:**
```bash
    git clone [https://github.com/username-kamu/pacsmart.git](https://github.com/username-kamu/pacsmart.git)
    cd pacsmart
```
3.  **Create a New Branch:** Don't code in `main`! Create a branch according to your mission.
```bash
    git checkout -b feature/CoolFeatureName
    # or
    git checkout -b fix/AnnoyingBug
```

## 📜 Coding Guidelines (Rules of Play)

Pacsmart is written in **Bash Script**. To keep the code neat and readable, follow these rules:

* **Indentation:** Use 4 spaces (not tabs).
* **Variables:** Use `UPPER_CASE` for global variables and `snake_case` for local variables.
* **Functions:** Give functions descriptive names, for example: `smart_install`, `detect_aur_helper`.
* **Colors:** Use predefined color variables (`${C_PACMAN}`, `${C_INKY}`, etc.) to maintain a consistent theme.
* **Safety First:** Always quote variables (`“$VAR”`) to avoid space errors.

## 🚀 Submitting a Pull Request (Tu

# 🎮 Join the Dev Guild (Contributing Guide)

Thank you for your interest in becoming **Player 2** in the development of Pacsmart!

Pacsmart is an Open Source project, and we greatly appreciate every “Loot” (contribution) you bring, whether it's bug fixes (glitches), new features (DLC), or simply typo corrections in the documentation.

Here's a guide to help your contributions merge smoothly.

## 🛠️ Setup Gear (Preparation)

1.  **Fork this Repository:** Click the `Fork` button in the top right corner.
2.  **Clone to Local:**
```bash
    git clone [https://github.com/username-kamu/pacsmart.git](https://github.com/username-kamu/pacsmart.git)
    cd pacsmart
```
3.  **Create a New Branch:** Don't code in `main`! Create a branch according to your mission.
```bash
    git checkout -b feature/CoolFeatureName
    # or
    git checkout -b fix/AnnoyingBug
```

## 📜 Coding Guidelines (Rules of Play)

1.  **Test Your Code:** Make sure the script runs smoothly in your terminal. Try installing, removing, and updating packages.
2.  **Commit Changes:** Use clear commit messages (see the bottom of the main README for examples).
```bash
    git commit -m “feat: add new spaceship mode”
```
3.  **Push to Your Fork:**
```bash
    git push origin feature/CoolFeatureName
```
4.  **Open a Pull Request (PR):** Open GitHub, and click “Compare & pull request”.
5.  **Describe the PR:** Explain what you changed. Include screenshots if there are visual changes in the Arcade UI.

## 🤝 Credits
Every contributor whose PR is accepted will automatically be considered a **Member** and your name will be immortalized in Git history!

Happy Hacking! 🍒
