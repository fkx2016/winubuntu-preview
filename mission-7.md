
# Mission 7 (Full Depth) — Your First Real Project

*WinUbuntu · published-depth version.*

---

### Part 1 — The Pieces on the Table

Wendy looked at her screen and, for the first time, saw not a list of scary words but a set of *tools she owned.*

"I have Python. I have an AI that runs on my own machine. I can make files and move around. Could I… put them together? Make something that's actually *mine*?"

Alex leaned forward. "That's the whole point. Let's build it."

### Part 2 — The Elephant (almost gone)

Ulysses smiled. "Any fear left?"

"Honestly? Less fear. More — *can I really?*"

"That question answers itself the moment you hit Enter."

### Part 3 — The Answer

"You'll write a small Python program," Alex said, "that takes a question from you, hands it to your *local* AI, and prints the answer. Python talking to Ollama. Two things you already have — introduced to each other."

> **💡 Why it works — Programs can run other programs**
> Your script uses one new idea: Python's **`subprocess`** tool, which lets one program *run
> another and capture what it says back*. You already run `ollama` by hand; here, Python runs it
> for you, hands it your question, and catches the answer to print. That's *integration* — wiring
> tools together — and it's the heart of almost everything people "build" with AI.

### Part 4 — Crossing the Threshold

> **✅ First:** make sure Mission 3's Ollama is installed (`ollama list` should show your model).

**Step 1 — Go to your folder and create the program:**

```
cd ~/winubuntu
nano ask.py
```

**Step 2 — Type your first real app** (shorter than you'd think):

```python
import subprocess

question = input("Ask your local AI something: ")

result = subprocess.run(
    ["ollama", "run", "llama3.2:1b", question],
    capture_output=True, text=True
)

print("\nYour AI says:\n" + result.stdout)
```

Save and exit: **Ctrl+O**, **Enter**, **Ctrl+X**.

**Step 3 — Run your creation:**

```
python3 ask.py
```

**What you'll see:**

```
Ask your local AI something: Give me one tip for a nervous new Linux user.

Your AI says:
Take it one command at a time — you can't break anything by looking around...
```

It asked her a question. She typed one of her own. And a moment later, *her program* — running *her* AI, on *her* machine — printed an answer back.

Wendy sat very still. "I built that. It's not a website someone made. It's a thing *I* made, and it works."

"It's a thing you made. And it will still be here tomorrow, waiting for you to make it better."

### Part 5 — What Just Happened

Seven missions ago, "open your Ubuntu terminal" stopped a video cold and made you feel behind.

Today you *wrote a program that runs your own AI.*

That's not keeping up. That's building.

*Technology stopped being the destination. It became your toolbox.*

---

### 🧪 Try It Yourself

Reopen `nano ask.py` and make it smarter:

| Idea | How |
|---|---|
| Shape the answer | Change `question` to `"Answer in one short sentence: " + question` |
| Give it a job | Set a fixed prompt like `question = "Explain " + input("Explain what? ")` |
| Try a different brain | Swap `"llama3.2:1b"` for another model you've pulled (`ollama list`) |

*Change one line, run it, watch it behave differently. You now own the whole loop: write → run → improve.*

### ✅ What You Learned

- You **combined tools** — Python + your local AI — into a program that's yours.
- **`subprocess`** lets one program run another and capture its output.
- You went from writing two lines (Mission 5) to building a small, working AI app.
- The build loop — **write, run, improve** — is now yours to repeat on anything.

### 📖 Words You Now Know

- **`import`** — bring an extra Python tool into your script.
- **`subprocess`** — run another program from inside Python.
- **Integration** — wiring separate tools together into one thing.
- **Build loop** — write → run → see → improve, repeated.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"FileNotFoundError: 'ollama'."**
  Python can't find Ollama. Confirm Mission 3 finished (`ollama list` should work in the terminal). If you *just* installed it, close and reopen Ubuntu so the new command is found.

- **It hangs, or says it can't connect to Ollama.**
  The model server needs to be up. Open a second Ubuntu window, run `ollama serve`, leave it running, and try `python3 ask.py` again.

- **"SyntaxError" or "IndentationError."**
  Reopen `nano ask.py`. The lines inside `subprocess.run( ... )` should match the example, and the whole block shouldn't have stray spaces at the far left. Straight quotes only: `"like this"`.

- **The answer is slow.**
  Normal on a small local model — it's genuinely thinking on your hardware. Keep the model small and questions short.

- **"can't open file 'ask.py'."**
  Wrong folder. `cd ~/winubuntu`, then `ls` to confirm `ask.py` is there, then run it.

> **The WinUbuntu promise:** a program that errors isn't broken *you* — it's a puzzle with a message
> attached. Read the last line; it almost always names the fix.

---

**Next mission:** the last one — where the bridge leads, and the surprising person you've become on the way across.


---
