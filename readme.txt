Git version control system tutorial notes:

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

6. git log
display log time line

6.1 git log --pretty=oneline
display each log in one line

7. git reset --hard HEAD^
go back to last version
7.1 git reset --hard 9f4d09b
go to version 9f4d09b
7.1.1 git log
check version if you want to go back to past
7.1.2 git reflog
check version if you want to go back to future


-------------------------------------------------

Other commands:

a. pwd: check current directory 
b. ls: display all files (=dir)

End
test line