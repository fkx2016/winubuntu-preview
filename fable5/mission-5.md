# Mission 5 — Speaking Python

*In which Wendy writes her first program, breaks it on purpose, and learns the truth about error messages.*

---

### Part 1 — The Word Everyone Uses

"Python," Wendy said, sitting down before anyone else had said a word. "It's time, right? It has to be time. Every AI video says it. Every job posting says it. You showed me it's *been on my machine* since Mission 2, just... waiting. Like a piano in the house of someone who doesn't play."

Alex laughed. "It's time. Today you play."

"I want to say the fear before Ulysses asks," Wendy said. "Because I've noticed something. My fears used to be about *breaking things*. This one's different. This one's about *me*. It's: programming is a thing programmers do, and I'm not one, and three missions of cows and folders don't change that. There's a wall between people who use computers and people who *program* them, and people like me don't get over it."

The table was quiet for a second.

"That," said Ulysses, "is the realest elephant anyone has named in this book. So let's kill it properly."

### Part 2 — The Elephant in the Room

"Here's what the wall is actually made of," he said. "Two things. One: the belief that programming means memorizing a language's worth of strange words before you can start. Two: the terror of getting it wrong — because error messages look like the machine *judging you*.

"Tonight destroys both. You'll write a complete, working program with **three lines** — no memorization, because I'll give you the lines. And then—" he glanced at Alex, who nodded, "—we're going to do something no beginner book does. We're going to **break your program on purpose**, read the error message together, and fix it. Because the difference between you and a programmer isn't knowledge. It's that errors stopped scaring them. We can install that tonight."

"You want me to make a mistake. Deliberately."

"I want you to make your first mistake while you're *expecting* it, with friends at the table — instead of alone at midnight thinking you broke Python."

### Part 3 — The Answer

"What a program actually is," Alex said, "you already know — you just don't know you know. A program is a **text file full of instructions**, read top to bottom. You made a text file last mission: your journal. Tonight's file is exactly that, except the machine *does* what the lines say instead of just storing them.

"Python is a language for those instructions — the AI world's favorite, because it reads almost like English. And the thing that reads your file and acts on it is called the **interpreter**. You have it: `python3`."

"Only two new words tonight," Ulysses said. "**`input(...)`** — ask the human something, wait for their answer. **`print(...)`** — say something to the human. Ask and answer. You've been having that exact conversation with the terminal for five missions — now you get to *write the other side of it*."

> **💡 Why it works — the whole trick of software**
> `input()` waits and listens; `print()` speaks; a **variable** (like `name`) is a labeled box that
> carries a value from one line to the next. Ask → hold → respond: that loop, elaborated, is a
> staggering fraction of all software. The AI chat from Mission 3? Ask, hold, respond — with a very
> fancy middle step. You are not learning a toy version of programming tonight. You're learning
> its actual skeleton.

### Part 4 — Crossing the Threshold

> **✅ First:** get to your folder — `cd ~/winubuntu`. (You know what that means now. Feel that?)

**Step 1 — Confirm the piano's in tune:**

```
python3 --version
```

**What you'll see:** `Python 3.12.3` (or similar — any 3.x is perfect).

**Step 2 — Write the program:**

```
nano hello.py
```

Type these three lines exactly — straight quotes, and the parentheses matter:

```python
name = input("What's your name? ")
print("Hello, " + name + "!")
print("You're writing Python now.")
```

Save and exit: **Ctrl+O**, **Enter**, **Ctrl+X**.

**Step 3 — Run it:**

```
python3 hello.py
```

**What you'll see:**

```
What's your name?
```

It's waiting. *Your program* is waiting — for you. Type your name. Press Enter.

```
What's your name? Wendy
Hello, Wendy!
You're writing Python now.
```

Wendy stared at it. "I need to say this precisely," she said, "because it feels important. A month ago I couldn't open a terminal. I just *wrote software*. It's three lines and it says hello, but it did not exist, and I made it, and it works."

"That's precisely what happened," Alex said. "Welcome over the wall. Now—" he cracked his knuckles theatrically, "—let's break it."

**Step 4 — The deliberate mistake.** "Reopen the file: `nano hello.py`. Now delete the closing quote after `Hello, ` — so the second line reads:"

```python
print("Hello,  + name + "!")
```

"Save, exit, run it again. Ready? This is the moment every beginner fears. We're walking into it on purpose."

```
python3 hello.py
```

**What you'll see:**

