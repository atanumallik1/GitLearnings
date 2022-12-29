
## Basic Commands

### Creating a new branch and pushing it remote
````
git checkout -b new_branch     // creates a local branch (as a copy of the current)
git push origin new_branch // push it to the remote server
````

### Restoring a file from an old commit into current branch
````
git checkout 8884788 -- /mtx-sidecar/package.json
````
