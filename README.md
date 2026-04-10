# Claude Code 101 — Pre-Workshop Setup

> **🤖 For Claude:** This file is a setup guide for a Claude Code workshop participant. If someone pastes you the prompt in Step 2, walk them through installing VS Code, Claude Code CLI (and logging in), Wispr Flow, and Google Drive for Desktop. Treat them as completely non-technical — one step at a time, plain language, verify each step works before moving on.

---

Welcome. This page will get your laptop ready for the workshop — without you having to Google anything, copy commands, or figure out what a terminal is.

**The trick:** you don't set things up yourself. You paste one prompt into Claude, and Claude walks you through the whole thing like a patient friend sitting next to you.

**What you'll have at the end:**

- **VS Code** — a clean editor where we'll do our work
- **Claude Code** — the AI agent that works with files on your computer, logged in and ready
- **Wispr Flow** — voice dictation so you can talk to Claude instead of typing
- **Google Drive for Desktop** — so Claude Code can read your Google Docs as if they were local files
- **A dedicated workshop folder** on your Desktop

Total time: about 20 minutes. Most of it is just waiting for things to install.

---

## How It Works (Big Picture)

```
  You                  Claude (in browser)         Your Mac/PC
┌──────┐              ┌───────────────────┐       ┌──────────────────┐
│ 😊   │── paste ────>│ Walks you through │ ─────>│ VS Code          │
│ You  │   prompt     │ each step, one    │       │ Claude Code CLI  │
│      │<── answers ──│ at a time         │<──────│ Wispr Flow       │
└──────┘              └───────────────────┘       │ Google Drive     │
                                                  └──────────────────┘
```

You'll use Claude in the browser (or the desktop app) to **install** everything. Then, during the workshop, you'll use **Claude Code in your terminal** to actually work with files. Both are Claude — just different interfaces.

---

## Step 1. Get access to Claude

You need to be able to chat with Claude in a browser. Either works:

- **Browser:** Go to [claude.ai](https://claude.ai) and sign in
- **Desktop app:** Download from [claude.ai/download](https://claude.ai/download)

If you're unsure, just use the browser. That's the fastest path.

> **Don't have an account yet?** Create one on [claude.ai](https://claude.ai). A free account is enough for setup. For the workshop itself, a paid plan (Pro or Max) makes things much smoother, but you can get started without it.

---

## Step 2. Let Claude set up your laptop

Open a fresh Claude chat in your browser. Copy the prompt below. Paste it in. Hit send.

Claude will ask you a few questions (like "what's your operating system?"), walk you through each install one at a time, and wait for you after each step. You just follow along.

<PROMPT>
You are my setup assistant for a Claude Code workshop. I'm non-technical — I may never have opened a terminal before. Act like a patient friend sitting next to me, explaining things in plain language. One step at a time. Don't dump everything on me at once.

Here's what I need you to help me install, in this exact order:

1. **Figure out my operating system** — ask me if I'm on Mac or Windows.
2. **VS Code** — walk me through installing it from https://code.visualstudio.com/. After install, have me open it once to confirm it works.
3. **Node.js** — install the LTS version from https://nodejs.org/. After install, have me open a new terminal window and run `node --version` to confirm.
4. **Claude Code CLI** — in the terminal, run `npm install -g @anthropic-ai/claude-code`. Then run `claude --version` to confirm. Then run `claude` to start it up and walk me through the login flow (it'll open a browser window).
5. **Wispr Flow** — install from https://wisprflow.ai/. Explain what it does: voice dictation that works in any app. It's how we'll talk to Claude Code instead of typing.
6. **Google Drive for Desktop** — install from https://www.google.com/drive/download/. This is important: it syncs my Google Drive as a regular folder on my Mac/PC, so Claude Code can read my Google Docs directly as local files. No more copy-paste. After install, have me sign in with my Google account and wait for initial sync.
7. **Create a working folder** — create a folder called `claude-code-101` on my Desktop. Then open it in VS Code (File → Open Folder).

How to guide me:
- Ask one question at a time. Wait for my answer before moving on.
- Explain *why* each tool matters, briefly. I want to understand what I'm installing, not just follow steps.
- If I've never opened a terminal, explain what it is and how to open it (Cmd+Space → "Terminal" on Mac, or Windows Terminal on Windows).
- After each install, have me verify it worked before moving to the next step.
- If something goes wrong, don't just show me the error — explain what it means and suggest a fix. Common gotchas:
  - **Mac + npm "Permission denied":** explain `sudo` and that the password you type is invisible (it's not broken, just hidden).
  - **Windows + npm access errors:** run the terminal as Administrator.
  - **Mac + Node.js:** if the installer is blocked, walk me through System Settings → Privacy & Security to allow it.
  - **Google Drive for Desktop:** explain that initial sync can take a while and that's fine — we just need the folder to exist, not be fully synced.

Important:
- Use the web to look up the latest install instructions if anything has changed.
- Draw simple diagrams or show terminal commands in code blocks so I can copy them.
- Keep app and menu names in English (Terminal, Finder, Spotlight, Settings) — most systems are in English.

At the end, verify everything by running these in the terminal:
- `node --version`
- `claude --version`
- Confirm VS Code opens
- Confirm Wispr Flow is in my menu bar / system tray
- Confirm Google Drive for Desktop is syncing (check Finder sidebar on Mac or This PC on Windows for the Google Drive folder)
- Confirm `~/Desktop/claude-code-101` folder exists and opens in VS Code

If everything is in place, congratulate me — I'm ready for the workshop.
</PROMPT>

---

## Step 3. Quick sanity check

After Claude walks you through everything, do one final test in the terminal:

```bash
cd ~/Desktop/claude-code-101
claude
```

You should see Claude Code start up inside your workshop folder. Say hi. If it responds, you're done.

Close it with `Ctrl+C` or just closing the terminal window. We'll open it again together during the session.

---

## Why Google Drive for Desktop matters (don't skip this)

This is the one install people tend to skip — and then regret during the workshop.

Claude Code can read any file on your hard drive. Google Drive for Desktop turns your entire Google Drive into a regular folder on your computer. That means during the workshop, you can say things like:

> "Read the document at `~/Library/CloudStorage/GoogleDrive-me@gmail.com/My Drive/Q2 Plan.docx` and summarize it"

...and Claude Code just does it. No upload, no copy-paste, no screenshots. If you skip this install, you'll be the one person in the room manually uploading files while everyone else is working on their real documents.

---

## Pre-workshop checklist

Use this to self-verify before the session:

- [ ] I can sign in to Claude (browser or desktop app)
- [ ] VS Code is installed and opens
- [ ] `node --version` shows a version number
- [ ] `claude --version` shows a version number
- [ ] Running `claude` starts Claude Code and I'm logged in
- [ ] Wispr Flow is installed and I've done a quick voice test
- [ ] Google Drive for Desktop is installed and syncing
- [ ] I have a `claude-code-101` folder on my Desktop
- [ ] I can open that folder in VS Code

---

## If something breaks

Don't panic and don't try to fix it alone. Go back to your Claude chat from Step 2 and tell it what went wrong. Paste the exact error message. Claude will walk you through it.

If you're completely stuck, show up to the workshop a few minutes early and we'll fix it together. A non-working setup is a very common, very fixable problem. The one thing you *should* avoid is showing up without having even tried — we won't have time to do the full install during the session.

---

## You don't need a perfect setup

You just need a working one. If the items above are in place, you're in great shape. See you at the workshop.
