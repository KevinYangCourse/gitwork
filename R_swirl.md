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

### section7 - matrices and data frames

45. my_vector <- 1:20, = c(1,2,3,...,20)
46. dim(my_vector), result NULL
47. length(my_vector), result 20
48. dim(my_vector) <- c(4,5)
49. dim(my_vector), attribures(my_vector): check attributes
50. class(my_vector): result "[1] "matrix"" /  class(my_data): result "[1]"numeric""
51. my_matrix2 <- matrix(1:20,4,5, FALSE, NULL)
52. identical (my_matrix, my_matrix2): result "TRUE"
53. patients <- c("Bill", "Gina", "Kelly", "Sean")
54. cbind(patients, my_matrix): add column of patient names in the matrix
55. my_data <- data.frame(patients, my_matrix): don't change numeric element to chr
56. class(my_data): result "[1] "data.frame""
57. cnames <- c("patient","age", "weight", "bp", "rating", "test")
58: colnames(my_data)<-cnames : add titles to each columns

### section8 - logic

59. TRUE & c(TRUE, FALSE, FALSE): & compare all elements, result [1] TRUE FALSE FALSE
60. TRUE && c(TRUE, FALSE, FALSE): && only compare 1st element, result [1] TRUE
61. |,||: OR
62. !=: NOT EQUAL
63. XOR: 0 1 1 0
64. ints <- sample(10), ints > 5, result [1] TRUE FALSE TRUE ...
65. which(ints>7): result [1] 1 5 9
66. any(ints<0): result [1] FALSE, to see if any of the elements of ints are <0
67. all(ints>0): result [1] TRUE, to see if all of the elements of ints are >0

### section9 - functions

68. Sys.Date()
69. mean(c(2,4,5))
70. Sys.Date: only function name will display its source code
71. args(remainder): check arguments in the function 'remainder'
72. some_function <- function(func){ func(2,4)}
73. evaluate(function(x){x+1},6)
74. evaluate(function(x){x[3]}, c(8,4,0))
75. evaluate(function(x){x[lenght(x)]}, c(8,4,0))
76. paste(..., sep=" ", collapse=NULL):All arguments after an ellipses must have default values.
77. my_1func <- function(x=1,y=2,z=3){x+y+z}
78. telegram <- function(...){paste("START", ..., "STOP")}
79. mad_libs <- function(...){
	theargs <- list(...)
	place <- theargs[["place"]]
	adjective <- theargs[["adjective"]]
	noun <- theargs[["noun"]]
    }

80. "%p%" <- function(left,right){
	paste(left, right)
	}

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

1. Everything that exists is an object.
2. Everything that happens is a function call.


