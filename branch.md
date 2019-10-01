# Branch 

Use a branch to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

you can use branches to:

* Develop feature
* Fix bugs
* Safely experiment with new ideas

Once you're satisfied with the changes in your branch, you can open a pull request to merge your branch (the head branch) into another branch (the base branch).

# How to create the branch by Git Bash

view the local branch 

    git branch
![b1](/images/b1.PNG)    

view the remote branch

    git branch -r
![b2](/images/b2.PNG)    

view all branch

    git branch -a
![b3](/images/b3.PNG)    

creat the branch named dev 

    git branch dev
![b4](/images/b4.PNG) 

switch to the new branch

    git checkout dev
![b5](/images/b5.PNG)    
    
push the new branch to the github

    git push origin dev
![b6](/images/b6.PNG) 


