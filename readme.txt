Git version control system tutorial notes:

work space --------(git add)-----> index (stage) --------(git commit)-----------> master

Commands explanation:

1. git init 

initial a repository

2. git add xxx.txt xxx2.txt xxx3.txt
add file/s to the repository

3. git commit -m "declare what changes have been made here - eg. added 3 files"

write commit of  changes

4. git status

check changes history

5. git diff
check what is changed
5.1 git diff HEAD -- test.txt
check different between work space and version repository( master)

6. git log
display log time line

6.1 git log --pretty=oneline
display each log in one line

7. git reset --hard HEAD^
go back to last version
7. 1 git reset --hard HEAD~55
go back to version 55

7.2 git reset --hard 9f4d09b
go to version 9f4d09b

7.2.1 git log
check version if you want to go back to past

7.2.2 git reflog
check version if you want to go back to future

8. git checkout -- readme.txt

discard modifications in workspace

9. git reset HEAD test.txt + git checkout -- test.txt
discard modifications in stage
9.1 git reset --hard HEAD 3as4df
restore to last version in version repository (master)

10. rm test.txt 
10.1 git checkout -- test.txt
recovery file test.txt
10.2 git rm test.txt
permanently delete file test.txt

11.1 git remote add origin git@server-name:path/repo-name.git
connect to a remote repository

11.2. git push -u origin master
Push all content from master to origin repository first time

11.3.git push origin master
push modifications
.
12. git clone https://github.com/kevinyangcourse/gitwork3
clone origin repository to local area

13. git branch dev
create branch dev
13.1 git checkout -b dev
create branch dev and switch to dev
13.2 git branch
check current branch
13.3 git checkout master
change to branch master
13.4 git merge dev
merge branch dev to master
13.5 git branch -d dev
delete branch dev

14. create feature1 branch--> add line, save / add/commit --> checkout to master -->
open file, add line with conflict content --> save / add / commit -->
 merge --> conflict --> check and fix conflict, save file -> submit

14.1git log --graph
check branch status
14.2 git log --graph  --pretty=online --abbrev-commit
check brief report of branch status


15. git merge --no-ff -m 'merge with no-ff' dev
merge branch without fast forward argue.

Fast forward cannot keep the record.

16. git stash
save current job and suspend.

-------------------------------------------------

Other commands:

a. pwd: check current directory 
b. ls: display all files (=dir)
c. cat: display file (cat readme.txt)
d. git push origin master (push changes to cloud side)
e. gitk: graphic view

End
