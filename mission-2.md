
# Mission 2 (Full Depth) — Your First Tool, Installed by Your Own Hand

*WinUbuntu · published-depth version.*

---

### Part 1 — The Empty Room

Wendy opened Ubuntu again the next morning. The prompt sat exactly where she'd left it.

```
wendy@wendy-pc:~$
```

She typed `whoami`, just to feel it answer. It did. She smiled — then it faded.

"Okay. I'm *in*. But… now what? A blinking cursor isn't a tool. It's an empty room."

Alex overheard. "That is the perfect question for today."

### Part 2 — The Elephant in the Room

"Say the quiet fears out loud again," Ulysses said. "*What if I install the wrong thing? What if I fill my computer with junk I can't remove? Don't I have to be a programmer?*"

Wendy nodded at all three.

"Ubuntu installs software the *clean* way — everything's tracked, and anything you install you can remove just as easily. And no — you don't write one line of code today. You type three short words."

### Part 3 — The Answer

"Windows has a Store. Ubuntu has one too — you reach it through the terminal, and it's faster. It's called **apt**." Alex wrote three *ideas*, not commands:

> **Refresh** the catalog. **Install** the tool. **Done.**

"Two start with `sudo`," Ulysses added — "*'super-user do'* — telling Ubuntu *'I know this is powerful, and I mean it.'* It'll ask your password. Remember —"

"— the screen won't show it," Wendy finished.

> **💡 Why it works — What `apt` really does**
> `apt` is Ubuntu's package manager. Instead of hunting the web for installers (and hoping they're
> safe), you ask one trusted catalog — the *repositories* — for a tool by name. `apt` fetches it,
> installs it, and *remembers* it. That memory is the magic: because every piece is tracked, you
> can remove anything just as cleanly as you added it. You will never "clutter" Ubuntu the way
> stray downloads clutter Windows.

### Part 4 — Crossing the Threshold

"We'll pick a *silly* tool on purpose — so if anything felt scary, you'll see there was nothing to fear."

**Step 1 — Refresh the catalog:**

```
sudo apt update
```

It asks for your password (typed invisibly). **What you'll see** is a stream of lines ending near:

```
Reading package lists... Done
```

"Did I do something dangerous?" Wendy asked, watching it scroll.

"You asked a library for its newest catalog. Nothing on your machine changed. It's just *reading*."

**Step 2 — Install the tool:**

```
sudo apt install cowsay -y
```

**What you'll see** (a few lines, then it stops — that's success):

```
Setting up cowsay ...
```

*(The `-y` simply means "yes, go ahead" so it doesn't stop to ask.)*

**Step 3 — Use it:**

```
cowsay "I did it"
```

**What you'll see:**

```
 ________
< I did it >
 --------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

Wendy laughed out loud. "A *cow* said my words." — "And you installed it. From nothing. In under a minute."

### Part 5 — What Just Happened

"Look at what you typed. `sudo apt install` *a tool's name*. That is the **exact** command that installs Python, Git, Docker, and nearly every AI tool you will ever meet."

"So I just… learned to install *anything*?"

"You learned the single most useful pattern in Ubuntu. We practiced on a cow so it would never feel frightening."

One more gift:

```
python3 --version
```

```
Python 3.12.3
```

"Ubuntu came with **Python** already inside — the language of AI. It's been waiting for you."

*You didn't fill your computer with junk. You didn't need to be a programmer. You installed a tool — and learned the pattern that installs them all.*

---

### 🧪 Try It Yourself

You now hold a superpower. Try it on two more harmless tools — and then prove how *clean* it is by removing one:

| Type this | What happens |
|---|---|
| `sudo apt install fortune-mod -y` then `fortune` | installs a tool that prints a random quote, then runs it |
| `sudo apt install figlet -y` then `figlet WinUbuntu` | makes big letters out of text |
| `sudo apt remove cowsay -y` | *removes* the cow — cleanly, no trace. (Miss it? Reinstall it.) |

### ✅ What You Learned

- Ubuntu installs software through **`apt`**, from a trusted catalog — cleanly and reversibly.
- The pattern is always the same: **`sudo apt update`** → **`sudo apt install <name> -y`**.
- **`sudo`** means "I mean it" and asks your password (typed invisibly).
- The very same pattern installs the *real* AI tools you'll meet next.

### 📖 Words You Now Know

- **Package** — a piece of software `apt` can install.
- **`apt`** — Ubuntu's package manager (its terminal "app store").
- **`sudo`** — run a command with permission to make powerful changes.
- **Repository** — the trusted online catalog `apt` installs from.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"Unable to locate package cowsay."**
  Your catalog is stale or the network hiccuped. Run `sudo apt update` again, then retry the install.

- **"Could not get lock /var/lib/dpkg/… — is another process using it?"**
  Ubuntu is already installing something in the background (it does this occasionally after setup). Wait a minute and try again.

- **"E: Failed to fetch…" or it hangs.**
  A network/DNS blip inside WSL. Check your internet, then re-run. If it persists, close Ubuntu, and in PowerShell run `wsl --shutdown`, then reopen Ubuntu.

- **The password prompt seems stuck.**
  It's not — Ubuntu hides password characters (from Mission 1). Type it, press Enter.

> **The WinUbuntu promise:** none of these mean you broke anything. `apt` is designed to fail
> *safely* — it either works or it doesn't do anything at all.

---

**Next mission:** you know the install pattern. Let's point it at something extraordinary — a real AI, running on your own machine.


---
