---
layout: layouts/post.njk
title: 'Guide to the Computing Science Student''s Setup, 2019 insIDE club edition.'
date: 2019-06-21T04:47:00.000Z
---
## Introduction
This guide will cover how to install the majority of tools you will be using
throughout a typical Computing Science (CS) degree.
This guide covers installations for **MacOS** and **Windows**, and assumes that anyone who is using **Linux** already has a setup they are comfortable with.

## package managers

### The problem

Here's a typical scenario of software installation. You hear about a tool called `a_cool_tool` that you want to download.

You first try Googling for it, but unfortunately the name is so generic that you
get a ton of unrelated results (I'm looking at you, [Rust](https://www.rust-lang.org)).

You finally find what you think is the right thing, but now you have to read
through a ton of introduction, ads, and / or have to sign up for a newsletter to
download the software.

Once the software downloads and you run the installer, you realize that the
version you downloaded doesnt work for your operating system / version.
Feeling frustrated, you look for fixes until you finally get it working.
However, you still get an annoying prompt to re-visit the site and download the
latest version everytime theres an update. Not only that, but to uninstall it,
chances are you either need to dig through hidden folders and scrape out all the
hidden files, or hope that you can find the uninstaller and that it does its
job.

### The solution

Package managers come to the rescue. For **Windows**, head to [https://chocolatey.org/](https://chocolatey.org/) and click
the "Install Chocolatey Now" button. for **MacOS**, open *Terminal* and enter 
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`.

### Installing packages
One thing to note about *Homebrew* is that it separates Command Line Interface (CLI) applications from Graphical User 
Interface applications. If you're not sure what the difference between each is, a summary is explained below.

Installing CLI packages with *Homebrew* is done with `brew install the_package_name`. For GUI applications, use
`brew cask install the_package_name`. *Chocolatey* allows you to install packages simply by entering
`choco install the_package_name`.

### Other commands
Both *Chocolatey* and *Homebrew* allow you to search for a package using the `brew/choco search package_to_search` command,
and to upgrade packages using `brew/choco upgrade package_to_upgrade`. *Homebrew* can upgrade all packages simply by
running `brew upgrade`, whereas *Chocolatey* uses `choco upgrade all`.

### Example
Say you want to install the latest version
of [Python](https://www.python.org/). For *Chocolatey*, just type
`choco install python` and it will automatically find a compatible version of
Python and install it for you! *Homebrew* is similar, simply type in `brew install python3` 
(entering `python` will install Python version 2, which you do **not** want!).

On **MacOS**, I highly suggest installing `sl`, `lolcat`, `cowsay`,  `fortune`, and `neofetch` (purely for work purposes, I promise!)
and playing around with them. Try using the `|` to get interesting combinations, such as `sl | lolcat`. Unfortunately
for **Windows**, I do not know of any fun packages to install, unless you install the *Linux Subsystem for Windows*
(more on that below).

## Text editor
Almost all of your software development is going to be spent in a test editor of some sort, so it's a good idea to get a
good one. [VSCode](https://code.visualstudio.com/) is my personal favorite, which you can install from the link or a
package manager as a GUI application (use the `cask` command for *Homebrew*!). Once it's download, install it and then
open it.

### Extensions
*VSCode* is already quite powerful by itself, but we cna easily extend it and personalize it with its numerous extensions
(there's even one for Spotify!). I suggest installing the following extensions:
- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) 
- [C / C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
- [Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)

You can create a new file and then save it with the appropriate extension (eg `.py` for *Python*), 
and *VSCode* will automatically do syntax highlighting and linting on your code, saving you alot of time and mistakes!

### Built-in terminal
*VSCode* has a built-in terminal, which you can activate by pressing both `control` and \`. From here you can enter all
the commands you normally would, such as `python my_code.py`.

## Recommended installations

### Common languages / tools
I suggest installing the following using your respective package managers, or from the web:
- [Python](https://www.python.org/), a common programming language
- [NodeJS](https://nodejs.org/en/), a JavaScript runtime (for webapps)

### Windows only 
- [Visual Studio IDE](https://visualstudio.microsoft.com/), **make sure to install C++ tools!**
- [Windows Terminal](https://github.com/microsoft/terminal), still in development at the time of writing, but definitely the best terminal for windows.
### MacOS only
- Xcode & Xcode CLI tools: install Xcode from the app store, and run `xcode-select --install`
- [iTerm2](https://www.iterm2.com/), my favorite terminal for MacOS (use instead of Terminal)

### Extras
These extras are either more of a personal recommendation, or are related to insIDE club events.
- *Latex*: I highly advise installing and learning to use Latex. The installation method varies between operating systems and distributions, and so would likely need its own tutorial (there are many good ones on the web).
- [Rust](https://www.rust-lang.org): A new language which offers many appealing features.
- [GameBoy Studio](https://www.gbstudio.dev), easily make GameBoy games!
- [Hylia](https://hylia.website), a static website tool

## Github
### Purpose
The main purpose of *GitHub*, besides hosting your projects, is Version Control. This is essentially *undo* / *redo* on
steroids. If you make a mistake, you can easily undo it. When you want to save changes to your project, you can use `commit` to commit changes, and 
see how they compare to previous versions or what exactly you have changed. Then, to actually push the update from your computer to *GitHub*, you use `push`.
When you commit a change, you are required to enter a *commit message*. While this may initially be annoying, this is a very good practice,
so that incase something goes wrong in the future, you can look back at your changes and see the description of each commit.
This will help keep track of when and what you did.
### Register
Make to register at [https://github.com/](https://github.com/), so you can access its vast collection of repositories 
and make your own. Respositories are essentially packages containing things like tools, projects, or apps that other
fellow developers have made. For example, *Google* has their repositories [here](https://github.com/google), and you can find my own [here](https://github.com/pnadon?tab=repositories).

### GitHub Desktop
The easiest way to manage your repositories is by downloading and installing [GitHub Desktop](https://desktop.github.com/) for Version Control (you'll need this soon, and use it indefinitely).
Sign into your *GitHub* account from within *Github Desktop*, and then head to *File* -> *Options* for **Windows**, or *GitHub Desktop* -> *Preferences* for **MacOS**.
From there, click the *Advanced* tab, and select your preferred External Editor and Shell (in my case, *Visual Studio Code*, and *iTerm2*).


**Make sure to sign up using your university email, so you can get the perks of being a student. This applies to many other services (Spotify, etc.) so keep an eye out!**

## Windows Subsystem for Linux
After going through this tutorial, you start to see why so many people find **MacOS** / **Linux** appealing. When it comes to software development, the support for tools and languages typically goes (from most / soonest support to latest) **Linux** -> **MacOS** -> **Windows**. **MacOS** usually gets support around the same time as **Linux**, and has even occasionally gotten it sooner due to *Apple's* influences and internal development, [LLVM](https://llvm.org) being an excellent example (LLVM forms the backend of a significant portion of emerging programming languages, read more [here](https://en.wikipedia.org/wiki/LLVM)).

## CLI vs GUI
Let's start by explaining what each is. 

### CLI (Command Line Interface)
CLI is the most "basic" form of computer-human interaction, where a user would enter a command or series of commands into a terminal, 
and the computer would think for a bit and spit out an output. This form of interaction far precedes GUIs, and is still
a popular and even preferred approach of interfacing due to productivity reasons. 

For example, on **Linux** (and **MacOS**), 
If you have a test file named `my_paper.txt` in your home folder's `Download` directory, and you want to find how many times the
word `the` appears in it, all you have to do is type `grep -o -i the ~/Desktop | wc -l`, and voila. 

You can get stuff done in a fraction of the time, assuming you're patient enough to learn the commands 
(or just use Google like I do). You might have also noticed the `|` symbol in the above command. That's the "pipe"
symbol, and its used to take the output of the previous command and put it in the next. In the above case, the `grep ..`
portion reads the file and spits out all words matching the filter you used (`the`). This means it would also catch
`there` or `they` since i didn't specify that the word had to only contain `the`. Then, `|` would take those `the`'s and
input them into `wc`, which stands for *word count*, which counts the number of words inputted, and finally outputs `6` 
(in my case at least).

### GUI
On the other hand, GUIs are designed to be used with a mouse and navigate by clicking buttons and such. The advantage of
GUIs is that they have a very shallow learning curve (just click the thing you want), and are better designed for things
like media consumption (imagine text-based instagram or youtube) where the desired output cannot be easily expressed
with simple text. However, as you become more comfortable with software development, you may begin to prefer CLI due
to the previously explained reasons.
