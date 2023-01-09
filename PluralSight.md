## 4 Major Areas

![image](https://user-images.githubusercontent.com/8110582/210778851-ecbac434-4f4e-4b02-8ea2-93541ae9c0af.png)

- Working Area 
  - changes are in  our local directory , git is not tracking the changes 
- Index/Stage 
  - files added to index are tracked by Git
- Repository
  - added into git commit history 
- Stash
  - temporary area to keep some data / change ; not commmitted in git


However `stash ` is not so important ; so we consider 3 areas


![image](https://user-images.githubusercontent.com/8110582/210806468-c9d93a7d-d3f7-4b3a-b3a1-bf5f9943424e.png)

- command git `diff`
  - git diff
  - git diff --cached
  - git diff branch1 branch2

![image](https://user-images.githubusercontent.com/8110582/210807060-1f8261a2-4234-41e2-8b3d-1e758a58462a.png)
![image](https://user-images.githubusercontent.com/8110582/210807196-cbd92315-4566-4c25-9ce0-cf0da48f65fb.png)


### Left To Right 

Working Area `---------->` Stage / Index `--------------------->` Repository
            `git add`                      `git commit -m`

### Right To Left
Working Area `<----------` Stage / Index `<---------------------` Repository
`git checkout branchname`



### Remove command `rm`

Removes the file from working area and index/stage
````
git rm <Fiename>
````
Removes the file from   index/stage and leaves it in working area
````
git rm <Fiename> --cached
````


### rename command `mv`

Rename a file
````
git mv <Fiename1> <FileNewName>
````


## 4 Major Areas : Advanced Tools

Stash is a temporary area where we can temporarily store the changes
### Stash 

````
git stash 
git stash  --include-untracked
git stash  list

git stash pop // kick out the last stash
git stash apply // apply the stash 
````