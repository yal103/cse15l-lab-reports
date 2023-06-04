# Lab Report 5 - Putting it All Together
**Yangyang Liu \
CSE 15L Section B02 \
PID: A17360266**

This lab report designs a debugging scenerio on EdStem and has a reflection of the lab during the second half of the quarter.

&nbsp;
&nbsp;

## Part 1 - Debugging Scenario
> **_NOTE:_** I am using parts of the code from Week 9 Lab Scenario 4, found [here](https://ucsd-cse15l-s23.github.io/week/week9/#scenario-4).

### 1. Original Post

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?**

I am using a MacBook Pro Max operating on macOS Ventura 13.3.1. My main web browser is Google Chrome. I use VS Code to edit my programs. 

&nbsp;

**Detail the symptoms you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying "it doesn't work".**

I am trying to run my `Code.java` using a bash script, `run.sh`. The Java program is supposed to check if a file exists and print a message acoordingly. However, it's giving an incorrect output. Testing with the `Dune.txt` file, which exists in my `textfiles/novels` directory, the program is printing that the file does not exist, which is not expected.



&nbsp;

**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.**
