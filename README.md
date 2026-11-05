# 🚀 awesome-cli-productivity  

![Stars](https://img.shields.io/github/stars/your-username/awesome-cli-productivity?style=flat)  
A curated collection of powerful **bash** / **zsh** aliases and functions that super‑charge your terminal workflow. Designed for developers who spend a lot of time in the shell, this repo gives you ready‑to‑use shortcuts for Git, Docker, npm, system monitoring, and more—so you can focus on code, not typing.

---  

## 📖 What’s Inside?

| Category | Alias / Function | Description |
|----------|------------------|-------------|
| **Git** | `gco` | `git checkout` |
| | `gcm` | `git commit -m` |
| | `gpr` | `git pull --rebase && git push` |
| **Docker** | `dps` | `docker ps --format "table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Ports}}"` |
| | `drmi` | `docker rmi $(docker images -q -f "dangling=true")` |
| **Node** | `ncu` | `npm-check-updates -u && npm install` |
| | `nr` | `npm run` (shows scripts) |
| **System** | `meminfo` | `free -h && vmstat -s` |
| | `cpuinfo` | `lscpu` |
| **Search** | `ff` | `function ff(){ find . -type f -iname "*$1*" }` |
| **Navigation** | `..` | `cd ..` |
| | `...` | `cd ../..` |
| **GitHub** | `ghpr` | `gh pr create --fill` (requires GitHub CLI) |
| **Custom** | `mkcd` | `function mkcd(){ mkdir -p "$1" && cd "$1"; }` |

All aliases are safe, POSIX‑compatible, and can be loaded in either **bash** or **zsh**.

---  

## 📦 Installation  

### 1. Clone the repository  

```bash
git clone https://github.com/your-username/awesome-cli-productivity.git
```

### 2. Source the file  

Add the following line to your `~/.bashrc`, `~/.zshrc`, or any shell startup file you use:

```bash
# Load awesome-cli-productivity
source "$HOME/awesome-cli-productivity/awesome-cli.sh"
```

> **Tip:** If you keep the repo in a different location, update the path accordingly.

### 3. Reload your shell  

```bash
source ~/.bashrc   # or source ~/.zshrc
```

You’re ready! All aliases and functions are now available.

---  

## 🛠️ Usage  

Just type the alias or function name as you would any command.

```bash
# Git shortcuts
gco main          # checkout the main branch
gcm "Fix bug #42" # commit with a message

# Docker shortcuts
dps                # pretty list of containers
drmi               # clean up dangling images

# Node workflow
ncu                # update all npm dependencies
nr                 # list npm scripts

# System info
meminfo            # show memory usage
cpuinfo            # show CPU details

# Quick navigation
...                # go up two directories
mkcd new_folder    # create and enter a new folder
```

---  

## 🎯 Examples  

### 1. One‑liner to clean up your repo  

```bash
# Remove all untracked files, dangling Docker images, and npm cache
git clean -fdx && drmi && npm cache clean --force
```

### 2. Fast GitHub PR creation  

```bash
# After making changes on a feature branch
ghpr
```

*(Requires the official GitHub CLI: `brew install gh` or `sudo apt install gh`)*

### 3. Search for a file anywhere in the project  

```bash
ff config.yml   # finds any file whose name contains "config.yml"
```

---  

## 🤝 Contributing  

Contributions are welcome! If you have an alias or function that you find indispensable, feel free to:

1. Fork the repo  
2. Add your alias/function to `awesome-cli.sh` (keep the same formatting)  
3. Write a short description in the table above (in `README.md`)  
4. Submit a Pull Request  

Please ensure your additions are **POSIX‑compatible**, have **no side effects**, and include a brief comment describing the purpose.

---  

## 📜 License  

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---  

## 🙏 Support This Project  

If this helped you, consider buying me a coffee! ☕  

[![PayPal](https://img.shields.io/badge/PayPal-Donate-blue.svg)](https://www.paypal.com/paypalme/manhcuong0810)  
PayPal: manhcuong0810@gmail.com  

---  

Happy hacking! 🎉  