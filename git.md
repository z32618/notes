# git commands

#### unstage a file
```text
git restore --staged file
```


#### deleting a file
```text
rm file
git add file
git commit -m "deleted file"
git push

(or)

git rm file
git commit -m "deleted file with git rm file"
git push
```


#### show configuration settings: 
```text
git config --list
```


#### fork and branch
```text
fork a repository
add collaborators
git clone the repository via SHH
git switch -c  temporary_branch_ilja
touch file
git add file
git file -m “made some changes”
git push --set-upstream origin  temporary_branch_ilja
open pull request on GitHub, add reviewer, wait for approval
got to Pull Requests on GitHub, merge, delete the temporary branch
git switch main
git branch
git pull

git switch  temporary_branch_ilja
git merge main
 (or)
git swich main
git branch --delete  temporary_branch_ilja
```


#### create and push a repo
```text
git init repo
cd repo
touch code.py file.txt
git add code.py file.txt
git commit -m “my first commit”
git log

create a new repo on GitHub; generate a token

git remote add origin https://github.com/leztien/repo.git
git branch -M main
git push --set-upstream origin main
```


#### setting the pull behaviour for fast forward
```text
git config --global pull.ff only
```



#### git starter routine (working locally)
```text
mkdir repo
cd repo
git init
git config --global user.email "me@mail.com"
git config --global user.name "My Name"
git commit  (optional)

echo “# master” >> readme.md
git add readme.md
git commit -m "my first comment"

git branch new_branch; git checkout new_branch
  or:
git checkout -b new_branch

git branch -a

echo “## new branch” >> readme.md
git add .
git commit -m "first changes on the new branch"

git checkout master
echo “## master” >> readme.md

touch code.py
git add code.py readme.md
git commit -m “made changes to readme.md and created a new file on the master branch”

git checkout new_branch
ls
(want to bring the changes – including the new code.py file into the new_branch)
git merge master -m "merged the master branch into the new_branch"
(the code.py file is added but the readme.md file stays the same)

git checkout master

git branch --delete new_branch

ls --all
rm *   (deletes all files in the current folder)
find . -name ".git"
rm -rf .git
cd ..
rm -rf repo   OR  rm repo
```

#### push
```text
(create a new repository on github, and generate token)
echo "# local" >> README.md
git init
git config --global user.email "me@mail.com"
git config --global user.name "My Name"
git add README.md
git commit -m "first commit"
git branch -M main    (-M renames the ‘master’ branch to ‘main’)
git branch -a
git remote add origin https://github.com/leztien/repo.git
git push -u origin main (same as git push --set-upstream origin my-branch)
```


#### pull
```text
git pull origin main

echo "# on local" >> readme.md
git status

git add .
git commit -m “changes to readme.md on local”
git push

(make some changes to readme.md on github manually)
git pull
git push
```

