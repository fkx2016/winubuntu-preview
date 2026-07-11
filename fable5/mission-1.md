# Mission 1 — Why Does AI Keep Sending Me to Ubuntu?

*In which a paused video finally gets unpaused.*

---

### Part 1 — The Blinking Cursor

The video was paused again. Same video. Same sentence.

*"...just open your Ubuntu terminal—"*

But tonight Wendy wasn't alone with it. Ulysses and Alex sat across the kitchen table, and on the laptop screen, behind the frozen video, a small black window waited. A single line of text. A cursor, blinking.

On. Off. On. Off.

"Twenty years," Wendy said. "I've used Windows for twenty years. I've fixed printers. I've survived every redesign they ever shipped. And now every tutorial on earth ends with a sentence that assumes I know an entirely different operating system. When did that happen? *Why* did that happen?"

Ulysses leaned forward. "Can I tell you something about that question? It's better than you think it is. Most people never ask it — they just quietly decide the door is locked and walk away."

"The door being…?"

He nodded at the black window. At the cursor. On. Off. On.

"It's not blinking at you like a warning," Alex said. "It's blinking like a doorbell. It's been *waiting.*"

### Part 2 — The Elephant in the Room

"Before I answer anything," Ulysses said, "let's do the honest part. You're wondering things you haven't said out loud. Probably these three: *Am I already too late? Will I break my computer if I try this? Is Linux only for experts?*"

Wendy laughed — startled. "…All three. In that order."

"Good. The honest answers are **no, no, and no** — and I'm going to earn each one, not just say them.

"*Too late?* The AI era is a few years old. The people who seem 'years ahead' mostly started eighteen months before you. You're not late to a lifetime; you're late to a *semester*, and this book is the catch-up course.

"*Break your computer?* What we install today lives in a sealed compartment. Windows won't just survive it — Windows won't even be inconvenienced by it. I'll show you exactly why in a minute, because you deserve the reason, not just the reassurance.

"*Only for experts?* Ubuntu is specifically the version of Linux built on the opposite belief. Its whole reason for existing is that this stuff should be usable by humans."

### Part 3 — The Answer

"So here's the real answer to your question," Ulysses said. "Why does AI keep sending you to Ubuntu?

"Because the tools of AI **grew up on Linux**. The servers that train AI models — Linux. The cloud machines that run them — overwhelmingly Linux. The open-source projects, the frameworks, the tutorials, the documentation — written by people working on Linux, for people working on Linux. It's not a conspiracy and it's not snobbery. It's just *where that world happened to grow up*, the way film grew up in Hollywood.

"And **Ubuntu** is the friendliest, most popular neighborhood of the Linux world. So when a tutorial says *'open your Ubuntu terminal,'* it isn't demanding you abandon Windows. It's speaking the shared language of the place where the tools were born."

"But I don't *have* Ubuntu," Wendy said. "That's the entire problem. I have Windows."

Alex smiled, and turned his laptop around. "That's the part nobody puts at the start of their videos. You don't have to choose. Microsoft — *Microsoft themselves* — built a way to run a real, genuine Ubuntu **inside** Windows. Not a website pretending. Not a slow imitation. The real thing, in its own space, side by side with everything you already have. It's called **WSL** — the Windows Subsystem for Linux."

"Microsoft built a way to run *Linux*? On purpose?"

"On purpose, a decade ago, and they've been polishing it ever since. Windows developers begged for it. It might be the most beginner-friendly thing Microsoft has ever shipped, and almost no beginner has heard of it."

> **💡 Why it works — what WSL actually is**
> WSL runs a genuine Ubuntu in a lightweight, sealed compartment alongside Windows. The honest
> analogy is a **guest suite**: it has its own door, its own space, its own things — but it's
> inside your house, so visiting takes two seconds. Your Windows files, apps, and settings are
> not touched, moved, or modified. Nothing about your hard drive is "partitioned" or erased.
> And if you ever want the guest gone, one command removes it entirely — Windows wouldn't even
> notice it had been there. That sealed design is *why* today is safe: you're not renovating
> your house. You're furnishing a spare room.

### Part 4 — Crossing the Threshold

Alex closed the video — the paused one, the one from a month of Tuesdays. "You don't need it anymore. Let's open the door ourselves."

