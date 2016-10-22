# Chem122-2016

This repository contains visualization exercises for *Chemical Principles 2016* (Chem 122) at Kenyon College, along with the code necessary to do them.

These exercises assume that you have a Cloud9 account and a Linux workspace ready to go. [Cloud9](https://c9.io) is a cloud-based computing environment. It allows you to control a remote Linux workspace through a browser-based web app called the Cloud9 IDE. 


## Getting started with Cloud9

You will receive an email invitation to join the `chem122` team at Cloud9. Accept the invitation and select **Create new account**. Select a display name, a username, and identify as a **student** doing **coursework**. You should *not* be asked for a credit card. Finish by selecting **Join team**. Check your email and click the activation link to set your password.

At your dashboard, click **Workspaces > Create a new workspace**. Set the following options:

- Workspace name: `vsepr`
- Team: `Chemical Principles`
- Hosted workspace: **Public**
- Clone from Git URL: `https://github.com/garcias/Chem122-2016.git`
- Choose a template: **Blank**

After a few minutes, Cloud9 will present a layout with a few tabs. Click through the guided tour, reading the comments if you are curious. Close the `README.md` tab to view the `Welcome` tab. Set the following options:

- Preset: **Full IDE**
- Main Theme: *light or dark, whichever is easiest on your eyes*
- Split Layout: **Two Horizontal Split**
- Editor Theme: *your preference, though Cloud9, Solarized, and Tomorrow themes are popular*
- Keyboard Mode: **Default** (unless you have a preference for Vim or Sublime)
- Soft Tabs: `4`

Close the `Welcome` tab.

## Guided tour of using your workspace

In the lines below, the `$` represents the end of the terminal prompt; type only the text after the `$`. Lines starting with `#` indicate the computer's response to your command. In Linux, upper and lower case make a difference, as do spaces.

This repository was cloned to your workspace from GitHub. To see this, use the `ls` command in the terminal window. The terminal should display a listing of the same files and folders as on the Github page.

```bash
    $ ls
#   JSME/  README.md  caffeine.htm  jsmol/  orbitals/  shape/  vsepr/  welcome/
```

To see what's in the `welcome/` folder, you can "change directory" using the `cd` command; and then list its contents using `ls`. You should see a single file named `primera.md`. You can view the contents of this file (and of any text-based file) using the `c9 open` command.

```bash
    $ cd welcome
    $ ls
#   primera.md
    $ c9 open primera.md
```

Close the file (**File > Close File** or click x in the tab). Now copy this file using the `cp` command, giving it a new name of `segunda.md`. Use `ls` to verify there are now two files. Open the new file.

```bash
    $ cp primera.md segunda.md
    $ ls
#   primero.md    segunda.md
    $ c9 open segunda.md
```

Change its text however you like, and then save it. You can use either the Cloud9 menu (**File > Save**) or a keyboard shortcut (ctrl-S on Windows, cmd-S on Mac).

To return to the parent folder, use `cd` again. In Linux, double periods `..` refers to the "parent directory" of the current one.

```bash
    $ cd ..
```

Congratulations! You are in control of your very own Linux machine! You can now work on the visualization exercises in the other directories (`vsepr`, `shape`, etc). Enjoy!
