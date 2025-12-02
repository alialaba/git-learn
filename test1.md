### If you only ever rebase commits that have never left your own computer, you’ll be just fine. If you rebase commits that have been pushed, but that no one else has based commits from, you’ll also be fine. If you rebase commits that have already been pushed publicly, and people may have based work on those commits, then you may be in for some frustrating trouble, and the scorn of your teammates.
### If we’re collaborating with others and want to undo a commit we just made, we can instead use git revert!

- git revert HEAD
- git push origin main

### So now that we’ve learned about the various dangers of git push --force, you’re probably wondering why it exists and when to use it. A very common scenario in which developers use git push --force is updating pull requests.

#### So now that we’ve learned about the various dangers of git push --force, you’re probably wondering why it exists and when to use it. A very common scenario in which developers use git push --force is updating pull requests.

##### When attempting to rewrite history, always check the dangers of the particular command you’re using and follow these best practices for the commands we’ve covered:
* If working on a team project, make sure rewriting history is safe to do and others know you’re doing it.
* Ideally, stick to using these commands only on branches that you’re working with by yourself.
* Using the -f flag to force something should scare you, and you better have a really good reason for using it.
* Don’t push after every single commit, changing published history should be avoided when possible.
* Regarding the specific commands we’ve covered: 
  - For git commit --amend never amend commits that have been pushed to remote repositories.
  - For git rebase never rebase a repository that others may work off of.
  - For git reset never reset commits that have been pushed to remote repositories.
  - For git push --force only use it when appropriate, use it with caution, and preferably default to using git push --force-with-lease.

## Resources
- https://think-like-a-git.net/sections/about-this-site.html
- https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/about-merge-conflicts 
- https://www.youtube.com/watch?v=iIaM7j3tMuk (why use revert instead reset)
- https://cbea.ms/git-commit (commit message)