Wendy's stomach tightened, and she said so. Nobody told her it shouldn't.

"Tightened stomach and doing it anyway," said Ulysses, "has a name. It's called *courage*. Ready?"

> **✅ 30-second readiness check**
> - You're on **Windows 10 (updated recently) or Windows 11**. Nearly any machine from the last few years qualifies.
> - You have about **20 minutes**, including one restart.
> - That's the whole list. Nothing to buy, nothing to download by hand, no account to create.

**Step 1 — Open PowerShell as Administrator.**

Click **Start**, type `powershell`, then **right-click** on *Windows PowerShell* and choose **Run as administrator**. Windows will ask if you're sure — click **Yes**.

> *Why "as administrator"?* You're about to install an entire operating environment — a genuinely
> powerful action. Windows just wants you to say "yes, I meant to do that" in a way an accidental
> click can't. Right-click → Run as administrator is how you say it. This is a seatbelt, not an exam.

A blue window opens with a prompt. Notice something: *you're already in a terminal.* This one belongs to Windows — you've been living one keystroke away from a terminal for twenty years and nobody mentioned it.

**Step 2 — Type the one command that does everything:**

```
wsl --install
```

Press Enter. **What you'll see:** a few lines appearing over a couple of minutes, something like —

```
Installing: Virtual Machine Platform
Installing: Windows Subsystem for Linux
Downloading: Ubuntu
Installing: Ubuntu
The requested operation is successful. Changes will not be effective until the system is rebooted.
```

"That's… it?" Wendy said. "One command? The thing I've been dreading for a month is *one command*?"

"One command," Alex said. "Microsoft did the other ten thousand steps for you. When it asks for a **restart**, let it."

**Step 3 — Restart, then open Ubuntu.**

After the reboot, click **Start**, type `ubuntu`, and click the orange **Ubuntu** icon. A black window opens:

```
Installing, this may take a few minutes...
```

Let it finish — this is the last step settling in. Then it asks you to create a **username** (lowercase, no spaces — your first name is perfect) and a **password**.

> **⚠️ The password will look broken. It isn't.**
> When you type the password, the screen shows **nothing**. No dots. No stars. No movement at all.
> This is the single most common panic moment for new Linux users, so hear it clearly in advance:
> Linux hides passwords *completely* — even their length — as a privacy habit from its shared-computer
> ancestry. **It is registering every keystroke.** Type the password, press Enter, type it again to
> confirm, press Enter. Blind, and correct.

Wendy typed her name. Then the password — staring at a screen that showed nothing, trusting her fingers. "This feels like typing with my eyes closed."

"It is exactly that," said Ulysses. "And you just did it. Look up."

```
wendy@wendy-pc:~$
```

"That," he said quietly, "is Ubuntu. A real one. Running inside the Windows machine you've had all along. Say hello."

**Step 4 — Your first two commands.**

Type this and press Enter:

```
whoami
```

**What you'll see:**

```
wendy
```

Wendy blinked. Then laughed. "It knows my name."

"It knows the name you gave it two minutes ago," Alex grinned. "But yes. Now ask it what *it* is:"

```
lsb_release -a
```

**What you'll see** (your version number may differ — that's fine):

```
Distributor ID: Ubuntu
Description:    Ubuntu 24.04 LTS
Release:        24.04
Codename:       noble
```

Wendy sat back and looked at the little black window — really looked at it. The same kind of window that had been pausing her videos for a month.

"I'm in Ubuntu," she said. "Inside Windows. And nothing broke. My files are all still—" she flipped to her desktop: photos, documents, everything, untouched — "…everything's still *here*."

"Everything's still here," Ulysses agreed. "You didn't move. You just gained a room."

### Part 5 — What Just Happened

Count what you actually did tonight: opened one program, typed one command, restarted, chose a name, typed two more commands. Ten minutes of doing.

Now count what you proved: *you're not too late* — you're in. *You didn't break anything* — go look, it's all there. *It isn't only for experts* — you did it at a kitchen table with cold tea.

Three fears, held for a month, disproven in ten minutes. That ratio — a month of dread to ten minutes of doing — is worth remembering, because you'll meet it again. It's nearly always the ratio.

