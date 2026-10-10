<div align="center">

# 🚀 MEM-CLEAN 🧹
## ⚡ Ultimate System Performance Monitor & Memory Optimizer ⚡

<img src="https://img.shields.io/badge/Made%20with-Python-3776ab.svg?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Platform-Linux-green.svg?style=for-the-badge&logo=linux&logoColor=white" alt="Linux">
<img src="https://img.shields.io/badge/Status-Active-brightgreen.svg?style=for-the-badge" alt="Active">
<img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License">

### 🎨 **CREATED BY '[WickedSyntax](https://github.com/WickedSyntax)' WITH ❤️** 🎨

---

*🎯 A badass Linux system monitoring and optimization tool that provides real-time system statistics and powerful cleanup capabilities! 🎯*

</div>

---
<div align="center">
  
## 🌟 FEATURES THAT WILL BLOW YOUR MIND 🌟
</div>
<div align="center">
<table cellpadding="0" cellspacing="0" style="border-collapse: collapse; border: none;">
<tr>
<td align="center" valign="top" style="padding: 10px; border: none;">

### 🧠 **MEMORY MONITORING**
 - 📊 Real-time RAM usage percentage & stats
 - 💡 Available memory tracking
 - 🧹 Memory cache clearing superpowers
 - 🔥 Lightning-fast performance analysis

</td>
<td align="center" valign="top" style="padding: 10px; border: none;">

### ⚡ **CPU MONITORING** 
- 🎯 CPU usage percentage tracking
- 🏗️ Core count & frequency information
- 👑 Top memory-consuming process hunter
- 🚀 Real-time performance insights

</td>
<td align="center" valign="top" style="padding: 10px; border: none;">

### 💾 **STORAGE MONITORING**
- 📈 Disk usage percentage & statistics  
- 🆓 Free space tracking
- 🔍 Large file detection & reporting
- 📁 Smart storage analysis

</td>
<td align="center" valign="top" style="padding: 10px; border: none;">

### 🧹 **SYSTEM CLEANUP BEAST**
- 🗑️ Memory cache clearing (sudo required)
- 🧽 Temporary file obliteration (skips in-use & recent files)
- 🎯 Large file identification for review
- 🚀 Full system optimization

</td>
<td align="center" valign="top" style="padding: 10px; border: none;">

### 📡 **LIVE MONITOR**
- 🖥️ Real-time dashboard (RAM, SWAP, CPU, DISK, PSI pressure)
- 📈 RAM usage history sparkline
- 🤖 Auto-free: clears page cache when RAM crosses your threshold
- ⏱️ Configurable refresh interval, threshold and cooldown

</td>
</tr>
</table>
</div>


---
  
## 🎮 HOW TO USE THIS BEAST 🎮


### 🎪 **Interactive Mode (The Fun Way!)** 🎪
```bash
🎯 ./MEM-CLEAN
# or the cool shortcut
🚀 ./mem-clean
```

### 💻 **Command Line Ninja Mode** 💻
```bash
📋 ./MEM-CLEAN --help                 # 📖 Show the sacred help scrolls
📊 ./MEM-CLEAN --status               # 🎯 Quick system status check
🧹 ./MEM-CLEAN --clean                # 💨 Clear that memory cache!
🔍 ./MEM-CLEAN --large-files          # 🕵️ Hunt down those chunky files
🗑️ ./MEM-CLEAN --temp-clean           # 🧽 Preview/confirm temp cleanup
👑 ./MEM-CLEAN --processes            # 🔥 Show the memory hogs
📡 ./MEM-CLEAN --watch                # 🖥️ Live monitor + auto-free at 85% RAM
📡 ./MEM-CLEAN --watch 5 --threshold 90 --cooldown 120  # 🎛️ Custom live monitor
🚫 ./MEM-CLEAN --watch --no-auto-free # 👀 Monitor only, never touch the cache

# 🎛️ Advanced Wizardry Options
🧙‍♂️ ./MEM-CLEAN --large-files --directory /path/to/scan --size 50 --limit 10
🧙‍♂️ ./MEM-CLEAN --temp-clean --dry-run          # Preview only
🧙‍♂️ ./MEM-CLEAN --temp-clean --yes --min-age 3  # Non-interactive, files ≥ 3 days
```

---

## 📦 REQUIREMENTS & SETUP 📦

### 🛠️ **What You Need:**
- 🐍 Python 3.6+ (The snake that rules them all)
- 📊 psutil library (`pip3 install psutil`)
- 🐧 Linux operating system (Tux approved!)
- 👑 sudo privileges (For the memory cache clearing magic)

### 🚀 **Installation Steps:**
```bash
1️⃣ git clone <this-awesome-repo> || download MEM-CLEAN folder
2️⃣ chmod +x MEM-CLEAN mem-clean  # 🔐 Grant execution powers
3️⃣ pip3 install psutil           # 📊 Install the monitoring magic
4️⃣ ./MEM-CLEAN                   # 🎉 Launch and enjoy!
```

### 🤖 **Auto-Free Setup (for `--watch`):**
The live monitor can automatically drop the page cache when RAM usage
crosses your threshold. For that it needs non-interactive sudo:
```bash
sudo -v              # 🎫 Cache your sudo ticket (lasts ~15 min)
./MEM-CLEAN --watch  # 📡 Monitor + auto-free enabled
# or simply run it as root:
sudo ./MEM-CLEAN --watch
```
Set `NO_COLOR=1` to disable ANSI colors (useful for logs/pipes).

---

