
# Appendix A — Command Reference

*Every command taught in WinUbuntu, on one page. Keep it beside you.*

---

### Setup (one time)
| Command | What it does | Mission |
|---|---|---|
| `wsl --install` | install Ubuntu inside Windows *(run in PowerShell as admin)* | 1 |

### Knowing where you are
| Command | What it does | Mission |
|---|---|---|
| `whoami` | show your username | 1 |
| `pwd` | print the folder you're in ("where am I?") | 4 |
| `ls` | list what's in the current folder | 4 |
| `ls -l` | list with details (size, date) | 4 |
| `lsb_release -a` | show which Ubuntu version you're running | 1 |
| `history` | show every command you've run | 8 |

### Moving and making
| Command | What it does | Mission |
|---|---|---|
| `cd foldername` | go into a folder | 4 |
| `cd ~` | go home (your "take me back" button) | 4 |
| `mkdir name` | make a new folder | 4 |
| `nano file.txt` | create/edit a file | 4 |
| `cat file.txt` | print a file's contents | 4 |

### Installing software (the universal pattern)
| Command | What it does | Mission |
|---|---|---|
| `sudo apt update` | refresh the catalog of available software | 2 |
| `sudo apt install NAME -y` | install a tool | 2 |
| `sudo apt remove NAME -y` | remove a tool, cleanly | 2 |

### Local AI (Ollama)
| Command | What it does | Mission |
|---|---|---|
| `curl -fsSL https://ollama.com/install.sh \| sh` | install Ollama | 3 |
| `ollama run llama3.2:1b` | download (first time) and chat with a small model | 3 |
| `/bye` | leave the AI chat | 3 |
| `ollama list` | list the models you've downloaded | 3 |
| `ollama serve` | start the AI service (if a program can't connect) | 3 |

### Python
| Command | What it does | Mission |
|---|---|---|
| `python3 --version` | confirm Python is installed | 5 |
| `python3 file.py` | run a Python script | 5 |
| `input("...")` | *(in code)* ask the user and wait | 5 |
| `print("...")` | *(in code)* show text on screen | 5 |

### Git & GitHub
| Command | What it does | Mission |
|---|---|---|
| `git --version` | confirm Git is installed | 6 |
| `git config --global user.name "..."` | set your name for Git | 6 |
| `git config --global user.email "..."` | set your email for Git | 6 |
| `git config --global --list` | check your Git settings | 6 |
| `git clone URL` | copy a project from GitHub to your machine | 6 |
| `git log` | see a project's history *(press `q` to quit)* | 6 |

### Nano editor shortcuts *(`^` = the Ctrl key)*
| Keys | Action |
|---|---|
| **Ctrl+O**, then **Enter** | save ("write Out") |
| **Ctrl+X** | exit |

### Handy Windows-side (PowerShell)
| Command | What it does |
|---|---|
| `wsl --update` | update the WSL engine (fixes some install errors) |
| `wsl --shutdown` | fully restart WSL if Ubuntu acts stuck |

---
*Rule of thumb: `pwd`, `ls`, and `cd ~` can never break anything — use them freely whenever you feel lost.*


---
