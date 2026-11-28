# Korvogami Orchestrator

Give work to Claude on a board, and it gets done while you do something else.

You write what you want on a card in your own Jira board ("research three ideas for a birthday present", "fix the bug where the menu doesn't open"). The orchestrator, running on your computer, picks the card up, has Claude Code do the work, and writes a report on the card in plain words. It can run a few cards at once, waits by itself when your Claude plan's limit runs out, and asks you on the card when it needs a decision.

It installs in about 15 minutes, with no terminal and nothing to type but your board's address.

## Download

| Your computer | Download |
|---|---|
| Windows 10 or 11 | [Korvogami-Orchestrator-Setup.exe](https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-Setup.exe) |
| Mac (macOS 13 or newer) | [Korvogami-Orchestrator-mac.dmg](https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-mac.dmg) |
| Arch Linux (Omarchy too) | No download yet. A Linux computer can join a setup that already runs, from a terminal: the setup's owner has the step-by-step guide. |

Older versions and each file's fingerprint are on the [Releases](https://github.com/korvogami/orchestrator-app/releases) page.

## What you need

- **A paid Claude plan** (Pro or Max) on your own Claude account. The work runs on it.
- **A free Jira board.** The app shows you how to make one, step by step, and checks it.

That's all to start your own. You don't need a GitHub account for it. Only adding a computer to a setup that already runs needs one ([sign up](https://github.com/signup)), let in by that setup's owner.

## Install it

1. Download the file for your computer (above).
2. **Windows:** double-click it. If Windows says "Windows protected your PC", click **More info**, then **Run anyway**.
   **Mac:** open it and drag the app into **Applications**. The first time, right-click the app and choose **Open**, then **Open** again.
3. Follow the three steps on screen: install what's missing (one button), sign in to Claude on Claude's own page, then **Start my own**.

Every message on the way says what went wrong and what to do. The [install guide](INSTALL.md) has every step, what to do if something fails, and a second way to install:

**Or ask Claude to set it up with you.** Install the [Claude desktop app](https://claude.com/download), open its **Code** tab, and paste the short note from the [install guide](INSTALL.md#the-note-to-paste). Claude installs everything and explains each step in plain words. You never paste a password or key into the chat.

## Good to know

- **Your accounts stay yours.** You sign in to Claude on Claude's own page. The app never sees, copies or keeps your Claude sign-in, and it runs Anthropic's own, unchanged Claude Code.
- **Your keys stay on your computer.** Your Jira key is kept on your computer only, locked to your account.
- **It uses your Claude plan.** When your plan's limit runs out, it waits until it comes back, and says so on your board.
- **It works for you, on your computer.** Workers can install and run things on your computer to get a job done, the way Claude Code can. Give it work you'd give a helper with access to your computer.
- **Not made by Anthropic.** Korvogami Orchestrator is made by Korvogami. It uses Claude Code, but isn't made, endorsed or supported by Anthropic.
- **It keeps itself up to date.** On Windows the app installs each new version by itself when nothing is running. On a Mac it tells you when a new version is here, with a button to this page. With your own setup, the orchestrator also takes each new version from this page by itself, on Windows and Mac.
- **Removing it.** Windows: Settings, Apps, Korvogami Orchestrator, Uninstall. Mac: drag it from Applications to the Bin.

Something not working? [Tell us here](https://github.com/korvogami/orchestrator-app/issues/new), in plain words: what you pressed and what it said. (Posting there needs a free GitHub account.)
