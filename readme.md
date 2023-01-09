# Basic Commands

## Creating a new branch and pushing it remote
````
git checkout -b new_branch     // creates a local branch (as a copy of the current)
git push origin new_branch // push it to the remote server
````

## Restoring a file from an old commit into current branch
````
git checkout 8884788 -- /mtx-sidecar/package.json
````


## Step 1. Clone your repository to your local system
````Shell
$ git clone

https://emmap1@bitbucket.org/emmap1/bitbucketstationlocations.git 

Cloning into 'bitbucketspacestation'...
fatal: could not read
Password for 'https://emmap1@bitbucket.org': No such file or directory
````

If you get this error you need to do something like this 

````Shell
  $ git config --global core.askpass
````

## Step 2. Add a file to your local repository  
- Checking the status
    ````Shell
    $ git status 
    ````

    The file is `untracked`, meaning that Git sees a file not part of a previous commit. The status output also shows you the next step: adding the file.


- Tell Git to track your new locations.txt 
    ````Shell
    $ git add locations.txt
    ````
    The `git add` command moves changes from the working directory to the Git staging area. The staging area is where you prepare a snapshot of a set of changes before committing them to the official history.

    ![Image](/Images/1/1.svg)

- Check the status of the file.
    ````Shell
    $ git status 
    ````
- Commit the changes
    ````Shell
    $ git commit -m 'Initial commit' 
    [main (root-commit) fedc3d3] Initial commit
      1 file changed, 1 insertion(+)
      create mode 100644 locations.txt
    ````
    The `git commit` takes the staged snapshot and commits it to the project history. Combined with `git add`, this process defines the basic workflow for all Git users.

    ![Image](/Images/1/2.svg)


## Step 3. Pushing to Remote Repo

This command specifies that you are pushing to the `bitbucket2` branch (the branch on GitHub) on origin (the GitHub server). 
````
git push origin bitbucket2  
````

Another Syntax:

````
git push origin bitbucket:bitbucket
````


## Step 4 : Pullin from Remote Repo

````
git pull // Only pulls the current Branch
git pull --all
````


## Merge your branch Locally
- We are in branch `main` and we want to merge the content from branch `bitbucket` ; after this the local `main` branch will be updated . We need to push it to remote via a PR
````
git merge bitbucket    // merges the content of branch bitbucket into main
````


## Merge your branch Remotely
Raise PR
## Delete a Branch

Delete a Remote branch 
````
git push -d origin <remote branch name> 

```` 

Delete a Local branch 
````
git branch -d  <local branch name> 
git branch -D  <local branch name>   // Force Delete
````


## Push your code remotely
You need to raise a PR in real life apps. But in small application we can use command `merge`
````
$ git push origin main
````
![Image](/Images/1/3.svg)


## Git Difference 

Find difference between Working Area and Index/Staging area
````
git diff
````
Find difference between  Index/Staging area and Local Repository ( which holds committed data)
````
git diff  --cached
````

Find difference between  branches
````
git diff master feature_branch
````

## Reference 
- https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud#create-the-repository