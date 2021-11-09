---
title: Getting Started on GitHub
nav: GitHub
---

Let's take a look at an example repository on GitHub.

## Get a GitHub Account

[GitHub](https://github.com/){:target="_blank" rel="noopener"} is a Git repository hosting service, a place to store and sync your work in the cloud. 

Visit <https://github.com> and sign up for a free account. 
Be sure to verify your email to get all features activated!

When signing up, think a bit about which email address and user name you want to use--especially if you will be doing professional work on the platform.

Your email and user name will be recorded with every commit.
This helps ensure integrity and authenticity of the history.
Most people keep their email public. 
Alternatively, check GitHub's tips on how to [set up email privacy](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#about-commit-email-addresses){:target="_blank" rel="noopener"}. 
GitHub can provide a no-reply email address that can be found via your email settings on your profile.

## GitHub Web Interface

Log in to [GitHub](https://github.com){:target="_blank" rel="noopener"} and go to our [git-example repository](https://github.com/uidaholib/git-example){:target="_blank" rel="noopener"}.

The main page of a repository is the "Code" tab, which has a representation of the files, and displays the `README`.
Follow this demo to explore the basic features of the GitHub interface and start to understand the concept of a version controlled project:

1. Click the "Fork" button in the upper right--you now have your own personal version of the repo! [Forking](https://guides.github.com/activities/forking/){:target="_blank" rel="noopener"} is a GitHub concept that allows you to create a new copy of a repository, yet maintain a connection so that changes can be sent back to the original via "Pull Requests" (PR). It is a common workflow for collaborating on bigger projects.
2. On your `git-example` web page, click the "Commits" button below the description. The Commits page allows you to review and navigate the entire history of the repo.
3. Click back on the "Code" tab, then click on one of the file names. This will display the file's contents on the page. 
4. Click the edit pencil on the upper right side of the document to open the web editor. 
5. Make some changes or add some new text, then scroll down to the "Commit Changes" box. 
6. Enter a commit message and click the green button to save your edits to the history. You just made your first commit--you used Git! You added one snapshot to the history.
7. Click back to the "Code" tab and "Commits" to view your updated history.

> Note: GitHub allows [Markdown](https://guides.github.com/features/mastering-markdown/){:target="_blank" rel="noopener"} formating for READMEs and comments through out the site.

## Create a New Repository

The most common way to work with Git is to create or fork a repository on GitHub, then `clone` it to your local machine.
You will then work on the files locally, before using `push` to send your changes to the "remote" repository.
To create a new remote repository:

1. Click the plus sign on the upper right and select "New repository" from the drop down
2. Give it a nice name
3. Check "Initialize this repository with a README"
4. Click "Create repository"

> Every GitHub repo has handy project management features builtin. 
> Check the [Issues](https://guides.github.com/features/issues/){:target="_blank" rel="noopener"}, Projects, and Wiki tabs to start organizing your work!
> To delete a repository, click on the "Settings" tab and scroll down to the bottom to find the delete button.
