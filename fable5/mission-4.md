# Mission 4 — Making Yourself at Home

*In which Wendy gets a room of her own, and finds a door between two worlds.*

---

### Part 1 — Where Am I?

Wendy had her AI open — she'd started leaving a chat running while she worked, the way some people leave a radio on — when the question hit her.

"Wait. Hold on. When Ollama downloaded that model. A gigabyte and a half. Where did it *go*? When I'm typing in this window — where *am* I? Is there a... place? Windows has drives and folders and Documents. Does this have anything? Or is it all just—" she waved a hand, "—void?"

Ulysses looked genuinely delighted. "Do you know what kind of question that is? That's not a visitor's question. Visitors ask *what do I type*. You just asked *where do things live*. That's the question of someone about to move in."

### Part 2 — The Elephant in the Room

"Fears," he said. "Though I suspect we're down to one."

Wendy considered. "Just... getting lost, I guess? Putting something important in the wrong place and never finding it again. Or wandering somewhere I shouldn't be and knocking something over."

"That's not even a full elephant," Alex said. "That's maybe a large dog."

"Here's the safety rail," Ulysses said, "and it's absolute: the three commands you'll use most tonight — *where am I*, *what's here*, *go there* — **change nothing**. You can look around this entire system all day and leave no mark. And there's one command, two characters long, that teleports you home from anywhere, always. You cannot get lost. There is a 'take me home' button."

### Part 3 — The Answer

"Everything in Ubuntu lives in one big **tree** of folders," Alex said. "Folders inside folders, all the way down from a single root. Your personal branch of the tree is called your **home** folder — `/home/wendy` — and here's the crucial part: *the terminal is always standing somewhere in that tree.* Right now it's standing in your home folder. It has been since Mission 1 — that's what the `~` in your prompt means. Home."

"The terminal has a *location*?"

"Always. Think of it as a person standing in a room of a house. Three little words cover everything:

- **`pwd`** — *where am I standing?*
- **`ls`** — *what's in this room?*
- **`cd`** — *walk to another room.*

"And when you want to *make* something — a folder with `mkdir`, or a text file with a little editor called `nano` — it happens in the room where you're standing."

> **💡 Why it works — the tree, and why home is safe**
> Ubuntu's entire world hangs off one root folder called `/`. System machinery lives in branches
> like `/usr` and `/etc` — interesting someday, not needed now. Your branch, `/home/wendy`
> (nickname: `~`), is **yours**: everything you create goes there, and nothing you do there can
> affect the system's machinery. It's your room in the house. And because this Ubuntu lives in
> WSL's sealed guest suite, there's a second wall beyond that: even the system machinery is just
> the suite's, not your Windows machine's. Room, inside a suite, beside your house. Explore freely.

### Part 4 — Crossing the Threshold

**Step 1 — Ask where you are** *(looking changes nothing):*

```
pwd
```

**What you'll see:**

```
/home/wendy
```

"Home," said Ulysses. "The terminal's been standing here patiently for three missions. Now look around the room:"

```
ls
```

**What you'll see:** possibly very little — maybe nothing at all yet. An empty room. "Perfect," Alex said. "Blank canvas."

**Step 2 — Make a room of your own:**

```
mkdir winubuntu
cd winubuntu
pwd
```

**What you'll see:**

```
/home/wendy/winubuntu
```

"You just made a folder and *walked into it*. Look at the path — you can read it now, can't you? Home, then your folder. That's a **path** — a folder's full address in the tree."

**Step 3 — Create your first file.** "Now for `nano` — a friendly little text editor that lives right in the terminal:"

```
nano notes.txt
```

The window transforms: an editing space, with a row of shortcuts along the bottom. "This is where I tell you about the journal," Ulysses said.

"The journal?"

"One honest line, at the end of every mission, from tonight to the finish. About how it *felt* — not what you typed. Ten seconds. I won't explain why yet. You'll thank me in Mission 8."

Wendy gave him a look, but typed:

```
Mission 4. I have an address now: /home/wendy. The terminal isn't a void - it's a place, and I know where I'm standing.
```

**Saving in nano** — the bottom row shows `^O` and `^X`; the `^` means **Ctrl**:
- **Ctrl+O**, then **Enter** — save ("write **O**ut").
- **Ctrl+X** — exit.

**Step 4 — Read it back:**

```
cat notes.txt
```

Her own words, printed back by the machine. A file that hadn't existed two minutes ago, in a folder she'd made, at an address she understood.

**Step 5 — The door nobody tells you about.** Alex had been waiting, fidgeting slightly, for this part. "One more thing tonight. My favorite trick in all of WSL. Type this — note the space and the dot:"

