# Mission 3 — Your First Local AI

*In which Wendy turns off the internet, and the intelligence stays.*

---

### Part 1 — The Question Underneath

Wendy had been quiet for a while, which her companions had learned to recognize as a question assembling itself.

"Okay," she finally said. "Can I ask the one that might actually be silly? People keep saying you can run AI *on your own computer*. Not a website. Not 'the cloud.' Here." She tapped the laptop — the same one, years old, with the sticker half peeled off the lid. "This is a normal laptop. It struggles with too many browser tabs. You're telling me it can do what *ChatGPT* does?"

"Not what ChatGPT does," Alex said. "ChatGPT is a giant model running on warehouse computers. But can this laptop run a *real* AI — one that reasons, writes, explains, jokes — with no internet, no account, no subscription, nothing leaving this room?" He smiled. "Yes. Today. In about ten minutes. And at the end I'm going to prove the 'nothing leaving this room' part in a way you'll never forget."

### Part 2 — The Elephant in the Room

"Fears on the table," Ulysses said. "Though I notice the table's getting less crowded."

Wendy counted. "Isn't AI *enormous* — how would it fit? Won't it cost something eventually — nothing this good is free? And will it turn my laptop into a space heater?"

"Honest answers: AI models come in *sizes*, and there are small ones built exactly for ordinary laptops. Free means free — no trial, no card, no catch; it's open technology, the same spirit as Ubuntu itself. And your laptop will think hard while it answers — you'll hear the fan — but it's doing work you asked for, and it stops the moment you stop. Like any program."

"You'll also feel the difference in *kind*," Alex added. "A small local model is not as brilliant as the giant cloud ones — I want your expectations honest. It's more like a bright, eager assistant than a genius. But it's *yours*, it's *private*, and it works on an airplane. There are things the genius can't offer at any price."

### Part 3 — The Answer

"Two ideas tonight, and then we build," Alex said.

"First idea: **a model is a file.** That's the demystifying secret. All that talk of 'neural networks' and 'training' — the end product is one large file full of learned patterns. Running AI locally just means: your computer opens that file and uses it to generate answers. No magic, no server. A file, being read, by the laptop in front of you.

"Second idea: **Ollama.** Downloading and running model files by hand is fiddly, so the community built a wonderful tool that does it all — fetches models, runs them, gives you a chat right in the terminal. Think of Ollama as the *player*, and models as the *albums*."

"And I install it with…" Wendy raised an eyebrow. "`sudo apt install` something?"

"Almost! Ollama is newer than Ubuntu's catalog cycle, so it ships its own official installer — one command, from their website. Different door, same neighborhood. You'll use apt for one small helper first, so you still get your pattern practice."

> **💡 Why it works — how a "model" fits on your laptop**
> A model file is measured by its number of learned patterns — its *parameters*. The giants have
> hundreds of billions and need warehouse hardware. But researchers discovered that **small models
> (1–3 billion parameters, a file of 1–2 GB) are astonishingly capable** — and they run comfortably
> in an ordinary laptop's memory. When you ask a question, your processor reads the file, does the
> math, and produces the answer — locally, completely. Nothing is sent anywhere. There is no
> "anywhere" involved. Privacy here isn't a policy that a company promises. It's *physics*.

### Part 4 — Crossing the Threshold

> **✅ Before you start:** tonight involves a one-time download of about 1.3 GB (the model), so you
> want internet *for the setup*. After that — as you're about to prove personally — it runs offline
> forever. Total time: ~10 minutes plus download.

**Step 1 — Install a small helper** (your pattern, one more rep):

```
sudo apt update
sudo apt install curl -y
```

