# 커밋 이메일 변경하기

## 1. git filter-repo  설치
https://github.com/newren/git-filter-repo

## 2. git filter-repo 명령어 실행
```
git filter-repo --commit-callback '
if commit.author_email != b"[currente@email.com]":
commit.author_email = b"[currente@email.com]"
commit.committer_email = b"[currente@email.com]"
'
```

## 3. git repo 연결
```
git remote add origin [repo address]
```

## 4. git 강제 push
```
git push -u origin [branch name] --force
```
