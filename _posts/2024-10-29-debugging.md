# The Processes of Debugging 

## What is Debugging?

Debugging is known the process of finding and fixing errors or bugs in source code of any software. When your code does not work as expected, programmers run through their code step by step to figure out what is wrong with their code. The final step of debugging or workaround and make sure it works. Besides software development, we had hardware development, the debugging process looks for hardware components that are not installed or configured correctly. Debugging is a very long and draining process that programmers go through and sometimes it could take programmers hours upon days to find even one small problem in their code. 

## Example 1 
```python 
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```

This piece of code is supposed to count how many spaces are in a given string. This code is wrong and does not print out the count of how many spaces are in a given string. I spent time looking at this code, constantly trying to print out the input, changing between lines 4 and 7 and seeing if anything changes. In Line 5(if char == "";), the solution would be to add a space to the quotation marks(“ “) in order for the code to recognize the spaces. 

## Example 2

```python 
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```

This piece of code is intended to determine if numbers 1 to n are even or odd. The main problem with this code is that “n” is not a proper range for numbers and is recognized as a string. Even though, n is supposed to be recongized as a number inputted by the user. I changed this code was to give a range of (1-20) and then change the num % 2 < 0: to <= so it can determine whether the numbers from the range given is even or odd.

## Example 3

```python
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result)
```

This code is intended for a user to input an integer and if the number is under 0 it will print, don't input any negative numbers. Then, whatever the user inputs then it will calculate the factorial of the number. The problem with this code is that firstly it has in line 2 (if num < -1) and prints no negative number while -1 is a negative number itself so it won't work as intended and also the print statement in the last line does not work as intended. What I fixed in this code was to change the range of num to 1 instead of -1 so it will changed to (num < 1):. In the For Loop, on line 7, I changed the range to (1, num +1) so it's able to add the number by 1 if the number is in range. Then I changed the final print statement to have str(num) so it can concatenate. 

## Example 4 

```python
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break
```

This code is intended to the ask the user to input the correct password and is given three attempts and the program already has a default correct password, and you will get an extra attempt, if not every time you get it wrong, it will say "Incorrect password" and then if you pass three attempts it will print "Too many attempts". The main problem with this code is when you enter the correct password which is “secret”, it shows up as an incorrect password and it shows up as an incorrect password as a correct password. To fix this code, I first changed the if statement of  (if password == correct_password): and secondly I moved the attempts += 1 until after the break statement so that it will reset the attempts even after the code is done. 









