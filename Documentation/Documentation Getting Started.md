# Getting Started with Git/GitHub and Markdown

This document is to help familiarize your with Git and Markdown: two major technologies related to this project.

## Git/GitHub

Git is a source code management system developed by Linus Torvalds (creator of Linux). It offers functionality like version control and branching.

GitHub is one of the most popular instances of Git. It hosts a majority of the world's open source software.

### Glossary

- Repository - a collection of source code, assets, and other files for a specific project or purpose. For example, this repository contains documents related to the documentation project of the FANUC Robot project.

- Clone - the process of making a copy of a repository.

- Branch - a snapshot of the repository at a specific point in time, which can be modified and merged into other branches. For example, when a repository is created, a default branch (main, master, primary, etc.) is made. From there, other branches can be established. In this project, "draft" is a branch of "main". <br /> "draft-\[name\]" are branches of "draft".

- Commit - the process of pushing changes from your local copy of a branch to the remote copy of a branch (i.e. the copy of the branch in GitHub.)

- Merging - taking changes from a branch and copying it into a parent branch. For instance, changes made to a "draft-\[name\]" branch can be copied into the "draft" branch. Changes in the "draft" branch can be copied into the "main" branch.

- Pull Request - a formal process for requesting changes to be merged into a branch. For instance, in order to merge changes in a "draft-\[name\]" branch into the "draft" branch, a pull request must be made.

### How to use

A good example of how to use Git and GitHub is by trying to retrieve this repository, and your specific branch!

1. Create a [GitHub account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)
2. Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [GitHub Desktop](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/installing-and-authenticating-to-github-desktop/setting-up-github-desktop) on your machine.
3. [Clone](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop) [this repository](https://github.com/wkuxrlab/fanucrobot-docs) using GitHub Desktop.
4. [Change current branch](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/managing-branches) in GitHub Desktop to "draft-\[Your Name\]".
5. [Pull latest changes](#how-to-use) from the "draft" branch.
6. Begin making changes!

### GitHub Cheat Sheet

[This video](https://www.youtube.com/watch?v=HkdAHXoRtos) provides a really good explanation on how to use Git and GitHub. 

A syntax guide/cheat sheet can be found [here](https://education.github.com/git-cheat-sheet-education.pdf).

## Markdown

Markdown is a markup (ironic) language that provides a simple means of formatting and presenting documents. For our purposes, we can create and modify Markdown documents (indicated with a .md file extension) which can be used in modern documentation websites (such as [Docusaurus](https://docusaurus.io/))

### Markdown Cheat Sheet

[This video](https://www.youtube.com/watch?v=HUBNt18RFbo) provides a really good explanation on how to use Markdown.

A syntaxguide/cheat sheet can be found [here](https://www.markdownguide.org/cheat-sheet/).