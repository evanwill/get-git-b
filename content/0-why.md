---
title: What is Version Control?
nav: Why?
youtubeid: L_S-ofOpDmg
---

Do you have files like `final.txt`, `final_revised.txt`, `final_revised2.txt`, `final_revised2_revised.txt`? 

{% include figure.html img="phd101212s.gif" alt="final doc comic showing string of many filenames to denote versions" caption="'FINAL.doc' from 'Piled Higher and Deeper' by Jorge Cham <a href='http://www.phdcomics.com/comics/archive.php?comicid=1531' target='_blank' rel='noopener'>www.phdcomics.com</a>" width="70%" %}

{% include figure.html img="phd052810s.gif" alt="file explorer window shows long series of filenames with adjectives added on" caption="'A story told in file names' from 'Piled Higher and Deeper' by Jorge Cham <a href='http://phdcomics.com/comics/archive.php?comicid=1323' target='_blank' rel='noopener'>www.phdcomics.com</a>" width="70%" %}

This is a sort of "local version control system" which depends on your memory and organization to avoid errors and utter confusion.
Luckily, we have software that can handle this task, from the basic "track changes" to big centralized systems such as [SVN](https://subversion.apache.org/).

A <span class="term">version control system</span> records the history of *what* changes are made to a folder of files, *who* made them, and *why* to facilitate development and collaboration on a project. 
The version control system allows you to explore that history to better understand the project's development and the choices made along the way, and to debug issues or undo errors.

Version control **WILL** make your life better!

## What is Git?

<span class="term">Git</span> is a [free](https://en.wikipedia.org/wiki/Free_and_open-source_software){:target="_blank" rel="noopener"}, <span class="term">[distributed version control system](https://en.wikipedia.org/wiki/Distributed_version_control){:target="_blank" rel="noopener"}</span> originally developed for coordinating huge software development projects (specifically the [Linux kernel](https://www.kernel.org/){:target="_blank" rel="noopener"}). 
However, it is fast and flexible enough to be used on any scale project (be it your personal notes, your research lab's code, your enterprise software source code, or your detailed plans for an intergalaxic empire)--and offers many benefits beyond "track changes".

When using Git, your project will be stored in a normal folder of files (on your computer or in the cloud), called a Git <span class="term">repository</span> (or "repo" for short).
Git is <span class="term">distributed</span> meaning that every copy of a repository contains the complete history. 
This is great for collaboration, fast performance, and offline usage.

Rather than storing a series of copies of a file with different filenames or revision numbers in the repo, Git captures a snapshot of your complete project each time you tell it to <span class="term">commit</span>.
Each commit records the creator, email, time, and changes made, then stores it permanently in the history.

{% include figure.html img="versions.png" alt="depiction of file + new changes = versions of a document" caption="Adapted from: Software Carpentry, <a href='http://swcarpentry.github.io/git-novice/01-basics/' target='_blank' rel='noopener'>Version Control with Git</a>" width="100%" %}

Try to think of your changes recorded in each commit as separate from the document itself.
From Git's point of view, the current file that you see in your folder is made up of a specific set of those changes.
It can reconstruct other versions by jumping to earlier commits, while the complete history of your project is always safely stored in a hidden ".git" directory.

This allows Git to efficiently branch, compare, and merge different sets of changes together, enabling people to work in parallel and sync their files.

{% include figure.html img="branch-merge.png" alt="arrows depict branch and merge of document versions" caption="Adapted from: Software Carpentry, <a href='http://swcarpentry.github.io/git-novice/01-basics/' target='_blank' rel='noopener'>Version Control with Git</a>" width="100%" %}

When committing to a repository Git only adds data, it never deletes information. 
This makes almost everything undoable.
With Git you can make changes and experiment without fear!

{% capture plain-text %}
Git works best tracking [plain text](https://en.wikipedia.org/wiki/Plain_text) files.
All code (`.c`, `.py`, `.r`, `.html`, `.md`, etc) is plain text.
Most images, video, or [proprietary](https://www.gnu.org/proprietary/proprietary.en.html) document formats (such as Word's `.docx`) are not.
Some data formats (`.csv`, `.tsv`, `.json`, `.yml`, `.xml`, etc) are plain text, while most proprietary spreadsheet and database files are not (`.xlsx`, `.mdb`, etc).

Git can tell *exactly* what changes in a plain text file, but can not understand the insides of a [binary file](https://en.wikipedia.org/wiki/Binary_file).
It will know when a binary file is changed, but it can not give you the exact differences.
Thus, Git is not optimal for managing Word docs, PDFs, or other binary files (and can lead to bloated repository sizes).
You will generally want to actively edit and track those types of files in a different platform.

If you are creating documentation or content writing, consider using a plain text writing workflow using [Markdown](https://evanwill.github.io/_drafts/notes/markdown-minute.html) or [LaTeX](https://www.latex-project.org/about/) instead of a proprietary document format--it simplifies your life, makes writing easier and more [sustainable](https://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown)!
{% endcapture %}
{% include card.html text=plain-text header="Plain Text Workflow" %}

## Approach in This Workshop

*Get Git* aims to present a pragmatic, hands on introduction to Git covering the basics you need to know to use version control on your own projects. 
There are lots of fancy and complex things Git can do--but the basics are truly all you need for 99% of collaborating and daily use (outside of giant software projects). 

To provide a solid understanding of these basics, this workshop introduces the workflow using Git on the command line. 
Once you start regularly working with Git repos, you will likely use GUI helpers integrated into your text editor or stand alone apps such as GitHub Desktop. 
However, a good understanding of the fundamentals will help clarify how these tools and the file system work.
So, while learning on the command line might sound intimidating, it will pay off in the end!
