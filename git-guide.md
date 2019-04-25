## Because git is as wonderful as it is weird


```
git fetch origin
git checkout -b {name} origin/{name}
```

```
git fetch all
git checkout master
git reset --hard origin/master
```

`git clean -d -f` ("-d" : directories, as well as files; "-f" : force)

`git remote prune origin`

`git branch` (-> local)

`git branch -a` (-> all)

`git branch -r` (-> remote)

### Squash / Rebase


`git rebase -i HEAD~n` SQUASH (HEAD : current branch; n : number of commits to squash)

`git rebase -i {branch}` SQUASH

`git pull --rebase origin {main branch}` REBASE

`git push origin --force {branch}`

---

`git status`
- fix conflics
- if conflicts in yarn.lock - delete file and run `yarn`

`git add {filename}`
- add **one by one**, NOT `add .`

`git rebase --continue`