Git
---
Display version
```sh
git --version
```

Test authentication to github:
```sh
ssh -T git@github.com
```

Display line numbers when greping:
```sh
git config --global grep.lineNumber true
```

Change editor:
```sh
git config --global core.editor vim
```

Checkout branch [[*]](http://stackoverflow.com/questions/1783405/checkout-remote-git-branch)
```sh
git fetch
git checkout branch_name
```
If multiple remotes
```sh
checkout -b branch_name remote-name/branch_name
```

Delete a branch locally
```sh
git branch -d <branch_name>
git branch -D <branch_name> # Force delete un-merged branches
```

Delete a branch remotely [[*]](http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely)
```sh
git push origin --delete <branch_name> # OR
git push origin :<branch_name>
```

Update remote branches list [[*]](https://junaidpven.wordpress.com/2011/12/29/how-to-update-remote-branch-list-on-local-machine/)
```sh
git remote update origin --prune
```

Generate ssh key [[*]](https://help.github.com/articles/generating-ssh-keys/)
```sh
ssh-keygen -t rsa -C "your_email@example.com"
```

Clean untracked files and directories
```sh
git clean -df
```

#### Stashes
List all stashes
```sh
git stash list
```

Save a stash with a name [[*]](http://stackoverflow.com/questions/11269256/how-to-name-a-stash-in-git)
```sh
git stash save "<stash_name>"
```

See what's in a stash without applying [[*]](http://stackoverflow.com/questions/10725729/git-see-whats-in-a-stash-without-applying-stash)
```sh
git stash show -p stash@{0}
```
Drop the last created stash
```sh
git stash drop
```
Drop a specific stash
```sh
git stash stash@{0}
```

Use multiple github accounts, change file ~/.ssh/config [[*]](http://code.tutsplus.com/tutorials/quick-tip-how-to-work-with-github-and-multiple-accounts--net-22574)
```sh
Host github-work
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_work
```
Then clone repository with
```sh
git clone git@github-work:account/repo-name.git
# instead of
git clone git@github.com:account/repo-name.git
```


References
---
- [Authentication](https://developer.github.com/guides/using-ssh-agent-forwarding/#testing-ssh-agent-forwarding)
