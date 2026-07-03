
# Appendix B — Troubleshooting Index

*Every "if something went wrong" from the book, gathered by symptom. Nothing here means you broke
your computer — each one is a small nudge with a calm fix.*

---

### Installing Ubuntu (Mission 1)
- **`wsl --install` printed help text instead of installing** → your Windows is older; run **Windows Update**, restart, retry. Or try `wsl --install -d Ubuntu`.
- **"requires elevation" / "Access denied"** → PowerShell wasn't opened as admin. Start → type PowerShell → **right-click → Run as administrator**.
- **Virtualization error / `0x80370102`** → enable *virtualization* in your PC's BIOS/firmware (search your model + "enable virtualization"), then retry. Or run `wsl --update`.
- **Ubuntu didn't open after restart** → open it yourself: Start → type **Ubuntu** → click.
- **The password won't type** → it *is* typing; Ubuntu hides password characters. Type it, press Enter, confirm.

### Installing software with apt (Missions 2, 3, 6)
- **"Unable to locate package NAME"** → run `sudo apt update`, then retry the install.
- **"Could not get lock … is another process using it?"** → a background install is running; wait a minute, retry.
- **"E: Failed to fetch" / it hangs** → network/DNS blip. Check internet; if it persists, run `wsl --shutdown` in PowerShell, reopen Ubuntu.

### Local AI / Ollama (Missions 3, 7)
- **"curl: command not found"** → `sudo apt install curl -y`, then re-run the installer.
- **"could not connect to ollama" / "connection refused"** → open a second Ubuntu window, run `ollama serve` (leave it), then retry. Often waiting a few seconds and re-running is enough.
- **Download is slow or stalls** → it's a one-time download; let it finish, or press `Ctrl+C` and re-run (it resumes).
- **Answers are very slow / fan spins up** → normal on modest hardware. Use the smallest model (`llama3.2:1b`), keep prompts short, close heavy apps.
- **"model … not found"** → check spelling; see what you have with `ollama list`.
- **`FileNotFoundError: 'ollama'` (from Python)** → confirm Ollama is installed (`ollama list`); if you just installed it, close and reopen Ubuntu.

### Files & navigation (Mission 4)
- **"No such file or directory" on `cd`** → typo, or it's not here. Run `ls` to see exact names (case-sensitive), or `cd ~` to reset home.
- **I feel lost** → `pwd` shows where you are; `cd ~` teleports home. Always works.
- **The `^O` / `^X` symbols in nano confuse me** → `^` means **Ctrl**. Save = **Ctrl+O**, Enter; exit = **Ctrl+X**.
- **"Permission denied" making a folder** → you wandered into a system area. `cd ~` first, then create in your home.

### Python (Missions 5, 7)
- **"python: command not found"** → use **`python3`**, not `python`.
- **"can't open file 'X.py'"** → wrong folder. `cd ~/winubuntu`, `ls` to confirm the file, then run it.
- **"SyntaxError"** → check quotes are straight `"..."` and every `(` has a `)`.
- **"IndentationError"** → remove stray spaces at the start of lines (or match the example's spacing exactly).

### Git & GitHub (Mission 6)
- **"git: command not found"** → `sudo apt install git -y`.
- **"Could not resolve host: github.com"** → network/DNS; retry, or `wsl --shutdown` then reopen.
- **"repository not found" / "Authentication failed"** → typo in the URL, or it's a private repo. Use the public HTTPS URLs exactly as written.
- **`git config` printed nothing** → that's success. Verify with `git config --global --list`.
- **`git log` filled the screen** → press **`q`** to quit.

---

> **The WinUbuntu promise:** if you hit something not on this list, you haven't failed and you haven't
> broken anything. Note the exact message you saw — that's the clue — and your local AI (Mission 3)
> or a search will almost always name the fix in one step.


---
