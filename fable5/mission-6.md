# Mission 6 — Joining the World

*In which "just clone the repo" becomes a thing Wendy does, and her journal gets a time machine.*

---

### Part 1 — The Town Square

"I unpaused the video," Wendy announced.

Alex looked up. "*The* video? Kitchen-table video? Fourteen-tabs video?"

"That one. I got through 'open your Ubuntu terminal' feeling — honestly? — smug. And then forty seconds later it said *'just clone the repo'* and I realized there's a second door." She pulled up the transcript on her phone and read aloud: "'Just clone the repo, cd in, and you're good to go.' *Just.* Everything in that sentence assumes I already live somewhere I've never been."

"GitHub," Ulysses said.

"GitHub. Which I've heard maybe four hundred times and could not define under oath."

"Then tonight's the night. GitHub is the town square of the entire software world — every AI tool you've heard of lives there, in public, free to take. And 'clone the repo' is nothing more than *making yourself a copy*. Tonight you'll do it for real. And then—" he smiled slightly, "—we'll do something better than taking. But that's for the end."

### Part 2 — The Elephant in the Room

"Fear check," Alex said.

Wendy thought about it — and then laughed at what she found. "It's tiny. It's honestly barely there. It's just... *am I allowed?* GitHub sounds like a professional place. Like I'd be wandering into an operating theater in a bathrobe."

"You wrote software last week," Ulysses said. "You debug by reading the error like an instrument. But to your question: GitHub's public projects are *published deliberately*, like books in a library. Cloning isn't sneaking — it's checking a book out, except the library has infinite copies and never wants them back. You are not just allowed. You're the exact person it was built for."

### Part 3 — The Answer

"Two names, constantly said together, doing different jobs," Ulysses said.

"**Git** is a tool — it lives on your machine — whose job is *remembering versions*. Every save-point of a project, forever, undoable, comparable. It's a time machine for files.

"**GitHub** is a website — a place — where people put their Git projects so others can find them. Project-in-a-Git is called a **repository** — 'repo.' And **cloning** is copying a repo, whole, with its entire history, onto your machine. One command."

"And here's the beat most tutorials skip," Alex added, "which is criminal, because it's the safety fact: cloning **reads from the internet and writes into one new folder.** That's all it can do. It doesn't install anything, run anything, or touch a single file outside the folder it makes. It's the safest thing you'll ever do in a terminal."

> **💡 Why it works — why *everything* lives on GitHub**
> Git's time machine solves the two ancient problems of building things: *"I broke it and can't get
> back"* (any version, always recoverable) and *"we can't work on it together"* (changes merge
> instead of overwrite). Because Git made collaborating safe, sharing exploded — and GitHub became
> the square where it happens: tens of millions of public projects, including essentially every AI
> tool you will ever hear named. When a tutorial says "clone the repo," it's saying: *the work is
> already done and published — come take your copy.*

### Part 4 — Crossing the Threshold

