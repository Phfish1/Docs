# GitHub

GitHub is a website where you can save your code. Or colaborate with others by improving their code, over the internet.
You upload your code using the [Git command](https://git-scm.com/downloads)

# Git

Git functions like a save station. Saving your projects/code, while still being able to revert back and forth through those changes.

**Branches**
And with use of branches you can copy a "saved project" and continue on that copy while not changing the original project(Master Branch)

___

Blue being the original project("**master** branch") and the purple and green are extra branches branching out from the original master/project.
![[GitBranch.png]]

___

**Merging**
Now lets say another person adds something to your code. He does so by making a new branch basicly copying your project and adds a BetterCode.html file. Now he wants to add HIS code to YOUR original master branch. You accept and they **Merge**. Adding HIS file(s) to the Master branch

LighBlue being YOUR master branch and LightGreen branch being HIS contribution
![[GitMerge.webp]]


### Git Terms

**Reporitory**
- Your working Folder.

But also holds folder history, branches and all the GitHub goodies

**HEAD**
- Points out the last commit. in the working branch

Reverts the latest commit
```
$ git revert HEAD
```