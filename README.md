# Lab 1 - Your First Hour with Bob

> **Never used an AI coding assistant before? Perfect - this lab is built for exactly that.**
> By the end you will have talked to Bob in plain English, watched it understand code, plan, and
> build a small working app - and you will have stayed in control the whole time.
>
> ~30-45 minutes · Nothing to install except Bob and a web browser you already have.

---

## Before you start - open your workspace

You need just a few things - **no Python, no Node, no setup**:

1. **Open VS Code** (your team installed it, with **IBM Bob** inside).
2. **Open a folder to work in.** In VS Code: **File → Open Folder…**, then create or pick an empty
   folder (for example, a new folder called `bob-lab` on your Desktop) and open it. This is where your
   work will live.
3. **Open the Bob panel** - click the **IBM Bob** icon in the sidebar so the chat is visible.
4. **Have any web browser ready** - Chrome, Edge, Safari, whatever you use.

> **New to VS Code? Totally fine.** Opening a folder is just like opening one anywhere else:
> **File → Open Folder…**, pick a folder, done. That empty folder is your workspace for this lab.

---

## Start here - let Bob fetch this lab for you

Your very first Bob task: have Bob grab this lab itself.

1. Open **VS Code** with the **Bob** panel, in any empty folder.
2. In the Bob chat, paste this (replace nothing - the link is already filled in):

   ```
   Clone the repository https://github.ibm.com/Boris-Acha/bob-first-lab into this folder,
   then open its README.md and tell me how to start Step 1.
   ```

3. Bob clones the repo and opens this guide. You just used Bob for the first time.

> **Prefer to do it by hand?** In a terminal: `git clone https://github.ibm.com/Boris-Acha/bob-first-lab`
> - or click the green **Code** button on the GitHub page and **Download ZIP**.

---

## Day 1 rules (read this first - 20 seconds)

A few ground rules so your first experience goes well:

- **Never paste secrets.** No passwords, API keys, tokens, or real customer data in the chat. Ever.
- **Read every change before you approve it.** Treat Bob like a teammate whose code you still review.
- **Work in small steps.** One small change at a time - not one giant request.
- **If a change goes wrong, don't fight it.** Reject it or undo it, then rephrase. Don't argue with it for 10 turns.
- **You own what you keep.** Bob helps; you're still responsible for the code you accept.

---

## What is Bob? (the 10-second version)

Bob is a smart teammate that lives inside your editor. You type what you want in plain English, and
Bob does the work - it reads code, writes code, and runs it for you.

But it does **not** go rogue. Before Bob changes anything, it shows you what it's about to do and
waits for your **OK**. You are always the boss.

---

## The one idea to hold onto: Bob has 3 "modes"

Think of them as three hats Bob can wear:

| Mode | What it does | Can it change your files? |
|------|--------------|---------------------------|
| **Ask** | Just talks and explains - it can look but not touch | No - totally safe |
| **Plan** | Thinks through the work and writes a plan *first* | No (just a plan) |
| **Agent** | Rolls up its sleeves and actually builds it | Yes - but only after **you approve** |

**To switch modes:** use the dropdown at the bottom of the Bob chat, or press **⌘ + .** (Mac) / **Ctrl + .** (Windows).

You'll use all three in this lab, in that order: **Ask → Plan → Agent.**

---

## Step 1 - Say hello (Ask mode, nothing can break)

> **What is Ask mode? (plain English)**
> Think of Ask mode like walking over to a teammate's desk and asking, *"hey, what does this do?"*
> They read it and explain - but they never touch your keyboard. Ask mode can **read** your files and
> answer questions, but it **can't change anything**. That's why we start here: you can't break a thing.

1. Set the mode to **Ask** (dropdown at the bottom of the chat).
2. Paste this and press Enter:

   ```
   What files are in this project and what is this repo for?
   ```

3. Bob reads the folder and answers.

 **Notice:** it looked at your files and told you about them *without changing anything*. That's
Ask mode - safe to poke around.

 **You just learned:** *Ask mode = read-only. Use it to explore and ask questions.*

---

## Step 2 - Plan something real (Plan mode)

> **What is Plan mode? (plain English)**
> Think of Plan mode like jotting the steps on a notepad *before* you start a job - "first I'll do
> this, then that." That's exactly what it does: it reads your code, thinks through *how* it would do
> the work, and writes the plan out as a simple notes file you can open and read (a markdown `.md`
> file). It does **not** touch your real code - it just hands you the plan so you can check it, tweak
> it, or say "yes, go." This is your chance to catch a wrong turn *before* a single line of code is written.

1. Switch the mode to **Plan**.
2. Paste this and press Enter:

   ```
   I want a simple Tip Calculator as ONE self-contained HTML file.
   The user types a bill amount and a tip percent, and it shows the tip and the total.
   Also include a small built-in test that checks the math and shows PASS or FAIL on the page.
   Plan it out step by step and save the plan as tip-calculator.md, and don't build anything yet.
   ```

3. Bob writes a step-by-step plan and saves it as **tip-calculator.md**. Open that file from the list
   on the left.

> **First time seeing a `.md` file? Turn on Preview.**
> A markdown (`.md`) file looks like plain text full of `#` and `*` symbols when you open it raw - a
> bit like French if you've never seen it. To read it the nice way, open the **Preview**: click the
> little **open-preview icon** (looks like a book/magnifying glass) at the **top-right** of the editor,
> or press **⌘ + Shift + V** (Mac) / **Ctrl + Shift + V** (Windows). You can flip between the raw text
> and the clean Preview anytime.

 **Notice:** Bob did **not** write any app code yet. It *thought first* and wrote the plan into