**Step 1 — Install Git.** Say the pattern before you type it. *(You did, didn't you?)*

```
sudo apt update
sudo apt install git -y
git --version
```

**What you'll see:** `git version 2.43.0` (or similar).

**Step 2 — Introduce yourself.** Git signs every save-point with its author, so it wants your name once:

```
git config --global user.name "Wendy"
git config --global user.email "wendy@example.com"
```

*(Use your real name and email if you like — or don't; nothing is sent anywhere. This is a label, not a registration.)*

**What you'll see:** *nothing.* Silence. "Is that—" Wendy started, and then answered herself: "No news is good news. Config jobs are quiet jobs." She checked anyway — `git config --global --list` — and there she was.

**Step 3 — Clone your first repository.** GitHub's classic hello-project:

```
cd ~
git clone https://github.com/octocat/Hello-World.git
```

**What you'll see:**

```
Cloning into 'Hello-World'...
remote: Enumerating objects: 13, done.
Receiving objects: 100% (13/13), done.
```

**Step 4 — Walk into what you just took.** You know these moves:

```
cd Hello-World
ls
cat README
```

A project from the world's town square, now sitting in her home folder like it had always been there. Then Ulysses said: "Now look at its *history*:"

```
git log
```

**What you'll see:** save-points — each with an author, a date, a note — going back years. Strangers' names. The project's whole life, visible. *(Press `q` to come back out.)*

"That's the time machine," Wendy said, scrolling. "You can see everyone who ever touched it."

"Every change, forever. Now." Ulysses sat forward. "Here's the part I promised was better than taking. You've been keeping a journal for three missions. It's real work — yours. Doesn't it deserve a time machine too?"

**Step 5 — Put *your* work under Git's protection:**

```
cd ~/winubuntu
git init
git add notes.txt hello.py
git commit -m "My journal and my first program - protected from tonight on"
```

**What you'll see** after `git init`: `Initialized empty Git repository in /home/wendy/winubuntu/.git/` — and after the commit, a summary of what was saved.

"What did I just do?"

"You made your folder a repository — same standing as any project on GitHub. `add` chose what to protect; `commit` pressed the save-point button, with your note attached and your name signed. From now on, any time you change these files, you can commit again — and *every version of your journal will exist forever*, recoverable. Try `git log`."

She did. One entry. Author: **Wendy**. Message: *"My journal and my first program - protected from tonight on."*

Her name, in the machine's history — the same kind of history she'd just read strangers' names in.

**Step 6 — Journal** (`nano notes.txt`):

```
Mission 6. I cloned a project from the world and put my own work under version control. Taking and keeping - same tools, both directions.
```

*(And why not: `git add notes.txt` then `git commit -m "Mission 6 journal"` — your second save-point. It's a habit now.)*

### Part 5 — What Just Happened

*"Just clone the repo"* — the sentence needed a translation four missions ago — is now something your hands know how to do. The town square where all of software lives, including every AI tool in your future, is open to you: one command, any public project, yours to read and run and learn from.

But hold onto the second thing. You didn't just take from the commons tonight — you started *keeping* like the people who build it do. Your journal has a history now. Your program has a history. That's not beginner behavior with training wheels; that's literally the same tool, used the same way, as every professional project on GitHub. The difference between you and them is now scale, not kind.

---

*The terminal had been hers for a while now — her workbench, her files, her small handmade things. Tonight it grew a horizon: the whole world's work reachable from her prompt, and her own work signed with her name. The workbench, it turned out, was connected to every other workbench on Earth.*

---

### 🧪 Try It Yourself

| Type this | Why |
|---|---|
| `cd ~ && git clone https://github.com/octocat/Spoon-Knife.git` | a second clone, to feel how routine it already is |
| `cd ~/winubuntu && git log` | re-read your own history (it grows from here) |
| `git status` | Git's favorite question-answerer: *what's changed since my last save-point?* |
| edit `notes.txt`, then `git status` again | watch Git *notice* — before you've told it anything |

*`git status` is the command you'll type most for the rest of your life. It's always safe. It only looks.*

### ✅ What You Learned

- **Git** = the time machine (on your machine). **GitHub** = the town square (on the web). **Repo** = a project in the machine.
- **`git clone <url>`** copies a public project — code and full history — into one new folder. It touches nothing else, ever.
- **`git init` → `git add` → `git commit -m "note"`** — your own work, under protection, in three moves.
- `git log` shows any project's whole life; `git status` shows what's changed right now.
- You're **allowed**. It was built for exactly you.

### 📖 Words You Now Know

- **Repository (repo)** — a project tracked by Git: files + entire history.
- **Clone** — take a full copy of a repo onto your machine.
- **Commit** — a save-point: a snapshot with your note and your name.
- **`git status` / `git log`** — what's changed now / everything that ever changed.
- **Open source** — work published for the world to use and learn from. The reason your future tools are free.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"git: command not found."**
  Step 1 again: `sudo apt install git -y`.

- **"Could not resolve host: github.com."**
  Network hiccup — is Wi-Fi on? (Mission 3 alumni: *did you ever turn it back on?*) If Windows has internet but Ubuntu doesn't: close Ubuntu, `wsl --shutdown` in PowerShell, reopen.

- **"fatal: repository not found" or an authentication prompt.**
  Almost always a typo in the URL — compare character by character. (Auth prompts mean a *private* repo; everything in this mission is public and needs no login.)

- **`git commit` complains "Please tell me who you are."**
  Step 2 got skipped — run the two `git config --global` lines, then commit again.

- **`git log` filled the screen and swallowed the prompt.**
  You're in the pager — it's showing you a long history one screen at a time. Arrow keys scroll; **`q`** quits back to your prompt.

- **"fatal: not a git repository."**
  You're standing outside the repo. `cd` into it (`cd ~/winubuntu` or `cd ~/Hello-World`) — Git commands work from inside. A where-am-I problem, and you own those.

> **The WinUbuntu promise:** cloning cannot harm your machine — worst case is a failed download and
> a second try. And once your work is committed, Git *never forgets it*. From tonight, losing your
> journal would take deliberate effort.

---

**Next mission:** inventory check — you have Python, a local AI, a home folder, and version control. Separately: tools. Wired together: a *project*. Next time, you build your first real one — a program of your own that talks to your own AI.
