# Changelog

## 🎉 Git Pull Agent v1.0.0 — Initial Release

The first stable release! Built specifically to make remote workshops, bootcamps, and live coding sessions completely frictionless for students.

### ✨ Features:
- **Interval Auto-Pull:** Configurable background polling that quietly fetches remote updates without locking up the editor.
- **Manual "Pull Now":** Instantly sync with the remote using the status bar button or the `Ctrl+Alt+Shift+P` keybinding. Timer resets automatically to prevent overlapping pulls.
- **Smart Status Bar UI:** Clear, visual indicators showing whether the agent is active (Green for ON) and a spinning animation when a pull is actively in progress.
- **Local Change Protection:** Intelligently detects if a student has modified files locally. Prevents terminal-crashing merge conflicts by prompting the user to either force-overwrite their changes or skip the sync to protect their work.
- **Force Overwrite Configuration:** Added `gitPullAgent.overrideLocal` for a true "read-only broadcast" mode, automatically discarding local changes in favor of the remote truth.
- **Auto-disposing Notifications:** Clean toaster notifications that confirm sync status without spamming the user during rapid interval pulls.