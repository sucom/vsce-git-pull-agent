# Git Pull Agent (VS Code Family Extension)

<p>
  <img src="images/icon-sm.png" alt="Git Pull Agent logo" width="120"/>
</p>

A frictionless, read-only Git auto-pull companion built specifically for workshop students and learners.

When following along with a live coding session, a bootcamp, or a workshop, you shouldn't have to constantly switch to the terminal to type `git pull` just to see the instructor's latest code. Git Pull Agent runs quietly in the background, keeping your local workspace perfectly in sync with the remote repository so you can focus entirely on learning the code.

## ⚡ Quick Start

1. **Install** Git Pull Agent from IDE's Extensions Panel.
2. **Clone** your instructor's or project's Git repository.
3. **Click** the `auto-pull: OFF` status bar button to open the quick settings menu and select a polling interval (e.g., 5 seconds).
4. Watch your files update in real-time as the instructor pushes new code!

## 🚀 Installation

1. Open Your IDE: VS Code / Antigravity / Cursor / Windsurf / VSCodium
2. Go to Extensions
3. Search for `git pull agent` and select this extension
4. Click **Install**

OR

- Install from [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-pull-agent) | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-pull-agent)


> #### The Perfect Companion for Instructors:
> Are you an instructor or workshop host?
> Use Git Snapshots - [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-snapshots) | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-snapshots)
> to easily broadcast your code to the remote repository, while your students use
> **Git Pull Agent** to seamlessly receive it.


## 🌐 Prefer the Browser? Try Git Live File Viewer

Don't want to clone an entire repository just to keep an eye on a single file? If you are following a webinar, a quick demo, or simply want to monitor a specific file without opening your editor, check out our companion browser extension.

**[Git Live File Viewer](https://chromewebstore.google.com/detail/git-live-file-viewer/ephkeppnaefbilkdegkihomgmellehkl)** is a lightweight Chrome extension that transforms any standard GitHub file page into a real-time, auto-updating presentation monitor.

**Why use the Chrome Extension?**
- **Zero Local Setup:** No cloning, no terminal, and no VS Code / IDE workspace required. Just open the GitHub URL.
- **Laser Focus:** Perfect for tracking a single, rapidly changing file (Live Coding Demo) in a secondary monitor.
- **Presenter-Ready UI:** Instantly expands into a sleek, dark-themed, full-screen overlay with syntax highlighting and a 1-click copy button.

👉 **[Download Git Live File Viewer from the Chrome Web Store](https://chromewebstore.google.com/detail/git-live-file-viewer/ephkeppnaefbilkdegkihomgmellehkl)**

## ✨ Other Related VS Code Family Extensions

- Git Snapshots -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-snapshots)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-snapshots)

- Git SSH Config Manager -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-ssh-config-manager)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-ssh-config-manager)

- Git Profile-Protocol Switcher -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-profile-protocol-switcher)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-profile-protocol-switcher)

- Git Repo Manager -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-repo-manager)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-repo-manager)

- Git Open Remote Repo/Files in Browser -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-open-remote-repo-file-in-browser)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-open-remote-repo-file-in-browser)

- Backup File -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/backup-file)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.backup-file)

- Tagged File Snapshots -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/tagged-file-snapshots)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.tagged-file-snapshots)

- Tagged Snapshots -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/tagged-snapshots)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=SPAjs.tagged-snapshots)

- Backup Folder -
  [Open VSX Registry](https://open-vsx.org/extension/SPAjs/backup-folder)
  | [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.backup-folder)

## ✨ Git Pull Agent Features

Git Pull Agent keeps things incredibly simple. It does one thing and does it perfectly: keeps your local repo in sync with the remote.

- **Interactive Settings Menu:** Click the `auto-pull` status bar icon to open a quick menu where you can set your exact polling interval or toggle advanced overrides.
- **Pull Now ( Ctrl + Alt + Shift + P ):** Click the `Pull Now` status bar icon to force an immediate sync with the remote repository. Resets the interval timer so you never get overlapping pulls.
- **Smart Local Protection:** If you experiment and change code locally, the agent won't blindly overwrite your work. It detects local changes and prompts you to either protect your work or overwrite it with the instructor's latest state.
- **Force Overwrite (Override Local):** Need the extension to act strictly as a read-only mirror? Toggle the Override Local setting ON from the status bar menu. The agent will aggressively update your workspace and visually warn you with an orange `Pull Now` icon.
- **Editor Agnostic:** All settings are saved securely in your repository's `.git/config` file, meaning the extension works perfectly without polluting your workspace `.vscode` settings.

## ⚙️ Configuration & Usage

Git Pull Agent configures itself directly per-repository.

1. Open a cloned Git repository in your editor.
2. Look at the bottom left of your Status Bar.
3. Click **`auto-pull: OFF`** to open the Quick Pick settings menu.
4. Select your desired polling interval (e.g., `5 seconds`, `10 seconds`, etc.). The icon will turn green to indicate it is actively listening.
5. If you want the agent to forcefully overwrite local changes without asking, select **`Force Pull (Override local) - ON`** from the same menu.
6. If you need to force an update instantly, click the **`Pull Now`** icon.

## 🛡️ Smart Protection & Conflicts

During a workshop, you might want to type along or test a piece of code yourself. If the instructor pushes an update while you have uncommitted changes in your editor, a standard `git pull` would normally crash or create messy merge conflicts.

Git Pull Agent handles this gracefully:
- If Override Local is **OFF** (Default): You will get a friendly warning asking if you want to **Overwrite Local** (discarding your experiments to catch up with the instructor) or **Skip** (keeping your changes, but pausing the updates).
- If Override Local is **ON**: The agent assumes the instructor's code is the absolute source of truth and will automatically reset your local folder to perfectly match the remote branch.

## 🛠️ Troubleshoot

### Pull Failed / Connection Error
---
***Error:***
> Git Pull Agent: Connection or pull failed. Check remote repository.

**→ Fix:** Ensure you have internet connectivity and that the repository you cloned still exists or hasn't changed its access permissions.

### Local changes detected
---
***Warning:***
> Local changes detected. Cannot apply instructor updates.

**→ Fix:** You have typed code into a file that the instructor is also modifying. Choose **Overwrite Local** to catch up to the instructor, or **Skip** if you want to preserve your local experiments.

## ☑️ Requirements

- VS Code v1.85.0 or higher (or compatible editors like Cursor, Windsurf, Antigravity).
- Git installed on your system.

## ⚖️ License

MIT

## 🏠 Home

[GitHub](https://github.com/sucom/vsce-git-pull-agent)
