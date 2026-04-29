# Git Pull Agent (VS Code Family Extension)

<p align="center">
  <img src="images/icon-sm.png" alt="Git Pull Agent logo" width="120"/>
</p>

A frictionless, read-only Git auto-pull companion built specifically for workshop students and learners.

When following along with a live coding session, a bootcamp, or a workshop, you shouldn't have to constantly switch to the terminal to type `git pull` just to see the instructor's latest code. Git Pull Agent runs quietly in the background, keeping your local workspace perfectly in sync with the remote repository so you can focus entirely on learning the code.

## ⚡ Quick Start

1. **Install** Git Pull Agent from the VS Code Marketplace.
2. **Clone** your instructor's or project's Git repository.
3. **Click** the `auto-pull: OFF` status bar button to toggle it `ON`.
4. Watch your files update in real-time as the instructor pushes new code!

## 🚀 Installation

- Install from [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-pull-agent) | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-pull-agent)
- Command Line: `code --install-extension spajs.git-pull-agent`

OR

1. Open VS Code
2. Go to Extensions
3. Search for `git pull agent` and select this extension
4. Click **Install**

> #### The Perfect Companion for Instructors:
> Are you an instructor or workshop host?
> Use Git Snapshots - [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-snapshots) | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-snapshots)
> to easily broadcast your code to the remote repository, while your students use
> **Git Pull Agent** to seamlessly receive it.

## ✨ Other Related Extensions

- Git SSH Config Manager -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-ssh-config-manager)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-ssh-config-manager)

- Git Snapshots -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.git-snapshots)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/git-snapshots)

- Backup File -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.backup-file)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/backup-file)

- Tagged File Snapshots -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.tagged-file-snapshots)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/tagged-file-snapshots)

- Tagged Snapshots -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=SPAjs.tagged-snapshots)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/tagged-snapshots)

- Backup Folder -
  [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=spajs.backup-folder)
  | [Open VSX Registry](https://open-vsx.org/extension/SPAjs/backup-folder)

## ✨ Git Pull Agent Features

Git Pull Agent keeps things incredibly simple. It does one thing and does it perfectly: keeps your local repo in sync with the remote.

- *Auto-Pull Interval* | *use status bar icon `auto-pull: ON`*
  Continuously polls the remote repository and pulls down new code automatically.

- *Pull Now* **( Ctrl + Alt + Shift + P )** | *use status bar icon `Pull Now`*
  Forces an immediate sync with the remote repository. Resets the interval timer so you never get overlapping pulls.

- *Smart Local Protection*
  If you experiment and change code locally, the agent won't blindly overwrite your work. It detects local changes and prompts you to either protect your work or overwrite it with the instructor's latest state.

- *Status bar icons*
  Visual shortcuts for all actions — you instantly know if the agent is actively listening for updates.

## ⚙️ Configuration

### Extension settings [ ctrl + , ] / gitPullAgent

- `gitPullAgent.intervalEnabled`: Enable or disable auto-pulling on interval. [default: false]
- `gitPullAgent.intervalMs`: Polling interval in milliseconds (minimum 1000ms). [default: 5000]
- `gitPullAgent.overrideLocal`: If true, forcefully overwrites any local changes you make without asking. If false, prompts you to overwrite or skip. [default: false]

## 🚀 Usage

1. Open the cloned workshop folder in VS Code.
2. Look at the bottom left of your VS Code Status Bar.
3. Click **`auto-pull: OFF`** to turn the agent **ON**. The icon will turn green.
4. If you need to force an update instantly, click **`Pull Now`** icon.

## 🛡️ Smart Protection & Conflicts

During a workshop, you might want to type along or test a piece of code yourself. If the instructor pushes an update while you have uncommitted changes in your editor, a standard `git pull` would normally crash or create messy merge conflicts.

Git Pull Agent handles this gracefully:
- If `overrideLocal` is **false** (Default): You will get a friendly warning asking if you want to **Overwrite Local** (discarding your experiments to catch up with the instructor) or **Skip** (keeping your changes, but pausing the updates).
- If `overrideLocal` is **true**: The agent assumes the instructor's code is the absolute source of truth and will automatically reset your local folder to perfectly match the remote branch.

> ### ⚠️ Important Setup Tip for Instructors
> Because Git Pull Agent saves its "ON/OFF" toggle state directly to the VS Code workspace configuration, it automatically modifies the `.vscode/settings.json` file.
>
> If the `.vscode` folder is tracked by Git, the moment a student turns the agent ON, Git will see it as a "local change," and the Smart Protection feature will block the auto-pull!
>
> **How to fix:** Always ensure you add `.vscode*/` to your workshop repository's `.gitignore` file before the session begins.

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

- VS Code v1.85.0 or higher.
- Git installed on your system.

## ⚖️ License

MIT

## 🏠 Home

[GitHub](https://github.com/sucom/vsce-git-pull-agent)