```
explorer.exe .
```

Wendy typed it — and burst out laughing. **Windows File Explorer** opened. Regular, familiar, twenty-years-of-muscle-memory File Explorer — showing `notes.txt`, sitting in the `winubuntu` folder. Her Ubuntu folder. In Windows.

"They can *see* each other?!"

"They're neighbors, remember? This is the door between the houses. Your Ubuntu home is right there in Explorer whenever you want it — look at the address bar: a network path starting with `\\wsl.localhost\`. Windows treats your Ubuntu like a friendly neighboring computer. You can copy files either way, drag things in and out — the two worlds you thought were an either/or choice are *literally looking at each other* on your screen right now."

Wendy looked from the black terminal to the white Explorer window and back — the same file, visible in both worlds at once.

"Everyone talks about walls," she said. "Nobody mentioned there's a door."

### Part 5 — What Just Happened

Tonight had no downloads, no installs, no AI — and it might be the mission that changes the most.

Because the terminal stopped being a *service counter* — a place you go to ask for things — and became a *place*. You know where you're standing (`pwd`). You can look around (`ls`) and walk (`cd`). You built a room (`mkdir`), left a note in it (`nano`), read it back (`cat`), and found the door connecting it to the Windows home you've had all along.

Getting lost is now impossible: `cd ~` teleports you home from anywhere, always. Say it once out loud — *I cannot get lost* — because it's the fear that keeps most beginners visiting instead of moving in.

---

*It occurred to Wendy, closing the laptop, that she'd stopped thinking of the terminal as a window she opens. It was a place she* goes. *The address was even starting to feel like it meant something: /home.*

---

### 🧪 Try It Yourself

| Type this | What it does |
|---|---|
| `cd ~` then `pwd` | the teleport-home button — try it, trust it |
| `mkdir ~/winubuntu/experiments` | make a folder *inside* your folder (paths compose!) |
| `ls -l` | the detailed view: sizes, dates — the room with the lights fully on |
| `nano ~/winubuntu/notes.txt` | reopen your journal from *anywhere* — you know its address |
| `explorer.exe ~` | open your whole Ubuntu home in Windows Explorer |

*Wander. Look inside everything. `pwd` when curious, `cd ~` when done. You have the safety rail now.*

### ✅ What You Learned

- Ubuntu is one **tree** of folders; your branch is **home** — `/home/you`, nickname `~`.
- The terminal always *stands somewhere*: **`pwd`** (where?), **`ls`** (what's here?), **`cd`** (go).
- **`mkdir`** builds folders; **`nano`** writes files (Ctrl+O, Enter, Ctrl+X); **`cat`** reads them back.
- **`cd ~` = home, from anywhere, always.** You cannot get lost.
- `explorer.exe .` opens your Ubuntu folder in Windows — the worlds are connected, not opposed.

### 📖 Words You Now Know

- **Directory** — Linux's word for folder (you'll see both; same thing).
- **Home (`~`)** — your personal folder; where the terminal starts.
- **Path** — a location's full address, like `/home/wendy/winubuntu`.
- **`nano`** — the beginner-friendly terminal text editor.
- **Working directory** — wherever the terminal is currently standing (`pwd` tells you).

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"No such file or directory" when you `cd`.**
  Typo, or the folder isn't where you're standing. `ls` to see exact names — **capitalization counts** (`Winubuntu` ≠ `winubuntu`). Or `cd ~` and restart your walk from home.

- **You're lost — the prompt shows somewhere strange.**
  `pwd` to see where you are; `cd ~` to go home. This works from anywhere, every time, forever.

- **nano's `^O` `^X` symbols are confusing.**
  `^` = the **Ctrl** key. `^O` = Ctrl+O (save; press Enter after to confirm the name), `^X` = Ctrl+X (exit). If you edited and try to exit, nano asks "Save modified buffer?" — press **Y**, then **Enter**.

- **"Permission denied" when creating something.**
  You've wandered out of your home branch into system territory (looking was fine! creating, no). `cd ~` and build in your own room.

- **`explorer.exe .` did nothing / an error.**
  Note the exact form: `explorer.exe` (with `.exe`), space, dot. The dot means "this folder." If it still balks, try the long way: in Windows Explorer's address bar, type `\\wsl.localhost\Ubuntu\home\` and your username.

> **The WinUbuntu promise:** in this mission's world, an error can only ever mean "not quite" —
> never "broken." The tree doesn't punish exploring. `cd ~` is always lit.

---

**Next mission:** you can make files now. Time to make one that *does something* — your first program. Three lines of Python, and one deliberate mistake we'll make on purpose, together.
