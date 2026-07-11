# Mission 2 — Your First Tool, Installed by Your Own Hand

*In which an empty room gets its first furniture, and it is a cow.*

---

### Part 1 — The Empty Room

Wendy opened Ubuntu the next evening without being told to.

She noticed that about herself — that she'd *wanted* to check it was still there. The window opened, and there it was, patient as ever:

```
wendy@wendy-pc:~$
```

She typed `whoami`, just to feel it answer. `wendy`. Still her.

"Okay," she said, when Ulysses and Alex arrived. "I'm in. I can get in whenever I want, apparently. But…" she gestured at the window. "Now what? I have a terminal that knows my name and tells me the date. That's a very polite empty room. Windows has *programs*. Where are the programs?"

Alex pulled up a chair. "That question — *now what* — is the exact right question, and today's answer might be the single most useful thing in this entire book. Not the most exciting. The most *useful*. Today you learn how software gets into Ubuntu."

"Please don't say 'go to twelve websites and download twelve installers.'"

"I am delighted to tell you it is the opposite of that."

### Part 2 — The Elephant in the Room

"Fears first," Ulysses said. "Smaller ones than last time, I'd guess, but say them."

Wendy counted on her fingers. "What if I install the wrong thing. What if I fill this thing up with junk I can't get rid of — my Windows machine has twenty years of mystery files and I *swore* this one would stay clean. And… installing software sounds like something where a typo does real damage."

"Notice something," Ulysses said. "Last mission your fears were *am I too late, will I break everything, is this even for me*. Tonight they're *what if I'm untidy*. Your elephants are getting smaller."

She blinked. "…Huh."

"Here's tonight's promise, which I'll prove before we're done: Ubuntu installs software the *clean* way. Everything comes from one trusted place, everything is tracked, and anything you install can be removed so completely it's like it was never there. You'll install something tonight — and then, to prove it, you'll *uninstall* it and watch it vanish without a trace."

### Part 3 — The Answer

"You know the Microsoft Store?" Alex asked. "Or the app store on your phone? One trusted catalog, you ask for a thing by name, it arrives, it's tracked, you can remove it cleanly?"

"Sure."

"Ubuntu had that idea *decades* before phones existed. It's called **apt**, and you use it right here in the terminal. No hunting the web for installers. No 'Download' buttons that are secretly ads. No next-next-next-finish. You ask the catalog for a tool by name, and it handles everything."

"The pattern has two beats," Ulysses said, holding up fingers. "**Refresh the catalog. Install the thing.** That's the whole dance:

"`sudo apt update` — *'check for the newest catalog.'*
"`sudo apt install <name>` — *'get me this, please.'*"

"What's `sudo`?" Wendy asked.

"The most famous word in Linux. It means *'super-user do'* — you're telling Ubuntu, *this action is powerful, and I mean it*. Ubuntu will ask for your password when you use it. Which reminds me — what do you already know about typing passwords here?"

Wendy smiled slowly. "The screen shows nothing. And it's working anyway."

"Mission 1 is still in there," said Alex. "Told you it would be."

> **💡 Why it works — what `apt` really does**
> `apt` is Ubuntu's **package manager**. Software comes in tracked bundles called **packages**,
> and they live in **repositories** — huge, curated, security-reviewed catalogs maintained by the
> Ubuntu project. When you `apt install` something, apt fetches it from the catalog, installs it,
> and — this is the key — **writes down everything it did.** That memory is why removal is truly
> clean: apt doesn't have to guess what to delete; it has the receipt. Compare that with the
> Windows ritual of downloading `setup.exe` from a website you hope is the real one. Here, there's
> one source, it's trusted, and everything is reversible. You will never clutter this system the
> way stray downloads clutter a Windows machine — the design doesn't allow it.

### Part 4 — Crossing the Threshold

"Now," Alex said, rubbing his hands together, "we could install something *serious* for your first time. A developer tool. Something impressive."

"But we won't?"

"But we won't. We're going to install the silliest program in the entire Ubuntu catalog — *on purpose*. Because I want your memory of 'the first thing I ever installed on Linux' to make you laugh, not sweat. Fear can't survive contact with what we're about to do."

**Step 1 — Refresh the catalog:**

```
sudo apt update
```

It asks for your password — type it blind, like a pro, press Enter. **What you'll see:** a waterfall of lines — `Get:1 ...`, `Hit:2 ...`, URLs scrolling past — ending with something like:

```
Reading package lists... Done
Building dependency tree... Done
```

"That's a lot of output," Wendy said, watching it scroll. "Did I just change something?"

"Not one thing. You asked the library for its newest card catalog, and it read the whole thing out loud while handing it over. Linux is chatty like that — lots of output usually just means *working, and narrating*. Silence or a short 'Done' at the end is success."

**Step 2 — Install the tool:**

```
sudo apt install cowsay -y
```

*(The `-y` means "yes, go ahead" — it skips the 'are you sure?' pause. And notice: no password prompt this time. `sudo` remembers you for a few minutes.)*

**What you'll see:** a few brisk lines, ending near:

```
Setting up cowsay (3.03+dfsg2-8) ...
```

"Cowsay," Wendy said flatly. "I have a feeling about this."

**Step 3 — Use your new tool:**

