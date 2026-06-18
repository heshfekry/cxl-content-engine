# Setup for Mac

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
2. Click the big blue **Download for Mac** button.
3. Open your **Downloads** folder, find the file, and drag the **Visual Studio Code**
   icon into your **Applications** folder.
4. Open **Applications** and double-click **Visual Studio Code** to launch it once.
   If macOS asks "are you sure you want to open it," click **Open**.

---

## Step 2: Open the Terminal inside VS Code

The Terminal is a place where you type commands. VS Code has one built in.

1. In VS Code, look at the top menu bar and click **Terminal**, then **New Terminal**.
2. A panel opens at the bottom of the window. That is the Terminal. You will type the
   next commands there. To "run" a command, paste it and press **Return**.

---

## Step 3: Install Git

1. In the Terminal, type this and press **Return**:

   ```
   git --version
   ```

2. If you see a version number, Git is already installed. Skip to Step 4.
3. If a box pops up offering to install "command line developer tools," click
   **Install** and wait for it to finish, then run `git --version` again.

---

## Step 4: Install Claude Code

1. In the same Terminal, paste this and press **Return**:

   ```
   curl -fsSL https://claude.ai/install.sh | bash
   ```

2. Wait for it to finish. When it is done, **close the Terminal panel and open a new one**
   (Terminal menu, New Terminal) so it picks up the new tool.
3. Check it worked by typing:

   ```
   claude --version
   ```

   A version number means you are good.

> You will need a Claude account to use it. The first time you run `claude`, it will
> walk you through signing in. Follow the prompts.

---

## Step 5: Download this folder (the Content Engine)

1. In the Terminal, go to where you keep your documents. To put it in your home folder,
   just type:

   ```
   cd ~
   ```

2. Download the folder by pasting this command:

   ```
   git clone https://github.com/heshfekry/cxl-content-engine.git
   ```

   Press **Return** and wait. A new folder appears.

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

2. Type this and press **Return**:

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
