## Exercises to perform :- 

1. Create a new repository on GitHub and clone it to your local machine
- To create a new repository, click on '+' icon, and go to New Repository
- Give your repository a name. For example, `learn-devops` in front of username. Give it a description about the repository
- Make the repository public or private as per your need
- If needed, click on README.md file to provide details of your repo in a markdown file
- Now click 'Create Repository'. Your repo is now been created.
- To clone the repo in your local machine, use command ``git clone <repository-link>``

2. Make some changes to a file in the repository and commit them to the repository using Git
- Add a file to the local git repository. Here, add a simple 'new_file.txt' and some content to it
-  Save the file. Now add the file from working area to staging area with `git add new_file.txt`
-  Now commit the file with command, `git commit -m "add new file to project"`

3. Push the changes back to the repository on GitHub
-  To push the files to the remote repository on Github, use command `git push origin main`
> If it asks for an upstream branch not being set, you need to specify it. Use command `git push --set-upstream origin main` This will set the main branch as upstream branch
