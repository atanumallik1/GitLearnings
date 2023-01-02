# VSCode with Git

1. [Using Git with Visual Studio Code (Official Beginner Tutorial)](https://www.youtube.com/watch?v=i_23KUAEtUM&t=327s)
    - Creating Project in Local and Pushing to Github
    - Creating new branch  in Local and Pushing to Github
    - Cloning from Github and Setting up in Local 
    - Identifying Changes 
        - RED : Content Deleted
        - GREEN : Content Added
        - BLUE : Content changes
    - Copmare changes in Local file 
        - Git View --> Click on File
2. [Git: Commits in Visual Studio Code](https://www.youtube.com/watch?v=E6ADS2k8oNQ)
    - Following commands to be executed directly from Git Source Control Tab --> Buttons on teh files
    - Staging `git add -A -- /Users/I072405/Documents/git/GitExperiments/File1.md`
    - Unstage `git reset -q HEAD -- /Users/I072405/Documents/git/GitExperiments/File1.md `
    - Reverting a Commit Locally :
        - click on `...` --> `Commit`-->`Undo Last Commit` ; this will revert the changes
        - next you need to cleanup local workspace : 
            - unstage the file 
            - click on discard changes button 
    - `Stash`
        - You can `stash` the files / changes in a branch using `...`-->`stash`
        - You can also stash untracked files using another option 