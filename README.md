Rprogram
========

online R course

R version 3.1.0 (2014-04-10) -- "Spring Dance"
Copyright (C) 2014 The R Foundation for Statistical Computing
Platform: x86_64-w64-mingw32/x64 (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

  Natural language support but running in an English locale

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

[Previously saved workspace restored]

> swirl()
Error: could not find function "swirl"
> library(swirl)

| Hi! Type swirl() when you are ready to begin.

> swirl()

| Welcome to swirl! Please sign in. If you've been here before, use the same
| name as you did then. If you are new, call yourself something unique.

What shall I call you? GeekinMeasurement

| Please choose a course, or type 0 to exit swirl.

1: R Programming
2: Take me to the swirl course repository!

Selection: 2

| OK. I'm opening the swirl courses web page in your browser.

| Leaving swirl now. Type swirl() to resume.

> swirl()

| Welcome to swirl! Please sign in. If you've been here before, use the same
| name as you did then. If you are new, call yourself something unique.

What shall I call you? GeekinMeasurement

| Please choose a course, or type 0 to exit swirl.

1: R Programming
2: Take me to the swirl course repository!

Selection: 1

| Please choose a lesson, or type 0 to return to course menu.

1: Basic Building Blocks
2: Sequences of Numbers
3: Vectors
4: Missing Values
5: Subsetting Vectors
6: Matrices and Data Frames

Selection: 1


  |                                                                            
  |                                                                      |   0%

| In this lesson, we will explore some basic building blocks of the R
| programming language.

...


  |                                                                            
  |==                                                                    |   3%
| If at any point you'd like more information on a particular topic related to
| R, you can type help.start() at the prompt, which will open a menu of
| resources (either within RStudio or your default web browser, depending on
| your setup). Alternatively, a simple web search often yields the answer
| you're looking for.

...


  |                                                                            
  |====                                                                  |   6%
| In it's simplest form, R can be used as an interactive calculator. Type 5 + 7
| and press Enter.

> 5+7
[1] 12

| Keep up the great work!


  |                                                                            
  |=======                                                               |   9%
| R simply prints the result of 12 by default. However, R is a programming
| language and often the reason we use a programming language as opposed to a
| calculator is to automate some process or avoid unnecessary repetition.

...


  |                                                                            
  |=========                                                             |  12%
| In this case, we may want to use our result from above in a second
| calculation. Instead of retyping 5 + 7 every time we need it, we can just
| create a new variable that stores the result.

...


  |                                                                            
  |===========                                                           |  16%
| The way you assign a value to a variable in R is by using the assignment
| operator, which is just a 'less than' symbol followed by a 'minus' sign. It
| looks like this: <-

...


  |                                                                            
  |=============                                                         |  19%
| Think of the assignment operator as an arrow. You are assigning the value on
| the right side of the arrow to the variable name on the left side of the
| arrow.

...


  |                                                                            
  |===============                                                       |  22%
| To assign the result of 5 + 7 to a new variable called x, you type x <- 5 +
| 7. This can be read as 'x gets 5 plus 7'. Give it a try now.

> x <- 5+7

| That's a job well done!


  |                                                                            
  |==================                                                    |  25%
| You'll notice that R did not print the result of 12 this time. When you use
| the assignment operator, R assumes that you don't want to see the result
| immediately, but rather that you intend to use the result for something else
| later on.

...


  |                                                                            
  |====================                                                  |  28%
| To view the contents of the variable x, just type x and press Enter. Try it
| now.

> x
[1] 12

| You are amazing!


  |                                                                            
  |======================                                                |  31%
| Now, store the result of x - 3 in a new variable called y.

> y <- x-3

| You nailed it! Good job!


  |                                                                            
  |========================                                              |  34%
| What is the value of y? Type y to find out.

> y
[1] 9

| You got it!


  |                                                                            
  |==========================                                            |  38%
| Now, let's create a small collection of numbers called a vector. Any object
| that contains data is called a data structure and numeric vectors are the
| simplest type of data structure in R. In fact, even a single number is
| considered a vector of length one.

...


  |                                                                            
  |============================                                          |  41%
| The easiest way to create a vector is with the c() function, which stands for
| 'concatenate' or 'combine'. To create a vector containing the numbers 1.1, 9,
| and 3.14, type c(1.1, 9, 3.14). Try it now and store the result in a variable
| called z.

> c(1.1,9,3.14)
[1] 1.10 9.00 3.14

| You're close...I can feel it! Try it again. Or, type info() for more options.

| Inputting z <- c(1.1, 9, 3.14) will assign the vector (1.1, 9, 3.14) to a new
| variable called z. Including single spaces after the commas in the vector is
| not required, but helps make your code less cluttered and more readable.

> z <- c(1.1, 9, 3.14)

| That's a job well done!


  |                                                                            
  |===============================                                       |  44%
| Anytime you have questions about a particular function, you can access R's built-in help files via the `?` command. For example, if you want more information on the
| c() function, type ?c without the parentheses that normally follow a function name. Give it a try.

> ?c()
Error in .helpForCall(topicExpr, parent.frame()) : 
  no documentation for function ‘c’ and signature ‘x = "missing"’
In addition: Warning message:
In .helpForCall(topicExpr, parent.frame()) :
  no method defined for function ‘c’ and signature ‘x = "missing"’
> ?c
starting httpd help server ... done

| Nice work!


  |                                                                            
  |=================================                                     |  47%
| Type z to view it's contents. Notice that there are no commas separating the values in the output.

> z
[1] 1.10 9.00 3.14

| Nice work!


  |                                                                            
  |===================================                                   |  50%
| You can combine vectors to make a new vector. Create a new vector that contains z, 555, then z again in that order. Don't assign this vector to a new variable, so
| that we can just see the result immediately.

> c(z,555,z)
[1]   1.10   9.00   3.14 555.00   1.10   9.00   3.14

| Excellent job!


  |                                                                            
  |=====================================                                 |  53%
| Numeric vectors can be used in arithmetic expressions. Type the following to see what happens: z * 2 + 100.

> z *2 + 100
[1] 102.20 118.00 106.28

| That's a job well done!


  |                                                                            
  |=======================================                               |  56%
| First, R multiplied each of the three elements in z by 2. Then it added 100 to each element to get the result you see above.

...


  |                                                                            
  |==========================================                            |  59%
| Other common arithmetic operators are `+`, `-`, `/`, and `^` (where x^2 means 'x squared'). To take the square root, use the sqrt() function and to take the
| absolute value, use the abs() function.

...


  |                                                                            
  |============================================                          |  62%
| Take the square root of z - 1 and assign it to a new variable called mySqrt.

> mySqrt <- sqrt(z-1)

| You are amazing!


  |                                                                            
  |==============================================                        |  66%
| Before we view the contents of the mySqrt variable, what do you think it contains?

1: a vector of length 3
2: a vector of length 0 (i.e. an empty vector)
3: a single number (i.e a vector of length 1)

Selection: 1

| Nice work!


  |                                                                            
  |================================================                      |  69%
| Print the contents of mySqrt.

> mySqrt
[1] 0.3162278 2.8284271 1.4628739

| That's correct!


  |                                                                            
  |==================================================                    |  72%
| As you may have guessed, R first subtracted 1 from each element of z, then took the square root of each element. This leaves you with a vector of the same length as
| the original vector z.

...


  |                                                                            
  |====================================================                  |  75%
| Now, create a new variable called myDiv that gets the value of z divided by mySqrt.

> myDiv <- z/mySqrt

| Keep up the great work!


  |                                                                            
  |=======================================================               |  78%
| Which statement do you think is true?

1: myDiv is a single number (i.e a vector of length 1)
2: The first element of myDiv is equal to the first element of z divided by the first element of mySqrt, and so on...
3: myDiv is undefined

Selection: 2

| You got it!


  |                                                                            
  |=========================================================             |  81%
| Go ahead and print the contents of myDiv.

> myDiv
[1] 3.478505 3.181981 2.146460

| That's correct!


  |                                                                            
  |===========================================================           |  84%
| When given two vectors of the same length, R simply performs the specified arithmetic operation (`+`, `-`, `*`, etc.) element-by-element. If the vectors are of
| different lengths, R 'recycles' the shorter vector until it is the same length as the longer vector.

...


  |                                                                            
  |=============================================================         |  88%
| When we did z * 2 + 100 in our earlier example, z was a vector of length 3, but technically 2 and 100 are each vectors of length 1.

...


  |                                                                            
  |===============================================================       |  91%
| Behind the scenes, R is 'recycling' the 2 to make a vector of 2s and the 100 to make a vector of 100s. In other words, when you ask R to compute z * 2 + 100, what
| it really computes is this: z * c(2, 2, 2) + c(100, 100, 100).

...


  |                                                                            
  |==================================================================    |  94%
| To see another example of how this vector 'recycling' works, try adding c(1, 2, 3, 4) and c(0, 10). Don't worry about saving the result in a new variable.

> c(1,2,3,4) + c(0,10)
[1]  1 12  3 14

| You nailed it! Good job!


  |                                                                            
  |====================================================================  |  97%
| If the length of the shorter vector does not divide evenly into the length of the longer vector, R will still apply the 'recycling' method, but will throw a warning
| to let you know something fishy might be going on.

...


  |                                                                            
  |======================================================================| 100%
| Try c(1, 2, 3, 4) + c(0, 10, 100) for an example.

> c(1,2,3,4) + c(0,10,100)
[1]   1  12 103   4
Warning message:
In c(1, 2, 3, 4) + c(0, 10, 100) :
  longer object length is not a multiple of shorter object length

| You got it right!

| Are you currently enrolled in the Coursera course associated with this lesson?

1: Yes
2: No

Selection: 1

| Would you like me to notify Coursera that you've completed this lesson? If so, I'll need to get some more info from you.

1: Yes
2: No
3: Maybe later

Selection: 1

| Is the following information correct?

Course ID: rprog-003
Submission login (email): yi.du.lin0020@gmail.com
Submission password: k3EJSKqtpa

1: Yes, go ahead!
2: No, I need to change something.

Selection: 1

| I'll try to tell Coursera you've completed this lesson now.

| Great work!

| I've notified Coursera that you have completed rprog-003, Basic_Building_Blocks.

| You've reached the end of this lesson! Returning to the main menu...

| Please choose a course, or type 0 to exit swirl.

1: R Programming
2: Take me to the swirl course repository!

Selection: 1

| Please choose a lesson, or type 0 to return to course menu.

1: Basic Building Blocks
2: Sequences of Numbers
3: Vectors
4: Missing Values
5: Subsetting Vectors
6: Matrices and Data Frames

Selection: 
