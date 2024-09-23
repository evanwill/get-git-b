---
title: Install and Setup Git
nav: Git
youtubeid: aErB_K7ZvMs
---

In the last section we created a new project on GitHub--the next step is to `clone` that repository to our local machine to start working on it.
To do that, you will need Git installed on your computer.

## Install Git

Installing this free and open source software is pretty straightforward:

{% capture windows %}
Download and run the [Git for Windows](https://git-scm.com/downloads){:target="_blank" rel="noopener"} installer. 
Using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". 

This package will give you Git, Git Bash, and Git GUI. 
Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows.
{% endcapture %}
{% capture mac %}
Choose one of these options:

- Installing the "Xcode Command Line Tools" will provide Git and a variety of other developer helpers. Open a terminal (to find your terminal search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. 
- For newest version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank" rel="noopener"}.
{% endcapture %}
{% capture linux %}
Your distribution's software center or package manager will be able to install Git (it is pre-installed on many distros, check by typing `git --version` into a terminal).

To install on Ubuntu, use: `sudo apt install git`.
{% endcapture %}
{% include accordion.html title1="Windows" text1=windows title2="Mac" text2=mac title3="Linux" text3=linux %}

## Open a Terminal

For this workshop we will be using Git on the command line.
Although there are GUI clients to manage Git repositories, being familiar with the command line version will help you better understand the basic workflow.

So the first step is to open a terminal window! 

On Windows you will have to use "Git Bash" which comes packaged with the Git installer. 
This provides a UNIX-like environment, so your commands are the same as on Linux or Mac.
Open your Start menu and search for "Git Bash" to open your terminal. 
You can also right click on a folder in File Explorer and choose the option "Git Bash Here"--this can save time navigating around on the command line!

On Mac and Linux, your terminal app is called "terminal"!
Search for it and open.
You are ready to go!

{% include figure.html img="gitbash.png" alt="git bash terminal window" %}

Check the [command line navigation cheatsheet]({{ '/content/cheatsheet.html#command-line-navigation' | relative_url }}) or this [mini-lesson](https://evanwill.github.io/_drafts/notes/commandline.html){:target="_blank" rel="noopener"} if you need a refresher.

## Git Setup

Some initial setup is necessary the **first time** you use Git on a computer.
You will use these commands only once, unless you want to change something.

Set your user name and email (matching your GitHub account):

```
git config --global user.name "example name"
git config --global user.email "myemail@gmail.com"
```

(If you set [set up email privacy](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#about-commit-email-addresses){:target="_blank" rel="noopener"} on GitHub, remember to use the correct email alias!)

Next, set your default text editor. 
The current versions of the Git for Windows installer allow you to set the default editor during setup, so Windows users should not need to complete this step.
In general Linux and Mac users should set their Git `core.editor` to `"nano -w"` as well.
Nano is a basic command line editor that is *fairly* easy to use.
Set the default editor with this command:

```
git config --global core.editor "nano -w"
```

Git opens the default editor to ask for commit messages if you did not provide one--which you are most likely to encounter it when merging.

The default default is Vim, which can be confusing...
If you are stuck in Vim and can't figure out how to escape, type `Esc` then `:wq` then `Enter` to save and quit ([VIM quick ref](https://w3.cs.jmu.edu/bernstdh/Web/common/help/vim.php){:target="_blank" rel="noopener"}, and don't worry, you are [not alone in confusion](https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/){:target="_blank" rel="noopener"}).

With our test repository ready on GitHub and Git configured on your computer, we can move on to the basic [Git workflow]({{ '/content/3-workflow.html' | relative_url }})!

*Note:* one more config you might run in to is for pull. 
Recent Git installations do not have a default behavior set for `git pull`, so the first time you encounter a conflict and merge, you will get a big error message asking which approach you want to use (merge or rebase). 
To avoid this, you can set the old default behavior in your config, which is `git config --global pull.rebase false`.

{% capture auth %}
## Authentication 

When you push to GitHub or other platforms you will need to authenticate. 
The exact details of authenticating from the terminal will depend on the platform, security settings, and your operating system.

- On Windows git will come with a builtin credential manager--the first time you try to `push` you should be redirected to your web browser to authorize on GitHub. 
- On Mac (and Windows) GitHub Desktop or Visual Studio Code also bundle a git credential manager--however, you may need to make your first push on on those tools to initially set up authorization, then it will work on the terminal as well. 
- On Linux you will probably want to [manually set up a credential manager](https://evanwill.github.io/_drafts/notes/git-credential.html).

Check the [authentication docs on GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#authenticating-with-the-command-line) for more info.

{% endcapture %}
{% include card.html text=auth %}

{% capture local %}
## Create Repository Locally

*P.S.* 
In general it is easiest to start a repository on GitHub then clone to your local machine. 
However, if you really want to, you can create a local repository:

```
mkdir example-repo
cd example-repo
git init
```

If you want to connect this local repository to GitHub, you have to use `git remote add` to set up the "remote".
{% endcapture %}
{% include card.html text=local %}
