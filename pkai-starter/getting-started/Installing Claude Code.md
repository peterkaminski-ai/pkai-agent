# Installing Claude Code

Claude Code is a command-line tool that runs in a terminal. It can read and write files on your computer, manage Git operations, and help you with all kinds of knowledge work. You install it once, then connect it to Obsidian in a later step.

## Mac

### Step 1: Install Node.js

Claude Code requires Node.js to run.

1. Go to [nodejs.org](https://nodejs.org/)
2. Click the **LTS** download button (LTS means "Long Term Support" — it's the stable version)
3. Open the downloaded `.pkg` file
4. Follow the installer prompts like any Mac app

> [!tip]
> If you installed Homebrew earlier, you can also install Node.js with `brew install node` in Terminal.

### Step 2: Install Claude Code

In a browser, go to [claude.ai/code](https://claude.ai/code). You'll see several options — choose **Terminal** (not VS Code, not Desktop). Copy the install command shown on the page.

Go to Terminal. Paste the command and — before hitting Enter — check that it looks right. Then hit Enter. The download may take a minute or two.

After the install finishes, you may see a line starting with `echo` followed by a long string. Copy that entire line and paste it into Terminal, then hit Enter. It will look like nothing happened — that's correct. This line adds Claude Code to your system path so you can run it from anywhere.

> [!tip]
> As a general rule, never paste commands from the internet into your terminal without verifying them. In this case, you're trusting Anthropic's official install page.

### Step 3: Run Claude Code for the First Time

Type `claude` and hit Enter. You'll be walked through a brief setup:

1. Hit Enter to accept the default settings
2. Choose **Claude Pro** billing (not API billing) — hit Enter
3. A browser tab will open asking you to authorize Claude Code with your Claude account. Click to allow, then close that browser tab
4. Back in Terminal, you'll see "Login successful." Hit Enter to continue
5. You'll see a warning about prompt injection — hit Enter (or "Yes") to acknowledge
6. When asked about adding Claude Code to your terminal profile, choose **No** (option 2) — you'll be running Claude Code inside Obsidian instead

That's it — Claude Code is installed on your Mac.

---

## Windows

### Step 1: Install Node.js

1. Go to [nodejs.org](https://nodejs.org/)
2. Click the **LTS** download button
3. Run the downloaded installer and follow the prompts

### Step 2: Install Claude Code

Open **Git Bash** (not Command Prompt — Claude Code needs bash). In a browser, go to [claude.ai/code](https://claude.ai/code). Choose **Terminal**. Copy the install command.

Paste it into Git Bash (right-click to paste) and hit Enter. The download may take a minute or two.

After the install finishes, you may see a line starting with `echo` followed by a long string. If so, copy that entire line and paste it into Git Bash, then hit Enter. This adds Claude Code to your system path.

### Step 3: Run Claude Code for the First Time

In Git Bash, type `claude` and hit Enter. Follow the setup prompts:

1. Hit Enter to accept the default settings
2. Choose **Claude Pro** billing (not API billing) — hit Enter
3. A browser tab will open asking you to authorize Claude Code. Click to allow, then close that browser tab
4. Back in Git Bash, you'll see "Login successful." Hit Enter to continue
5. You'll see a warning about prompt injection — hit Enter (or "Yes") to acknowledge
6. When asked about adding Claude Code to your terminal profile, choose **No** (option 2) — you'll be running Claude Code inside Obsidian instead

That's it — Claude Code is installed on your Windows machine.

> [!warning]
> **Windows troubleshooting:** If you see an error about `pip install pywinpty` when you later open the Claude sidebar in Obsidian, run `pip install pywinpty` in Command Prompt, then restart Obsidian. If `pip` isn't recognized, you may need to install Python first from [python.org](https://python.org/).

---

## Other Ways to Run Claude Code

The sidebar in Obsidian (covered in [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md)) is the recommended way to use Claude Code alongside your notes. But you can also run it in:

- **VS Code** — via the official Claude Code extension
- **Any terminal** — Terminal/iTerm2 on Mac, Git Bash/PowerShell on Windows

You can mix and match depending on where your focus is.

## Next Step

Move on to [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md) to set up the sidebar plugin.
