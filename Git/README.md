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

Delete a branch both locally and remotely [[*]](http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely)
```sh
git push origin --delete <branch_name> # OR
git push origin :<branch_name>
```


Generate ssh key [[*]](https://help.github.com/articles/generating-ssh-keys/)
```sh
ssh-keygen -t rsa -C "your_email@example.com"
```

Clean untracked files and directories
```sh
git clean -df
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