```
cowsay "I did it"
```

**What you'll see:**

```
 __________
< I did it >
 ----------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

Wendy laughed — the real kind, the kind that surprises you. "A cow. A cow is saying my words. This is what the terrifying Linux terminal does?"

"This is what it does when you tell it to," Alex said. "It does what you tell it to. That's the entire secret of the whole thing."

**Step 4 — Now the proof.** "Remember your fear about junk you can't remove?" Ulysses said. "Watch closely."

```
sudo apt remove cowsay -y
```

A few lines. `Removing cowsay...` Done. Now try the cow:

```
cowsay "hello?"
```

```
Command 'cowsay' not found...
```

"Gone," Ulysses said. "Completely. Not 'moved to a recycle bin.' Not 'uninstalled but left seventeen mystery folders.' Gone, because apt had the receipt. **That** is why you'll never fear installing things here — every door you open, you can close."

Wendy stared at the message. "…Can I have the cow back?"

"You know how."

She typed `sudo apt install cowsay -y` — no hesitation, no notes, from memory — and the cow returned. Second install of her life. It had taken her nine seconds.

### Part 5 — What Just Happened

Look at the command you now know:

```
sudo apt install <name> -y
```

Tonight, `<name>` was a talking cow. But this is — character for character — the **exact command** that installs Python's tools, Git, and nearly every piece of AI software you will ever be told to get. When a tutorial says *"install the dependencies,"* this is what they mean. You didn't learn a party trick tonight. You learned the master key, and practiced it on a door that couldn't possibly hurt you.

One more thing. Alex leaned over. "Type this. Small gift before we go."

```
python3 --version
```

```
Python 3.12.3
```

"That's Python," he said. "The language nearly all of AI is built in. It didn't install just now — it was *already here*. Ubuntu ships with it. It's been sitting in your machine since Mission 1, waiting for Mission 5."

*You didn't fill your computer with junk — you proved you can't. You didn't need to be a programmer. You installed, removed, and reinstalled software by hand, from a catalog you can trust, with a pattern you already know by heart.*

---

*The terminal had answered her every time tonight — catalog, cow, removal, cow again. Not an empty room anymore. A room that brings you things when you ask. She caught herself thinking of it, for the first time, as* handy.

---

### 🧪 Try It Yourself

You hold a master key. Try it on two more harmless tools:

| Type this | What happens |
|---|---|
| `sudo apt install fortune-mod -y` then `fortune` | installs a tool that tells (occasionally wise) fortunes |
| `sudo apt install figlet -y` then `figlet hello` | prints your words in giant letters |
| `fortune \| cowsay` | the fortune teller and the cow, working together — your first *pipeline* (more someday) |
| `apt list --installed \| wc -l` | count how many packages your system has (the number is big — Ubuntu itself is packages all the way down) |

*Install freely. You've already proven you can undo any of it.*

### ✅ What You Learned

- Ubuntu installs software with **`apt`**, from one trusted, curated catalog — no web-hunting, no installers.
- The pattern forever: **`sudo apt update`** (refresh) → **`sudo apt install <name> -y`** (get).
- **`sudo`** = "this is powerful and I mean it"; it asks your password (typed invisibly — old news to you now).
- Removal is *genuinely* clean — `sudo apt remove <name>` — because apt keeps the receipt.
- **Python was already on your machine.** The AI world's language ships with Ubuntu.

### 📖 Words You Now Know

- **Package** — a tracked bundle of software apt can install or remove.
- **Package manager (`apt`)** — the tool that fetches, installs, tracks, and removes packages.
- **Repository** — the trusted online catalog packages come from.
- **`sudo`** — "super-user do": run one command with elevated permission.
- **`-y`** — "yes, proceed" — skips the confirmation pause.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"Unable to locate package cowsay."**
  The catalog is stale (or Step 1 got skipped). Run `sudo apt update` first, then retry the install.

- **"Could not get lock /var/lib/dpkg/lock-frontend… is another process using it?"**
  Ubuntu is quietly installing its own updates in the background — common in a system's first days. Wait a minute or two and try again. (Both of you can't use apt at once; it's a one-key kitchen.)

- **"E: Failed to fetch…" or the download hangs.**
  A network hiccup inside WSL. Check your internet works in Windows, then retry. If it keeps failing: close Ubuntu, open PowerShell, run `wsl --shutdown`, wait ten seconds, reopen Ubuntu, and try again.

- **"wendy is not in the sudoers file."**
  Rare — it means your account wasn't created as an administrator. The cleanest fix at this stage: in PowerShell, `wsl --unregister Ubuntu` then reinstall via Mission 1 (it takes minutes — you've lost nothing but the cow, and you know how to get the cow back).

- **The password prompt seems frozen.**
  It isn't — Linux hides your typing (Mission 1). Type the password, press Enter.

> **The WinUbuntu promise:** `apt` is engineered to fail *safely* — it either completes or changes
> nothing at all. There is no half-installed wreckage to fear. Worst case, you read a message and
> try again.

---

**Next mission:** you now know how software arrives. So let's point that skill at something that shouldn't be possible on a kitchen-table laptop: a real artificial intelligence, running entirely on your machine. Tomorrow, your computer learns to talk.
