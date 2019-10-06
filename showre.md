# remote remove and show

* remote remove

Delete the added remote address

before we delete, we can See which remote addresses have been added locally

    git remote -v

![rev](/images/rev.PNG)

Then we can delete by use

    git remote remove  git@github.com:dujiaxin/miniprogect1-601-djx.git

* remote show

View the remote repository, as well as the relationship with the local repository. This command lists which remote branches you will automatically push to when you perform a git push on a particular branch.It also lists which remote branches are not local to you, which remote branches have been removed from the server, and which branches merge automatically when you perform git pull.

    git remote show origin

![show](/images/show.PNG)
