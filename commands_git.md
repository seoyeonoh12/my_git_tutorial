# Commands from Git

### I. Starting with Git
**!** NEVER intialize git project under the sub-folder of git project!


1. Initialize git project on your working directory (a folder for the project)

    `$ git init` returns
    
     ```
     Initialized empty Git repository in /Users/seooh/Desktop/Trainings/VIB_Git_Github2024/my_git_tutorial/.git/
     ```

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


###  II. Basic routine for commiting


That is how I save a snapshot/point in time

```
git add <name of the file>
git commit -m "meaningful msg"
```

### III. How to check the status of my files/directories in my git project

`$ git status` tells you
- Which branch you are in master/main or other branches
- Changes to be committed, changes not staged (developing area, working on it before), Untracked files (= completely new)

Check if they are uncommitted, unstaged or untracked

```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Dictionary_git.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        vib.png
```

`$ git restore`

- Discards changes in working directory e.g. if you regret about changes you have made, let the changes exit from the stagin area and discard changes

### IV. Commiting without -m
If you try `$ git commit` without -m, It might give an error.

Change editor to get it back to vi:

`$ git config --global --unset-all core.editor`

If you do `$ git commit` again, you will open the config file via vi editor
- In the opened file, you can add text for the title of the new commit


### V. At staging area: Add files that you want to commit together

- git all files `$ git add *`

- git all pdf files `$ git *.pdf`

- `$ git add <pattern>.*`

- `$ git add file1 file2` 


### VI. Exercises: Knowing my timeline
A. How can I travel within the timeline to check for differences in my versions? 
- by `$ git diff`, you can compare the differences between the current version and previous version (the last time you committed). 
    - `$ git diff <commit id1> <commit id2>` 
    - The order of the commits matters +/-
    - Show changes between different states	Compare working dir, staged, or commits	Line-by-line file changes
- Or, `$ git show` is similar to `$ git diff` but shows the differences with more details
    - `$ git show <commit id1> <commit id2>`, you will see a merged comparativer version printed

B. How can I see the history of my timeline? 
- by `$ git log` it shows history of commits from HEAD -> main/master (HEAD: the most updated version)
- or `$ git log --abbrev-commit` with abbreviated version of commit ID
- View commit history	Listing commits	Commit metadata (author, message, date)


In Summary:

- git log is for viewing commit history.
- git diff is for viewing file differences.
- git show is for inspecting a specific commit or object.

### VI. Linking the local repository to remote repository

1. Create a bridge and then check the status of the current Git
```
$ git remote add origin git@github.com:seoyeonoh12/my_git_tutorial.git
$ git status
```
Expected output:
```
On branch main
nothing to commit, working tree clean
```
2. `$ git push` : sending the local repos. to remote repos. 
If you "push" for the first time, it will give an error with the following message:
```
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

Then, run the command

 `$ git push --set-upstream origin main`
 
**!** A bridge works both ways: Always push first and then pull to synchronize local and remote repository


```
Enter passphrase for key '/Users/seooh/.ssh/id_ed25519': 
Everything up-to-date
```

3. `$ git pull` : fetch and download content from a remote repository and immediately update the local repository to match that content
`$ git pull`


**!** If you lost your local repository by accident, clone the remote repository to your local one by 
`git clone <SSH repo>`


### VII. Checking the user information

Run command `git config --global --list`

    Expected output:

    filter.lfs.smudge=git-lfs smudge -- %f
    filter.lfs.process=git-lfs filter-process
    filter.lfs.required=true
    filter.lfs.clean=git-lfs clean -- %f
    user.name=Seoyeon Oh
    user.email=Seoyeon.Oh@UGent.be
    core.editor=code --wait


**!** *Git does not store a separate copy of every file in every commit, but keeps track of changes made in each commit!*


### VIII. Running a parallel timeline - Branches
1. Create a branch outside Main/master

    `$ git branch <Branch name>` 

2. Check the list of branches

    `$ git branch -a`

3. Enter the branch you created 

    `$ git checkout <Branch name>`

    --list: shows only branches at local repository
    
    -a : shows all branches


4. Check which branch you are in now 

    `$ git status`

5. To return back to the main 
    `$ git checkout main`

**!** The files you created in your branch will not be shown in the Main.

### IX. Tagging
Creating a name to a certain versioned commit

```
$ git tag V1.0
$ git tag --list
V1.0
$ git push --tags
```
Then the head commit is tagged as V1.0.

! Always include --tags when you want to push with the tags you created.

