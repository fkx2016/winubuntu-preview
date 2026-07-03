
# Mission 5 (Full Depth) — Speaking Python

*WinUbuntu · published-depth version.*

---

### Part 1 — The Word Everyone Uses

"There's a word I keep hearing," Wendy said. "*Python.* Everyone in AI says it. And back in Mission 2, you told me it was already on my computer."

"It is," said Alex. "It's been waiting this whole time. Today you say your first words in it."

### Part 2 — The Elephant

"The old fear wants a turn," Ulysses said. "*Isn't programming for programmers? Won't I need years of training?*"

Wendy half-laughed. "Yes, that one."

"Today you'll write *two lines* and run them. Programming isn't a personality you're born with. It's a sentence you learn to say — and then another."

### Part 3 — The Answer

"Python is a language for telling the computer what to do — in words that read almost like English," Alex said. "You'll write it into a file, the way you made `notes.txt`, and then *run* it with `python3`."

> **💡 Why it works — What "running a script" means**
> A *script* is just a text file full of instructions. Python's **interpreter** (`python3`) reads
> your file top to bottom and does exactly what each line says. Two commands do all the work here:
> `input(...)` *asks you something and waits*, and `print(...)` *shows something on screen*. That's
> the whole trick behind an astonishing amount of software — ask, decide, show. You already
> understand it.

### Part 4 — Crossing the Threshold

> **✅ First:** make sure you're in your folder — `cd ~/winubuntu`.

**Step 1 — Confirm Python is here** *(a gift from Mission 2):*

```
python3 --version
```

**What you'll see:** something like `Python 3.12.3`.

**Step 2 — Write your first program:**

```
nano hello.py
```

Type these two lines *exactly* (quotes and all):

```python
name = input("What's your name? ")
print("Hello, " + name + ". You're writing Python now.")
```

Save and exit: **Ctrl+O**, **Enter**, **Ctrl+X**.

**Step 3 — Run it:**

```
python3 hello.py
```

**What you'll see:**

```
What's your name? Wendy
Hello, Wendy. You're writing Python now.
```

The program asked her a question. She typed her name. It answered her — *by name*, in words she had written herself.

"I didn't run someone else's code," Wendy said. "I wrote that."

"You wrote that."

### Part 5 — What Just Happened

You just crossed a line that feels enormous from the outside and turns out to be a single step: you stopped *using* programs and started *writing* them.

Two lines today. It only grows from here — one sentence at a time.

---

### 🧪 Try It Yourself

Reopen the file (`nano hello.py`) and make it yours:

| Change | Try adding this line |
|---|---|
| Ask a second question | `mood = input("How are you feeling about Ubuntu? ")` |
| Use the answer | `print("Feeling " + mood + "? That's exactly right for Day 5.")` |
| A little math | `print("You've done 5 missions. Only a few to go!")` |

Save, then `python3 hello.py` again. *Change one thing, run it, see what happens — that's how everyone learns to code.*

### ✅ What You Learned

- **Python** is a readable language; you write it into a `.py` file and run it with `python3`.
- **`input(...)`** asks and waits; **`print(...)`** shows.
- You went from *using* software to *writing* it — the real threshold of "building."
- Editing + running your own file is now a loop you can repeat forever.

### 📖 Words You Now Know

- **Python** — a beginner-friendly programming language, central to AI.
- **Script** — a file of instructions the computer runs.
- **Interpreter (`python3`)** — the program that reads and runs your Python.
- **Variable** — a named place to hold a value (like `name`).

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"python: command not found."**
  On Ubuntu the command is **`python3`**, not `python`. Use `python3 hello.py`.

- **"can't open file 'hello.py': No such file or directory."**
  You're in a different folder than the file. Run `cd ~/winubuntu`, then `ls` to confirm `hello.py` is listed, then run it.

- **"SyntaxError" — usually about quotes or a parenthesis.**
  Reopen with `nano hello.py` and check the two lines match *exactly*: straight quotes `"like this"`, and each `(` has a matching `)`.

- **"IndentationError."**
  Python cares about spaces at the start of a line. For these two lines, neither should have any spaces before it — they start at the very left edge.

> **The WinUbuntu promise:** an error message is Python *helping* — it tells you the line number and
> what confused it. Errors aren't failure; they're the conversation.

---

**Next mission:** the whole world shares code in one place, and every tutorial assumes you're there. Let's join it — Git and GitHub.


---
