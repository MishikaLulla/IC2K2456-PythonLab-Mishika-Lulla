
## section a: concept check

1. the value must be stored **outside** the main loop so it can remember the value between different choices.
2. we need to **import** the random module.
3. the same principle is called **binary** search.
4. the transaction should be **rejected** and an error message should be displayed.
5. the variable must be **updated** correctly on every iteration.

## section b: trace the logic

### 1 atm simulation

starting balance = 5000
* check balance → balance is 5000
* withdraw 2000 → balance becomes 3000
* deposit 500 → balance becomes 3500
* withdraw 4000 → rejected because 4000 is more than the current balance of 3500
final balance = 3500

### 2. reverse guessing game

secret number = 37
starting range = 1 to 100
* first guess = 50 → too high → new range is 1 to 49
* second guess = 25 → too low → new range is 26 to 49
* third guess = 37 → correct

the computer finds the number in 3 guesses.

### 3. grade calculator
marks are:
85 92 78 60 55
total marks = 370
average = 370 / 5 = 74
according to the grading system the grade is **c**.

# section c: programs

## 1. atm simulation

### aim
the program simulates a simple atm with options to check balance deposit money withdraw money change pin and exit

### logic

the program first checks the user's pin before showing the menu
a loop keeps the menu running and updates the balance after deposits and withdrawals
withdrawals are rejected when the amount is greater than the current balance

### sample input and output

enter pin  1234

1. check balance
2. deposit
3. withdraw
4. change pin
5. exit
enter choice  1
balance 5000

1. check balance
2. deposit
3. withdraw
4. change pin
5. exit
enter choice  2
enter deposit amount 200
deposit successful
balance 5200.0



## 2 student grade calculator

### aim

the program takes marks for five subjects and calculates the average and grade of the latest student

### logic

the marks are stored in a list and the average is calculated using the total marks
conditional statements are used to assign the grade based on the average
the latest student's data is stored so it can be viewed from the menu

### sample input and output
enter marks for 5 subjects:
85
92
78
60
55

average: 74
grade: c
```

invalid case:

```text
enter marks for 5 subjects:
85
120
invalid marks
```

---

## 3. reverse guessing game

### aim
the program lets the computer guess a number selected by the user

### logic
the computer starts with a range and guesses the middle value.
based on the user's feedback it removes half of the possible numbers and continues until the correct number is found.

### sample input and output

enter the lower limit:  1
enter the upper limit:  100

think of a number between 1 and 100

computer guess: 50
enter too high too low or correct:  too high

computer guess: 25
enter too high too low or correct:  too low

computer guess: 37
enter too high too low or correct:  correct
the computer found your number
number of guesses: 3

## 4. guessing game with hints and scoring

### aim
the program generates a random number and asks the user to guess it while giving hints and maintaining a score

### logic

the game starts with 100 points and removes 10 points after every wrong guess.
after each wrong guess the program gives even or odd and multiple of 5 hints.
the game ends when the user guesses correctly or reaches the maximum number of attempts.

### sample input and output

guess the number between 1 and 100
enter your guess 50
your guess is too low
hint: the number is even
hint: the number is not a multiple of 5
attempts left: 9
enter your guess 82
your guess is too low
hint: the number is even
hint: the number is not a multiple of 5
attempts left: 8
enter your guess 92
your guess is too low
hint: the number is even
hint: the number is not a multiple of 5
attempts left: 7
enter your guess 102
your guess is too high
hint: the number is even
hint: the number is not a multiple of 5
attempts left: 6
enter your guess 98
correct
your score is 60

## 5. combined application

### aim
the program combines the atm grade calculator and guessing game into one application

### logic
a top-level menu allows the user to select any of the three programs.
each program runs inside its own menu and returns to the main menu when the user chooses exit.

### sample input and output

```text
1. atm
2. grade calculator
3. guessing game
4. exit

enter choice: 1

atm menu
1. check balance
2. deposit
3. withdraw
4. change pin
5. exit

enter choice: 5

1. atm
2. grade calculator
3. guessing game
4. exit
```

invalid case:

```text
enter choice: 7
invalid choice
please select a valid option
```

---

# section d: analysis

## 1. reverse guessing game

binary search is much faster because every guess removes about half of the possible numbers
for a range of 1 to 100 the computer needs at most about 7 guesses to find the number
checking numbers one by one could take up to 100 guesses

## 2. atm withdrawal bug

if the balance is checked after subtracting the amount then the balance can become negative before the program notices the problem
for example if the balance is 3000 and the user withdraws 5000 the balance would first become -2000

## 3. guessing game hints
yes the hints make the game easier because they give the user extra information about the secret number
the user can remove some possible numbers after every wrong guess
because of this the expected number of guesses becomes lower than in a plain guessing game


## 4. combined application

the individual programs were written using functions so they can be called from the main menu
instead of ending the whole program when the user selects exit each function returns control to the top-level menu
this allows the user to move between the atm grade calculator and guessing game without restarting the program


# section e: documentation summary

all five programs use loops and conditional statements where required
the programs also handle invalid input and rejected transactions without crashing
the combined application uses separate functions for each program so control can return to the main menu
