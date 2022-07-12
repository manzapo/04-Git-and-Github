## Questions
Answer the following questions

1. What is the difference between `git reset` and `git revert`. When would you use one over the other? 
2. What is the difference between `git merge` and `git rebase`. When would you use one over the other? 
3. What is the difference between `git stash pop` and `git stash apply`. When would you use one over the other?

## Answers
1. - `git reset` : Reset current HEAD to the specified state. [Reference](https://git-scm.com/docs/git-reset)
   - `git revert`: Revert some existing commits. [Reference](https://git-scm.com/docs/git-revert)

2. - `git merge` : Join two or more development histories together. [Reference](https://git-scm.com/docs/git-merge)
   - `git rebase` : Reapply commits on top of another base tip. [Reference](https://git-scm.com/docs/git-rebase)

3. - `git stash pop` : Remove a single stashed state from the stash list and apply it on top of the current working tree state. [Reference](https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-pop--index-q--quietltstashgt)
   - `git stash apply` : Like `pop`, but do not remove the state from the stash list. Unlike `pop`, `<stash>` may be any commit. [Reference](https://git-scm.com/docs/git-stash#Documentation/git-stash.txt-apply--index-q--quietltstashgt)