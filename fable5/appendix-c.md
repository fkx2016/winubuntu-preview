# Appendix C — Glossary

*Every term the book taught, gathered and alphabetized. Each entry notes the mission where you learned it — not as trivia, but so you can revisit the story that made it stick.*

---

**apt** *(M2)* — Ubuntu's package manager: installs, tracks, and removes software from one trusted catalog. The master pattern: `sudo apt update` → `sudo apt install <name> -y`.

**Clone** *(M6)* — copy an entire repository — files plus full history — from the internet into one new folder on your machine. Reads the web, writes that folder, touches nothing else.

**Cloud / GPU machine** *(M8)* — a powerful computer you rent and reach through a terminal. Runs Ubuntu almost always — meaning it speaks exactly the language this book taught you.

**Command** *(M1)* — one instruction, typed at a prompt, sent with Enter.

**Commit** *(M6)* — a Git save-point: a snapshot of your chosen files, stamped with your note, your name, and the time. `git commit -m "note"`.

**Directory** *(M4)* — Linux's word for a folder. Same thing, both words used everywhere.

**Home (`~`)** *(M4)* — your personal folder, `/home/<you>`; where your terminal starts and your work lives. `cd ~` returns you there from anywhere, always.

**Integration** *(M7)* — wiring existing tools together into something new. Most of what building software actually is. Your `ask.py` — Python wired to Ollama — is integration.

**Interpreter** *(M5)* — the program that reads your script and performs it: `python3`.

**Iteration** *(M7)* — the builder's rhythm: rough version first, prove it works, improve it. The actual secret of everyone who makes things.

**Local AI** *(M3)* — an AI model running entirely on your own machine. No internet, no account, nothing leaves the room. Privacy by physics, not by promise.

**Loop / `while True:`** *(M7)* — instructions that repeat until told to stop; `break` is "told to stop."

**Mentor** *(M8)* — someone who remembers what it felt like not to know. The book's last threshold is becoming one.

**Model** *(M3)* — the large file of learned patterns that *is* an AI. Small ones (1–3 GB) run on ordinary laptops.

**nano** *(M4)* — the friendly terminal text editor. Ctrl+O, Enter = save; Ctrl+X = exit; `^` on its help bar means Ctrl.

**Ollama** *(M3)* — the tool that downloads and runs AI models locally. The player; models are the albums.

**Open source** *(M6)* — software published for the world to use, study, and build on. Why nearly every tool in this book was free.

**Package** *(M2)* — a tracked bundle of software that apt can install or cleanly remove.

**Parameters** *(M3)* — an AI model's learned patterns. More parameters: smarter, bigger, hungrier.

**Path** *(M4)* — a location's full address in the folder tree, like `/home/wendy/winubuntu`.

**Prompt** *(M1, M3)* — the terminal's "ready" signal (the line ending `$`); also the message you send an AI (at `>>>`). Both meanings: *an invitation to speak.*

**pwd / ls / cd** *(M4)* — where am I / what's here / go there. The three moves of living in a terminal. All safe; looking never changes anything.

**Repository (repo)** *(M6)* — a project tracked by Git: its files plus its entire history. GitHub hosts millions, publicly.

**Script** *(M5)* — a program stored as a text file (like `hello.py`), performed top-to-bottom by an interpreter.

**SSH** *(M8)* — open a terminal on a distant machine as if it were in front of you. How your skills travel up the ladder.

**sudo** *(M2)* — "super-user do": run one command with elevated permission. Ubuntu asks your password (typed invisibly) to confirm you mean it.

**subprocess** *(M7)* — Python's toolkit for running other programs and capturing their output. Turns your whole terminal toolkit into program components.

**SyntaxError** *(M5)* — Python saying "I couldn't read this — line N, right here (see arrow)." A helper wearing a scary name.

**Terminal** *(M0–M8)* — the text window where you talk with a computer in words. Began this book as a symbol of uncertainty; check your journal for what it became.

**Ubuntu** *(M0)* — the friendliest, most widely used Linux; the AI world's home ground. Named for a Southern African concept often rendered *"I am because we are"* — which, if you think about the last threshold of Mission 8, is the whole book in one word.

**Variable** *(M5)* — a labeled box that carries a value between lines of a program (`name`, `question`).

**WSL (Windows Subsystem for Linux)** *(M1)* — Microsoft's technology that runs a genuine Ubuntu in a sealed compartment inside Windows. The guest suite. The bridge.