`tip-calculator.md` so you can read it, tweak it, or say "yes, go." This is your chance to catch a
wrong turn before a single line of code is written.

 **You just learned:** *Plan mode = Bob thinks and designs before building.*

---

## Step 3 - Build it (Agent mode) - and approve the change

> **What is Agent mode? (plain English)**
> Agent mode is the one that actually rolls up its sleeves and *does* the work - it writes and changes
> real code files, and can even run them for you. Think of it like handing a trusted teammate your
> keyboard. Here's the safety part: it shows you **every** change and waits for your **OK** before it's
> kept. It builds; **you** approve.

> **A good prompt recipe:** tell Bob *what* you want, *what "done" looks like*, and *what to touch*.
> Vague prompts like "make it better" let Bob guess. Be specific and you'll love the results.

1. Switch the mode to **Agent**.
2. Paste this and press Enter - notice the **`@`** in front of the file name:

   ```
   Looks good, build the app now as tip-calculator.html, following the plan in @tip-calculator.md.
   ```

   > **What's the `@` for?** Typing **`@`** lets you point Bob at a specific file to use as context.
   > Here, `@tip-calculator.md` tells Bob *"build exactly what the plan says."* Get used to `@` - it's
   > how you hand Bob the right file instead of hoping it finds it on its own.

3. Bob reads your plan and writes the file. **It will show you the new code and ask you to approve it.**
4. Read the change (the green lines are what's being added). **Before you click Approve, say in one
   sentence what this change does.** If you can't, read it again - then click **Approve**.

> **This one habit matters most.** People who read the diff before approving keep succeeding with
> Bob. People who approve blindly eventually get burned and quit. Read first, every time.

 **Notice:** Bob didn't just do it silently - it showed you *exactly* what it was adding and waited
for your **OK**. This is the whole idea: Bob does the work, **you stay in control**.

 **You just learned:** *Agent mode builds - and you approve every change.*

---

## Step 4 - See it actually work (and watch the test PASS)

1. Find **tip-calculator.html** in the file list on the left.
2. Open it in your browser - right-click the file → **Reveal in Finder/Explorer**, then double-click
   it; or just drag it into a browser tab.
3. Try it: enter a bill of **50** and a tip of **20%**. It should show a **$10 tip** and a **$60 total**.
4. Look for the built-in test result on the page - it should say **PASS** .

 **Notice:** you now have a real, working app that you built by *talking* - and a test proves the
math is right.

 **You just learned:** *Bob builds real, working things - and a test gives you confidence it works.*

---

## Step 5 - Change one thing (Bob iterates)

1. Go back to the Bob chat (still in **Agent** mode).
2. Paste this and press Enter:

   ```
   Add a rule: if the bill is empty or 0, show the message "Please enter a bill amount"
   and don't calculate. Update the built-in test to cover this too.
   ```

3. **Approve** the change.
4. Refresh the browser page. Try an empty bill - you should see the new message. The test should
   still say **PASS**.

 **Notice:** small change, your approval, done. That's how real work with Bob feels - a
conversation, one step at a time.

 **You just learned:** *Bob improves things step by step, with your approval each time.*

---

## Step 6 - Undo with a Checkpoint (your safety net)

Don't like a change Bob made? You can always roll back.

1. In the Bob chat, look for the **checkpoint** marker next to the message *before* your last change
   (Bob saves a checkpoint at each step).
2. Click it and choose **Restore / Revert** to that point.
3. Your files snap back to how they were. Nothing is ever permanent.

 **You just learned:** *Checkpoints let you undo. You can experiment freely - you can always go back.*

---

## Step 7 - Start fresh for your next task

When you move on to a different job, start a clean slate so Bob isn't carrying old context:

- Click **New task / New conversation** (the **+** at the top of the Bob chat).

 **You just learned:** *Start a new conversation when you switch to a different task.*

---

## You did it!

In under an hour, with **zero** prior experience, you:

- Explored code safely in **Ask** mode
- Had Bob design a plan in **Plan** mode - and read it in markdown **Preview**
- Pointed Bob at that plan with **`@`** and built the app in **Agent** mode - approving every change
- Saw a **test pass**
- Made a change, then **undid** one with a checkpoint
- Started a fresh conversation

**That's the complete core of working with Bob.** Everything else is built on top of this.

### Your one deliverable

Write **3-4 sentences** and keep them (or share in the team channel):
*What did Bob build for you? What did you approve, and did you reject or undo anything - and why?*

This tiny reflection is the point of the whole lab: you stayed in control and you can say exactly
what you accepted.

---

## What's next

** [Lab 2 - Teach Bob your way (the `.bob` folder: rules & skills)](./LAB2.md)**
Now that you've got the basics, Lab 2 shows you how to teach Bob your *standards* and give it
*reusable recipes* - the same mechanism the IBM i version uses. Do it next; it's ~20-30 minutes.

After that, we'll point this *same* Bob at **IBM i code** (RPG, and more). Here's the good news:
**everything you learn in Labs 1 and 2 stays exactly the same.** The IBM i features are just skills
and rules built for RPG, bolted on top of this same base Bob - same modes, same approvals, same
safety net. Once this feels natural, the i part is easy.

---

## If you get stuck

- **Can't find the mode switch?** It's the dropdown at the bottom of the Bob chat, or press **⌘ + .** / **Ctrl + .**.
- **Bob did something you didn't expect?** Use a **checkpoint** (Step 6) to roll back.
- **Not sure how to do something?** Ask Bob itself - in **Ask** mode, type *"how do I ...?"*. It's happy to explain.
- **Still stuck?** Post in the team channel - someone will help.
