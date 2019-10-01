# Git Flow
## What is the Git Flow

Conventions about how to use Git: Not only code should have specification, but code management should also have normative process,so many engineers are using gitflow solution now.

## The benefit of Git Flow

* Parallel Development

One of the great things about GitFlow is that it makes parallel development very easy, by isolating new development from finished work. New development (such as features and non-emergency bug fixes) is done in feature branches, and is only merged back into main body of code when the developer(s) is happy that the code is ready for release.

* Collaboration

Feature branches also make it easier for two or more developers to collaborate on the same feature, because each feature branch is a sandbox where the only changes are the changes necessary to get the new feature working. That makes it very easy to see and follow what each collaborator is doing.

* Release Staging Area

As new development is completed, it gets merged back into the develop branch, which is a staging area for all completed features that haven’t yet been released. So when the next release is branched off of develop, it will automatically contain all of the new stuff that has been finished.

* Support For Emergency Fixes

GitFlow supports hotfix branches - branches made from a tagged release. You can use these to make an emergency change, safe in the knowledge that the hotfix will only contain your emergency fix. There’s no risk that you’ll accidentally merge in new development at the same time.

## How it Works

* Master branch: One basic rule to follow is that all commit on the master branch should be tag. And Develop branch clone based on master branch.

![master&develop](/images/master&develop.PNG)

* Feature branch: Feature branches are branched off of the develop branch, and finished features and fixes are merged back into the develop branch when they’re ready for release.

![develop&feature](/images/develop&feature.PNG)

* Release branch: When it is time to make a release, a release branch is created off of develop.

![develop&release&master](/images/develop&release&master.PNG)

The code in the release branch is deployed onto a suitable test environment, tested, and any problems are fixed directly in the release branch. This deploy -> test -> fix -> redeploy -> retest cycle continues until you’re happy that the release is good enough to release to customers.

* hotfix: The master branch tracks released code only. The only commits to master are merges from release branches and hotfix branches.

Hotfix branches are used to create emergency fixes:

![hotfix&maser&develop](/images/hotfix&maser&develop.PNG)

They are branched directly from a tagged release in the master branch, and when finished are merged back into both master and develop to make sure that the hotfix isn’t accidentally lost when the next regular release occurs.

## help you use Git Flow

Here's a graphical tool that supports Git Flow perfectly: [Link to Source Tree](https://www.sourcetreeapp.com/)

[Back to git tutorial](/git.md)

[Back to README](/README.md)





