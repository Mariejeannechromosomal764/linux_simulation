<div align="center">

# ⚡ Cyber Assassins
### Linux Terminal Simulator

[![License: MIT](https://img.shields.io/badge/License-MIT-bc8cff.svg?style=for-the-badge)](./LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-7ee787.svg?style=for-the-badge)](./CONTRIBUTING.md)

<br/>

**A fully interactive, browser-based Linux terminal simulator for cybersecurity students and beginners.**  
Practice 100+ real Linux commands with zero setup — no VM, no installation, no risk.

<br/>

[🚀 **Live Demo**](https://linux-simulation.netlify.app/) &nbsp;·&nbsp;
[📋 **Command List**](#-commands-reference) &nbsp;·&nbsp;
[🎨 **Themes**](#-themes) &nbsp;·&nbsp;
[🏆 **Practice Challenges**](./CHALLENGES.md) &nbsp;·&nbsp;
[🤝 **Contributing**](#-contributing)

<br/>

> 💡 **Tip for your repo:** record a short screen capture of the terminal in action (boot animation → running a few commands → switching themes), save it as `assets/demo.gif`, and it will automatically appear here.

</div>

---

## 📖 What Is This?

**Cyber Assassins** is a zero-dependency, fully client-side Linux terminal simulator that runs entirely in your browser. It is designed for:

- 🎓 **Cybersecurity students** learning Linux for the first time
- 🧠 **Beginners** who want to practice without breaking a real system
- 🏆 **CTF players** brushing up on command-line fundamentals
- 👩‍💻 **Developers** who want a quick Linux command reference

Everything runs in-memory in your browser. No data is sent anywhere. No installation needed. Just open and type.

---

## ✨ Features

### 🖥️ Terminal Experience
| Feature | Details |
|---|---|
| **100+ Commands** | Full coverage of navigation, files, permissions, processes, networking, and more |
| **Virtual Filesystem** | In-memory filesystem that mirrors real Linux structure (`/home`, `/etc`, `/var`, `/tmp`, etc.) |
| **Interactive nano Editor** | Full nano simulation with `Ctrl+O` save and `Ctrl+X` exit |
| **Command History** | Arrow keys navigate history, just like a real shell |
| **Tab Autocomplete** | Completes commands and filenames instantly |
| **Multiple Tabs** | Open multiple terminal sessions side by side |
| **Piping Support** | Basic pipe `|` between commands |
| **Redirection** | `>` and `>>` operators write to virtual files |

### 🔐 Real Permission System
- `chmod 755`, `chmod +x`, symbolic and numeric modes
- `chown` / `chgrp` restricted to root
- `sudo` and `sudo su` with password authentication
- Root prompt changes from `$` to `#`
- `Permission denied` errors on restricted paths

### 👤 User & Session Simulation
- Default user: `student` · password: `toor` (Kali default)
- `sudo su` → prompts for password → switches to root
- `passwd` → interactive password change flow
- `exit` from root → returns to student
- `whoami`, `id`, `groups` return realistic output

### 📚 Educational Layer
- **💡 Inline Tips** — contextual tips appear after commands (40% chance, non-spammy)
- **📋 Command Cheatsheet** — full sidebar with all 100+ commands, click any to insert
- **🗂 File Explorer** — visual sidebar showing the virtual filesystem tree
- **⚠️ Danger Zone Warnings** — `rm -rf /` shows a real-world impact warning
- **📖 Man Pages** — `man <command>` shows simplified, readable manual pages

### 🎨 Customization
- **8 Built-in Themes** — GitHub Dark, Matrix, VS Code, Kali Red, Midnight, Hacker, Dracula, Light
- **Custom Color Picker** — change background, prompt, text, and accent colors live
- **Font Size Control** — increase/decrease with `+`/`−` buttons
- **Collapsible Panels** — sidebar and cheatsheet can be toggled

---

## 🚀 Getting Started

### Option 1 — Open Directly (Recommended)
```bash
# Just open index.html in any browser — no server needed
open index.html
```

### Option 2 — GitHub Pages
Fork this repo → Go to **Settings → Pages** → Set source to `main` branch → Done.

### Option 3 — Local Server
```bash
git clone https://github.com/Shivam-pro-hacker/linux_simulation.git
cd cyber-assassins


# Node.js
npx serve .

# Then open: http://localhost:8080
```

---

## 📋 Commands Reference

### 🗂 Navigation
| Command | Description |
|---|---|
| `pwd` | Print working directory |
| `ls` | List directory contents |
| `ls -la` | Detailed listing with hidden files |
| `cd <dir>` | Change directory |
| `cd ..` | Go up one level |
| `cd ~` | Go to home directory |
| `cd -` | Go to previous directory |
| `tree` | Show directory tree |

### 📁 File Operations
| Command | Description |
|---|---|
| `touch file` | Create empty file |
| `mkdir dir` | Create directory |
| `mkdir -p a/b/c` | Create nested directories |
| `rm file` | Remove file |
| `rm -r dir` | Remove directory recursively |
| `rm -rf dir` | Force remove (shows danger warning) |
| `cp src dst` | Copy file |
| `cp -r src dst` | Copy directory |
| `mv src dst` | Move or rename |
| `ln -s src link` | Create symbolic link |

### 👁 View & Edit Files
| Command | Description |
|---|---|
| `cat file` | Display file contents |
| `cat -n file` | Display with line numbers |
| `less file` | Paginate through file |
| `head file` | First 10 lines |
| `head -n 20 file` | First N lines |
| `tail file` | Last 10 lines |
| `tail -f file` | Follow log file |
| `wc -l file` | Count lines |
| `wc -w file` | Count words |
| `nano file` | Open interactive editor |
| `echo "text"` | Print text |
| `echo "text" > file` | Write to file |
| `echo "text" >> file` | Append to file |

### 🔐 Permissions
| Command | Description |
|---|---|
| `chmod 755 file` | Set permissions (numeric) |
| `chmod +x file` | Add execute permission |
| `chmod u+r file` | Add user read permission |
| `chmod o-w file` | Remove others write |
| `chown user file` | Change file owner (root only) |
| `chgrp group file` | Change file group |
| `umask` | Show default permission mask |

### 🔍 Search & Find
| Command | Description |
|---|---|
| `grep "pattern" file` | Search for pattern in file |
| `grep -r "pattern" .` | Recursive search |
| `grep -i "pattern" file` | Case-insensitive search |
| `grep -n "pattern" file` | Show line numbers |
| `grep -v "pattern" file` | Invert match |
| `find . -name "*.txt"` | Find by filename |
| `find . -type f` | Find files only |
| `find . -type d` | Find directories only |
| `locate filename` | Quick file search |
| `which command` | Locate a command |
| `whereis command` | Find binary, man, source |

### ⚙️ System Info
| Command | Description |
|---|---|
| `whoami` | Current username |
| `id` | User ID and group memberships |
| `groups` | List user groups |
| `uname -a` | Full system information |
| `hostname` | Machine hostname |
| `uptime` | System uptime and load |
| `date` | Current date and time |
| `cal` | Calendar |
| `df -h` | Disk space usage |
| `du -h` | Directory size |
| `lsblk` | Block devices |
| `env` | Environment variables |

### 🔄 Processes
| Command | Description |
|---|---|
| `ps` | Current shell processes |
| `ps aux` | All running processes |
| `top` | Live process monitor |
| `kill <PID>` | Send signal to process |
| `kill -9 <PID>` | Force kill |
| `jobs` | Background jobs |

### 👤 Users & Auth
| Command | Description |
|---|---|
| `sudo <command>` | Run command as root |
| `sudo su` | Switch to root shell |
| `su <user>` | Switch user |
| `passwd` | Change your password |
| `useradd <user>` | Create new user (root) |
| `adduser <user>` | Create user interactively (root) |
| `userdel <user>` | Delete user (root) |

### 🌐 Network
| Command | Description |
|---|---|
| `ping host` | Test connectivity |
| `ping -c 4 host` | Ping 4 times |
| `ifconfig` | Network interfaces |
| `ip addr show` | IP addresses (modern) |
| `ip route` | Routing table |
| `netstat` | Network connections |
| `nmap host` | Port scan (simulated) |
| `nmap -sV host` | Service version scan |
| `ssh user@host` | Remote login |
| `curl url` | Fetch URL |
| `wget url` | Download file |

### 📦 Archive & Compression
| Command | Description |
|---|---|
| `tar -czf archive.tgz dir/` | Create compressed archive |
| `tar -xzf archive.tgz` | Extract archive |
| `tar -tzf archive.tgz` | List archive contents |
| `zip -r file.zip dir/` | Create zip |
| `unzip file.zip` | Extract zip |
| `gzip file` | Compress with gzip |
| `gunzip file.gz` | Decompress gzip |

### 🔤 Text Processing
| Command | Description |
|---|---|
| `sort file` | Sort lines alphabetically |
| `sort -r file` | Reverse sort |
| `sort -n file` | Numeric sort |
| `uniq file` | Remove consecutive duplicates |
| `diff file1 file2` | Show differences |
| `cut -d: -f1 file` | Cut by delimiter |
| `wc file` | Word, line, byte count |
| `strings file` | Extract readable strings |

### 🛡️ Kali Security Tools (Simulated)
| Command | Description |
|---|---|
| `nmap` | Network mapper |
| `sqlmap` | SQL injection tester |
| `nikto` | Web server scanner |
| `john` | Password cracker |
| `hydra` | Login brute-forcer |
| `hashcat` | Hash cracker |
| `metasploit` / `msfconsole` | Exploit framework |
| `aircrack-ng` | WiFi security tool |
| `wireshark` | Packet analyzer (GUI note) |

### 🔧 Developer Tools (Simulated)
| Command | Description |
|---|---|
| `git init/status/log/clone` | Git version control |
| `python3 / python` | Python interpreter info |
| `pip install` | Python package manager |
| `apt install/update` | Package manager |
| `bash script.sh` | Run shell script |
| `crontab -l / -e` | Manage cron jobs |
| `systemctl status` | Service management |
| `journalctl` | System logs |

---

## 🎨 Themes

| Theme | Description |
|---|---|
| **GitHub Dark** | Clean dark with green accent (default) |
| **Matrix** | Classic green-on-black hacker look |
| **VS Code** | Familiar VS Code dark palette |
| **Kali Red** | Deep red inspired by Kali Linux |
| **Midnight** | Dark navy with purple accents |
| **Hacker** | Pure green terminal |
| **Dracula** | Popular Dracula color scheme |
| **Light** | Clean white theme for bright environments |

Custom colors: pick any hex for background, prompt, text, and accent.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Tab` | Autocomplete command or filename |
| `↑` / `↓` | Navigate command history |
| `Ctrl + L` | Clear terminal screen |
| `Ctrl + C` | Cancel current input |
| `Ctrl + O` *(in nano)* | Save file |
| `Ctrl + X` *(in nano)* | Exit nano editor |

---

## 🧠 Learning Path (Suggested Order)

```
1. Navigation       → pwd, ls, cd, tree
2. File Basics      → touch, mkdir, cat, echo, nano
3. File Management  → cp, mv, rm, ln
4. Permissions      → chmod, chown, sudo, su
5. Search & Filter  → grep, find, locate, which
6. Text Processing  → sort, uniq, diff, wc, head, tail
7. System Info      → ps, top, uname, df, env
8. Networking       → ping, ifconfig, nmap, ssh
9. Archive          → tar, zip, gzip
10. Security Tools  → nmap, sqlmap, nikto, metasploit
```

📘 Want guided, hands-on exercises instead? Work through **[CHALLENGES.md](./CHALLENGES.md)** — 10 progressive levels from "who am I?" to a full recon workflow, each with hidden solutions.

---

## 📁 Project Structure

```
cyber-assassins/
│
├── index.html          ← Single-file application (entire simulator)
│   ├── <style>         ← All CSS with CSS custom properties for theming
│   └── <script>        ← JavaScript modules:
│       ├── Virtual Filesystem (FS object)
│       ├── State management
│       ├── 100+ Command implementations
│       ├── Tab autocomplete engine
│       ├── Nano editor simulation
│       ├── sudo/su auth flow
│       ├── Theme system
│       └── Boot animation
│
├── CHALLENGES.md        ← 10 guided practice levels with solutions
├── CONTRIBUTING.md      ← How to add new commands
├── LICENSE              ← MIT License
├── .gitignore           ← Standard ignores for editors/OS files
└── README.md            ← This file
```

**Design decision:** The entire simulator lives in a single `index.html` file. This means:
- ✅ Zero dependencies
- ✅ Works offline
- ✅ One file to share, host, or fork
- ✅ No build step required

---

## 🤝 Contributing

Contributions are welcome! Here's how to add a new command:

```javascript
// In the COMMANDS object inside index.html:
mycommand(args) {
  // args = array of arguments passed to the command
  if (!args.length) return [cl('mycommand: missing argument', 'out-error')];
  
  const target = resolvePath(args[0]);  // resolve path
  
  return [
    cl('Output line 1', 'out-normal'),
    cl('Output line 2', 'out-success'),
  ];
},
```

**Color classes available:**
| Class | Color |
|---|---|
| `out-normal` | Default text |
| `out-success` | Green (good output) |
| `out-error` | Red (errors) |
| `out-warn` | Yellow (warnings) |
| `out-info` | Blue (informational) |
| `out-accent` | Purple (highlights) |
| `out-dim` | Grey (secondary text) |
| `out-dir` | Blue bold (directories) |
| `out-exec` | Green (executable files) |

### Adding Education Tips
```javascript
// In the TIPS object:
mycommand: 'Your tip about what this command does and when to use it.',
```

### Steps to Contribute
1. Fork the repository
2. Create a branch: `git checkout -b feature/add-command-xyz`
3. Make your changes in `index.html`
4. Test thoroughly in a browser
5. Submit a Pull Request with a description of what you added

---

## 🛡️ Security & Legal Notice

> This simulator is for **educational purposes only**.
>
> All security tool commands (`nmap`, `sqlmap`, `hydra`, `metasploit`, etc.) are **fully simulated** — they produce realistic-looking output but perform **zero real network activity, scanning, or exploitation**.
>
> In the real world, running security tools against systems you do not own or have explicit written permission to test is **illegal**. Always practice in authorized environments such as HackTheBox, TryHackMe, or your own lab.

---

## 📊 Stats

- **100+** Linux commands implemented
- **8** built-in color themes
- **0** dependencies
- **0** network requests (fully offline capable)
- **1** file to rule them all

---

## 📜 Changelog

### v1.0.0 (2026)
- Initial release
- 100+ commands implemented
- 8 themes + custom color picker
- Virtual filesystem with full CRUD
- Interactive nano editor
- sudo/su authentication flow
- Tab autocomplete + history navigation
- Educational tips system
- Multiple terminal tabs
- Boot animation sequence
- Sidebar file explorer + cheatsheet panel

---

## 📄 License

```
MIT License — Copyright (c) 2026 Shivam

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software to use, copy, modify, merge, publish, and
distribute, subject to the conditions in the LICENSE file.
```

See [LICENSE](./LICENSE) for full text.

---

<div align="center">

**Made with ❤️ by [Shivam](https://github.com/shivam-pro-hacker)**

*If this helped you learn Linux, please give it a ⭐ — it helps others find it too!*

[![GitHub stars](https://img.shields.io/github/stars/shivam-pro-hacker/linux_simulation?style=social)](https://github.com/Shivam-pro-hacker/linux_simulation)

</div>
