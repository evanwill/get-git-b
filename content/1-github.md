---
title: Getting Started on GitHub
nav: GitHub
youtubeid: vgQw2umuq_Q
---

## What is GitHub?

<span class="term">[GitHub](https://github.com/){:target="_blank" rel="noopener"}</span> is a popular web service for hosting Git repositories--a place to store and sync your work in the cloud, with benefits!
It provides a handy web interface for editing and collaborating on repos, including built in project management features, user access controls, static web hosting, and other useful features.

GitHub is where the distributed part of Git gets really cool. 
With a central repo hosted on GitHub, you can easily collaborate with anyone in the world, or yourself across multiple computers, and never get out of sync with your project!

**Just keep in mind that Git (version control system) and GitHub (web hosting platform) are two separate things!**

{% capture account %}
Visit <https://github.com> and sign up for a **free** account. 
Free accounts have full functionality for public repositories (additional features are available on a subscription pricing model, but you don't need a paid account!).
Be sure to verify your email to get all features activated!

When signing up, carefully consider which email address and user name you want to use--especially if you will be doing professional work on the platform.

Your email and user name will be recorded with every commit.
This helps ensure integrity and authenticity of the history.
Most people keep their email public. 
Alternatively, check GitHub's tips on how to [set up email privacy](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#about-commit-email-addresses){:target="_blank" rel="noopener"}. 
GitHub can provide a no-reply email address that can be found via your email settings on your profile.
{% endcapture %}
{% include card.html text=account header="Create a GitHub Account" %}

## Using the GitHub Web Interface

In a typical Git workflow, you will start on GitHub by setting up a project repository. 
You (and collaborators) will then `clone` a copy of that repository to your local machine(s).
You will then work on the files locally, before `push`-ing your new changes back to the GitHub "remote" repository.

So, the best way to start learning about Git, is to create a new repository on GitHub.

### Create a New Repository

To create a new repository:

1. Visit [GitHub](https://github.com){:target="_blank" rel="noopener"} and ensure you are logged in. If you are a new user, your home page might look pretty empty, but eventually will be filled with a feed of recent activity.
2. Click the "+" plus sign icon on the upper right of the nav bar and select "New repository" from the drop down menu. 
3. Fill in the "Create a new repository" page:
    - "Owner" is you. Every repo is associated with an individual or organization.
    - "Repository name" is what you want to call this repo. It must be unique among the owner's repos. Naming conventions depend on your project type, but generally avoid spaces and weird characters.
    - "Public" / "Private". Choose "Public". Anyone can visit a public repository--but that's okay! The entire web is public and GitHub is mostly open source code, i.e. public repositories with code people can view and copy for free (following the [license](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/licensing-a-repository){:target="_blank" rel="noopener"} applied by the owner).
    - Check the "Add a README file" option in the "Initialize this repository with" section. This makes it easier to get started.
4. Finally, click the green "Create repository" button. 

Welcome to your new repository!

You are now (hopefully) looking at your new repository's home page, i.e. the "Code" tab on GitHub.
Keep in mind that the *repository* is really just a folder of files!
In this case we have a folder (the name of your repository) with a single file "README.md".

### Edit a File

You will notice that by default the contents of the "README.md" file are displayed on the home page of your repository. 
This is a convention used in many code projects--<span class="term">README</span> is a place to write the basics *about* your repository so users will understand what it contains, who made it, and any other information they should know. 
On GitHub READMEs are usually written in [Markdown](#markdown) (thus the `.md` extension). 

Let's edit the "README.md" file using the web editor:

1. Click on the filename "README.md". This will bring you to the file's page, which displays the rendered content.
2. Click on the pencil icon in the upper right corner of the file box to open the web editor.
3. In the "Edit file" box, use the editor to add some new content. This is a plain text editor something like Notepad or TextEdit.
4. Scroll down to the "Commit changes" box.
5. Enter a commit message describing what changes you just did. This is your message to the future to help understand the code.
6. Click the green "Commit changes" button.

Congrats, you just made your first commit--you used Git! 
You added one snapshot to the history of the repository.

### Add a File

Let's add another file to the repository:

1. Click on the "Code" tab to get back to the home of your repository.
2. Click "Add file" above the file list, and select "Create new file" from the dropdown.
3. In the "Name your file..." box, type in a filename (usually something without spaces and ending with a file extension), such as "example.md".
4. In the "Edit file" box, use the editor to add some new content to the file.
5. Scroll down to the "Commit changes" box.
6. Enter a commit message describing what changes you just did.
7. Click the green "Commit changes" button.

### View History

Now that we have a few commits, let's view the history of the repository:

1. Click on the "Code" tab to get back to the home of your repository.
2. Click on "commits" on the right hand side of the file listing area. This provides a sequential list of all commits made in the repository.
3. Click on a commit message or hash to view the commit details. This page provides a "git diff" detailing the exact changes made by the commit.

### Other Features

Every GitHub repo has handy project management features built in. 
Take a minute to explore the Issues, Projects (trello board-like), Wiki, Insights, and Settings tabs of your repository: 

- Issues can be used to track work, ideas, bugs, and task lists. Can be used in conjunction with Projects (trello board-like task lists) to manage project development.
- Wiki can be used to document your repository.
- Insights provides statics about your work and collaborators.
- Settings tab:
    - "Manage access" is used to add collaborators using their GitHub user name.
    - To delete a repository scroll down to the bottom to find the delete button.
- [github.dev Web Editor](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor) is a browser-based text editor that you can open to edit any repository by pressing `.` or changing the URL from "github.com" to "github.dev". It basically a light-weight version of [Visual Studio Code](https://code.visualstudio.com/) that can be used without installing anything. 

{% capture resources %}
### GitHub

- [GitHub Guides](https://guides.github.com/){:target="_blank" rel="noopener"} provide handy reference, see [Hello World](https://guides.github.com/activities/hello-world/){:target="_blank" rel="noopener"} for an introduction.
- [GitHub Learning Lab](https://lab.github.com/){:target="_blank" rel="noopener"} provides in depth interactive lessons.
- [GitHub Education](https://education.github.com/) provides resources and benefits for educational use of GitHub.

### GitHub Organizations

A [GitHub organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations) is a useful tool to collaborate with a group or to brand, organize, and manage a set of related repositories as a group.
Orgs can help ensure continuity in situations when members may move on from a project or lab.

GitHub organizations are NOT a separate account or profile, but are a group of users, i.e. you can’t log in as an Org. 
One or more persons can be the Owner with full admin control over the org including managing members.

To start an organization, click the plus sign icon on the upper right of the GitHub menu bar and select "Create organization". 
Once created, add members!

Now, when creating a new repository, all members can use the "owner" dropdown option to create the repository under the organization (instead of their own account).
Repositories owned by the Org will be accessible and managed by the Owner accounts. 
They stay with the Org even if the original creator leaves the Org.

### Markdown 

Markdown is a standard to simplify writing content for the web designed to be easy to read and write. 
GitHub Markdown Flavor can be used any where on GitHub to format your writing in comments, Issues, and `.md` files.
The basics are intuitive, much like formatting a plain text email.

- [Mastering Markdown GitHub Guide](https://guides.github.com/features/mastering-markdown/){:target="_blank" rel="noopener"}
- [GitHub Markdown documentation](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax){:target="_blank" rel="noopener"}

### Alternatives

*Please note* that there are other version control systems ([Subversion](https://subversion.apache.org/){:target="_blank" rel="noopener"}, [mercurial](https://www.mercurial-scm.org/){:target="_blank" rel="noopener"}, etc) and repository hosts ([Bitbucket](https://bitbucket.org/){:target="_blank" rel="noopener"}, [Gitlab](https://about.gitlab.com/gitlab-com/){:target="_blank" rel="noopener"}, etc) out there...
However, Git and GitHub are by far the most popular.
{% endcapture %}
{% include card.html text=resources header="Resources" %}
