See the remote repo of a local repo: 
```
git ls-remote --get-url origin
```
Set upstream: 
```
git remote add upstream <link>
```
Compare changes between local and remote
```
git diff <local branch> <remote>/<remote branch> (e.g. git diff main origin/main)
```
