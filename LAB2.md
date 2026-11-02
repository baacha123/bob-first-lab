# Lab 2 - Teach Bob Your Way (the `.bob` folder: rules & skills)

> **Done with [Lab 1](./README.md)? Great - you've got the basics.** Now you'll do the thing that
> makes Bob *yours*: teach it your standards, and give it reusable recipes. All of this lives in a
> folder called **`.bob`**.
>
> **Why this matters:** this is the *exact same mechanism* the IBM i version of Bob uses for RPG.
> Learn it here on simple web code, and the advanced IBM i stuff will feel familiar instead of new.
>
> ~20-30 minutes · Keep working in the **same tip-calculator project** from Lab 1.

---

## The idea: so far you *asked*; now you *teach*

In Lab 1, Bob did what you asked, one request at a time. That's great - but you had to say it every
time.

Now you'll teach Bob two kinds of things that **stick**:

| Thing | Plain English | Lives in |
|-------|---------------|----------|
| **Rule** | A standing standard Bob follows *every time*, without you repeating it | `.bob/rules/` |
| **Skill** | A saved *recipe* Bob runs when the job matches - write once, reuse forever | `.bob/skills/` |

Both live in a folder called **`.bob`** in your project. (The Day-1 rules from Lab 1 still
apply - read every diff before you approve.)

---

## Part A - Teach Bob a standing rule (`.bob/rules/`)

> **What is a rule? (plain English)**
> A rule is like a team style guide pinned to the wall. You write it once, and Bob follows it on
> *every* job without being reminded. Rules live as plain files in `.bob/rules/`, and Bob reads them
> automatically at the start of every task.

### Step 1 - Create a rule

1. Switch to **Agent** mode.
2. Paste this and press Enter:

   ```
   Create a rule file at .bob/rules/style.md.
   The rule: every HTML file in this project must start with an HTML comment header that contains
   the file name, a one-line description of what the file does, and today's date.
   After you create it, tell me in one line that you'll follow it from now on.
   ```

3. Read the change and **Approve**.

 **Notice:** you didn't change any app code - you wrote down a *standard* for Bob to follow.

### Step 2 - Watch Bob follow the rule on its own

1. Still in **Agent** mode, paste:

   ```
   Create a new file called goodbye.html that shows a friendly "Goodbye!" message.
   ```

2. Read the change before approving. **Look at the top of the new file** - Bob added the comment
   header *automatically*, because of your rule. You never mentioned it in this request.
3. Approve.

 **You just learned:** *rules in `.bob/rules/` are always-on standards. Bob follows them on every
task, without you repeating yourself.*

---

## Part B - Give Bob a reusable skill (`.bob/skills/`)

> **What is a skill? (plain English)**
> A skill is a *saved recipe*. Instead of typing the same multi-step request over and over, you write
> the steps down once as a skill, and Bob runs that recipe whenever the job matches. Skills live in
> `.bob/skills/<name>/SKILL.md`. **This is exactly what the IBM i package is** - a set of recipes
> for RPG.

### Step 3 - Create a skill

1. Still in **Agent** mode, paste this:

   ```
   Create a skill at .bob/skills/new-page/SKILL.md.
   Use this format: start with frontmatter containing a "name" and a "description", then the steps.
   - name: new-page
   - description: Use when the user wants to create a new web page in this project.
   Steps the skill should follow:
   1. Ask me for the page title first.
   2. Create a self-contained HTML file named after the title (lowercase).
   3. Follow our .bob/rules/style.md header rule.
   4. Add a visible <h1> with the title and a footer that says "Tip Calculator project".
   ```

2. Read it and **Approve**.

 **Notice the two required pieces:** a **name** and a **description**. The description is how Bob
decides when to use the skill - *a skill with no description is ignored.*

### Step 4 - Use your skill

1. Start a **fresh task** (the **+** at the top of the chat) so we're starting clean.
2. In **Agent** mode, paste:

   ```
   Create a new page called About.
   ```

3. Watch what happens: Bob recognizes this matches your **new-page** skill, so it **asks you for the
   title first**, then builds the page following your recipe *and* your header rule.
4. Approve, and open the file to see it followed the recipe.

 **You just learned:** *skills in `.bob/skills/` are reusable recipes. Bob picks the right one based
on its description and follows your steps - every time.*

---

## Peek inside `.bob` (30 seconds)

In the file list on the left, open the **`.bob`** folder. You'll see:

```
.bob/
├── rules/
│   └── style.md          ← your standing standard
└── skills/
    └── new-page/
        └── SKILL.md       ← your reusable recipe
```

 They're just **plain files**. Nothing magic. You can read them, edit them, and they travel with
your project in version control - so your whole team gets the same standards and recipes.

> **Bonus - `AGENTS.md`:** there's also a file called `AGENTS.md` you can put at your project's root.
> Think of it as your project's front-page standards - Bob loads it automatically too. Rules and
> `AGENTS.md` do a similar job; use whichever fits. (We'll see `AGENTS.md` again with IBM i.)

---

## You did it - and here's the big payoff

You just taught Bob to work *your* way: a standing **rule** and a reusable **skill**, both living in
the `.bob` folder.

**This is the whole foundation of the advanced IBM i work.** The IBM i Premium Package for Bob is
exactly what you just built - a bundle of **skills and rules**, tuned for RPG and IBM i, living in
this same `.bob` folder. So when we show you things like *"extract the business rules from this RPG
program"* or *"build a test suite"* - those are just **skills**. You already know what a skill is,
where it lives, and how Bob decides to use it.

Nothing about IBM i will be new. It's this same Bob, with recipes built for your world.

---

## Recap - what you now know

- **Ask / Plan / Agent** modes (Lab 1)
- **Approvals, the diff, checkpoints** - you're always in control (Lab 1)
- **Rules** (`.bob/rules/`) - always-on standards Bob follows automatically
- **Skills** (`.bob/skills/`) - reusable recipes Bob applies when they match
- **`.bob`** is just a folder of plain files you version-control with your project

That's everything you need to be productive with base Bob - and everything you need to make IBM i
feel easy when we get there.
