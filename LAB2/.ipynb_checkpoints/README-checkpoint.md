PYTHON LAB 2 

# 1 ARMSTRONG NUMBER
AIM
to check whether a given number is an armstrong number and to print all armstrong numbers within a range given by the user

LOGIC
the program takes a number and finds the total number of digits
each digit is raised to the power of the total number of digits and all the values are added
if the final sum is equal to the original number then it is an armstrong number
the same logic is used with a loop to find all armstrong numbers in the given range

SAMPLE INPUT OUTPUT
input
153
output
153 is an Armstrong number.


range

1 to 20

output
Armstrong numbers are:
1
2
3
4
5
6
7
8
9

# 2 PRIME NUMBER
AIM
to check whether a given number is prime and to print all prime numbers up to a given limit

LOGIC
the program checks whether the number is divisible by any number other than 1 and itself
if no divisor is found then the number is prime
a loop is then used to check every number up to the limit and print all prime numbers

SAMPLE INPUT OUTPUT

input
23

output
23 is a prime number

limit
3

output
prime numbers up to 3 are
2 3 

# 3 PERFECT NUMBER
AIM
to check whether a given number is a perfect number and to print all perfect numbers up to a given limit

LOGIC
the program finds all the proper divisors of the given number
these divisors are added together
if their sum is equal to the original number then it is a perfect number
the same logic is repeated for all numbers up to the given limit

SAMPLE INPUT OUTPUT

input
6

output
6 is a perfect number

limit
10

output
perfect numbers up to 10 are:
6

# 4 PALINDROME
AIM
to check whether a number and a string are palindromes

LOGIC
for the number the digits are reversed using arithmetic operations without converting the number into a string
the reversed number is compared with the original number
for the string the reversed string is compared with the original string
if both values are the same then the input is a palindrome

SAMPLE INPUT OUTPUT

number input
11

output
11 is a palindrome

string input
mom

output
mom is a palindrome

# 5 FIBONACCI SERIES
AIM
to print the fibonacci series using both a loop and recursion and compare the recursive function calls

LOGIC
the loop version generates each new number by adding the previous two numbers
the recursive version calls the same function again to calculate previous fibonacci values
a counter is used to keep track of how many times the recursive function is called

SAMPLE INPUT OUTPUT

input
6

output
fibonacci series using loop
0 1 1 2 3 5 
Fibonacci series using recursion
0 1 1 2 3 5 
number of recursive function calls: 34

# 6 PATTERN PRINTING
AIM
to print different star and number patterns using nested loops

LOGIC
the program takes the number of rows from the user
nested loops are used to control the rows and the values printed in each row
separate logic is used for the star triangle number pattern and centered pyramid

SAMPLE INPUT OUTPUT

input
4
output
right angled triangle
*
**
***
****

number pattern:
1
12
123
1234

pyramid pattern:
   *
  ***
 *****
*******


# 7 MENU DRIVEN APPLICATION
AIM
to combine the programs from armstrong number to pattern printing into one menu driven application

LOGIC
the program displays a menu and asks the user to select an option
based on the selected choice the required function is called and the corresponding operation is performed
a while loop keeps showing the menu until the user chooses to exit
invalid choices are handled so that the program does not crash

SAMPLE INPUT OUTPUT

input

choice 2
number 22

output
22 is not a prime number

# 8 NUMBER GUESSING GAME
AIM
to create a number guessing game where the user has a limited number of attempts to guess a random number

LOGIC
the program generates a random number between 1 and 100
the user enters a guess and the program tells whether the guess is too high or too low
the game continues until the correct number is guessed or the maximum number of attempts is reached
the total number of attempts is displayed when the user guesses correctly

SAMPLE INPUT OUTPUT

welcome to the number guessing game!
guess the number between 1 and 100
you have 7 attempts

enter your guess  50
too low!

enter your guess  60
too high!

enter your guess  55
too high!

enter your guess  52
correct!
you guessed the number in 4 attempt(s)




## ANALYSIS
FOR LOOP AND WHILE LOOP

i used a for loop when the number of repetitions was already known such as checking numbers in a range generating fibonacci terms and printing patterns
i used a while loop when the program needed to continue until a condition changed such as in the menu driven application and the number guessing game

FIBONACCI LOOP AND RECURSION
the recursive version repeats more work as the value of n increases because the same fibonacci values are calculated again and again
the loop version calculates each term only once so it is faster and more efficient

PRIME NUMBER DIVISOR
to check whether a number is prime we only need to check divisors up to the square root of the number
if a number has a divisor greater than its square root then it will also have a corresponding divisor smaller than the square root

NUMBER GUESSING GAME STRATEGY
the best strategy is binary search
the user can start by guessing the middle number and then use the too high or too low result to remove half of the remaining possibilities after every guess
this helps in finding the correct number in fewer attempts