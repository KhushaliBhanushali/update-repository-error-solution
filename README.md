# update-repository-error-solution

Second Commit Step

1. git add .
2. git commit -m "second commit"
3. git push

When update repository(next commit) :- 

Error:-----

[rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/UserName/RepositoryName.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

solution:-----

First Do this ...

git fetch origin master
git merge  master

Then, do this ...

git fetch origin master:tmp
git rebase tmp
git push origin HEAD:master
git branch -D tmp

Now everything works well.
