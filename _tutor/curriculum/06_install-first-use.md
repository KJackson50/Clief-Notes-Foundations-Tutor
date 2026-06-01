# Lesson 6 — Install and First Use

<!-- Source: Lesson 4.1.md, 4.1 transcript video.md -->

## Brief

What You'll Get From This

ChatGPT and Codex working on your machine. A clear sense of when to use each interface. And your first real task run on your own files.



The Lesson

How most people use ChatGPT

Most people use ChatGPT like a search engine that writes better sentences. You type a question, you get an answer, you copy and paste it somewhere. That works. But it is like using a car to check the mailbox. The car can take you across the country. You just have not left the driveway yet.

Today we leave the driveway.



Two interfaces, one model

This is the thing most people miss. ChatGPT and Codex are not two unrelated AIs. They are two ways to work with OpenAI models. The difference is what each interface lets the model see and do.

ChatGPT

The app or the website. A conversational tool. Great for planning, thinking through ideas, getting answers, building drafts. But there is a limit to what it can do at scale. It cannot see your local files directly. It cannot run code on your machine. It cannot edit anything in your project unless you give it those files through the chat experience.

That is not because the model is limited. The model is extremely powerful. The problem is the interface. It just cannot reach your stuff. If you have ever felt like ChatGPT kind of gets it but not quite, it is probably because you are working from a pasted excerpt instead of your actual project.

Codex

This is what you use when the work lives in files. Codex reads your project, edits your files, runs commands, and checks its work. You do not copy and paste anything. You describe what you need and it works directly inside the folder.

VS Code (Visual Studio Code) is a coding environment made by Microsoft. If you have never opened it, do not worry. It is simpler than it looks and we will walk through setup. You do not need to know how to code. VS Code just lets you see your folders as a file tree and open documents without clicking through layers of windows.

If you are familiar with Cursor, Windsurf, Copilot, or other coding assistants, the idea is similar: the assistant is connected to your files. This course is specifically for Codex inside the OpenAI environment.

Codex in the terminal

The terminal version is better for when your work does not live in a code project. Processing a folder of documents. Managing files. Cleaning up your downloads folder. Anything where you need Codex to read a bunch of files and do something with them.



The real difference

ChatGPT is the conversation layer. Codex is the file-working layer.

Interface Best for Can see your files? Can edit your files? ChatGPT Thinking, planning, quick questions, drafting Only if you upload them No Codex Building, editing, working inside a project Yes, in the current folder Yes



Installing everything

Let's get both working.

Step 1: ChatGPT

If you do not have it already:

Go to chatgpt.com or open the ChatGPT app. Sign in with your ChatGPT account.

That is it. You now have the conversational interface.

Step 2: Codex

The easiest install is the official Codex installer.

On Mac or Linux, open a terminal and run:

```
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

On Windows, use WSL2 and run the same command inside your WSL terminal.

You can also install with npm if you already have Node.js:

```
npm install -g @openai/codex
```

Once it finishes, you can type codex in any folder and Codex will launch.

Step 3: Codex in your editor

If you use VS Code or another supported editor, install the Codex extension from that editor's extension marketplace.

You do not need the editor extension for this course. Terminal Codex is enough.



Troubleshooting

"codex: command not found" — Close your terminal completely, reopen it, and try again. If it still fails, rerun the install command.

"npm: command not found" — Only matters if you chose the npm install path. Install Node.js LTS, then try again.

Codex launches but asks for authentication — Follow the link it gives you to sign in with ChatGPT. Use a ChatGPT plan that includes Codex access.

Editor extension does not show up — Make sure the extension installed, restart your editor, and open a folder before launching Codex.

If you get stuck on any of this, post in the community or Discord with your OS and the error message. Someone has hit the same wall.

---

## Build

<!-- Runtime instructions for Codex — not prose delivered to the user -->

Reframe: the user is already using Codex — they're here right now. This lesson is about verifying their setup, not doing a fresh install from scratch.

Start with this reframe: "You already have Codex running — you're using it right now. This lesson is about making sure everything is set up correctly and filling in any gaps you may have skipped. Let's verify your setup."

**Step 1: Platform check.**
- Instruction: "First — are you on Mac, Linux, or Windows with WSL2?"
- Note what they report.

**Step 2: Verify Codex version.**
- Instruction: "Open a terminal (separate from this session). Type: `codex --version`. Tell me what you see."
- Inspect: Note the version number. If they get an error, troubleshoot before continuing.

**Step 3: Verify interface.**
- Instruction: "Are you running Codex from the terminal, an editor extension, or both? Tell me how you're currently set up."
- Note what they report.

**Step 4: Write setup-verified.md.**
- Instruction: "Create a file called `setup-verified.md` in your workspace folder. Fill it in with what you just found:

```
# Setup Verified

Platform: [Mac / Linux / Windows with WSL2]
Environment: [Terminal / Editor extension / Both]
Codex version: [version number]
Date verified: [today's date]
```

Save it. Tell me when it's done."

- Inspect: Read the file. Confirm it has real data (not placeholder text) and the platform/architecture fields are filled in.

**Artifact:** `[user-named-folder]/setup-verified.md`

---

## Check-in

<!-- Runtime instructions for Codex -->

1. Inspect `[user-named-folder]/setup-verified.md` — verify all five fields are filled with real data. No placeholder text.

2. Ask: "You've got ChatGPT for thinking and Codex for working in files. Based on the kind of work you described in your workspace setup, which one do you think you'll use most first, and for what?"

3. Record in `_tutor/progress.md`:
   - lesson: "06_install-first-use"
   - artifacts_inspected: ["[path]/setup-verified.md"]
   - comprehension.question: "You've got ChatGPT for thinking and Codex for working in files. Based on your work, which one will you use most first, and for what?"
   - comprehension.answer: "[user's verbatim response]"
   - comprehension.pass: [true/false]

4. A good answer names a specific interface and a specific use case that fits their work. A bad answer is generic ("I'll use them all for different things") without naming what those things are.
