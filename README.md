# Subsense × Claude Code — Pre-Training Setup

> **🤖 For Claude:** This file is a setup guide for a Subsense executive joining a Claude Code training session. If someone pastes you the prompt in Step 2, walk them through installing VS Code, Claude Code CLI (and logging in), Wispr Flow, and Google Drive for Desktop. Treat them as completely non-technical — one step at a time, plain language, verify each step works before moving on.

---

**Training date:** April 15, 2026 · **Duration:** 2.5 hours

Welcome, Subsense execs. This page will get your laptop ready for our training session — without you having to Google anything, copy commands, or figure out what a terminal is.

**The trick:** you don't set things up yourself. You paste one prompt into Claude, and Claude walks you through the whole thing like a patient friend sitting next to you.

**What you'll have at the end:**

- **VS Code** — the clean editor we'll work in during the session
- **Claude Code** — the AI agent that reads and edits files on your computer, logged in and ready
- **Wispr Flow** — voice dictation so you can talk to Claude instead of typing
- **Google Drive for Desktop** — so Claude Code can read your Subsense Google Docs directly as local files
- **A dedicated `subsense-ai` folder** on your Desktop — your home base for the session

Total time: about 20 minutes. Most of it is just waiting for things to install.

---

## What we're building toward

On training day, you'll move from "I use ChatGPT" to "I have an AI agent that works across my Subsense email, calendar, and Drive." The setup on this page is the foundation — without it, you'll be copy-pasting while everyone else is working on real Subsense documents.

```
  You                  Claude (in browser)         Your Mac/PC
┌──────┐              ┌───────────────────┐       ┌──────────────────┐
│ 😊   │── paste ────>│ Walks you through │ ─────>│ VS Code          │
│ Exec │   prompt     │ each step, one    │       │ Claude Code CLI  │
│      │<── answers ──│ at a time         │<──────│ Wispr Flow       │
└──────┘              └───────────────────┘       │ Google Drive     │
                                                  └──────────────────┘
```

You'll use Claude in the browser (or the desktop app) to **install** everything. Then, during training, you'll use **Claude Code in your terminal** to actually get work done. Both are Claude — just different interfaces.

---

## Heads up: we're focusing on Claude Code, not OpenClaw

Some of you signed up expecting this session to be about OpenClaw — that was the original plan when we scoped the training. Two things changed between then and now:

- **Claude Code got noticeably better.** In the last few months Anthropic has shipped fast. Claude Code now handles real executive workflows — email, calendar, Drive, document review, debugging — more smoothly and more "human" than OpenClaw does today, with no server of your own to maintain.
- **OpenClaw got meaningfully more expensive.** On April 4, 2026, Anthropic stopped supporting OpenClaw on its flat subscription. It now runs on pay-per-token pricing, and for an always-on agent monitoring email, running crons, and doing multi-step workflows 24/7, that can easily hit $500–$1,000 per person per month. Claude Code is still a predictable flat subscription.

There's also a learning argument. Both tools work the same way underneath — you describe a task, the agent executes across your tools, you debug together. The real difference is autonomy: Claude Code works alongside you in a supervised session; OpenClaw works without you, running on its own server 24/7. Learning to scope tasks, connect tools, and recover from errors in the supervised tool *first* — then graduating to the autonomous one once you know which workflows you actually want running unattended — is the right order. Walking before running.

So here's the plan for April 15: we'll spend most of the session building real workflows in Claude Code, and close with a short OpenClaw preview — what it does, why it's the natural next step, and what a follow-up session on it would cover.

---

## Step 1. Get access to Claude

You need to be able to chat with Claude in a browser. Either works:

