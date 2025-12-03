<style>

</style>


Caleb Ogboe
<br>
Dec/5/2025
<br>
Debugging Blog


<h2>Debugging Intro</h2>


Debugging is the process in which you try to figure out what's wrong with the code. Troubleshooting the code to see what's wrong with it and how you can go about fixing the bugs or error in the code that's making it act up. 

For how I go debugging, I read the code to first see what the purpose of the code is, then I scan to see where the issue might be residing and I begin taking action. Among the various types of errors such as Syntax, RunTime, Identation, and logical, the most common errors are sometimes Syntax errors, which is when you accidentaly put the wrong notation, or forgot to put the notation for that part of the code. Then based on my knowledge of coding, and some help from the internet, I fix the code according to its error.

Debugging Example 1:

<img src="/blog/images_for_debugging/debug1.png" alt= "Debugging Example 1" height = auto width = "400px" > 

Here is an example of a debugging that needs to be done. First thing to do would be to scan the code to see what it's supposed to do. After a quick analysis, we can tell that it's supposed to count how many spaces are in the given string. But as we can see, it's not working. The issue resides in the if statement. Right now, the if statement is only checking if there is am empty string, not a space between the given strings. To fix it, we would change from
<br>
    <strong> * if char == "": to if char == " ": *</strong>
<br>
So that the new if statement counts the space in the given string instead of an empty string.

Debuggin Example 2: 

<img src="/blog/images_for_debugging/debug2.png" alt= "Debugging Example 2" height = auto width = "400px" >

A second example of a code that needs to be debugged. First thing to do as usual would be to scan the code to see what it's supposed to do. This code is supposed to be able to take in a number and tell you if the number is odd or even. Now it won't work since they're a few errors in it. 
To fix it, the first step would be to change the <strong> 'n = input()' to 'n = int(input())' </strong>. Why you may ask? Well, python will automatically read the input as a string, which isn't wrong, but since we're checking for numbers, the for loop will need the input to be an interger/number, so the code doesn't crash. That's the first step. 

The second step would be to fix the range in the for loop. <strong>range(1,n)</strong> doesn't work because <strong>'range()'</strong> excludes the end value, meaning that <strong>'n'</strong> won't be included and the range stops before that. Instead we fix that by adding 1 to the n, <strong>'range(1,n+1)'</strong> so that the end value is included and it's counted.

The 3rd step to make sure this code fufill its duty is to change the if statement. Change it from it's original code to 
<strong>'if num % 2 == 0:'</strong>. Now the code can know if the number inserted is even or odd. <strong>'0'</strong> meaning it's even since even numbers when divided have no remainder, but odd numbers when divided have a remainder. So if it was switched it would be <strong>'if num % 2 == 1'</strong>.

Here's what the fixed version should look like:

<img src="/blog/images_for_debugging/debug2fix.png" alt="Debugging Example 2 fixed" height=auto width = "400px">

Debugging Example 3: 

<img src="/blog/images_for_debugging/debug3.png" alt="Debugging Example 3" height=auto width="400px"> 

After scanning the code, we can tell that it's supposed to take in any number and give you the factorial of that number. But as usual, there are a few errors within the code preventing it from functioning properly.

First order of business is to fix the <strong>if statment.</strong> Right now it says <strong> if num < -1:</strong>, it should print no negative numbers. The issue is that if you put -1, it's still going to create an issue, because the if statement says if it's less than -1, which also means it's going to allow -1 in the statment, so we change that from <strong> if num < -1: to if num < 0:</strong> so that it doesn't go below zero and cause an error.

Second step is to fix the <strong>range(1, num)</strong>. The error is similar to that of debugging example 2. <strong>'range()'<strong> as stated earlier excludes the last value of a number you give it. For example, if you said 'range(1, 8)' it's going to stop at 7, right before 8, excluding it. So similar fix to debugging example 2, we change it from <strong>range(1, num):</strong> to <strong>range(1, num + 1)</strong> so that the last value is added. 

Third step is to fix the issue that resides in the print statement. At first, it looks right, but we have to look closer. A rule of point when coding python is that you can't add intergers and strings together, it's going to create an error. So, ...of " + num + "is" + result is going to create the following error <strong>TypeError: can only concatenate str (not "int") to str</strong>. Hence we use the ',' when trying to add an interger and a string together to avoid such errors.

Here's what the fixed version should look like:

<img src="/blog/images_for_debugging/debug3fix.png" alt="Debugging Example 3 fixed" height=auto width="400px">


