
# Mission 1 (Full Depth) — Why Does AI Keep Sending Me to Ubuntu?

*WinUbuntu · "Published depth" sample — the same Mission, layered with output, sidebars,
troubleshooting, and an exercise, to show what a full book page count looks like.*

---

### Part 1 — The Blinking Cursor

The blinking cursor waited.

Wendy stared at the screen. Every article, every video, every AI tutorial from the past month seemed to end the same way.

*"Open your Ubuntu terminal."*

"I've used Windows for over twenty years," she said. "Why does everyone suddenly expect me to know Ubuntu?"

Across the table, Ulysses smiled. "That's a better question than you realize."

Alex closed his laptop. "And it's exactly the question that brought us here."

The cursor kept blinking. Patient. Waiting.

Not as a warning. **As an invitation.**

### Part 2 — The Elephant in the Room

Before Ulysses answered, he did something unexpected. He named the fear out loud.

"You're probably wondering a few things you haven't said. *Am I already too late? Will I break my computer if I try this? Is Linux only for experts?*"

Wendy laughed, startled. "All three, actually."

"Good. Because the honest answers are: no, no, and no. You're not behind — you just reached a door everyone else walked through, and nobody told you it was unlocked."

### Part 3 — The Answer

"The tools of AI grew up on Linux," Ulysses said. "The servers that run AI, the frameworks that build it, the open-source projects everyone shares — almost all of them were born there. And **Ubuntu** is the friendliest, most popular Linux there is. So *'open your Ubuntu terminal'* isn't asking you to abandon Windows. It's speaking the shared language of that whole world."

"But I don't *have* Ubuntu," Wendy said. "I have Windows."

"That's the part nobody tells you," said Alex. "You don't have to choose. Microsoft built a way to run a *real* Ubuntu **inside** Windows — in its own space. It's called **WSL** — Windows Subsystem for Linux. Windows stays exactly as it is. Ubuntu just moves in next door."

> **💡 Why it works — What WSL actually is**
> WSL runs a genuine Linux system in a lightweight, sealed compartment alongside Windows —
> think of it as a *guest suite* with its own door. Your Windows files, apps, and settings
> are untouched. If you ever wanted Ubuntu gone, you could remove it in one step and Windows
> wouldn't notice. That sealed-off design is exactly why experimenting here is *safe*: there's
> very little you can break, and nothing that reaches back into Windows itself.

### Part 4 — Crossing the Threshold

Alex smiled. "Let's stop talking about the door. Let's open it."

Wendy's stomach tightened. But she nodded. *"I'll try."*

> **✅ 30-second readiness check** *(before you begin)*
> - You're on **Windows 10 (recent update) or Windows 11**. Most machines from the last few years qualify.
> - You can **restart** your computer in a few minutes (the install asks for one reboot).
> - That's it. No downloads to hunt for, no accounts to make.

**Step 1 — Open PowerShell as Administrator.**
Click the Start menu, type **PowerShell**, right-click **Windows PowerShell**, and choose **Run as administrator**. Click **Yes** when Windows asks permission.

> *Why "as administrator"?* Installing a whole new system is a powerful action, so Windows
> wants you to confirm you meant it. Right-click → Run as administrator is how you say "yes, I do."

**Step 2 — Run the one command that does everything:**

```
wsl --install
```

**What you'll see:** a few lines scroll by as Windows fetches and enables the pieces — something like:

```
Installing: Virtual Machine Platform
Installing: Windows Subsystem for Linux
Installing: Ubuntu
The requested operation is successful. Changes will not be effective until the system is rebooted.
```

"That's it?" Wendy asked.

"That's it. It's fetching Ubuntu and settling it in. When it asks you to **restart**, let it."

**Step 3 — Restart, then open Ubuntu.**
After the reboot, open the Start menu, type **Ubuntu**, and click it. A black window opens and says *"Installing, this may take a few minutes…"* — the last step finishing. Then it asks you to **create a username and password.**

