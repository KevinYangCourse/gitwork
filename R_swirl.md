## R Swirl Brief List

1. x<-c(5,2.2,88)
2. x^2: square
3. sqrt(): square root
4. c(1,2,3,4) + c(0,10)
5. c(1,2,3,4) + c(0,10,100)
6. old.dir<-getwd()
7. dir.create("testdir")
8. setwd("testdir")
9. file.create("mytest.R")

10. 1:20 pi:10 15:1
11. seq(1,20)
12. ?':': help for character ':'
13. seq(5,10, by=0.5)
14. my_seq<-seq(5,10, length=30)
15. 1:length(my_seq) == seq(along.with = my_seq) == seq_along(my_seq)
16. rep(0,times=40)
17. rep(c(0,1,2),times=10): repeat 10 times 0,1,2
18. rep()

19. my_char<-("my","name","is")
20. paste(my_char,collapse=" ")
21. paste(1:3,c("X","Y","Z"), sep="")
22. paste(LETTERS, 1:4, sep="-"): numeric vector is coerced into the character vector
23. 

---------------------------------
###Swirl common command:

* skip(): skip the current question
* play(): try youself
* nxt(): stop play() and back to swirl session
* bye(): exit swirl
* main(): swirl main menu
* info(): display above options again

---------------------------------

###Common commmand:

* getwd():	 show the working directory
* ls():		 list current values/variables
* list.files():	 list file
* list.dirs():	 list folder
* dir.create("newFolder"): = cmd/mkdir
* setwd("newFolder"): set up 'newFolder' as working directory
* file.create("newFile.txt"): create new file
* file.exists("newFile.txt"): file exists or not, value = TRUE/FALSE
* file.info("newFile.txt"): file details
* file.info("newFile.txt")$mode: permission details
* args(file.path): list arguments in the function

---------------------------------
###How to get help

* ?file.create
* ?list.files
* ?ls

---------------------------------

### Install Swirl + R Programming in Rstudio

1. Open Rstudio - run as administrator
2. install.packages("swirl")
3. library(swirl)
4. install_from_swirl("R Programming") - take a while, don't close/reset
5. swirl()

---------------------------------