- **Browser:** Go to [claude.ai](https://claude.ai) and sign in
- **Desktop app:** Download from [claude.ai/download](https://claude.ai/download)

If you're unsure, just use the browser. That's the fastest path.

> **Don't have a Subsense Claude account yet?** Alex Karpman may have already provisioned one for you — **check with Alex first.** If not, create one on [claude.ai](https://claude.ai) using your Subsense email. A free account is enough for setup. For the training itself, a paid plan (Pro or Max) makes things much smoother — Alex can confirm which plan Subsense is providing.

---

## Step 2. Let Claude set up your laptop

Open a fresh Claude chat in your browser. **Copy everything inside the box below** (from `You are my setup assistant...` down to `...ready for the Subsense training.`). Paste it into Claude. Hit send.

Claude will ask you a few questions (like "what's your operating system?"), walk you through each install one at a time, and wait for you after each step. You just follow along.

> 👇 **Copy from here** 👇

```text
You are my setup assistant for a Subsense AI training session. I'm a non-technical Subsense executive — I may never have opened a terminal before. Act like a patient friend sitting next to me, explaining things in plain language. One step at a time. Don't dump everything on me at once.

Here's what I need you to help me install, in this exact order:

1. Figure out my operating system — ask me if I'm on Mac or Windows.
2. VS Code — walk me through installing it from https://code.visualstudio.com/. After install, have me open it once to confirm it works.
3. Node.js — install the LTS version from https://nodejs.org/. After install, have me open **VS Code's built-in terminal** (View → Terminal, or `` Ctrl+` ``) and run `node --version` there to confirm. **From this point on, every terminal command happens inside VS Code — no switching to the system Terminal app or Windows Terminal.**
4. Claude Code CLI — in the same VS Code terminal, run `npm install -g @anthropic-ai/claude-code`. Then run `claude --version` to confirm. Then run `claude` to start it up and walk me through the login flow (it'll open a browser window). I should log in with the same Subsense account I use on claude.ai.
5. Wispr Flow — install from https://wisprflow.ai/. Explain what it does: voice dictation that works in any app. It's how I'll talk to Claude Code during training instead of typing everything out.
6. Google Drive for Desktop — install from https://www.google.com/drive/download/. This is critical for the training: it syncs my Subsense Google Drive as a regular folder on my Mac/PC, so Claude Code can read my Subsense Google Docs directly as local files. No more copy-paste. After install, have me sign in with my Subsense Google account and wait for initial sync.
7. Create a working folder — create a folder called `subsense-ai` on my Desktop. Then open it in VS Code (File → Open Folder). This will be my home base during training. Once it's open, have me open VS Code's built-in terminal (View → Terminal, or `` Ctrl+` ``) — that's where we'll run Claude Code from. During training, VS Code is both the file browser (left sidebar) and the terminal (bottom panel), so I never have to leave it.

How to guide me:
- Ask one question at a time. Wait for my answer before moving on.
- Explain why each tool matters for the Subsense training, briefly. I want to understand what I'm installing, not just follow steps.
- If I've never opened a terminal, explain what it is and how to open **VS Code's built-in terminal** (View → Terminal menu, or the `` Ctrl+` `` shortcut). We are not using the system Terminal app or Windows Terminal — everything runs inside VS Code.
- After each install, have me verify it worked before moving to the next step.
- If something goes wrong, don't just show me the error — explain what it means and suggest a fix. Common gotchas:
  - Mac + npm "Permission denied": explain `sudo` and that the password you type is invisible (it's not broken, just hidden).
  - Windows + npm access errors: run the terminal as Administrator.
  - Mac + Node.js: if the installer is blocked, walk me through System Settings → Privacy & Security to allow it.
  - Google Drive for Desktop: explain that initial sync can take a while and that's fine — we just need the folder to exist, not be fully synced.

Important:
- Use the web to look up the latest install instructions if anything has changed.
- Draw simple diagrams or show terminal commands in code blocks so I can copy them.
- Keep app and menu names in English (Terminal, Finder, Spotlight, Settings) — most systems are in English.

At the end, verify everything by having me open VS Code's built-in terminal (inside my `subsense-ai` folder) and run:
- `node --version`
- `claude --version`
- `claude` (should start Claude Code logged in)

Also confirm:
- VS Code shows my `subsense-ai` folder in the left sidebar
- Wispr Flow is in my menu bar / system tray
- Google Drive for Desktop is syncing (check Finder sidebar on Mac or This PC on Windows for the Google Drive folder)

If everything is in place, congratulate me — I'm ready for the Subsense training.
```

> ☝️ **Copy up to here** ☝️

---

## Step 3. Quick sanity check

During training we'll run everything **inside VS Code** — VS Code is both your file browser (left sidebar shows your folder) and your terminal (bottom panel runs Claude Code). No jumping between windows.

Do this one final test:

1. Open VS Code
2. **File → Open Folder** → select `~/Desktop/subsense-ai`
3. Open the built-in terminal: **View → Terminal** (or `` Ctrl+` `` on Mac/Windows)
4. In that terminal, run:
   ```bash
   claude
   ```

You should see Claude Code start up inside your `subsense-ai` folder, right there in VS Code's bottom panel. Say hi. If it responds, you're set.

Close it with `Ctrl+C`. We'll open it again together at the start of the session.

---

## Why Google Drive for Desktop matters (don't skip this)

This is the one install participants tend to skip — and then regret 10 minutes into the training.

Claude Code can read any file on your hard drive. Google Drive for Desktop turns your entire Subsense Drive into a regular folder on your computer. That means during training, you can say things like:

> "Read the document at `~/Library/CloudStorage/GoogleDrive-you@subsense.com/My Drive/Subsense Projects/Q2 Plan.docx` and summarize it"

...and Claude Code just does it. No upload, no copy-paste, no screenshots. If you skip this install, you'll be the one person in the room manually uploading files while your colleagues are working on real Subsense documents in real time.

---

## Three things to bring besides your laptop

The setup above gets your machine ready. These three get *you* ready. Skip any of them and part of the training stops working.

### 1. Export your ChatGPT history — no later than April 13

One of the demos is built around reading your actual ChatGPT history back to you: "What have I been using AI for? What am I missing? What's automatable?" Without the export, that demo doesn't happen for you.

- Go to ChatGPT → Settings → Data Controls → **Export data**
- You'll get an email with a ZIP file within ~24 hours
- Download the ZIP to your laptop (no need to unzip it — Claude Code will handle that during the session)
- Drop the ZIP into your `subsense-ai` folder so it's right there when we need it

Do this **no later than April 13** — OpenAI takes up to 24 hours to deliver the export, so don't leave it to the night before.

### 2. Come with one-two real workflows in mind

The 75-minute hands-on block is where you build one working automation from *your actual job*. Not a hypothetical, not "something marketing-ish." One (or more) specific, boring, recurring task you do every week that you wish you didn't.

As I suggested in the Loom prep video, take ten minutes before the session and jot down a candidate or two:

- One thing you do every Monday that feels like middleware between your own tools
- One report you regularly assemble by copy-pasting from Gmail / Calendar / Drive
- One decision you keep making from the same inputs every time

Bring at least one. If you show up without a candidate, you'll burn the first 20 minutes of the build session figuring out what to build instead of building.

### 3. Know what NOT to paste into the chat

Subsense handles clinical results,  novel research and proprietary IP. The workshop rules:

- **No regulated data in the chat.** No patient records, no raw clinical results, no proprietary IP. Anything that passes through the agent's context window passes through Anthropic's servers. Even though Anthropic claims they never use it or disclose it, let's rather not risk it.
- **Be careful with automatic external actions** — sending emails, posting messages, updating shared docs. Review before you let the agent send anything.
- **Always review important outputs** before they leave your laptop.
- **If in doubt, work on a copy** of the file, not the original. This is still early technology.

We'll cover this live at the start of the session, but knowing it going in means you won't freeze up the first time the agent asks to touch something sensitive.

---

## Pre-training checklist

Use this to self-verify before the session:

- [ ] I can sign in to Claude (browser or desktop app) with my Subsense account
- [ ] I have a `subsense-ai` folder on my Desktop
- [ ] I opened that folder in VS Code (File → Open Folder)
- [ ] I can see my folder in VS Code's left sidebar (the file browser)
- [ ] I can open VS Code's built-in terminal (View → Terminal, or `` Ctrl+` ``)
- [ ] `node --version` shows a version number (in the VS Code terminal)
- [ ] `claude --version` shows a version number (in the VS Code terminal)
- [ ] Running `claude` inside VS Code's terminal starts Claude Code and I'm logged in
- [ ] Wispr Flow is installed and I've done a quick voice test
- [ ] Google Drive for Desktop is installed and my Subsense Drive is syncing
- [ ] My ChatGPT history export is downloaded and sitting in the `subsense-ai` folder
- [ ] I have at least one real workflow from my job in mind for the build session
- [ ] I know the "no regulated data in the chat" rule

---

## If something breaks

Don't panic and don't try to fix it alone. Go back to your Claude chat from Step 2 and tell it what went wrong. Paste the exact error message. Claude will walk you through it.

If you hit a wall Claude can't get you past — especially anything that looks like a Subsense IT restriction — ping Dom. If you're still stuck on training day, show up a few minutes early and we'll fix it together. 

A non-working setup is a very common, very fixable problem. The one thing to avoid is showing up without having tried — we won't have time to run the full install during the session.

---

## The setup is the boring part. What you'll build on top of it isn't.

On April 15, you walk out of this room with one working automation that does a real slice of your job — not another chatbot you have to copy-paste into. This page just gets your laptop out of the way so we can skip straight to that. See you then.