```
  File "/home/wendy/winubuntu/hello.py", line 2
    print("Hello,  + name + "!")
                              ^
SyntaxError: unterminated string literal (detected at line 2)
```

"Okay," Ulysses said. "Before the adrenaline talks: what did the machine just *actually say*? Read it like a note, not a verdict."

Wendy read it slowly. "...It says the file name. It says... *line 2*. There's an arrow pointing at a spot. And 'unterminated string literal' means..." she frowned, then got it: "a quote I opened and never closed. It's telling me *exactly where I broke it.*"

"It's telling you exactly where you broke it. That's what an error message is: **the machine helping you find the problem.** It's not offended. It's not judging. It never says 'bad programmer.' It says *line 2, right here, this kind of problem.* Programmers don't read errors less than beginners — they read them *more*, hundreds a day, like a navigator reads instruments."

"Now fix it," said Alex. "You know the line, you know the spot."

She reopened nano, restored the quote, ran it. `Hello, Wendy!` Working again — broken and repaired by the same pair of hands.

**Step 5 — Journal.** One line, you know the drill (`nano notes.txt` — you're already in the right folder):

```
Mission 5. I wrote a program, broke it on purpose, and fixed it. Error messages are directions, not verdicts.
```

### Part 5 — What Just Happened

Two thresholds tonight, and the second one matters more.

The first: you wrote and ran a program. The wall between "computer user" and "person who programs" — the one you said people like you don't get over — you're standing on the far side of it. It was three lines tall.

The second: you broke a program, *read the error*, and fixed it. That experience — error, read, fix, working again — is the actual daily life of everyone who builds things. Not flawless typing: **confident repairing.** You've now done, in miniature, the whole loop. Everything bigger is this loop, repeated.

---

*She'd talked to the terminal for five missions. Tonight the terminal had run words* she authored *— asked her name because she'd told it to ask. It wasn't a place anymore, exactly. It was starting to feel like a workbench. Her workbench.*

---

### 🧪 Try It Yourself

Reopen `nano hello.py` and make it yours — change one thing, run, look, repeat:

| Idea | Line to try |
|---|---|
| Ask a second question | `feeling = input("How's the journey so far? ")` |
| Use the answer | `print("Feeling " + feeling + " is exactly right for Mission 5.")` |
| Let the machine do math | `print("Missions done: " + str(5) + " of 8")` |
| Break it differently | remove a `(` — run it — read the error *calmly* — fix it. You've done this. |

*The loop is: change → run → read → adjust. Nobody types perfect code. Everybody runs the loop.*

### ✅ What You Learned

- A **program is a text file of instructions**; the **interpreter** (`python3`) performs it top to bottom.
- **`input()`** listens, **`print()`** speaks, a **variable** carries values between lines — the skeleton of nearly everything.
- **Error messages are directions**: file, line number, arrow, problem type. The machine is helping.
- The real skill isn't typing flawlessly — it's the loop: **write, run, read, fix.**

### 📖 Words You Now Know

- **Python** — the AI world's favorite programming language; readable, beginner-kind.
- **Script** — a program in a text file (yours: `hello.py`).
- **Interpreter** — the program that reads and performs your script (`python3`).
- **Variable** — a labeled box for a value (`name`).
- **SyntaxError** — "I couldn't read line N — look right here." A helper wearing a scary name.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"python: command not found."**
  Ubuntu's command is **`python3`** — the `3` is part of the name here.

- **"can't open file ... hello.py: No such file or directory."**
  You're standing in a different folder than the file. `cd ~/winubuntu`, confirm with `ls` that `hello.py` is there, run again. (Where-am-I problems are Mission 4 problems — you own those now.)

- **`SyntaxError` you *didn't* plan.**
  Congratulations, a real one! Read it like we practiced: line number, arrow. Usual suspects: curly “smart quotes” (must be straight `"` — type them in nano, don't paste from a word processor), or an unmatched `(` `)`.

- **`IndentationError: unexpected indent`.**
  Python is strict about spaces at line *starts*. These three lines should each begin at the very left edge — delete any leading spaces.

- **It runs but prints something odd.**
  It did exactly what the file says — which is sometimes not what you meant. `cat hello.py` and read your lines out loud. (This, too, is the daily life of programmers.)

> **The WinUbuntu promise:** from tonight on, an error message is never an emergency. It's the
> machine's handwriting, and you can read it now.

---

**Next mission:** your program lives alone on your laptop. But every tutorial keeps saying *"just clone the repo"* — the whole world's software lives in one shared town square. Let's walk in. And while we're there, we'll put *your* work under protection too.
