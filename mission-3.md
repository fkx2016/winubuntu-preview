
# Mission 3 (Full Depth) — Your First Local AI

*WinUbuntu · published-depth version.*

---

### Part 1 — The Question Underneath

Wendy had been quiet for a minute, staring at the cow from yesterday.

"Can I ask something that might sound silly? Everyone keeps saying I can run AI *on my own computer*. Not a website. Not the cloud. Here. On this laptop." She tapped it. "Is that real? Or only for people with giant machines?"

Alex set down his coffee. "It's real. And today, it's yours."

### Part 2 — The Elephant in the Room

"The fears first," Ulysses said. "*Isn't AI too big to fit on my computer? Won't it cost money? Will it slow everything down?*"

Wendy nodded — exactly that.

"There are small, free AI models built to run on ordinary laptops. No subscription. No internet needed once it's downloaded. You'll pick a *small* one, so your machine stays comfortable. If it ever feels slow, you close it — like any program."

### Part 3 — The Answer

"There's a friendly tool that makes local AI simple," Alex said. "It's called **Ollama** — a little engine that downloads a model and lets you *talk to it* right in your terminal."

"And installing it uses the pattern from yesterday?"

"You tell me."

> **💡 Why it works — What "a model" is, and why it can live on your laptop**
> An AI *model* is a single (large) file full of learned patterns. "Running it locally" means your
> own processor reads that file to generate answers — no server, no internet, nothing leaving your
> machine. Big models need big hardware; but there are **small models** (1–3 GB) tuned to run on
> everyday laptops. They're a little less capable than the giant cloud ones — and completely private,
> free, and yours. Perfect for learning.

### Part 4 — Crossing the Threshold

> **✅ Before you start:** you'll download a model once (a few minutes, needs internet). After that,
> it runs offline forever.

**Step 1 — Get the helper `curl`** (using the pattern you already know):

```
sudo apt install curl -y
```

**Step 2 — Install Ollama** (its official one-line installer):

```
curl -fsSL https://ollama.com/install.sh | sh
```

**What you'll see:** a short progress readout ending with Ollama reporting it's installed and ready.

**Step 3 — Meet your first model.** Pick a *small* one:

```
ollama run llama3.2:1b
```

**What you'll see** the first time — a one-time download, then a new prompt:

```
pulling manifest
pulling ... 100%
success
>>> Send a message (/? for help)
```

"Go on," said Ulysses. "Ask it anything."

```
>>> In one sentence, what is Ubuntu?
```

And her laptop — offline, no browser, no cloud — *answered her.*

She read it twice, then looked up, quieter than before. "That came from *my* computer. Not a website."

"Your computer," Alex agreed. "It's thinking. Because you taught it how."

*(To leave the chat, type `/bye` and press Enter.)*

### Part 5 — What Just Happened

You just ran artificial intelligence on your own machine. No subscription. No internet. Nothing watching over your shoulder.

Three missions ago, the terminal was a black window that frightened you. Today it's the place where *your* AI lives.

*Fear became curiosity. Curiosity became this.*

---

### 🧪 Try It Yourself

| Type this (at the `>>>` prompt, or in the terminal) | What it does |
|---|---|
| `>>> Write a haiku about a nervous new Linux user` | see it be creative |
| `>>> Explain what a terminal is, to a total beginner` | see it teach |
| `/bye` | leave the chat |
| `ollama list` | list the models you've downloaded |

*Ask it to explain the very things you're learning — it makes a patient study partner.*

### ✅ What You Learned

- AI can run **locally**, on your own machine — private, offline, and free.
- **Ollama** downloads and runs models for you; **small models** fit on ordinary laptops.
- You installed it with the **same `apt` pattern** plus a one-line official installer.
- You held a real conversation with an AI that lives *on your computer*.

### 📖 Words You Now Know

- **Model** — the file of learned patterns that "is" the AI.
- **Ollama** — the tool that runs AI models locally.
- **Local AI** — AI that runs on your own machine, not a website.
- **Prompt** — the message you send the model.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"curl: command not found."**
  Step 1 didn't finish. Run `sudo apt install curl -y` again, then re-run the installer.

- **"Error: could not connect to ollama app" or "connection refused."**
  The Ollama background service isn't up yet. Open a **second** Ubuntu window and run `ollama serve` (leave it running), then try `ollama run llama3.2:1b` in your first window. Often, simply waiting a few seconds and re-running is enough.

- **The download is very slow or stalls.**
  The model is a one-time download and needs internet. Let it finish; if it stalls, press `Ctrl+C` and run the `ollama run` command again — it resumes.

- **It runs but answers *very* slowly, or your fan spins up.**
  Your machine is thinking hard. Use the smallest model (`llama3.2:1b`), close other heavy apps, and keep prompts short. Slow is normal on modest hardware — nothing is wrong.

- **"model … not found."**
  Check the spelling: `llama3.2:1b`. See what you have with `ollama list`.

> **The WinUbuntu promise:** a model that won't load or a slow answer is never a broken computer.
> It's a setting to nudge — smaller model, a moment's patience, one retry.

---

**Next mission:** the terminal is starting to feel like yours. Let's make it a *home* — a place where you find your way around and make things of your own.


---
