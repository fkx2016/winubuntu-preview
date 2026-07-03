
# Mission 6 (Full Depth) — Joining the World

*WinUbuntu · published-depth version.*

---

### Part 1 — The Other Word

"There's one more word," Wendy said. "*GitHub.* Every project I've ever looked at lives there, and every tutorial says 'just clone the repo' like I'm supposed to know what that means."

Ulysses nodded. "It's the town square of the whole software world. Today you walk into it."

### Part 2 — The Elephant

"Smaller fear this time?" he asked.

"Smaller," Wendy agreed. "Just… *am I allowed? Isn't that for real developers?*"

"You already are one — you wrote Python yesterday. GitHub is just where people keep and share their work. Copying someone's project to your machine has a name — *cloning* — and it doesn't touch a single thing you didn't ask it to."

### Part 3 — The Answer

"**Git** is a tool that tracks versions of files — every change, saved and undoable," Ulysses said. "**GitHub** is the website where people store Git projects and share them. To bring one to your computer, you *clone* it."

> **💡 Why it works — Git, GitHub, and "cloning"**
> **Git** is a time machine for files: it records every version, so nothing is ever truly lost.
> **GitHub** is a website that hosts Git projects so people can share them. A shared project is a
> **repository** ("repo"). *Cloning* makes a full copy of a repo on your machine — code and its
> entire history — with one command. It only ever *reads* the internet and *writes* into a new
> folder you name. Nothing else on your computer is touched.

### Part 4 — Crossing the Threshold

**Step 1 — Install Git** *(the pattern, one more time):*

```
sudo apt install git -y
git --version
```

**What you'll see:** e.g. `git version 2.43.0`.

**Step 2 — Introduce yourself** *(Git likes to know who makes changes):*

```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

**What you'll see:** *nothing.* That's correct — silent success. (Check it worked with `git config --global --list`.)

**Step 3 — Clone your first repository** — GitHub's classic little demo project:

```
cd ~
git clone https://github.com/octocat/Hello-World.git
```

**What you'll see:**

```
Cloning into 'Hello-World'...
remote: Enumerating objects...
Receiving objects: 100% ...
```

**Step 4 — Step inside what you just downloaded:**

```
cd Hello-World
ls
```

"That whole folder came from the internet, onto my machine, with one command," Wendy said. "And I know exactly where it is and how to look inside."

"You just did the thing every tutorial assumed you already knew. You're in the square now."

### Part 5 — What Just Happened

"Clone the repo" will never again be a wall. It's a door you know how to open. The entire open-source world — millions of projects, including every AI tool you'll ever want — is now reachable from your terminal.

*You didn't just learn a command. You joined a conversation the whole world is having.*

---

### 🧪 Try It Yourself

| Type this | What it does |
|---|---|
| `git config --global --list` | see the name/email you just set |
| `cd ~/Hello-World` then `git log` | see the project's history of changes (press `q` to quit) |
| `cat README` | read the project's description file |
| `cd ~` then clone another: `git clone https://github.com/octocat/Spoon-Knife.git` | grab a second repo |

*Cloning is safe and repeatable — each one just makes a new folder.* (In `git log`, press **`q`** to return to the prompt.)

### ✅ What You Learned

- **Git** tracks versions; **GitHub** hosts and shares projects called **repositories**.
- **`git clone <url>`** copies an entire project — with history — into a new folder.
- Cloning only reads the web and writes a new folder; it can't disturb your other files.
- "Just clone the repo" is now something *you* do.

### 📖 Words You Now Know

- **Git** — the version-tracking tool.
- **GitHub** — the website that hosts Git projects.
- **Repository (repo)** — a shared project (code + its history).
- **Clone** — make a full local copy of a repo.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"git: command not found."**
  Step 1 didn't complete. Re-run `sudo apt install git -y`.

- **"Could not resolve host: github.com."**
  A network/DNS hiccup in WSL. Check your internet and retry. If it persists, close Ubuntu, run `wsl --shutdown` in PowerShell, and reopen.

- **"fatal: repository ... not found" or "Authentication failed."**
  Usually a typo in the URL, or you're trying to clone a *private* repo (which needs a login). For practice, use the public HTTPS URLs above exactly as written.

- **`git config` printed nothing — did it work?**
  Yes — no news is good news for `config`. Verify with `git config --global --list`.

- **`git log` filled the screen and I'm stuck.**
  Press **`q`** to quit back to the prompt.

> **The WinUbuntu promise:** cloning can't harm your machine — worst case, a download fails and you
> simply try again.

---

**Next mission:** you have Python, a local AI, and freedom to move around. Time to put them together — your first real project.


---
