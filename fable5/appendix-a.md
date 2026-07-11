# Appendix A — Command Reference

*Every command in the book, one page, organized two ways: by mission (the order you learned them) and by job (the order you'll need them). Nothing here is new — this is your own toolkit, catalogued.*

---

## By Mission

### Mission 1 — Arrival
| Command | What it does | Run it in |
|---|---|---|
| `wsl --install` | installs WSL + Ubuntu (one time) | PowerShell (as admin) |
| `wsl --shutdown` | fully stops WSL (the "off and on again" fix) | PowerShell |
| `whoami` | prints your username | Ubuntu |
| `lsb_release -a` | shows which Ubuntu this is | Ubuntu |
| `date` / `cal` | current date/time · this month's calendar | Ubuntu |
| `echo "text"` | repeats your words back | Ubuntu |

### Mission 2 — Installing
| Command | What it does |
|---|---|
| `sudo apt update` | refresh the software catalog (do this before installing) |
| `sudo apt install <name> -y` | install a package — **the master pattern** |
| `sudo apt remove <name> -y` | remove a package, cleanly and completely |
| `apt list --installed` | list everything installed |
| `python3 --version` | confirm Python is present (it ships with Ubuntu) |

### Mission 3 — Local AI
| Command | What it does |
|---|---|
| `curl -fsSL https://ollama.com/install.sh \| sh` | install Ollama (official installer, one time) |
| `ollama run llama3.2:1b` | download (first time) + chat with a model |
| `/bye` | leave the chat (at the `>>>` prompt) |
| `ollama list` | show your downloaded models |
| `ollama serve` | start the engine by hand (troubleshooting) |

### Mission 4 — Home
| Command | What it does |
|---|---|
| `pwd` | *where am I?* |
| `ls` (and `ls -l`) | *what's here?* (detailed view) |
| `cd <folder>` | go there |
| `cd ~` | **teleport home — from anywhere, always** |
| `mkdir <name>` | make a folder |
| `nano <file>` | create/edit a file (Ctrl+O, Enter = save · Ctrl+X = exit) |
| `cat <file>` | print a file's contents |
| `explorer.exe .` | open this Ubuntu folder in Windows Explorer |

### Mission 5 — Python
| Command | What it does |
|---|---|
| `python3 <file>.py` | run a Python script |
| `python3 --version` | which Python you have |

### Mission 6 — Git & GitHub
| Command | What it does |
|---|---|
| `sudo apt install git -y` | install Git |
| `git config --global user.name "Name"` | sign your work (once) |
| `git config --global user.email "email"` | ditto |
| `git clone <url>` | copy a repo from the world (safe: writes one new folder only) |
| `git init` | make the current folder a repository |
| `git add <files>` | choose what the next save-point includes |
| `git commit -m "note"` | press the save-point button |
| `git status` | *what's changed since my last commit?* — always safe |
| `git log` | the project's whole history (press `q` to exit) |

### Mission 8 — Perspective
| Command | What it does |
|---|---|
| `history` | everything you've ever typed, numbered |
| `history \| wc -l` | ...counted |
| `ssh user@machine` | a terminal on a distant computer *(your future)* |

---

## By Job

**"I'm lost / confused"** → `pwd` (where am I) → `ls` (what's here) → `cd ~` (go home) → `git status` (what changed)

**"I want to install something"** → `sudo apt update` → `sudo apt install <name> -y` *(newer tools: check their site for an official one-liner, like Ollama's)*

**"I want to make something"** → `mkdir` (a folder) → `nano` (a file) → `python3 file.py` (run it) → `git add` + `git commit` (protect it)

**"I want to talk to my AI"** → `ollama run llama3.2:1b` (directly) → `python3 ask.py` (through your own program)

**"Something's weird, reset it"** → close Ubuntu → PowerShell: `wsl --shutdown` → wait 10 seconds → reopen Ubuntu

---

### The habits worth keeping

1. **Say the pattern before you type it.** (Refresh, install. Where am I, what's here, go.)
2. **Read errors bottom line first** — the last line usually names the problem; the line number points at it.
3. **Commit when you like what you've made.** Future-you is the beneficiary.
4. **When in doubt: `pwd`, `ls`, `git status`.** All three only look. Looking is always free.
