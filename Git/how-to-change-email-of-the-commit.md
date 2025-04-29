```
git filter-repo --commit-callback '
if commit.author_email != b"currente@email.com":
commit.author_email = b"currente@email.com"
commit.committer_email = b"currente@email.com"
'
```

```
git remote add origin [repo 주소]
```

```
git push -u origin master --force
```
