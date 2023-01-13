## Task 1
### Set your user name and email address, which will be associated with your commits

- To set username in git, use command `git config --global user.name "RohitChavan"` You can check whether the username is set correctly with, `git config user.name` It will display the username you have set
- To set email in git, use command `git config --global user.email "rohitchavan@gmail.com"` You can check whether the email is set correctly with, `git config user.email` It will display the username you have set

## Task 2
- To create new repository, follow the steps mentioned in tasks of day08. { [Link to file](https://github.com/rohit-chavan-2151/90DaysOfDevOps/blob/master/2023/day08/day08-tasks-rohitChavan.md) }
- Connect your local repository to remote repo on Github with `git remote add origin <repo-link>`
- To create a new file in Devops/Git/Day-02.txt :- 
    +  First create folder inside Devops repo with `mkdir Git` and then `cd Git`
    +  Create a file Day-02.txt with either `touch Day-02.txt` or `vim Day-02.txt`. Add some content to it.
    +  Add your commits with `git add .` and then commit those changes with `git commit -m "Add Day-02.txt file and create content"`
    +  Now push your changes to the remote repo on Github with `git push origin main`
