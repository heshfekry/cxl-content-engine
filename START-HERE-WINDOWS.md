# Setup for Windows

Follow these in order. It takes about 20 minutes the first time. You only do this once.

Every term is explained the first time it appears. If a step looks scary, it is not.
You are just installing three free tools and then opening this folder.

---

## What you are installing and why

1. **VS Code** is a free editor from Microsoft. Think of it as a window for looking at
   the folder and the files inside it. You will not write code in it.
2. **Claude Code** is the assistant that does the work. It lives inside the folder and
   does things when you ask it in plain English.
3. **Git** is the tool that downloads (and later updates) this folder from the internet.

---

## Step 1: Install VS Code

1. Go to <https://code.visualstudio.com>.
2. Click the big blue **Download for Windows** button.
3. Open the downloaded file (in your **Downloads** folder) and click through the
   installer. The default options are fine. Tick **Add to PATH** if it offers it.
4. Launch **Visual Studio Code** from the Start menu once it finishes.

---

## Step 2: Install Git

1. Go to <https://git-scm.com/download/win> and the download starts automatically.
2. Open the downloaded file and click **Next** through the installer. The default
   options are fine. This also installs **Git Bash**, which you will use as your Terminal.

---

## Step 3: Open the Terminal inside VS Code

The Terminal is a place where you type commands. You want the **Git Bash** one.

1. In VS Code, click **Terminal** in the top menu, then **New Terminal**.
2. A panel opens at the bottom. If it says "PowerShell," click the small **down arrow**
   next to the **+** on the right of that panel and choose **Git Bash**.
3. That panel is your Terminal. To "run" a command, paste it and press **Enter**.

---

## Step 4: Install Claude Code

1. In the Git Bash Terminal, paste this and press **Enter**:

   ```
   curl -fsSL https://claude.ai/install.sh | bash
   ```

2. Wait for it to finish. Then **close the Terminal panel and open a new Git Bash
   Terminal** so it picks up the new tool.
3. Check it worked:

   ```
   claude --version
   ```

   A version number means you are good.

> You will need a Claude account to use it. The first time you run `claude`, it will
> walk you through signing in. Follow the prompts.

---

## Step 5: Download this folder (the Content Engine)

1. In the Terminal, go to your home folder:

   ```
   cd ~
   ```

2. Download the folder by pasting the command your workshop host gave you. It looks like:

   ```
   git clone <THE-LINK-YOUR-HOST-GAVE-YOU>
   ```

   Press **Enter** and wait. A new folder appears.

3. Move into the folder:

   ```
   cd cxl-content-engine
   ```

---

## Step 6: Open the folder in VS Code

1. In the Terminal, type:

   ```
   code .
   ```

   (That is the word `code`, a space, then a dot.) VS Code opens with the folder loaded.
   You will see all the files listed down the left side.

---

## Step 7: Start Claude Code and set up your engine

1. In the Terminal, type:

   ```
   claude
   ```

   You are now talking to the assistant.

2. Type this and press **Enter**:

   ```
   /setup
   ```

3. Answer the questions it asks. It will guide you through your brand, your voice, what
   you sell, and your best example articles. This is what makes the engine write like you.

---

## You are ready

Write your first article by typing, inside Claude Code:

```
/blog-pipeline "a topic you want to write about"
```

Stuck on anything? Open [docs/troubleshooting.md](docs/troubleshooting.md).
