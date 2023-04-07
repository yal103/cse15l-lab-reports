# Lab Report 1 - Remote Access and FileSystem

This is a quick tutorial on how to log into a course-specific account on `ieng6` and connect to a remote computer over the internet.

---

### SETUP
1. Find your CSE 15L course-specific account [here](<https://sdacs.ucsd.edu/~icc/index.php>). Use this [guide](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view?usp=share_link) to reset your password.
    > Note that it may take several minutes for the password reset to take effect.
2. Open Visual Studio Code.

   The window should look something like this.
     
   <img src="VSCode.png" width="40%" length="40%"> 

3. *Skip to Step 4 if you are on MacOS.* If you are using a **Windows** device, make sure that you have 'git' downloaded.

    [Download Git for Windows](https://gitforwindows.org/)

    After installing git, follow the these [steps](https://stackoverflow.com/a/50527994) to set your default terminal to use 'git bash' in Visual Studio Code.

4. Open a terminal in Visual Studio Code.
    - On **MacOS**, press control + ` , or use the menu option Terminal→New Terminal.
    - On **Windows**, press Ctrl + ` .
 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="Terminal1.png" width="25%" length="25%"> <img src="Terminal2.png" width="70%" length="70%">

---
        
### CONNECTING REMOTELY
1. In the terminal, type the command `ssh` followed by your CSE 15L course-specific account and press enter. \
For example: \
    ```$ ssh cs15lsp23mh@ieng6.ucsd.edu```
2. If this is your first time you are connecting to the server on your device, you will likely receive a message like this:

    ```
    The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established. 
    RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
    Are you sure you want to continue connecting (yes/no/[fingerprint])?
    ```
    Type `yes` and press enter.

3. You will be asked to enter the password to your CSE 15L course-specific account.
    > Note: What you type will not visibly appear in the terminal but will be inputed.

4. Once you are successfully logged in, your terminal should display something like this.

