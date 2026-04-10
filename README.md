# claude-code-101

A simple setup guide for participants joining a live **Claude Code** workshop.

This page is here to help you get ready in advance, with as little friction as possible.

---

## What you should install before the training

Please set up these items before the session:

1. **Claude**
   - Install the **Claude desktop app**, or
   - Make sure you can log in at [claude.ai](https://claude.ai)

2. **Claude Code**
   - Install via **npm** in Terminal

3. **VS Code**
   - Install [Visual Studio Code](https://code.visualstudio.com/)

4. **Git**
   - Install Git on your computer

5. **GitHub account**
   - Create one if you do not already have it

6. **Wispr Flow** (optional, recommended)
   - Helpful for voice dictation during the workshop

7. **A dedicated working folder**
   - Create one clean folder for the training

---

## Claude vs Claude Code

This is the most important distinction to understand:

### Claude
**Claude** is the AI assistant itself.

You can use it:
- in the **Claude desktop app**, or
- in your browser at **claude.ai**

Think of this as the place where you chat with Claude.

### Claude Code
**Claude Code** is a coding tool that connects Claude to files and projects on your computer through the command line.

Think of it as:
- **Claude** = the assistant
- **Claude Code** = the tool that helps Claude work with code and folders locally

You will likely use both during the workshop.

---

## Claude app vs claude.ai website

Both are fine for training.

### Claude desktop app
Good if you want:
- a cleaner, more focused experience
- an app that feels separate from your browser tabs
- easier day-to-day use

### claude.ai in the browser
Good if you want:
- the fastest setup
- no extra app installation
- a simple fallback if the desktop app is not available

If you are unsure, use whichever is easier for you.  
The key thing is: **make sure you can sign in successfully before the session**.

---

## Install VS Code

Please install **VS Code** before the workshop:

[https://code.visualstudio.com/](https://code.visualstudio.com/)

Why we use it:
- it is clean and beginner-friendly
- it makes folders and files easy to work with
- it is a common environment for AI-assisted coding

After installing, open it once to confirm it works.

---

## Install Claude Code

Claude Code is installed from the Terminal using npm.

### Step 1: Make sure Node.js is installed
If you do not already have Node.js, install it first:

[https://nodejs.org/](https://nodejs.org/)

### Step 2: Install Claude Code
Open **Terminal** and run:

```bash
npm install -g @anthropic-ai/claude-code
```

### Step 3: Check that it installed
Run:

```bash
claude --version
```

If you see a version number, you are ready.

---

## Install Git

Install Git here:

[https://git-scm.com/downloads](https://git-scm.com/downloads)

Then open Terminal and check:

```bash
git --version
```

If you see a version number, Git is installed correctly.

---

## GitHub basics you may need for the workshop

You do **not** need to be advanced with Git or GitHub.

For this session, it is enough if you can:

- sign in to your GitHub account
- open a repository link
- clone a repository if needed
- understand that Git tracks file changes
- understand that GitHub is where repositories live online

### Optional but useful
You may also want to set up:

- **SSH access to GitHub**, or
- GitHub authentication through your browser

If you already use GitHub comfortably, great.  
If not, that is completely fine, we will keep things simple.

---

## Optional: Wispr Flow for voice dictation

**Wispr Flow** is optional, but recommended if you like speaking instead of typing.

It can be useful for:
- prompting faster
- drafting ideas naturally
- reducing typing fatigue during hands-on work

If voice input helps you think more clearly, it is worth installing ahead of time.

---

## Create a dedicated working folder

Before the workshop, create one clean folder on your computer just for this training.

For example:

```text
claude-code-101
```

or

```text
workshops/claude-code-101
```

Why this helps:
- keeps your files organized
- makes the session easier to follow
- avoids mixing workshop files with older projects

Once you create the folder:
1. Open it in **VS Code**
2. Keep it ready for the session
3. If asked during training, use this folder for exercises and practice

---

## Simple pre-workshop checklist

Use this quick checklist before the session:

- [ ] I can log in to Claude, either in the app or at claude.ai
- [ ] I have VS Code installed and it opens normally
- [ ] I have Node.js installed
- [ ] I installed Claude Code with npm
- [ ] Running `claude --version` works
- [ ] I installed Git
- [ ] Running `git --version` works
- [ ] I have a GitHub account and can sign in
- [ ] I created a dedicated folder for the workshop
- [ ] Optional: I installed Wispr Flow

---

## If you want to be extra ready

If you have a few extra minutes, it helps to also:

- open Terminal once and make sure you are comfortable with it
- open VS Code and your workshop folder
- confirm your internet connection is stable
- update any tools that are obviously out of date

---

## That’s it

You do not need a perfect setup.  
You just need a working one.

If the items above are in place, you will be in great shape for the workshop.
