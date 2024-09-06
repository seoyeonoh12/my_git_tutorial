# Github tutorial 
## Dictionary - Git & Github 2024

### I. What is Git and GitHub?

- Git, as a version control system, creates a timeline with multiple versions of a project. 1 Git = 1 Project

- Github allows to share changes with others. Backup of all time lines in a single place. 

### II. Use:
- Tracking code changes
- Tracking who made changes
- Coding collaboration

### III. What does Git do?

- Manage projects with Repositories
- Clone a project to work on a local copy
- Control and track changes with Staging and Committing
- Branch and Merge to allow for work on different parts and versions of a project
- Pull the latest version of the project to a local copy
- Push local updates to the main project

### IV. 4 Conceptual areas of Git

1. Developing Area:

    Where do you develop a project? The folder where you initialize git and where the project is developed.

2. Staging Area:
    Location used to prepare new snapshots to the timeline before commiting. 
    Q. How often should we use git commit? Why Staging Area is important?
    -   It goes differently by project and person
    -   If you commit too often, you will end up too many updates (too redundant) that make it difficult to track back important changes you've made.

3. Local Repository:
    The place where you store the snapshots of your timeline. 
    Where you save snapshots. Check by `ls -la`
    `git add` 

4. Remote Repository:






### V. Working with Git

1. Initialize git project on your working directory (a folder for the project)

    `$ git init`
    
    returns
    
     ```
     Initialized empty Git repository in /Users/seooh/Desktop/Trainings/VIB_Git_Github2024/my_git_tutorial/.git/
     ```


**!** NEVER intialize git project under the sub-folder of git project!

2. Check the respository 
`$ ls -a` shows all the hidden files

    

3. Take a snapshot of my work (Commit)

    `$ git commit -m "meaningful message"`

    Explain the purpose to keep the change in the timeline
    
    **! What is meaningful?**
    - Why was it changed
    - How this addresses the issue
    - Effects due to the change
    - Limitations of the change


### VI. Checking the user information

Run command `git config --global --list`

    Expected output:

    ```
    filter.lfs.smudge=git-lfs smudge -- %f
    filter.lfs.process=git-lfs filter-process
    filter.lfs.required=true
    filter.lfs.clean=git-lfs clean -- %f
    user.name=Seoyeon Oh
    user.email=Seoyeon.Oh@UGent.be
    core.editor=code --wait
    ```

**!** *Git does not store a separate copy of every file in every commit, but keeps track of changes made in each commit!*


### VII. Push and Pull
**!** A bridge works both ways: Always push first and then pull to synchronize local and remote repository

### VIII. Running a parallel timeline: Branches
1. Create a branch outside Main/master

    `$ git branch <Branch name>` 

2. Check the list of branches

    `$git branch -a`

3. Enter the branch you created 

    `$git checkout <Branch name>`

4. Check which branch you are in now 

    `$ git status`

5. To return back to the main 
    `$ git checkout main`

**!** The files you created in your branch will not be shown in the Main.


$ git branch
--list: shows only branches at local repository
-a : shows all branches


### Summary
1. Initialize Git on a folder, making it a Repository
2. Git creates a hidden folder to keep track of changes in that folder
3. When a file is changed, added or deleted, it is considered modified
4. You select the modified files you want to Stage
5. The Staged files are committed, which prompts Git to store a permanent snapshot of the files
    - Git allows you to see the full history of every commit.
7. You can revert back to any previous commit.
8. Link a bridge between local repository and remote repository
    - Give the same names (advised)



### Some other tips to visualize a markdown file
#### Press Command+Shift+V will show the preview
**bold**
*italic*
Code `location $ ls`
```

Several lines of codes

```


