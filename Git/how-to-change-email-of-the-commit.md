```
git filter-repo --commit-callback '
if commit.author_email != b"[currente@email.com]":
commit.author_email = b"[currente@email.com]"
commit.committer_email = b"[currente@email.com]"
'
```

```
git remote add origin [repo address]
```

```
git push -u origin [branch name] --force
```
