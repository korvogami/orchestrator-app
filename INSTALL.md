# Installing the orchestrator

For anyone, no technical knowledge needed. About 15 minutes, plus 5 if you're making your own Jira board. You never need to type a command.

There are two ways. Pick one:

- **Way 1: the installer.** Double-click it and follow the three steps on screen.
- **Way 2: ask Claude.** Paste a short note into the Claude app and Claude does the setup with you, explaining each step.

Both end in the same place: the orchestrator running on your computer, ready for its first job.

## What you need first

- **A computer:** Windows 10 or 11, or a Mac (macOS 13 or newer).
- **A paid Claude plan on your own account** (Pro or Max). The workers run on it. The free plan can't run them.
- **The installer file**, from the orchestrator's download page on GitHub, [github.com/korvogami/orchestrator-app](https://github.com/korvogami/orchestrator-app) (or from whoever shared the orchestrator with you). You don't need a GitHub account to download it:
  - Windows: [`Korvogami-Orchestrator-Setup.exe`](https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-Setup.exe)
  - Mac: [`Korvogami-Orchestrator-mac.dmg`](https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-mac.dmg)
  - Each version's files, with their fingerprints, are on the page's **Releases**.
- **One of these:**
  - **Joining a setup** (another computer for an orchestrator that already runs): a join code from that computer, and a free GitHub account (make one at github.com/signup) that the setup's owner has added to that orchestrator's code on GitHub.
  - **Starting your own:** nothing more, and no GitHub account. You'll make a free Jira board on the way.

## Way 1: the installer

### On Windows

1. Double-click the installer. (If your browser held the download back, choose **Keep** in its downloads list first. In Edge: the three dots by the file, **Keep**, **Show more**, **Keep anyway**.)
2. Windows may say **"Windows protected your PC"**. That's because the app isn't signed with a paid certificate yet, not because something is wrong. Click **More info**, then **Run anyway**.
3. It installs by itself in a few seconds (no questions) and opens.
4. Follow the three steps on screen (below).

### On a Mac

1. Double-click the `.dmg` file. Drag **Korvogami Orchestrator** into **Applications**.
2. The first time only: open **Applications**, **right-click** (or Control-click) **Korvogami Orchestrator**, choose **Open**, then **Open** again. The Mac asks because the app isn't from a paid Apple developer account yet.
   - On macOS 15 or newer, if it still says it can't be opened: open **System Settings**, then **Privacy & Security**, scroll down, and click **Open Anyway** next to Korvogami Orchestrator. Type your Mac's password if it asks.
3. Follow the three steps on screen (below).

### The three steps on screen

**1. Install what's missing.** The app checks for the five tools the workers use: Claude Code, Git, Node.js, the GitHub CLI and Chrome. Press **Install everything**: they install one after another, in a few minutes.

- Windows may ask **"Do you want to allow this app to make changes to your device?"**. Click **Yes**.
- A Mac may ask for your password (the one you sign in to the Mac with), or show a box from Apple about "command line developer tools": click **Install**.
- If one won't install, its line says why and has a **Get it yourself** button: it opens that tool's own download page. Download it, open the file, click through with the usual choices, then press **Check again**.

**2. Sign in.** Two buttons, each opening that service's own sign-in page in your browser. The app never sees your passwords, and never sees or keeps your Claude sign-in.

- **Sign in to Claude:** sign in on Claude's page with your own Claude account.
- **Sign in to GitHub:** only if you're joining a setup. Starting your own doesn't need it: leave that line as it is. To sign in, press **Sign in to GitHub**: GitHub's page opens in your browser, and the app shows a short code (already copied). Type or paste it on GitHub's page and approve. The line turns green by itself. If both computers are yours, use the same Claude, GitHub and Jira accounts as on the first one.
- Then press **Check again**. The line for each sign-in you did turns green.

**3. Join a setup, or start your own.**

