## R Swirl Brief List

### section1 & 2 - Basic building blocks & workspace and files
1. x<-c(5,2.2,88)
2. x^2: square
3. sqrt(): square root
4. c(1,2,3,4) + c(0,10)
5. c(1,2,3,4) + c(0,10,100)
6. old.dir<-getwd()
7. dir.create("testdir")
8. setwd("testdir")
9. file.create("mytest.R")

### section3 - sequences of Numbers

10. 1:20 pi:10 15:1
11. seq(1,20)
12. ?':': help for character ':'
13. seq(5,10, by=0.5)
14. my_seq<-seq(5,10, length=30)
15. 1:length(my_seq) == seq(along.with = my_seq) == seq_along(my_seq)
16. rep(0,times=40)
17. rep(c(0,1,2),times=10): repeat 10 times 0,1,2
18. rep()

### section4 - Vectors

19. my_char<-("my","name","is")
20. paste(my_char,collapse=" ")
21. paste(1:3,c("X","Y","Z"), sep="")
22. paste(LETTERS, 1:4, sep="-"): numeric vector is coerced into the character vector

### section5 -  Missing values

23. y<-rnorm(1000)
24. z<- rep(NA, 1000)
25. my_data <- sample(c(y,z),100)
26. my_na <- is.na(my_data)
26.1 my_data == NA : ==is.na(my_data)
27. sum(my_na): TRUE=1,FALSE=0, the result shows how many 'TRUE's
28. 0/0: [1] NaN = Not a Number
29. Inf - Inf: [1] NaN, Inf = infinity

### section6 - subsetting vectors

30. x[1:10}
31. x[is.na(x)]: a vector of all NAs
32. y<- x[!is.na(x)]
33. y[y>0] / x[x>0]: positive elements of y / positive elements of x and NAs
34. x[!is.na(x) & x > 0]
35. x[c(3,5,7)]
36. x[0]: R is 1-based indexing - start from 1, C/C# is 0 based language
37. x[3000]: result [1] NA, R still shows whatever you ask, make sure the correct scope
38. x[c(-2,-10)] = x[-c(2,10)]: shows elements 1 - 40 except 2nd and 10th.
39. vect <- c(foo=11,bar=2, norf=NA)
40. names(vect): display name only
41. vect2 <- c(11,2, NA) --->  names(vect2) <- c("foo","bar","norf")
42. identical(vect,vect2): compare 2 vectors
43. vect["bar"]
44. vect[c("foo","bar")]

### section7 - 
### section8 -
### section9 - 
### section10 -
### section11 - 
### section12 - 
### section13 - 
### section14 - 
### section15 - 

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
* identical(vect,vect2): compare 2 vectors

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




