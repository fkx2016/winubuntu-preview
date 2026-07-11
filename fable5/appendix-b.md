# Appendix B — Troubleshooting Index

*Every error in the book, organized by **symptom** — what your screen actually looks like — because that's how problems arrive. Find the symptom, follow the fix. And hold onto the book's first law: **an error message is the machine helping, not judging.***

---

## Golden rules (read once, they cover half of everything)

1. **The password prompt showing nothing is not a symptom.** Linux hides passwords completely. Type it blind, press Enter. *(Mission 1's most important lesson — forever.)*
2. **Read the LAST line of any error first.** That's usually the actual problem; everything above it is the machine showing its work.
3. **The universal reset:** close Ubuntu → PowerShell: `wsl --shutdown` → wait 10 seconds → reopen. Fixes a remarkable share of "weird" (network hiccups, stuck installs, unresponsive windows). Loses nothing — your files all remain.
4. **`cd ~` cures all lostness.**

---

## "It won't install" (Missions 1–3, 6)

**`wsl --install` prints a wall of help text, installs nothing** → older Windows. Run Windows Update fully, restart, retry. Still? → `wsl --install -d Ubuntu`.

**"requires elevation" / "Access is denied"** → PowerShell isn't running as administrator. Start → `powershell` → right-click → **Run as administrator**.

**Error mentions "Virtual Machine Platform" / virtualization / `0x80370102`** → virtualization is off in your machine's firmware. One-time, harmless fix: search *"<your PC model> enable virtualization BIOS"*, flip it on, retry.

**"Unable to locate package <name>"** → stale catalog. `sudo apt update`, then retry the install.

**"Could not get lock /var/lib/dpkg/…"** → Ubuntu is installing its own updates in the background. Wait 1–2 minutes, retry. (One key, one kitchen.)

**"E: Failed to fetch…" / downloads hang** → network hiccup inside WSL. Confirm Windows has internet → golden rule 3 (the reset) → retry.

**"<you> is not in the sudoers file"** → account wasn't created as admin (rare). Cleanest early fix: PowerShell → `wsl --unregister Ubuntu` → redo Mission 1 (minutes).

---

## "The AI won't work" (Missions 3, 7)

**"could not connect to ollama app" / "connection refused"** → the engine's not up. Wait 10 seconds, retry. Persisting: second Ubuntu window → `ollama serve` → leave it open → retry in the first.

**Model download stalls** → `Ctrl+C`, re-run — it resumes where it stopped.

**"model requires more system memory" / crash mid-answer** → close other apps (browsers especially); make sure it's `llama3.2:1b`, the small one.

**Answers are very slow, fan roaring** → normal: real AI on modest hardware. Small model, short prompts, fewer open apps. Slow ≠ broken.

**`FileNotFoundError: 'ollama'` from Python** → does `ollama list` work by itself? If freshly installed, close and reopen Ubuntu so the command is found.

---

## "I'm lost / it can't find my file" (Missions 4–7)

**"No such file or directory" (from `cd`, `cat`, `nano`…)** → typo or wrong room. `ls` for exact names — **capitalization counts** — or `cd ~` and walk again.

**"can't open file 'hello.py'"** → you're standing elsewhere. `cd ~/winubuntu` → `ls` to confirm → rerun.

**"Permission denied" creating things** → you've wandered into system territory. `cd ~`; build in your own branch.

**nano confusion (`^O`? `^X`?)** → `^` = Ctrl. Save = Ctrl+O then Enter. Exit = Ctrl+X. Exiting with unsaved changes asks "Save modified buffer?" → **Y**, Enter.

**`explorer.exe .` does nothing** → exact form: `explorer.exe` + space + `.` — or in Windows Explorer's address bar: `\\wsl.localhost\Ubuntu\home\<you>`.

---

## "My program is broken" (Missions 5, 7)

**`SyntaxError`** → the message names the file, the line, and points an arrow at the spot. Usual culprits: a missing quote, an unmatched `(`, curly "smart quotes" pasted from a word processor (retype them straight in nano), a missing `:` after `while True` or `if`.

**`IndentationError`** → Python reads leading spaces as structure. Simple scripts: lines start at the left edge. Loops: everything inside is indented the same amount (4 spaces is the custom).

**It runs, but does something odd** → it did exactly what the file says. `cat` the file, read it out loud, find where what-it-says differs from what-you-meant. (This is real debugging — the daily craft.)

---

## "Git is complaining" (Mission 6)

**"git: command not found"** → `sudo apt install git -y`.

**"Please tell me who you are"** → the two `git config --global` lines from Mission 6, then commit again.

**"Could not resolve host: github.com"** → internet check (Mission 3 alumni: is Wi-Fi back on?) → golden rule 3.

**"fatal: repository not found" / login prompt** → URL typo (compare character by character), or a private repo — the book's repos are public, no login ever needed.

**"fatal: not a git repository"** → you're standing outside the repo. `cd` into it.

**Screen swallowed by `git log`** → you're in the pager. Arrows scroll; **`q`** returns you.

---

## Still stuck?

You have a private, judgment-free expert **on your own machine**: `ollama run llama3.2:1b`, paste the error, ask what it means. (Or `python3 ask.py` — let your own project help you fix your other projects, which is about as Level-4 as life gets.)

> **The WinUbuntu promise, in appendix form:** nothing in this book can break your computer. Every
> symptom above ends in "retry" or "read and adjust" — never in damage. The worst possible outcome
> of any mission is a fresh start that takes minutes. Explore accordingly.