Every tutorial on the internet that says *"open your Ubuntu terminal"* is now speaking to **you**.

---

*The cursor blinked on, off, on — exactly as it had in the paused video, exactly as it had for a month of Tuesdays. Nothing about it had changed. But tonight it didn't look like a test. It looked like a door, standing open.*

---

### 🧪 Try It Yourself

These commands only *ask* — none of them change anything. Type each one, press Enter, and see what your new Ubuntu says back:

| Type this | What it does |
|---|---|
| `date` | shows the current date and time |
| `cal` | prints a little calendar of this month |
| `pwd` | tells you which folder you're standing in (more on this in Mission 4) |
| `echo "Hi from Ubuntu"` | repeats your words back to you |
| `uname -a` | the machine's technical self-introduction (it's fine not to understand it — just wave) |

*If a command does something unexpected: nothing broke. You cannot damage anything by asking questions. That's not a pep talk — it's how these commands are built.*

### ✅ What You Learned

- The AI world says "Ubuntu" because its tools **grew up on Linux** — it's geography, not gatekeeping.
- Windows can run a **real Ubuntu inside itself** using **WSL** — sealed, safe, removable.
- The whole install is **one command** (`wsl --install`) and one restart.
- Linux hides passwords completely while you type them — **blank is normal.**
- A terminal is just a way of talking to a computer in words instead of clicks — and you now have two of them.

### 📖 Words You Now Know

- **Terminal** — the text window where you type commands and read answers.
- **WSL (Windows Subsystem for Linux)** — Microsoft's technology for running Ubuntu inside Windows.
- **Ubuntu** — the friendly, hugely popular Linux the AI world treats as home ground.
- **Command** — one instruction, typed and sent with Enter (like `whoami`).
- **Prompt** — the line ending in `$` that means *"ready when you are."*

---

### 🔧 If Something Went Wrong — Troubleshooting

*Every one of these has a calm fix, and none of them mean your computer is harmed.*

- **`wsl --install` printed a page of help text instead of installing anything.**
  Your Windows is slightly older, from before this command's one-step version. Run **Windows Update** (Settings → Windows Update), install everything, restart, and try again. If it still shows help text, use the explicit form: `wsl --install -d Ubuntu`.

- **"The requested operation requires elevation" or "Access is denied."**
  PowerShell wasn't opened as administrator. Close it and redo Step 1: Start → type `powershell` → **right-click → Run as administrator**.

- **An error mentioning "Virtual Machine Platform," virtualization, or the code `0x80370102`.**
  A hardware feature called *virtualization* is switched off in your machine's firmware. It's common, harmless to enable, and one-time: search the web for your PC model plus "enable virtualization in BIOS," flip the setting, and re-run the install. (Many machines already have it on — you may never see this.)

- **"WSL is already installed" or you see WSL-related messages you don't understand.**
  Someone (possibly past-you, possibly a work IT policy) enabled WSL before. Try `wsl --install -d Ubuntu` to add Ubuntu specifically, and `wsl --update` to freshen the plumbing. Then continue from Step 3.

- **After the restart, Ubuntu didn't open by itself.**
  Completely normal — it doesn't always auto-launch. Start menu → type `ubuntu` → click the icon. It'll finish setting up and ask for your username.

- **The username was rejected.**
  Use all lowercase letters, no spaces, no capital letters — `wendy`, not `Wendy K`.

- **The password "won't type."**
  It *is* typing — see the ⚠️ box above. Blank screen while typing a password is Linux working correctly. Type it blind, press Enter.

- **The Ubuntu window opened but shows an error instead of asking for a username.**
  Close the window. In PowerShell, run `wsl --shutdown`, wait ten seconds, and open Ubuntu from the Start menu again. This "turn it fully off and on again" resolves most first-launch hiccups.

> **The WinUbuntu promise:** if you hit something not on this list, you haven't failed and you haven't
> broken anything — you've found exactly the kind of moment this book exists for. Copy the message you
> see. In a few missions, you'll have an AI on your own machine you can paste it to.

---

**Next mission:** you have a working Ubuntu, and it's nearly empty — a new apartment with no furniture. Time to learn the single pattern that furnishes it: how to install *anything*. We'll practice on something deliberately ridiculous.
