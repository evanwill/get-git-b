---
title: What is Version Control?
nav: Why?
---

Do you have files like `final.txt`, `final_revised.txt`, `final_revised2.txt`, `final_revised2_revised.txt`? 

{% include figure.html img="phd101212s.gif" alt="final doc comic showing string of many filenames to denote versions" caption="'Piled Higher and Deeper' by Jorge Cham <a href='http://www.phdcomics.com/comics/archive.php?comicid=1531' target='_blank' rel='noopener'>www.phdcomics.com</a>" width="70%" %}

This is a "local version control system" which depends on your memory and organization to avoid errors and utter confusion.
Luckily, we have software that can handle this task, from the basic "track changes" to big centralized systems such as [SVN](https://subversion.apache.org/).

A <span class="term">version control system</span> tracks the history of *what* changes are made to a folder of files, *who* made them, and *why* to facilitate development and collaboration on a project. 

Version control **WILL** make your life better!

## Why Git Version Control?

<span class="term">Git</span> is a [free](https://en.wikipedia.org/wiki/Free_and_open-source_software){:target="_blank" rel="noopener"}, <span class="term">[distributed version control system](https://en.wikipedia.org/wiki/Distributed_version_control){:target="_blank" rel="noopener"}</span> originally developed for coordinating huge software development projects (specifically the [Linux kernel](https://www.kernel.org/){:target="_blank" rel="noopener"}). 
However, it is fast and flexible enough to be used on any scale project, from your personal notes to your research lab's code--and offers many benefits beyond "track changes".

Rather than storing a series of copies of a file with different filenames or revision numbers, Git captures a snapshot of your complete project each time you tell it to <span class="term">commit</span>.
Each commit records the creator, email, time, and changes made.
Git permanently stores this series of snapshots to create the project's history. 

Try to think of your changes recorded in each commit as separate from the document itself.
The current file that you see in your folder is made up of a specific set of those changes.
We can reconstruct other versions by jumping to earlier commits, while the complete history of your project is always safely stored in a hidden ".git" directory.

{% include figure.html img="versions.png" alt="depiction of file + new changes = versions of a document" caption="Adapted from: Software Carpentry, <a href='http://swcarpentry.github.io/git-novice/01-basics/' target='_blank' rel='noopener'>Version Control with Git</a>" width="100%" %}

Your project will be stored in a normal folder of files (on your computer or in the cloud), called a Git <span class="term">repository</span> (or "repo" for short).
Git is <span class="term">distributed</span> meaning that every copy of a repository contains the complete history. 
This is great for collaboration, fast performance, and offline usage.
Git can efficiently branch, diff, and automatically merge different sets of changes together, enabling people to work in parallel and sync their files.

{% include figure.html img="branch-merge.png" alt="arrows depict branch and merge of document versions" caption="Adapted from: Software Carpentry, <a href='http://swcarpentry.github.io/git-novice/01-basics/' target='_blank' rel='noopener'>Version Control with Git</a>" width="100%" %}

With Git you can make changes and experiment without fear!
When committing to a repository Git only adds data, it never deletes information. 
This makes almost everything undoable!

## What is GitHub?

<span class="term">[GitHub](https://github.com/){:target="_blank" rel="noopener"}</span> is a popular web service for hosting Git repositories--with benefits!
It provides a handy web interface for editing and collaborating on repos, as well as, built in project management features and static web hosting.
Accounts are free for public repositories--with additional features available on a subscription pricing model (you don't need a paid account!).

GitHub is where the distributed part of Git gets really cool. 
With a central repo hosted on GitHub, you can easily collaborate with anyone in the world, or yourself across multiple computers, and never get out of sync with your project!

**Just keep in mind that Git (version control system) and GitHub (web hosting platform) are two separate things!**

*Also note* that there are other version control systems ([Subversion](https://subversion.apache.org/){:target="_blank" rel="noopener"}, [mercurial](https://www.mercurial-scm.org/){:target="_blank" rel="noopener"}, etc) and repository hosts ([Bitbucket](https://bitbucket.org/){:target="_blank" rel="noopener"}, [Gitlab](https://about.gitlab.com/gitlab-com/){:target="_blank" rel="noopener"}, etc) out there...
However, Git and GitHub are by far the most popular.

## Plain Text Workflow

Git works best tracking [plain text](https://en.wikipedia.org/wiki/Plain_text) files.
All code (`.c`, `.py`, `.r`, `.html`, `.md`, etc) is plain text.
Most images, video, or [proprietary](https://www.gnu.org/proprietary/proprietary.en.html) document formats (such as Word's `.docx`) are not.

Git can tell exactly what changes in a plain text file, but can not understand the insides of a [binary file](https://en.wikipedia.org/wiki/Binary_file).
It will know when a binary file is changed, but it can not give you the exact differences.
Thus, Git is not optimal for managing Word docs, PDFs, or other binary files (and can lead to bloated repository sizes).

Instead of using proprietary formats, consider a plain text writing workflow using [Markdown](https://evanwill.github.io/_drafts/notes/markdown-minute.html) or [LaTeX](https://www.latex-project.org/about/)--it simplifies your life, makes writing easier and more [sustainable](https://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)!

## Approach in This Workshop

Get Git aims to present a pragmatic, hands on introduction to Git covering the basics you need to know to use version control on your own projects. 
There are lots of fancy and complex things Git can do--but the basics are truly all you need for 99.9% of collaborating and daily use (outside of giant software projects). 

To provide a solid understanding of these basics, Get Git introduces the workflow using the command line. 
Once you start regularly working with Git repos, you will likely use GUI helpers integrated into your text editor or stand alone apps such as GitHub Desktop. 
However, a good understanding of the fundamentals will help clarify how these tools and the file system work.
So, while learning on the command line might sound intimidating, it will pay off in the end!