## 🛡️ SAFETY FIRST! 🛡️

<div align="center">

| 🔒 Safety Feature | 📝 Description |
|-------------------|----------------|
| 🕵️ **Non-Destructive Scanning** | Read-only large file detection |
| 🧹 **Safe Cleanup** | Only touches standard temp locations; skips in-use & recent files (min age enforced) |
| ✋ **Confirmation Required** | Temp cleanup asks before deleting (or needs `--yes` when non-interactive) |
| 👀 **Process Monitoring** | No termination capabilities |
| 🤖 **Bounded Auto-Free** | Live monitor auto-free has a cooldown and reports exactly what it released |
| 🚨 **Error Handling** | Graceful permission issue handling, proper exit codes |

</div>

---

## 🎪 INTERACTIVE MENU - THE CONTROL CENTER 🎪

<div align="center">

| 🎯 Option | 🎪 Action | 📝 Description |
|-----------|-----------|----------------|
| **1️⃣** | 📊 **System Status** | Display RAM, SWAP, CPU, PSI and storage stats |
| **2️⃣** | 🧹 **Clear Memory Cache** | Free up system memory (sudo needed) |
| **3️⃣** | 🔍 **Find Large Files** | Hunt files above size threshold |
| **4️⃣** | 🗑️ **Clean Temp Files** | Remove temp & cache files (asks for confirmation) |
| **5️⃣** | 👑 **Top Memory Hogs** | List processes eating your RAM |
| **6️⃣** | 📡 **Live Monitor** | Real-time dashboard + auto-free (Ctrl+C to stop) |
| **7️⃣** | 🚀 **Full System Cleanup** | Complete optimization blast |
| **0️⃣** | 👋 **Exit** | Say goodbye (but why would you?) |

</div>

---

## 🎨 SCREENSHOTS & EXAMPLES 🎨

### 🖥️ **System Status Display**
```
═══════════════════ SYSTEM STATUS ═══════════════════
2026-10-10 13:16:29  ·  uptime 00:40:13

🧠 MEMORY
   RAM   ████████████████▋░░░░░░░░░░░  59.0%  8.6 GB / 14.6 GB  (avail 6.0 GB)
   SWAP  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0.0%  972.0 KB / 4.0 GB
   PSI   memory pressure avg10 = 0.00  (0=idle, 100=stalled)

⚡ CPU
   █▌░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   5.0%  16 cores  load 3.17 3.09 2.46

💾 STORAGE
   ████████▊░░░░░░░░░░░░░░░░░░░░░░░░  31.2%  138.1 GB / 466.3 GB  (free 304.4 GB)
```

### 📡 **Live Monitor (`--watch`)**
```
╭─ MEM-CLEAN · LIVE MONITOR · 13:16:42 ─────────────────────────────────────────╮
│ RAM   ████████████████▋░░░░░░░░░░░  59.0%  8.6 GB/14.6 GB avail 6.0 GB       │
│ SWAP  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0.0%  972.0 KB/4.0 GB                   │
│ CPU   █████████████▍░░░░░░░░░░░░░░░  33.2%  16 cores  load 2.83 3.02         │
│ DISK  ████████▊░░░░░░░░░░░░░░░░░░░░  31.2%  free 304.4 GB                    │
│ PSI   memory pressure avg10 = 0.00                                            │
│                                                                                │
│ TOP MEMORY                                                                     │
│     18463    7.7%    0.0%  QtWebEngineProcess                                  │
│      3287    6.5%    0.0%  clamd                                               │
│                                                                                │
│ RAM HISTORY last 120 samples                                                   │
│   ▁▂▃▅▆▅▄▃▂▁▁▂▄▆█▇▅▄▃▂▁▂▄▆█▇▆▄▂▁▂▄▆█▇▆▄▂▁▂▄▆█▇▆▄▂▁▂▄▆█▇▆▄▂▁▂▄▆█▇▆▄▂▁▂▄▆█▆▄▂ │
╰────────────────────────────────────────────────────────────────────────────────╯
 Ctrl+C to stop · auto-free at ≥85% RAM, cooldown 60s
```

### 📁 **Large Files Detection**
```
📁 LARGE FILES DETECTED:
      Size  File Path
──────────────────────────────────────────────────────────────
    7.2 GB  ~/Downloads/huge-file.gguf
    3.6 GB  ~/Downloads/big-model.gguf
  512.0 MB  ~/Downloads/linux-distro.iso
```


---

## 🤝 CONTRIBUTING 🤝

Want to make this tool even more awesome? 🎉

1. 🍴 Fork this bad boy
2. 🌟 Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. 💫 Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. 🚀 Push to the branch (`git push origin feature/AmazingFeature`)
5. 🎁 Open a Pull Request

---

## 📜 LICENSE 📜

<div align="center">

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Free to use, modify, and distribute! 🎉**

</div>

---

## 🌟 SHOW SOME LOVE 🌟

<div align="center">

If this tool saved your system (and your sanity), consider:

⭐ **Starring this repo**  
🐦 **Sharing it with friends**  
💝 **Contributing improvements**  
☕ **Buying me a coffee** (just kidding, stars are enough!)

---

### 🎯 **Made with 💖 by [WickedSyntax](https://github.com/WickedSyntax)** 🎯
### 🚀 **"Making Linux systems run like rockets since 2024!"** 🚀

<img src="https://media.giphy.com/media/3o7aD2saalBwwftBIY/giphy.gif" width="200">

---

**🎪 Happy System Monitoring! 🎪**

</div>
