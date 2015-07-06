
##Git version control system tutorial notes:

work space --------(git add)-----> index (stage) --------(git commit)-----------> master(locl repo)

##Commands explanation:

###1. git init 

initial a repository

###2. git add xxx.txt xxx2.txt xxx3.txt
add file/s to the repository

###3. git commit -m "declare what changes have been made here - eg. added 3 files"

write commit of  changes

###4. git status

check changes history

###5. git diff
check what is changed
####5.1 git diff HEAD -- test.txt
check different between work space and version repository( master)

###6. git log
display log time line

####6.1 git log --pretty=oneline
display each log in one line

###7. git reset --hard HEAD^
go back to last version
####7. 1 git reset --hard HEAD~55
go back to version 55

####7.2 git reset --hard 9f4d09b
go to version 9f4d09b

####7.2.1 git log
check version if you want to go back to past

####7.2.2 git reflog
check version if you want to go back to future

###8. git checkout -- readme.txt

discard modifications in workspace

###9. git reset HEAD test.txt + git checkout -- test.txt
discard modifications in stage
####9.1 git reset --hard HEAD 3as4df
restore to last version in version repository (master)

###10. rm test.txt 
####10.1 git checkout -- test.txt
recovery file test.txt
####10.2 git rm test.txt
permanently delete file test.txt

###11. Create connection between local repo and remote repo
####11.1 git remote add origin git@server-name:path/repo-name.git
connect to a remote repository

####11.2. git push -u origin master
Push all content from master to origin repository first time

####11.3.git push origin master
push modifications

###12. git clone https://github.com/kevinyangcourse/gitwork3
clone origin repository to local area

###13. git branch dev
create branch dev
####13.1 git checkout -b dev
create branch dev and switch to dev
####13.2 git branch
check current branch
####13.3 git checkout master
change to branch master
####13.4 git merge dev
merge branch dev to master
####13.5 git branch -d dev
delete branch dev

###14. create feature1 branch--> add line, save / add/commit --> checkout to master -->
open file, add line with conflict content --> save / add / commit -->
 merge --> conflict --> check and fix conflict, save file -> submit

####14.1 git log --graph
check branch status
####14.2 git log --graph  --pretty=online --abbrev-commit
check brief report of branch status


###15. git merge --no-ff -m 'merge with no-ff' dev
merge branch without fast forward argue.

Fast forward cannot keep the record.

###16 fix emergent buy - use git stash to save current job and create new branch issue101

####16.1 git stash
save current job and suspend.


####16.2 git stash list
check if the suspend job exists

####16.3 git stash pop = git stash apply + git stash drop
restore suspend job


###17. git branch -D feature
force to delete un-merged branch feature.

###18. multiple user co-work:

git push origin dev  ---->  failed, origin got newer version, git pull, and merge 
-----> failed,  assign local dev branch to connect origin branch: git branch --set-upstream dev origin/dev
 ---> pull again ---> merge and push, git push origin dev
 
### 19. git tag
 add tag to branch
#### 19.1 git tag v1.0 51023a
 add tag to special commit
 use git log --pretty=oneline --abbrev-commit to find commit list
 
#### 19.2 git show v0.9
 show tags' details
####19.3 git show.
 
###20. git push origin v1.0
 push 1 tag
####20.1 git push origin --tags
 push all tags
####20.2 git tag -d v0.2
 delete tag v0.2
####20.3 git push origin :refs/tags/v1.0
 remote delete tag


###21. create .gitignore file and add 'test2.txt', 'test3.txt' in to ignore changes in these files.

.gitignore is in the workspace.


###22. git config --global alias.ci 'commit -'
     git config --global alias.co checokout
     git config --global alias.br branch

     Add alias name to short commands.

###23. cat .git/config
check git configuration

----------------------------------------------------
##Other common/UNIX commands:

* a. pwd: check current directory 
* b. ls: display all files (=dir)
* c. cat: display file (cat readme.txt)
* d. git push origin master (push changes to cloud side)
* e. gitk: graphic view
* f. clear: clear screen = dos/cls
* g. touch: create an empty file
* h. mv: move file = dos/copy+paste
* h1.mv file1.txt file2.txt: rename file from file1 to file2
* i. git config --list: all details of configuration
* j. git config --global user.name 'usernam': input username at first time to use

* j1. git config --global user.email 'email': input email 
----------------------------------------------

##Ref
###Tutorial: 
http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

###git-creatsheet:

http://liaoxuefeng-liaoxuefeng.stor.sinaapp.com/learngit/git-cheatsheet.pdf

###Markdown Help
http://daringfireball.net/projects/markdown

End
