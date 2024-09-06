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

4. Remote Repository: github repository



### V. Summary
1. Initialize Git on a folder, making it a Repository
2. Git creates a hidden folder to keep track of changes in that folder
3. When a file is changed, added or deleted, it is considered modified
4. You select the modified files you want to Stage
5. The Staged files are committed, which prompts Git to store a permanent snapshot of the files
    - Git allows you to see the full history of every commit.
7. You can revert back to any previous commit.
8. Link a bridge between local repository and remote repository
    - Give the same names (advised)
9. You can create tag to a certain commit e.g. V1.0
10. You can work on the same project with your collaborators. To avoid conflicts, it is better to make use of branches.
11. You can merge branches to the master/main branch.



### VI. Some other tips to visualize a markdown file
#### Press Command+Shift+V will show the preview
**bold**
*italic*
Code `location $ ls`
```

Several lines of codes

```
