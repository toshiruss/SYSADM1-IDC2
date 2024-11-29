+----------------------------------+---------------------------------+---+
| ![](vertopal_                    |                                 |   |
| b6a4e146ccc648e78ed37a7e38c92b65 |                                 |   |
| /media/image1.png){width="2.4in" |                                 |   |
| height="0.5881944444444445in"}   |                                 |   |
|                                  |                                 |   |
| SCHOOL OF INFORMATION AND        |                                 |   |
| TECHNOLOGY                       |                                 |   |
+----------------------------------+---------------------------------+---+
| NAME: VICENTE, RUSSEL C.         | DATE PERFORMED: 21 NOVEMBER     |   |
|                                  | 2024                            |   |
+----------------------------------+---------------------------------+---+
| Section: IDC2                    | DATE SUBMITTED: 21 NOVEMBER     |   |
|                                  | 2024                            |   |
+----------------------------------+---------------------------------+---+

# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   Git is basically a version control system that will help to track
    the codes of the developer, if they will be doing any changes in
    their codes. It\'s important because it allows multiple developers
    can collaborate efficiently, keeps track of all changes and also to
    make the codes more organized.

2.  How does Git track changes in a project?

-   Git tracks changes by saving snapshots of files and directories at
    various points. Each change is stored as a \"commit,\" which
    contains the difference (or \"diff\") from the last snapshot.

3.  What is the difference between a local repository and a remote
    repository in Git?

-   Their main difference is that, the local repository can be accessed
    to the specific computer or workstation only, while the remote
    repository in Git can be accessed anytime and anywhere, you just
    need the same Git account to access the files or repositories.

4.  What are the basic Git commands?

-   **git clone**

-   **git commit**

-   **git init**

-   **git push**

-   **git pull**

-   **git status**

5.  How do you check the status of a Git repository?

-   By executing the **git status** command

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   The Branches allow developers to work on different features or fixes
    independently without affecting the main codebase. To create a new
    branch, use git branch \<branch-name\>, and to switch between
    branches, use git checkout \<branch-name\>.

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   GitHub and GitLab are web-based platforms for hosting Git
    repositories. GitLab Desktop is a graphical user interface for
    interacting with GitLab. They provide tools for collaboration, but
    **Git** itself is just the version control system that manages the
    code.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

-   You use the command git remote add origin \<repository-URL\> to link
    your local repository to a remote repository. Then, you can push and
    pull changes using git push and git pull.

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

To collaborate:

-   Fork the repository (on GitHub/GitLab).

-   Clone the fork to your local machine.

-   Create a new branch and work on your changes.

-   Commit and push your changes.

-   Create a pull request for others to review and merge your changes.

10. How do you resolve merge conflicts in Git?

-   If there is a conflict, Git will mark the file with conflict
    markers. You need to manually edit the file to resolve the conflict,
    then mark the conflict as resolved with git add \<file\> and commit
    the changes.

11. What is a pull request, and why is it used in GitHub?

-   A pull request is a way to propose changes from one branch to
    another. It allows collaborators to review, discuss, and approve the
    changes before merging them into the main codebase.

12. What are some best practices for writing commit messages?

-   Keep commit messages clear and concise. Start with a short summary
    of the change (50 characters max) followed by a more detailed
    explanation if necessary.

Reference

Atlassian. (n.d.). *Basic Git Commands \| Atlassian Git Tutorial*.
https://www.atlassian.com/git/glossary#commands