- **Join a setup** (a second computer):
  1. On the computer that already runs the orchestrator, open the app, go to **Keys and settings**, press **Add a computer**, then **Copy it**. Send it to yourself (an email or a note). It has no passwords or keys in it, and it works once, for 30 minutes: if it runs out, press **Add a computer** again. No app on that computer yet? Install it there first, with the same installer: it finds the orchestrator that's already running.
  2. Paste the whole thing into **Join code** (it starts with JOIN-; the short code on the card isn't enough on a new computer), give this computer a short name (like "Desk PC"), and type your Jira email and a Jira key (the app's link makes one: name it after this computer).
  3. Press **Join**. It copies the orchestrator from GitHub and checks the board.
- **Start my own** (you're new): seven short steps, one screen each, with a picture of what to look for. Press **Next** after each.
  1. **Claude:** it checks Claude is installed and signed in. If not, press **Install Claude Code** or **Sign in to Claude**: Claude's own page opens in your browser. Sign in and click **Authorize**; the screen turns green by itself.
  2. **Your name:** your first name.
  3. **Your own Jira:** **Make a free Jira** (sign up with your email) and **Make a Jira key** open the right pages. On the key page, use the first button, **Create API token**, not the one "with scopes". Type your Jira site, email and key.
  4. **Your board:** press **Make my board**. It's ready straight away, with Jira's own three columns (To Do, In Progress, Done): there's nothing to add or change on it. A job that needs your answer gets a `needs-you` tag there instead of a column of its own, and your Claude chat tells you about it.
  5. **Your settings:** press **Make my orchestrator**.
  6. **Your Claude chat:** connect Atlassian in Claude's settings, then **Copy my instructions** and paste them into your Claude profile.
  7. **Your first job:** press **Start my orchestrator**. In 2 to 5 minutes it says **"Your first job is finished. You're done!"**, with a welcome note.

After **Join a setup**: **All set**. Leave **Start the orchestrator each time this computer starts** ticked, and press **Start the orchestrator**.

**Started your own?** Step 6, **Your Claude chat**, hands you the note for your own Claude (**Copy my instructions**). If you skipped it, see "Tell your Claude about it" below: the same note stays in the app.

**New versions, with your own setup:** on Windows the app installs each new version from the page by itself; on a Mac it tells you when there is one (download it and drag it into Applications, choosing Replace). Once the new app opens, your orchestrator takes the new version by itself the next time no job is running, and restarts on it. Your orchestrator also looks at the download page by itself a few times a day and takes a new version from there the same way, on Windows or a Mac, even with the app closed. If it ever can't, your status page says "A newer version is ready to download" and where to get it. Only the orchestrator itself changes: your settings, keys, board and jobs stay as they are. If a new version won't start, it goes back to the one that worked by itself.

### If something goes wrong

Every message in the app says what happened and what to do. The common ones:

| It says | Do this |
|---|---|
| Windows says Smart App Control blocked the installer | Some newer Windows 11 computers block every app that isn't signed with a paid certificate, with no "Run anyway". Look under **Settings**, **Privacy & security**, **Windows Security**, **App & browser control**, **Smart App Control**. Turning it off lets the installer run, but lowers that protection for everything else, and Windows may not let you turn it back on. Or tell us on the download page and wait for the signed version. |
| Windows' own installer (winget) isn't on this computer yet | Open the Microsoft Store, search for **App Installer**, press **Update**, then press **Install** again. Or use **Get it yourself**. |
| There's no Jira site at ... | Open Jira in your browser and copy the address up to the first "/", like `yourname.atlassian.net`. |
| Jira didn't accept that email and key | Make a new key and paste the whole thing. Use the email you sign in to Jira with. |
| Joining: the board ... needs a column called "Review" | The setup you're joining moves finished jobs to a Review column. On its board, press the **+** after the last column and add **Review**, then move it before **Done**. (Starting your own never asks for this.) |
| This GitHub account can't see the orchestrator's code | Ask whoever gave you the join code to add your GitHub account to the orchestrator's code on GitHub. |
| GitHub didn't let this computer in | Press **Sign in to GitHub** again in step 2. |

Still stuck? Use Way 2: Claude can read where the setup stands and explain it.

## Way 2: ask Claude to set it up

**Which Claude to use: the Claude desktop app, in its Code tab.** Download it from claude.com/download and sign in with your own Claude account.

Why this one:

- It's a normal app you install like any other, with no terminal.
- In its **Code** tab, Claude can actually do the setup on your computer. It asks before each step (you click **Allow**), and you can see everything it does.
- The Claude website and the phone app can only talk: they can't install anything on your computer.
- Claude Code in a terminal works too, but a beginner shouldn't need a terminal.

Steps:

1. Download the installer file into your **Downloads** folder (the links above). If you skip this, Claude downloads it for you.
2. Open the Claude desktop app, go to the **Code** tab, and start a new session on this computer. When it asks for a folder, choose **Downloads**. Leave it on asking before it runs things.
3. Copy the whole note below, paste it, and send it.
4. Each time Claude asks to run something, read its one-line reason and click **Allow**.
5. When it asks you to do something in the orchestrator app (signing in, typing your Jira key), do it there. Never paste a password, token or key into the chat.

### The note to paste

```text
Please set up "the orchestrator" on this computer for me, start to finish. I'm a beginner: before each step, tell me in one or two plain sentences what you're about to do and why, and never ask me to type commands myself.

What it is: a desktop app called "Korvogami Orchestrator" that runs Claude Code workers for jobs on a Jira board. Its installer should be in my Downloads folder: Korvogami-Orchestrator-Setup*.exe on Windows, or Korvogami-Orchestrator*mac.dmg on a Mac. If it isn't, download the newest one into Downloads from its GitHub page: https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-Setup.exe (Windows) or https://github.com/korvogami/orchestrator-app/releases/latest/download/Korvogami-Orchestrator-mac.dmg (Mac).

1. Tell me whether this is Windows or a Mac.
2. Install the app.
   - Windows: run the installer with /S (it installs silently for this user, no admin needed). The app ends up at %LOCALAPPDATA%\Programs\korvogami-orchestrator-desktop\Korvogami Orchestrator.exe.
   - Mac: open the .dmg, copy the app to /Applications, then tell me how to open it the first time (right-click it, Open, Open; on macOS 15 or newer: System Settings, Privacy & Security, Open Anyway).
3. Check where the setup stands by running the app with: --setup-status "<a file in my Downloads folder>" (it writes a plain-text list of what's installed and signed in, changes nothing and quits). Read that file. Run it again after each step to check.
4. Install whatever it lists as missing, one tool at a time, saying what each is for: Claude Code, Git, Node.js 20 or newer, the GitHub CLI (gh), Chrome (or Edge on Windows).
   - Windows: use winget, for example: winget install --id Git.Git --exact --source winget --accept-package-agreements --accept-source-agreements (and OpenJS.NodeJS.LTS, GitHub.cli, Google.Chrome). If winget is missing, tell me to update "App Installer" from the Microsoft Store.
   - Mac: use Homebrew if it's installed; otherwise run "xcode-select --install" for Git and send me to each tool's own download page for the rest.
   - Claude Code, if missing: Anthropic's own installer (Windows PowerShell: irm https://claude.ai/install.ps1 | iex; Mac: curl -fsSL https://claude.ai/install.sh | bash).
5. Sign-ins: I do these myself, in the app ("Sign in to Claude", and "Sign in to GitHub" only if I'm joining a setup). Never ask me for a password, token or key, and don't run any sign-in yourself.
6. Open the app and walk me through its step 3. Ask me first whether I'm joining a setup (I'd have a join code) or starting my own. For "Start my own", help me through its seven steps, one screen at a time: each says what I should see. I type the Jira key into the app myself, never into this chat.
7. If anything fails, read the message (or the status file), tell me in plain words what went wrong and what we'll do about it, and fix it. If you can't fix it, write me a short plain message I can post at https://github.com/korvogami/orchestrator-app/issues/new (what we pressed, what it said, and which computer this is), with nothing private in it.
8. When the status file says "set up" and "The orchestrator is running", tell me how to give it a first job.
9. If I started my own: the status file now ends with a note for my own Claude, and where it goes. Show me the note and walk me through pasting it into Claude's settings myself (Settings, Profile, the box for my personal preferences), and turning on the Atlassian connector (Settings, Connectors). It tells every Claude chat of mine, my phone's too, where my board is and to post my answers starting "From <my first name> (via Claude):", which is how the orchestrator knows they're mine. Then ask me whether to add the same note to Claude Code's own instructions on this computer (the file CLAUDE.md in the .claude folder of my home folder: at the end, keeping what's there). Only do that if I say yes.

Don't change anything else on this computer.
```

## Your first job

Make a card in your board's **To Do** column saying what you want in plain words. If it isn't about a code project, add a line `Repo: none`. Within a minute the orchestrator moves it to **In Progress**, starts a worker, and writes its report on the card.

You can also ask Claude (on your phone or computer, with Jira connected in its settings) to make the card for you: "Make a ticket on my orchestrator board: research three ideas for a birthday present. Repo: none."

## Tell your Claude about it

For a setup you started yourself. Do it once, and any Claude chat of yours, the app on your phone too, can tell you what's going on, make jobs for you, and pass on your answers.

1. In the orchestrator app, open **Keys and settings** and press **Copy the note for Claude** (it's the same note as **Copy my instructions** in step 6 of **Start my own**). The note has your board and your first name in it, and no passwords or keys.
2. In the Claude app on your computer, or on claude.ai, open **Settings**, then **Profile**, and paste it into the box for your personal preferences. It's saved to your Claude account, so your phone gets it too.
3. Under **Settings**, **Connectors**, turn on **Atlassian** (that's Jira) and sign in to your Jira.

Then just talk to Claude: "what's going on?", "make the button bigger on that last one", "yes, go with the first choice".

**Why it matters.** When a job asks you something, or you want a finished job changed, Claude posts your words on that job's card, starting "From Sam (via Claude):" (with your first name). That start is how the orchestrator knows the words are yours. It carries on with your answer, and on a finished job it starts a follow-up job by itself. On a finished job, a comment that doesn't start that way does nothing. And when you only want a reason kept on a card (why you closed or dropped it), Claude starts it "From Sam (via Claude): Note only, nothing to build:", and the orchestrator never starts a job from it.

- **Typing on a card yourself?** Start your comment the same way: "From Sam: make the button bigger".
- **Changed your first name in the orchestrator's settings?** Copy the note again and replace the old one in Claude.
- **Joined someone else's setup?** Skip this: the jobs and the answers are theirs.

## Good to know

- **Your accounts stay yours.** Each person signs in to Claude on Claude's own page, with their own account and plan. The app never collects, copies or keeps a Claude sign-in. That's Anthropic's rule for tools like this, and it's how the app works.
- **Your keys stay on your computer.** The Jira key is kept on this computer only, locked to your account (Windows' data protection, or the Mac's keychain).
- **It uses your Claude plan.** Workers use your plan's allowance. When it runs out, the orchestrator waits until it comes back, and says so.
- **It keeps itself up to date.** On Windows the app installs each new version by itself when no job is running, and opens again with everything as it was. On a Mac it says when a new version is on the download page: quit the app, download it, drag it into Applications and choose Replace. With your own setup, the orchestrator also takes new versions from the page by itself, on Windows and Mac. Your settings and board stay as they are either way.
- **Keep it running.** A sleeping computer can't start your jobs. Leave it plugged in and set it to never sleep while plugged in (Windows: Settings, System, Power. Mac: System Settings, Battery or Energy). After a restart, sign in to the computer and the orchestrator starts again by itself. Closing the app's window doesn't stop it; **Quit, and stop the orchestrator**, in its little icon by the clock, does.
- **Stopping or removing a joined computer.** For a while: **Pause this computer** in its app. For good, on that computer: open the app, go to **Keys and settings**, and press **Leave this setup**. Jobs it's in the middle of can finish first, or go back to the list for another computer. Then it stops, forgets the setup's key and leaves the status. For good, when it's off or gone: on another computer of the setup, press **Remove** next to it on the same screen, or tell Claude "remove Desk PC" (with its name). Either way, one thing is left for you: delete the Jira key you made for that computer on Jira's key page (the app says which). The other computers get a new lock on the keys they share by themselves. Changed your mind? Make a new code with **Add a computer** and press **Join again** on it.
- **Removing it.** Windows: Settings, Apps, Korvogami Orchestrator, Uninstall. Mac: drag it from Applications to the Bin. Your orchestrator's folder (in your home folder) stays until you delete it.
