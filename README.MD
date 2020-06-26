#start local reposutory

git init

#see file in working directory

ls

##see file in local directory

git ls-files

#add file from working to stage 

git add <file name>

# git commit for add message

git commit -m "some message"
git commit -a -m "message"

#git log for previous history

git log <file name>

git log

#git diff for check change

git diff <file name>
git diff --gtaged <filename>

#delete file 

git delete <file name>
git commit -m "delete file name"

# rm command
#rm command delete file from working repo  and local repo
# rm file from local repo not working repo

git rm --cached <filename>
git commit -m "del file"

#untracked file
create .gitignore file and add file name inside it what i dont want to track
git add .gitignore
git commit -m "ignore from file <file name>"

#remove the change from working directory/unstaged

git checkout --<filename>

#remove the change from staged/local repo area

git reset HEAD <file name>

#remove from commit level

git log --oneline[this cmd show the commit step by step]

git reset HEAD~1[delet first commit from local/staged  repo/not from log level]
git reset HEAD~2[delet  second commit]

git reset --mixed  HEAD~1[delet first commit/also from log level]

#you can get back the commit from workig dir from commit


#git soft reset can remove change from stage and it can be back easily with commit

git reset --soft HEAD~2

#reset from file level
git reset --soft <filename>

# heard reset will remove all but specific commit and nothing get back from work or local repo
git reset --heard HEARD~2 [it will remove upper two comments and 3rd one will bw first]



####################################branching######################################################

#show branch
git branch

#create new branch

git checkout -b <branch name>[its a copy of master branch]

git checkout -b <new branch> <master branch>[same as above]


#log of branch
git log --oneline <branch name>

#switch branch

git checkout <branchname>

#if you want to marge any branch with other

git merge <source branch> <destination branch>[source=which i get merge | destination= with which]

# if i am on master branch and merge with other then command will be

git merge <branch what i want to marge>

#if i want to marge any branch but both file are exist in both branch then i have to merge it manually
just open and delete head and branch name of that file and add and commit again



##########################stash############################

stash means if i work with 3 files.3rd file is completed but other two is not yet .then can stashed them in a temporary shell and 3rd will be commited and after that i can get bach those two stash file to work again

git stash

git stash list

git show stash

#unstash file
# pop / apply work same | pop will delete sash but apply wont delet stash
git stash pop <stash number>

git stash apply  <stash number>

#####partial stash

#i can stash a specific file 
git stash -p [just select y or n]

# delete/clear stash

git stash clear[will delete all stash]

git stash drop <stash id>[will delete specific stash file]





























































