---
title: Using Branches and Forks
nav: Branches
---


## git branch

[Branching](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell){:target="_blank" rel="noopener"} is a Git fundamental that allows you to test out ideas in parallel to your main repository without disrupting the master copy. 
Using branches strategically figures into many collaboration workflows, such as [Github flow](https://guides.github.com/introduction/flow/){:target="_blank" rel="noopener"}.
Often, the master branch is considered functioning, production ready code. 
Additional branches are created to develop and test new features.
When the new features are ready, the development branch can be merged into the master.

```
git branch test-branch 
git branch --list
git checkout test-branch
git checkout -b another-branch
git branch -D test-branch
```

## git merge 

Once you have branches, you will want to `merge` them together.
Luckily, Git has tools to automate merging. 
If it encounters a line that can not be automatically merged, Git will mark the file for you to manually fix before proceeding.
For details, check the Git Book [Basic Branching and Merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging){:target="_blank" rel="noopener"}.

```
git checkout -b new-branch
echo "new stuff" > newfile.txt
git add newfile.txt
git commit -m "new stuff"

git checkout master
git merge new-branch
git branch -D new-branch
```


## GitHub Fork and PR

[Forking](https://help.github.com/articles/fork-a-repo/){:target="_blank" rel="noopener"} a repo on GitHub, editing, then opening a Pull Request (PR) is a common workflow for collaborating on bigger projects.
Understanding how to fork and create a PR will allow you to contribute to open source or manage a centralized project for your team.
Check the [Forking Projects](https://guides.github.com/activities/forking/){:target="_blank" rel="noopener"} guide for an demo example, or the [BitBucket PR tutorial](https://www.atlassian.com/git/tutorials/making-a-pull-request){:target="_blank" rel="noopener"}.

Many projects will have a contributing guide, details are often listed in a file named `CONTRIBUTING`, to help you understand how they handle PRs or Issues.
For more information, check the [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/){:target="_blank" rel="noopener"} guide.

For an overview of workflows that might help your team collaborate, check BitBucket's [Git Workflow Tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows){:target="_blank" rel="noopener"}.

-----------

## Collaborate with Git activity

- create a new repository 
- clone to your local machine 

# Branch

- create a new branch
- make changes on the branch
- merge with master 
- create a new branch
- push branch to remote 
- switch branches 

# Conflicts 

Auto merge: 

- create a commit on web interface 
- create a commit locally on a different file
- try to push
- pull, auto merge
- push

Conflicts: 

- create a commit on web interface 
- create a commit locally in same place 
- try to push
- pull, enter merging state
- fix conflicts
- commit
- push

# Collaborating 

Collaborators and Branches: 

- add partner as collaborator
- accept partner's invite (check [notifications](https://github.com/notifications)) 
- clone partner's repo 
- make change locally and push
- create a new branch locally and push
- create a pull request 
- accept partner's PR

Forks: 

- fork partner's repo
- make changes in fork
- create pull request from fork
- accept partner's PR
