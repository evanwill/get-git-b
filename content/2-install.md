---
title: Install and Setup Git
nav: Git
---

## Install Git

Installing this free and open source software is pretty straightforward:

**Windows:** 

- Install [Git for Windows](https://git-scm.com/downloads){:target="_blank" rel="noopener"} using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows.

**Mac:** 

- Mac systems will require the "Xcode Command Line Tools" installed, so open a terminal (to find your terminal search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. If you want a newer version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank" rel="noopener"}.

**Linux:** 

- Install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

## Setup

To start learning Git we will use it on the command line.
Although there are GUI clients to manage Git repositories, being familiar with the command line version will help you better understand the basic workflow.
If you need a command line refresher, check out this [mini-lesson](https://evanwill.github.io/_drafts/notes/commandline.html){:target="_blank" rel="noopener"}.
So fire up your favorite shell, terminal, or Git Bash to get started!

Some initial setup is necessary the first time you use Git on a computer.
You will use these commands only once, unless you want to change something.

Set your name and email (matching your GitHub account):

```
git config --global user.name "Evan Will"
git config --global user.email "myemail@gmail.com"
```

> Your email and user name is recorded with every commit.
> This helps ensure integrity and authenticity of the history.
> Most people keep their email public, but if you are concerned about privacy, check GitHub's tips to [hide your email](https://help.github.com/articles/about-commit-email-addresses/){:target="_blank" rel="noopener"}.

Next, set your default text editor. 
The current versions of the Git for Windows installer allow you to set the default editor during [setup]({{ '/0-prep.html' | relative_url }}), so Windows users should not need to complete this step and should have nano set as the default editor.
In general Linux and Mac users should set their Git `core.editor` to `"nano -w"` as well.
Nano is a basic command line editor that is *fairly* easy to use.
Set the default editor with this command:

```
git config --global core.editor "nano -w"
```

> Git opens the default editor to ask for commit messages. 
> You are most likely to encounter it when merging.
> If you don't set a default editor, Git will use the default default--which might be surprising if you are not used to terminal-based editors such as [Vim](http://www.vim.org/){:target="_blank" rel="noopener"}. 
> If you are stuck in Vim and can't figure out how to escape, type `Esc` then `:wq` then `Enter` to save and quit ([VIM quick ref](https://w3.cs.jmu.edu/bernstdh/Web/common/help/vim.php){:target="_blank" rel="noopener"}, and don't worry, you are [not alone in confusion](https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/){:target="_blank" rel="noopener"}).

With our test repository ready and Git configured, we can move on to the basic [Git workflow]({{ '/3-workflow.html' | absolute_url }})!

## Create Repository Locally

*P.s.* If you really want to, you can create a local repository:

```
mkdir test
cd test
git init
```

If you want to connect this repository to GitHub, you have to `git remote add`.
Generally, it is easier to create the repo on GitHub first and `clone`, rather than using `init`.
However, `init` is useful if you will not be pushing to a remote repo.
