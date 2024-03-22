The README file: Read this file before continuing.

## GIT

Git is a distributed version control system where all developers have the code pipeline mirrored on their ends.

Details on Git and Git functions can be found here: https://git-scm.com/doc

It can be downloaded from here: https://git-scm.com/downloads
 

### Branches

The 'dev' or 'master' branch is by default the stable branch. The content of this branch has been through thorough scrutiny by members of the project. 

### New Branch

Data Scientists are expected to create their own branches (playgrounds, bugs, features) for their assigned tasks. Please initiate a branch using the following nomenclature:

<Initials_of_your_Name>_playground

It may also be that multiple scientists are working on the same feature. The suggested nomenclature in that case is 

feature/<feature_name>

Create new branch and push it to origin

```
git checkout dev
git checkout -b <branch>
git push -u origin <branch>
```

### Merge Requests

Once the assignment is finished and you're ready to merge your work into dev, you will need to make merge request, where your work will be reviewed by another member. This is usually done to ensure the sanity of the proposed logic or strategy and that all the required files have been included for the code to work.

Merge requests can be made both via command line and GUI. 

### Useful command-line git commands 

##### Branch Exploring and Switching

git branch -a (view the existing remote and local branches)
git checkout branch-name (switch to another branch)

##### Add a File

```
git pull 
git add new_file.ipynb 
git commit -am "adding a new file" 
git push 
```

It's not considered good practice to run the following:

```
git add *
```

Be specific as to what files need to be added. Do not add:

- the output of any program
- figures generated by any program
- data

##### Copy file from one branch into another

```
git checkout branch1
git checkout branch2 path_to_file_within_repo/file_name.ipynb
git commit -am "added file_name"
git push
```

##### Change the last git message

git commit --amend -m "New commit message."

##### Sketch a Tree

git log --all --decorate --oneline --graph

##### Delete a branch locally and remotely

```
(locally)
git branch -d branch_to_be_deleted
(remotely)
git push origin --delete rupal_aic
```

##### What to do when things go wrong?

https://m.xkcd.com/1597/

Go to somebody who's good at git.