*(`curl` is a little tool that fetches things from the web — you'll need it for exactly one step.)*

**Step 2 — Install Ollama, using its official installer:**

```
curl -fsSL https://ollama.com/install.sh | sh
```

> *What this does, honestly:* it downloads Ollama's official install script and runs it. You may
> be asked for your `sudo` password. This "fetch and run" style is common for newer tools — the
> rule that keeps it safe is: **only from the tool's official site, typed exactly**. This one is.

**What you'll see:** a progress readout, ending with Ollama announcing itself installed.

**Step 3 — Download and meet your first model.** We'll pick a small one, sized for real laptops:

```
ollama run llama3.2:1b
```

**What you'll see, first time only** — the download:

```
pulling manifest
pulling 74701a8c35f6... 100% ▕████████████████▏ 1.3 GB
verifying sha256 digest
writing manifest
success
>>> Send a message (/? for help)
```

That `>>>` is new. It isn't Ubuntu's prompt — it's the model, listening.

"Go ahead," Ulysses said. "Ask it something."

Wendy thought for a moment, then typed:

```
>>> In one sentence, what is Ubuntu?
```

A pause — a second, maybe two. She heard the fan wake up, softly, like something taking a breath.

And then her laptop — her ordinary, sticker-peeling, too-many-tabs laptop — *answered her.* A clean, correct sentence about Ubuntu, appearing word by word, generated on the spot by the machine under her hands.

She read it twice. "Okay. That's—" she stopped. "It's not connecting to some website that answers for it?"

Alex's grin widened. He'd been waiting the whole mission for this. "You tell me. **Turn off your Wi-Fi.**"

"What?"

"Windows: click the network icon, switch off Wi-Fi. Airplane mode if you like. Kill the internet. Then ask it another question."

Wendy did. The little globe icon went dark. No internet — the laptop as disconnected as a rock.

```
>>> Write me a short poem about a cow who learned to use a computer.
```

The fan breathed. And the poem arrived — word by word, slightly silly, entirely new, composed by nothing but the hardware in front of her.

Wendy sat very still for a moment.

"There's no trick," she said slowly. "It's *in there*. The intelligence is inside my laptop."

"Inside your laptop," Alex said. "A file, being read. Yours."

*(To leave the chat, type `/bye` and press Enter. And turn your Wi-Fi back on — Mission 6 needs it.)*

### Part 5 — What Just Happened

Three missions ago, you were pausing videos at the words "Ubuntu terminal."

Tonight you installed an AI engine, downloaded a model, and held a conversation with an intelligence running entirely on your own hardware — and you *proved* it was entirely yours, by cutting the wire and watching it keep thinking.

No subscription. No account. No one reading your questions. On an airplane, in a basement, in a blackout with a charged battery — it works, because there is nothing between you and it.

Level 3 of the landscape — the one that sounded like it needed a supercomputer. You're standing on it.

---

*The terminal had spent three missions answering her — telling her the date, printing her cow, following orders. Tonight, for the first time, it had* spoken back. *Not obedience — conversation. She noticed she'd stopped sitting slightly away from it.*

---

### 🧪 Try It Yourself

At the `>>>` prompt (run `ollama run llama3.2:1b` to get back in anytime):

| Try | Why |
|---|---|
| `>>> Explain what a terminal is, to a nervous beginner` | watch it teach — it's rather good at this |
| `>>> Write a haiku about invisible passwords` | see it be creative about *your* journey |
| `>>> I'm learning Ubuntu. Quiz me with 3 easy questions.` | it makes a patient, judgment-free study partner |
| `/bye` then `ollama list` | leave chat; see the models you own (yes, "own") |

*A private AI is the perfect place for "silly" questions — there is, quite literally, nobody watching.*

### ✅ What You Learned

- An AI **model is a file** of learned patterns — and small ones (1–3 GB) run on ordinary laptops.
- **Ollama** is the player; models are the albums; `ollama run <model>` starts a conversation.
- **Local means local** — you severed the internet and the AI kept working, because nothing about it lives anywhere but your machine.
- Privacy by physics beats privacy by promise.
- Honest expectations: a small model is an eager assistant, not a genius — and it's *yours*.

### 📖 Words You Now Know

- **Model** — the file of learned patterns that *is* the AI.
- **Parameters** — the learned patterns; more parameters = bigger, smarter, hungrier files.
- **Ollama** — the tool that downloads and runs models locally.
- **Local AI** — AI running on your own machine; nothing sent, nothing shared.
- **Prompt (`>>>`)** — the model's "listening" signal, and the message you send it.

---

### 🔧 If Something Went Wrong — Troubleshooting

- **"curl: command not found."**
  Step 1 didn't finish — run `sudo apt install curl -y`, then retry Step 2.

- **"Error: could not connect to ollama app, is it running?"**
  Ollama's background engine isn't up yet. Usually: wait ten seconds and retry. If it persists, open a **second** Ubuntu window (Start → Ubuntu), run `ollama serve` there, leave it open, and retry `ollama run llama3.2:1b` in the first window.

- **The download stalls or crawls.**
  It's a 1.3 GB one-time fetch — give it time. If it truly stalls: `Ctrl+C`, then re-run the command; it resumes where it left off.

- **Answers are slow, and the fan is loud.**
  Your laptop is genuinely thinking — this is the sound of local AI on modest hardware, and it's normal. Help it: stick with the `:1b` model, close heavy apps (browsers especially), keep questions short.

- **"model requires more system memory" or Ubuntu closes suddenly mid-answer.**
  The model needs more free memory than it found. Close other programs and retry; make sure you're on `llama3.2:1b` (the smallest), not a larger variant. On a machine with 8 GB+ of RAM, the 1b model should run comfortably.

- **"Error: pull model manifest: ..." during download.**
  Network hiccup — check Wi-Fi is on (ahem — did you turn it back on after the proof?), then retry.

> **The WinUbuntu promise:** a slow answer or a failed download is never a broken computer. It's a
> small model on a real machine, doing honest work — nudge it (smaller model, fewer apps, one retry)
> and it will meet you halfway.

---

**Next mission:** you have an AI living in your machine — but you're still a guest in your own terminal. Time to fix that: learn where things *are*, make a place of your own, and start a small journal you'll be very glad you kept. And I'll show you a door between Ubuntu and Windows that almost nobody knows is there.
