# 🎮 Play Games in Termux

> **By @Lumiquiver**

This guide covers how to play various types of games in **Termux**, including text-based games, emulators, graphical games, and online multiplayer options.

---

## 📜 Table of Contents
- [1. Text-Based Games (CLI)](#1-text-based-games-cli)
- [2. Retro Games (Emulators)](#2-retro-games-emulators)
- [3. Graphical Games (X11)](#3-graphical-games-x11)
- [4. Android Games via Termux (Steam & Wine)](#4-android-games-via-termux-steam--wine)
- [5. Online Games via SSH/Telnet](#5-online-games-via-sshtelnet)

---

## 1️⃣ Text-Based Games (CLI)
You can install and play classic **terminal-based games** using the following commands:

### 🎲 Rogue-like & ASCII Games
```bash
pkg install nethack
pkg install bsdgames   # Includes tetris, snake, hangman, etc.
pkg install ninvaders  # ASCII Space Invaders
pkg install moon-buggy # Drive a buggy on the moon
pkg install 2048-cli   # 2048 puzzle game
```
Run any game by typing its name, e.g., `nethack`.

---

## 2️⃣ Retro Games (Emulators)
Play classic games using emulators (you need to provide your own ROMs):

### 🎮 Install Emulators:
```bash
pkg install retroarch  # Multi-system emulator
pkg install mgba       # Game Boy Advance Emulator
pkg install fceux      # NES Emulator
```
Launch them by typing their name, e.g., `mgba`.

---

## 3️⃣ Graphical Games (X11)
To play GUI-based games, install an **X11 server** (like **XServer XSDL**) and enable graphics in Termux.

### 📌 Setup X11:
```bash
pkg install x11-repo
pkg install x11-utils xorg-xdpyinfo xorg-xrandr
export DISPLAY=:1
```

### 🕹️ Available Graphical Games:
```bash
pkg install dosbox      # DOS games emulator
pkg install quake       # Quake 1/2/3
pkg install openarena   # Quake 3 Clone
pkg install freeciv     # Civilization Clone
pkg install wesnoth     # Turn-based strategy game
```

Launch them using `DISPLAY=:1`.

---

## 4️⃣ Android Games via Termux (Steam & Wine)
You can run **PC Games** on Android using **Proot, Wine, and Steam**.

### ⚙️ Setup:
```bash
pkg install proot-distro
proot-distro install ubuntu
proot-distro login ubuntu
apt install wine
wine somegame.exe
```

May require **Box86/Box64** for better compatibility.

---

## 5️⃣ Online Games via SSH/Telnet
You can play **MUDs, Chess, and other online games** via SSH or Telnet:

### 🌐 Multiplayer Games:
```bash
ssh nethack@nethack.alt.org  # Public Nethack Server
ssh freechess.org            # FreeChess.org
```
Or play **classic MUD games**:
```bash
telnet alteraeon.com 3010
```

---

## 🎯 Conclusion
Termux is not just for hacking & development—it’s also a **gaming powerhouse**! Whether you love **classic ASCII games, retro emulators, or even full PC games**, there’s something for everyone. 🚀

Happy gaming! 🎮😃

---

## 📢 Credits
Maintained by **@Lumiquiver**.

Feel free to contribute by opening issues and pull requests! 🛠️

