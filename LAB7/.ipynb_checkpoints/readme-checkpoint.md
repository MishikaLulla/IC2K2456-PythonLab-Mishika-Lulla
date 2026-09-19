# python lab 7

## introduction

in this lab I studied time complexity and space complexity of different python programs
time complexity tells us how the running time of a program changes when the input size increases
space complexity tells us how much extra memory a program needs while running
we used big o notation to represent both time and space complexity

## what i learned

in this lab i learned how to find the time complexity of simple loops nested loops and recursive functions

i also learned that a single loop usually takes linear time while nested loops can take quadratic or cubic time

recursive programs can also use extra space because of the recursive calls stored in the call stack

some programs such as binary search are faster because they reduce the search space in every step

i also learned the difference between creating a new list and modifying an existing list in place

## programs covered

the lab contains twenty two snippets for finding time and space complexity

the first few snippets cover finding the maximum value checking duplicates summing digits and generating pairs

then we studied binary search matrix multiplication and converting a matrix into sparse form

we also studied programs with different types of loops including loops that run a fixed number of times

the lab also includes reversing an array factorial fibonacci and counting pairs with a given sum

other examples include generating all subsets merging sorted arrays checking palindromes and flattening a matrix

the last few snippets cover recursive power functions checking common elements and building a frequency map

## important concepts

a program with one loop running through n elements usually has linear time complexity

two nested loops that each depend on n usually give quadratic time complexity

three nested loops can give cubic time complexity

binary search has logarithmic time complexity because the search area becomes half after every step

recursive functions can require extra space because every recursive call is stored in the call stack

using a new list or dictionary can increase the space complexity depending on the number of elements stored

in place operations can use constant extra space when they only use a few variables

## conclusion

this lab helped me understand how different programming approaches affect the performance of a program

by finding time and space complexity i can compare different solutions and understand which one is more efficient

big o notation makes it easier to describe how a program behaves when the input size becomes larger
