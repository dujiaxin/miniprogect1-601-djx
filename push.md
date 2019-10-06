# push
After committing the changes from the staging area to the local repository using the git commit command, only the last step is to push the branch of the local repository to the corresponding branch on the remote server.

    git push <remote hostname><loacal branch name><remote branch name>

for example 

    git push origin master: refs/for/master

which pushes the local master branch to the remote host origin Corresponding to the master branch, origin is the remote host name.  The first master is the local branch name and the second master is the remote branch name.

    git push origin master
If the remote branch is omitted, the above indicates that the local branch is pushed to the remote branch with the tracking relationship (usually the same name). If the remote branch does not exist, it will be newly created.

    git push origin : refs/for/master

If the local branch name is omitted, it means that the specified remote branch is deleted, because this is equivalent to pushing an empty local branch to the remote branch, which is equivalent to git push origin --delete master
