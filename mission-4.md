
# Mission 4 (Full Depth) — Making Yourself at Home

*WinUbuntu · published-depth version.*

---

### Part 1 — Where Am I?

Wendy typed a command, then paused. "Okay, weird question. Where *am* I right now? When I save something, where does it go?"

Alex grinned. "Now you're thinking like someone who lives here — not just visits."

### Part 2 — The Elephant (a smaller one now)

Ulysses noticed the fear had shrunk. "Only one worry left, I think: *what if I get lost, or put something in the wrong place?*"

"A little," Wendy admitted.

"Then here's your safety net: in Ubuntu you can always ask *'where am I?'* and *'what's here?'* — and neither changes a thing. You can look around all day without breaking anything."

### Part 3 — The Answer

"A terminal is just standing inside a folder," Alex said. "Three little words let you look around and move:
**`pwd`** — *where am I?* · **`ls`** — *what's here?* · **`cd`** — *go there.*
And **`nano`** lets you *create and edit* a file, right in the terminal."

> **💡 Why it works — Folders are a tree, and you're always standing in one**
> Ubuntu organizes everything as folders inside folders — a *tree*. Your personal branch is called
> your **home** folder (`/home/yourname`), and you can shorten it to just `~`. The terminal is always
> "standing" in one folder at a time; `pwd` tells you which, `cd` walks you to another. Nothing you
> do in your home folder can hurt the system — it's your own room in the house.

### Part 4 — Crossing the Threshold

**Step 1 — Look around** *(these only look; they change nothing):*

```
pwd
ls
```

**What you'll see:** `pwd` prints your home, e.g. `/home/wendy`. `ls` lists what's in it (maybe just a few default folders for now).

**Step 2 — Make a room of your own:**

```
mkdir winubuntu
cd winubuntu
```

You created a folder and stepped inside it. Run `pwd` again — the path now ends in `/winubuntu`. You've moved.

**Step 3 — Create your first file** with the `nano` editor:

```
nano notes.txt
```

A simple editor fills the screen. Type a line:

```
Day 4. The terminal is starting to feel like mine.
```

Save and exit (the shortcuts run along the bottom, where **^** means the **Ctrl** key):
- **Ctrl+O**, then **Enter** — *save* ("write Out").
- **Ctrl+X** — *exit*.

**Step 4 — Read it back:**

```
cat notes.txt
```

**What you'll see:** your own words, printed back. "I made a file," Wendy said. "From nothing. And I know exactly where it is."

### Part 5 — What Just Happened

The terminal stopped being a place you *visit*. It became a place you *live* — you can look around, make a room, and leave notes for yourself.

*The Terminal will never change. You already have.*

---

### 🧪 Try It Yourself

| Type this | What it does |
|---|---|
| `cd ~` then `pwd` | jump back to home from anywhere, and confirm where you are |
| `mkdir projects` then `ls` | make another folder and see it appear |
| `ls -l` | list with details (size, date) |
| `cd winubuntu` then `nano notes.txt` | reopen your note and add a second line |

*`cd ~` is your "take me home" button. You can never truly get lost.*

### ✅ What You Learned

- Files live in a **tree of folders**; your branch is **home** (`~`).
- **`pwd`** = where am I, **`ls`** = what's here, **`cd`** = go there — and looking never changes anything.
- **`mkdir`** makes a folder; **`nano`** creates and edits files; **`cat`** shows a file's contents.
- Saving in `nano`: **Ctrl+O**, Enter, then **Ctrl+X**.

### 📖 Words You Now Know

- **Directory / folder** — a container for files (and other folders).
- **Home (`~`)** — your personal folder.
- **Path** — a folder's full address, like `/home/wendy/winubuntu`.
- **`nano`** — the beginner-friendly text editor built into Ubuntu.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"No such file or directory" when I `cd`.**
  A typo, or that folder isn't here. Run `ls` to see the exact names (they're case-sensitive!), or `cd ~` to reset to home and start again.

- **I feel lost — I don't know where I am.**
  Type `pwd` to see, or `cd ~` to teleport home. This always works.

- **In `nano`, the `^O` / `^X` symbols confuse me.**
  `^` just means the **Ctrl** key. `^O` = hold Ctrl and press O. So: **Ctrl+O**, Enter (save), then **Ctrl+X** (exit).

- **"Permission denied" making a folder.**
  You wandered outside your home folder into a system area. Run `cd ~` first, then create your folders there — that's your space.

> **The WinUbuntu promise:** an error here means "not quite," never "broken." `cd ~` is always your way back.

---

**Next mission:** you can make files now. Let's make one that *does* something — your first line of Python.


---
