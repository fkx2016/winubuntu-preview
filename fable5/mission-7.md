# Mission 7 — Your First Real Project

*In which the tools meet each other, and Wendy builds the way builders build.*

---

### Part 1 — The Pieces on the Table

Wendy came in carrying a piece of paper — an actual handwritten list — and set it down like a poker hand.

"I made an inventory," she said. "Indulge me. One: I have Python, and I can write it — a little. Two: I have an AI that lives *in my laptop*. Three: I have a home in the terminal, and my files are under version control like a real person's. Four—" she tapped the paper, "—and this is the thing I realized at two in the morning: *these are all on the same machine.* They can... they could *reach* each other. Couldn't they? Could my program *talk to my AI*?"

Alex looked at the list for a long moment, then at Ulysses. "You know what this list is? This is a *design document*. She's not asking permission. She's proposing a build."

"I'm asking if it's *possible*—"

"It's better than possible," Alex said. "It's tonight. And Wendy — everything that has ever been built with AI, everything in the news, every product, every startup — is at its heart the sentence you just said: *a program of mine, talking to a model.* You've arrived at the actual frontier. It just looks like a kitchen table."

### Part 2 — The Elephant in the Room

"Fear check," Ulysses said, "for tradition's sake."

Wendy searched honestly. "It's not fear anymore. It's more like — stage fright? *What if it's beyond me. What if this is the mission where I finally hit my ceiling.*"

"Then here's tonight's promise: we build it the way real builders build — which nobody shows beginners, and it changes everything. We do **not** write the perfect program in one go. We write the *crudest thing that works*, prove it works, then improve it. Rough first, better second. If the rough version works — and it will — there is no ceiling tonight."

### Part 3 — The Answer

"One new idea is all you need," Alex said. "Your script talks to Ollama the same way *you* do — by running the `ollama` command. Python has a tool for exactly that: **`subprocess`** — it lets your program run *another* program, hand it something, and catch what comes back.

"Think about what that means: everything in the terminal — every command you've learned — your programs can now use as parts. `subprocess` is the moment the whole toolbox becomes *components*."

> **💡 Why it works — integration is the whole game**
> `subprocess.run([...])` starts another program, waits, and hands you what it printed
> (`capture_output=True` catches it; `text=True` keeps it human-readable). Wiring existing tools
> together like this is called **integration** — and it is, honestly, most of what software
> engineering *is*. Not writing everything from scratch: connecting strong pieces. Tonight: your
> Python + your model. Same shape as any AI product you've ever heard of.

### Part 4 — Crossing the Threshold

