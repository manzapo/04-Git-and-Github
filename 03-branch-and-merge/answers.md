# Questions

[04-Git-and-Github/03-branch-and-merge/README.md](https://github.com/manzapo/04-Git-and-Github/blob/main/03-branch-and-merge/README.md)

# Answers

1. Membuang perubahan yang tidak dimasukkan kedalam staging area
2. - `-d` Normally, when no <path> is specified, git clean will not recurse into untracked directories to avoid removing too much. Specify -d to have it recurse into such directories as well. If any paths are specified, -d is irrelevant; all untracked files matching the specified paths (with exceptions for nested git directories mentioned under `--force`) will be removed.
   - `-f` If the Git configuration variable clean.requireForce is not set to false, git clean will refuse to delete files or directories unless given -f or -i. Git will refuse to modify untracked nested git repositories (directories with a .git subdirectory) unless a second -f is given.
3. `git branch <branchname>`
4. - Fast-forward Merge

   Often the current branch head is an ancestor of the named commit. This is the most common case especially when invoked from git pull: you are tracking an upstream repository, you have committed no local changes, and now you want to update to a newer upstream revision. In this case, a new commit is not needed to store the combined history; instead, the `HEAD` (along with the index) is updated to point at the named commit, without creating an extra merge commit.

   This behavior can be suppressed with the `--no-ff` option.

   - recursive

   This can only resolve two heads using a 3-way merge algorithm. When there is more than one common ancestor that can be used for 3-way merge, it creates a merged tree of the common ancestors and uses that as the reference tree for the 3-way merge. This has been reported to result in fewer merge conflicts without causing mismerges by tests done on actual merge commits taken from Linux 2.6 kernel development history. Additionally this can detect and handle merges involving renames. It does not make use of detected copies. This was the default strategy for resolving two heads from Git v0.99.9k until v2.33.0.
5. `git switch <branchname>`
6. How do you remove modified or deleted files from the working directory?
7. `git branch -d <branchname>`
8. Show changes between commits, commit and working tree, etc
9. `git restore --staged <file>`
10. - Decide not to merge. The only clean-ups you need are to reset the index file to the `HEAD` commit to reverse 2. and to clean up working tree changes made by 2. and 3.; `git merge --abort` can be used for this.
    - Resolve the conflicts. Git will mark the conflicts in the working tree. Edit the files into shape and `git add` them to the index. Use `git commit` or `git merge --continue` to seal the deal. The latter command checks whether there is a (interrupted) merge in progress before calling `git commit`.