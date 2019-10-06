# pull
Git pull is used to pull and consolidate code from a repository or local branch

# How to use it 

    git pull <remote host> <remote branch>:<local branch>

For example,To retrieve the next branch of the origin host and merge it with the local master branch, write the following

    git pull origin next:master

If the remote branch (next) wants to merge with the current branch, the following colon can be omitted.The above command can be abbreviated as:

    git pull origin next
