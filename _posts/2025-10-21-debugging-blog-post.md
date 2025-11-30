Caleb Ogboe
<br>
Oct 

<h2>Debugging Intro</h2>


Debugging is the process in which you try to figure out what's wrong with the code. Troubleshooting the code to see what's wrong with it and how you can go about fixing the bugs or error in the code that's making it act up. 

For how I go debugging, I read the code to first see what the purpose of the code is, then I scan to see where the issue might be residing and I begin taking action. Among the various types of errors such as Syntax, RunTime, Identation, and logical, the most common errors are sometimes Syntax errors, which is when you accidentaly put the wrong notation, or forgot to put the notation for that part of the code. Then based on my knowledge of coding, and some help from the internet, I fix the code according to its error.

Debugging Example 1:

<img src="/All_Images/images_for_debugging/debug1.png" alt= "Debugging Example 1" height=auto> 

Here is an example of a debugging that needs to be done. First thing to do would be to scan the code to see what it's supposed to do. After a quick analysis, we can tell that it's supposed to count how many spaces are in the given string. But as we can see, it's not working. The issue resides in the if statement. Right now, the if statement is only checking if there is am empty string, not a space between the given strings. To fix it, we would change from 
    if char == "": to if char == " ":
So that the new if statement counts the space in the given string instead of an empty string.
