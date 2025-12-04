<style>

</style>


Caleb Ogboe
<br>
Dec/5/2025
<br>
Debugging Blog


<h1>Debugging Intro</h1>


Debugging is the process in which you try to figure out what's wrong with the code. Troubleshooting the code to see what's wrong with it and how you can go about fixing the bugs or error in the code that's making it act up. 

For how I go debugging, I read the code to first see what the purpose of the code is, then I scan to see where the issue might be residing and I begin taking action. Among the various types of errors such as Syntax, RunTime, Identation, and logical, the most common errors are sometimes Syntax errors, which is when you accidentaly put the wrong notation, or forgot to put the notation for that part of the code. Then based on my knowledge of coding, and some help from the internet, I fix the code according to its error.

<div style="
  padding:8px 12px;
">

<h2 style="margin-top: 40px;">Debugging Example 1:</h2>
</div>

```python
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```

<div style="
  padding:8px 12px;
">

Here is an example of a debugging that needs to be done. First thing to do would be to scan the code to see what it's supposed to do. After a quick analysis, we can tell that it's supposed to count how many spaces are in the given string. But as we can see, it's not working. The issue resides in the if statement. Right now, the if statement is only checking if there is am empty string, not a space between the given strings. To fix it, we would change from
<br>
    <strong> * if char == "": to if char == " ": *</strong>
<br>
So that the new if statement counts the space in the given string instead of an empty string.

<p>Here's what the fixed version should look like.</p>
</div>

```python
text = "Hello, world, my name is "
count = 0

for char in text:
    if char == " ":
       count += 1

print(count)
```

<div style="
  padding:8px 12px;
">

<h2 style="margin-top: 40px;">Debuggin Example 2:</h2> 
</div>

```python
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```


<div style="
  padding:8px 12px;
">

<p>A second example of a code that needs to be debugged. First thing to do as usual would be to scan the code to see what it's supposed to do. This code is supposed to be able to take in a number and tell you if the number is odd or even. Now it won't work since they're a few errors in it.</p> 

<p>To fix it, the first step would be to change the <strong> 'n = input()' to 'n = int(input())' </strong>. Why you may ask? Well, python will automatically read the input as a string, which isn't wrong, but since we're checking for numbers, the for loop will need the input to be an interger/number, so the code doesn't crash. That's the first step.</p> 

<p>The second step would be to fix the range in the for loop. <strong>range(1,n)</strong> doesn't work because <strong>'range()'</strong> excludes the end value, meaning that <strong>'n'</strong> won't be included and the range stops before that. Instead we fix that by adding 1 to the n, <strong>'range(1,n+1)'</strong> so that the end value is included and it's counted.</p>

<p>The 3rd step to make sure this code fufill its duty is to change the if statement. Change it from it's original code to <strong>'if num % 2 == 0:'</strong>. Now the code can know if the number inserted is even or odd. <strong>'0'</strong> meaning it's even since even numbers when divided have no remainder, but odd numbers when divided have a remainder. So if it was switched it would be <strong>'if num % 2 == 1'</strong>.</p>

<p>Here's what the fixed version should look like:</p>
</div>

```python
print("give me a number")
n = int(input())

for num in range(1, n+1):
    if num % 2 == 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```

<div style="
  padding:8px 12px;
">

<h2 style="margin-top: 40px;">Debugging Example 3:</h2> 
</div>

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
<div style="
padding:8px 12px;
">

<p>After scanning the code, we can tell that it's supposed to take in any number and give you the factorial of that number. But as usual, there are a few errors within the code preventing it from functioning properly.</p>

<p>First order of business is to fix the <strong>if statment.</strong> Right now it says <strong> if num < -1:</strong>, it should print no negative numbers. The issue is that if you put -1, it's still going to create an issue, because the if statement says if it's less than -1, which also means it's going to allow -1 in the statment, so we change that from <strong> if num < -1: to if num < 0:</strong> so that it doesn't go below zero and cause an error.</p>

<p>Second step is to fix the <strong>range(1, num)</strong>. The error is similar to that of debugging example 2. <strong>'range()'</strong> as stated earlier excludes the last value of a number you give it. For example, if you said 'range(1, 8)' it's going to stop at 7, right before 8, excluding it. So similar fix to debugging example 2, we change it from <strong>range(1, num):</strong> to <strong>range(1, num + 1)</strong> so that the last value is added.</p> 

<p>Third step is to fix the issue that resides in the print statement. At first, it looks right, but we have to look closer. A rule of point when coding python is that you can't add intergers and strings together, it's going to create an error. So, ...of " + num + "is" + result is going to create the following error <strong>TypeError: can only concatenate str (not "int") to str</strong>. Hence we use the ',' when trying to add an interger and a string together to avoid such errors.</p>

<p>Here's what the fixed version should look like:</p>

</div>

```python
num = int(input("Enter an integer: "))

if num < 0:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num + 1):
    result *= i   

print(f"Factorial of ", num,"is", result)
```

<div style="
  padding:8px 12px;
">

<h2 style="margin-top: 40px;">Debugging Example 4:</h2> 
</div>

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

<div style="
  padding:8px 12px;
">

<p>Now this piece of code looks a teeny bit complex from the rest. After scanning through the code, we can tell that it's a password guessing code. In it, you're only supposed to have no more than 3 guesses to guess the password. But there are a few issues wrong within the code that won't make it behave as intended.</p>

<p>The first step is to delete the <strong>'attempts += 1'</strong> under <strong>'password = input("Enter your password: ")'</strong> as it is not needed because it'll start counting before checking if the password is correct or not. Moreover, it counts every input as a failed attempt, even the correctly guessed password.

<p>Second step is to change the <strong>if password == "incorrect_password":</strong> because that isn't the correct password given to us in the code. Instead we change it to <strong>if password == correct_password:</strong>.

<p>Third step would be to add a break after the following first if statement so that when you guess the correct code, the code stops running. Otherwise, the code just keeps running even if you get it right.</p>

<p>Fourth step is fixing the else statement. Here, we bring back the <strong>attempts+=1</strong> and put it under here. Why? because if the user doesn't guess the password right on the first try, this attempt cell begins counting how many tries the user has gotten before the right password; it starts incrementing by 1.</p>

<p>Lastly, we move the third if statement under the else statement so we can keep track, and create a condition for the user if they use up more than 3 attempts. Then we change the <strong>if attempts > 3:</strong> to <strong>if attempts == 3</strong> because we are only giving the user 3 tries to guess the password, not more than 3 tries. This allows the code to be more efficient instead of scattered.</p>

<p>Here's what the fixed version should look like.</p>

</div>


```python
attempts = 0
correct_password = "secret" 


while True:
    password = input("Enter your password: ")
    if password == correct_password:
        print("Correct password!")
        break
    else:
        attempts += 1
        print("Incorrect password")
        if attempts == 3:
            print("Too many attempts")
            break
```