> **⚠️ The password looks broken — but it isn't.**
> When you type your new password, **the screen shows nothing** — no dots, no stars, no movement.
> This is the single most common moment beginners panic. Don't. Linux hides passwords completely
> as a privacy habit. Just type it, press **Enter**, type it again to confirm, and continue. It
> *is* registering every keystroke.

Wendy typed her name. Chose a password (seeing nothing, trusting it anyway). And a new line appeared:

```
wendy@wendy-pc:~$
```

"That," said Ulysses quietly, "is Ubuntu. Running inside your Windows machine. Say hello to it."

**Step 4 — Your first two commands.**

```
whoami
```

**What you'll see:**

```
wendy
```

She laughed. "It knows my name."

"Ask it what it is," said Alex.

```
lsb_release -a
```

**What you'll see** (the version may differ — that's fine):

```
Distributor ID: Ubuntu
Description:    Ubuntu 24.04 LTS
Release:        24.04
Codename:       noble
```

Wendy sat back. "I'm… in Ubuntu. Inside Windows. And nothing broke."

"Nothing broke," Ulysses agreed. "The cursor answered you. It had been waiting to."

### Part 5 — What Just Happened

You didn't just install software. You crossed a threshold — and proved three fears wrong in about five minutes: *you're not too late, you didn't break anything, and the terminal isn't only for experts.*

Every tutorial that says *"open your Ubuntu terminal"* is now talking to **you**.

*The Terminal will never change. You will. You just did.*

---

### 🧪 Try It Yourself

You can't hurt anything here — these just *ask*, they don't change. Type each, press Enter, and see what your new Ubuntu says back:

| Type this | What it does |
|---|---|
| `date` | shows the current date and time |
| `cal` | prints a little calendar of this month |
| `pwd` | tells you which folder you're standing in |
| `echo "Hi from Ubuntu"` | repeats your words back to you |

*Experimenting is the whole point. If a command ever does something you didn't expect, nothing is broken — you're learning.*

### ✅ What You Learned

- Windows can run a real **Ubuntu inside itself**, safely, using **WSL**.
- You install it with **one command** (`wsl --install`) and one restart.
- The **terminal** is just a way to talk to the computer with words instead of clicks.
- You ran your **first commands** — and discovered that mistakes here are cheap, not catastrophic.

### 📖 Words You Now Know

- **Terminal** — the text window where you type commands.
- **WSL (Windows Subsystem for Linux)** — the technology that runs Ubuntu inside Windows.
- **Ubuntu** — the friendly, popular version of Linux the AI world uses.
- **Command** — a short instruction you type and run (like `whoami`).

---

### 🔧 If Something Went Wrong — Troubleshooting

*Every one of these has a calm fix. Nothing here can harm your computer.*

- **`wsl --install` just printed a wall of help text instead of installing.**
  Your Windows is a little older. Run **Windows Update** first (Settings → Windows Update), restart, and try again. Still stuck? Try `wsl --install -d Ubuntu`.

- **It said "The requested operation requires elevation" or "Access is denied."**
  PowerShell wasn't opened as administrator. Close it, then re-open: Start → type PowerShell → **right-click → Run as administrator**.

- **It mentioned "Virtual Machine Platform," a virtualization error, or error `0x80370102`.**
  A setting called *virtualization* is switched off in your computer's firmware. It's common and harmless to enable. Search your PC model + "enable virtualization in BIOS," flip it on, and re-run. (Many machines have it on already.)

- **After the restart, Ubuntu didn't open by itself.**
  That's normal — just open it: Start menu → type **Ubuntu** → click it. It'll finish the last step and ask you to create your username.

- **The password won't type.**
  It *is* typing — Linux just hides it (see the ⚠️ note above). Type it, press Enter, confirm it, continue.

> **The WinUbuntu promise:** if you hit something not on this list, you haven't failed and you
> haven't broken anything. You've found the exact kind of moment this book exists for. Note the
> message you saw, and we'll walk through it together.

---

**Next mission:** now that the door is open, we'll teach Ubuntu to *do* something for you — your first real tool, installed by your own hand.


---
