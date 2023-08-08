# Git Commands

Git allows you to basically maintain code history and go back to previous histories. <br><br>
## Setup
`git init`: Initialises an empty git repository to the path to maintain its history. Creates a hidden .git folder in the working directory. <br>
`git status`: To find the files in the directory. These can be tracked or untracked. <br>
`git add filename.txt`: Track all the changes in the folder from the last commit. It "stages" the changes. <br>
`git restore --staged filename.txt`: To untrack or "unstage" a file. Basically reverses the add statement. <br>
`git commit -m "Message to be filled here"`: To commit all changes to the branch. Removes the project from the "add" status to the "modified" status. <br>  
`git log` : To track all commits made. Each commit will have a hash code. These commits are made in a stack fashion. If you want to undo any changes, you have to restore the directory to the version of one commit. All commits made after that particular commit will be lost and undone. <br>
`git reset --hard commit_hash_id` : Goes back to the particular commmit and deletes any changes made after that. <br><br><br>
## Branches
`git remote add origin githubrepositorylink` : Connects your local directory to github. Any changes committed can be made to reflect on Github. <br>
`git remote -v` : To check which repository is the branch head currently on. <br>
`git push origin branchname` : Push your changes onto the specified branch. <br>
`git branch branch-name` : Creates a new branch with specified name. <br>
`git checkout branch-name` : To move the head to a different branch.<br>
`git merge branch-name` : Merges contents of new branch into the main branch. <br><br><br>
## Working with projects
We dont always have access to major projects. To work on any feature or piece of code in an existing repository, we can **Fork** it onto a repository in our account and work on the changes. Then usually the finished code does not get merged with the main branch. It needs to be added to another branch and then we merge the main and the new branch.<br><br>
`git clone url-of-the-repository` : Copies the whole URL content into your working directory. <br>
`git remote add upstream repository_url` : Adds the upstream URL - The repository from where the project files are downloaded. <br><br>
## Pull requests
Used to get your changes published <br>
You can have only 1 pull request for 1 branch <br>
`git push origin branchname` : Used to push all changes onto a branch.<br>
One issue that arises is when the upstream repository is updated, but forked repository is not updated.  To update the forked repository, we can use the code : 
`git checkout main    
git fetch --all --prune     
git reset --hard upstream/main    
git push origin main`<br>