> **✅ Preflight:** `ollama list` should show `llama3.2:1b` (Mission 3's model). And `cd ~/winubuntu` — build in your workshop.

**Step 1 — The rough version.** Crude on purpose — a fixed question, wired straight through:

```
nano ask.py
```

```python
import subprocess

result = subprocess.run(
    ["ollama", "run", "llama3.2:1b", "Say hello to Wendy, who built this program."],
    capture_output=True, text=True
)

print(result.stdout)
```

Save, exit, run:

```
python3 ask.py
```

A pause. The fan's little breath. And then:

```
Hello Wendy! Congratulations on building this program...
```

Wendy put both hands over her mouth. "*My program just talked to my AI.*"

"Rough version: **working**," Alex said. "Ninety seconds of typing. This is why builders build rough-first — you're already past the hard part, and everything from here is *improving a thing that works*, which is a fundamentally calmer activity than *hoping a thing will work*."

**Step 2 — Make it converse.** "Now, you know `input()`. Make it ask *you* for the question." He didn't reach for the keyboard. "You type it. You know all the pieces."

She did — `nano ask.py`, and after a minute's thought:

```python
import subprocess

question = input("Ask your AI: ")

result = subprocess.run(
    ["ollama", "run", "llama3.2:1b", question],
    capture_output=True, text=True
)

print("\n" + result.stdout)
```

*(That `"\n"` is a blank line, for breathing room — a builder's small courtesy to the reader.)*

```
python3 ask.py
```

```
Ask your AI: What should someone learn after their first Python program?
```

*...the pause, the breath...*

```
After a first program, great next steps are...
```

**Step 3 — Make it a companion.** "One more upgrade. A real assistant doesn't quit after one question. Python's `while True:` means *repeat forever* — and watch the indentation; the repeated lines step inward, that's how Python knows what's in the loop:"

```python
import subprocess

print("Your local AI. Ask anything - or 'bye' to leave.")

while True:
    question = input("\nAsk: ")
    if question == "bye":
        print("See you, Wendy.")
        break

    result = subprocess.run(
        ["ollama", "run", "llama3.2:1b", question],
        capture_output=True, text=True
    )
    print("\n" + result.stdout)
```

She ran it. Asked it three questions in a row. Typed `bye`. It said goodbye *in the words she'd written for it.*

**Step 4 — Protect it.** "It's real work now. You know what real work gets."

```
git add ask.py
git commit -m "ask.py - my first real project. Python talking to my own AI."
```

**Step 5 — Journal** (`nano notes.txt`):

```
Mission 7. I built a thing that didn't exist. Rough first, better second, mine the whole way. I'm not following the tutorials anymore - I'm the one building.
```

*(Commit that too. Obviously.)*

### Part 5 — What Just Happened

Look at the actual dimensions of tonight. About fifteen lines of Python. One new idea (`subprocess`). Every other piece — `input`, `print`, nano, your folder, your model, git — was already in your hands before you sat down.

And out of it: **a working AI application.** Not a toy imitation of one — the real shape: a program that takes a human's question, sends it to a model, and returns the answer. That's the skeleton of every AI chat product on Earth. Theirs are bigger. *None of them is more real.*

But the thing worth keeping from tonight is the *method*: rough first, prove it, improve it, protect it. That rhythm — not talent, not memorized syntax — is what building actually is. You've done the full loop now, end to end, on a project of your own. The loop is yours forever.

---

*For six missions the terminal had answered her, housed her, obeyed her. Tonight something new: it ran a thing she had* made *, and the thing she made used the machine's own powers as parts. Not her workbench anymore. Her* workshop *— and out of it, tonight, its first finished piece.*

---

### 🧪 Try It Yourself

`nano ask.py` — it's yours; renovate freely:

| Idea | How |
|---|---|
| Give it a personality | change the question line: `question = "Answer briefly and cheerfully: " + input("\nAsk: ")` |
| Give it a specialty | `question = "You are a patient Linux tutor. " + input("\nAsk about Linux: ")` |
| Count the conversation | before the loop: `count = 0` — inside it: `count = count + 1` — use it in the goodbye |
| Break it, on purpose | delete the `:` after `while True` — run — read the error like a navigator — fix. Old friends now. |

*Every change: save → run → read → adjust. Commit when you like what you've made. That's not practice for the real workflow. It* is *the real workflow.*

### ✅ What You Learned

- **`subprocess`** lets your program run other programs — the whole terminal becomes your parts bin.
- **Integration** — wiring strong pieces together — is most of what building software actually is.
- **Rough first, better second**: the builder's rhythm that makes hard things calm.
- `while True:` + `break` — programs that keep going until asked to stop (and indentation marks what repeats).
- Your work gets committed now. That's just what work gets.

### 📖 Words You Now Know

- **`import`** — bring one of Python's toolkits into your script.
- **`subprocess`** — the toolkit for running other programs from Python.
- **Integration** — connecting existing tools into something new.
- **Loop (`while True:`)** — repeat until told otherwise; `break` is "told otherwise."
- **Iteration** — rough → working → better. The actual secret of everyone who builds.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **`FileNotFoundError: ... 'ollama'`.**
  Python can't find the ollama command. Check Mission 3's install: does `ollama list` work in the terminal by itself? If you *just* installed it, close and reopen Ubuntu.

- **It hangs a long time with no answer.**
  First question after a while is slowest — the model's loading into memory (subsequent ones are quicker). If it's truly stuck: `Ctrl+C`, then check the engine — second Ubuntu window, `ollama serve`, leave it open, retry.

- **`SyntaxError` or `IndentationError`.**
  Read it like Mission 5 taught you: line number, arrow. Loop version: every line inside the loop starts with the same indent (4 spaces is the custom); the `:` after `while True` and after `if ...` is required.

- **It answers, but slowly.**
  It's genuinely thinking, on your hardware, for free. Small model, short questions, close the browser. (And notice: it bothers you less than it did in Mission 3. Your patience learned too.)

- **`can't open file 'ask.py'`.**
  You know this one. `pwd`, `cd ~/winubuntu`, `ls`. Not even a speed bump anymore.

> **The WinUbuntu promise:** tonight's errors are just the build loop breathing. Read, adjust, rerun.
> The rough version worked — everything after that is polish, and polish can't fail, only improve.

---

**Next mission:** the last one. How far do these skills actually reach? (Further than you think — we'll prove it.) Plus: a journal, read back from the beginning. And a threshold to cross that has no command at all.
