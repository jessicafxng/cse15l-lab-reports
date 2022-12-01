# Welcome to Jessica's Lab 4 Report (:

## How to: Use Vim

This week I will be using the shortest sequence of Vim commands I came up with to accomplish the following task: Changing the name of the *start* parameter and its uses to *base*. 

I cloned a copy of the repository from CSE15L-Fall-2022's first Skill Demonstration using this command in the terminal: `git clone https://github.com/ucsd-cse15l-f22/skill-demo1 lab4report-vim`. I entered Vim mode on the DocSearchServer File to perform the lab task using this command in the terminal: `vim DocSearchServer`. This is what the command looks like in terminal and the screen it leads to: 

![Image](lab4-sc00.png)
![Image](lab4-sc0.png)

Now that I am in Vim, I can start completing the lab task. There are 18 steps in total.

## Step 1: /start + < press enter to enter command > 

Since the task aims to change the name of the *start* parameter to *base*, I will utilize the command `/paths` to find the first occurence of the path; The path in this case is start. This is a more time-efficient alternative to find the path we aim to change instead of using cursor movements to navigate. This is what the command looks like in terminal:

![Image](lab4-sc0.5.png)

As you can see, it brings my cursor to the first character of the word *start*.  

## Step 2: Press capital letter *E* once

I will press capital letter *E* once to jump forward to the end of the word (including the punctuation). This is what pressing the key looks like in the terminal:

![Image](lab4-sc1.png) 

As you can see, my cursor goes to the end of the word *start*, including the punctuation attached to it (parenthesis). This saves a small step since I can immediately start backspacing and replacing the word *start* with *base* once I enter *insert mode*. 

## Step 3: Enter insert mode

I will type in the command *i* to enter *insert mode* right where my cursor is. The following *INSERT* text should pop up on the bottom of the screen to show that the mode has successfully been entered:

![Image](insert.png) 

## Step 4: Replace the word *start* with *base*

I will backspace up to the first character of the word *start* and type in *base*. This completes the task: Changing the name of the *start* parameter to *base*. This is what replacing the word looks like in *insert mode*:

![Image](lab4-sc2.5.png)

## Step 5: ESC key to leave insert mode 

After replacing the parameter name, I will press the ESC key to leave *insert mode*. This is where pressing the key brings me: 

![Image](lab4-sc3.png) 

As you can see, the screen has the same contents as the previous screen, without the *INSERT* text on the bottom. We are now back in the *normal mode*.

## Step 6: /start (again) + < press enter to enter command > 

Since the task also asks to change all the uses of the parameter, I will continue to use the command `/paths` command to find the next occurence of the path *start*. This is what the command looks like in terminal:

![Image](lab4-sc3.5.png)

As you can see again, it brings my cursor to the first character of the word *start*.  

## Step 7: Press lower case letter *e* once

I will press lower case letter *e* once to jump forward to the end of the word (NOT including the punctuation). This is what pressing the key looks like in the terminal:

![Image](lab4-sc5.png) 

As you can see, my cursor goes to the end character of the word *start*, NOT including the punctuation attached to it (parenthesis) like last time. It is more time-efficient to press the *e* key instead of the *E* key since *E* would bring the cursor to the end of the line where the parenthesis ends. Since the parenthesis ends much farther away than last time, it will take more time getting my cursor to the place where it should start replacing the word *start* to *base*.

## Step 8: Press right arrow key → on keyboard once

I will press the right arrow key once to get my cursor to the position where I can immediately start backspacing and replacing the word *start* with *base* once I enter *insert mode*. This is where the cursor should be after pressing the key:

![Image](lab4-sc6.png)

## Step 9: Enter insert mode (again)

I will type in the command *i* to enter *insert mode* right where my cursor is. Again, the following *INSERT* text should pop up on the bottom of the screen to show that the mode has successfully been entered:

![Image](insert.png) 

## Step 10: Replace the word *start* with *base* (again)

I will backspace up to the first character of the word *start* and type in *base*. This partially completes the task: Changing the uses of the parameter name from *start* to *base* (there is one more use that we will replace later). This is what replacing the word looks like in *insert mode*:

![Image](lab4-sc8.png) 

## Step 11: ESC key to leave insert mode (again)

After replacing first use of the parameter name in the method, I will press the ESC key to leave *insert mode*. This is where pressing the key brings me: 

![Image](lab4-sc9.png) 

As you can see, the screen has the same contents as the previous screen, without the *INSERT* text on the bottom. We are now back in the *normal mode*.

## Step 12: /start (again) + + < press enter to enter command > 

I will continue to change all the uses of the parameter by using the command `/paths` again to find the next and final occurence of the path *start*. This is what the command looks like in terminal:

![Image](lab4-sc10.png)

As you can see again, it brings my cursor to the first character of the word *start*.

## Step 13: Press lower case letter *e* once (again)

I will press lower case letter *e* once to jump forward to the end of the word like the previous time (NOT including the punctuation). This is what pressing the key looks like in the terminal:

![Image](lab4-sc10.5.png) 

Again, it is more time-efficient in this case to press the *e* key instead of the *E* key since *E* would bring the cursor to the end of the line where the parenthesis ends. Since the parenthesis ends much farther away than last time, it will take more time getting my cursor to the place where it should start replacing the word *start* to *base*.

## Step 14: Press right arrow key → on keyboard once (again)

Like last time, I will press the right arrow key once to get my cursor to the position where I can immediately start backspacing and replacing the word *start* with *base* once I enter *insert mode*. This is where the cursor should be after pressing the key:

![Image](lab4-sc12.png.png)

## Step 15: Enter insert mode (again)

I will type in the command *i* to enter *insert mode* right where my cursor is. Again, the following *INSERT* text should pop up on the bottom of the screen to show that the mode has successfully been entered:

![Image](insert.png) 

## Step 16: Replace the word *start* with *base* (again)

I will backspace up to the first character of the word *start* and type in *base*. Now, this completes the task: Changing the uses of the parameter name from *start* to *base*. This is what replacing the word looks like in *insert mode*:

![Image](lab4-sc13.png) 

## Step 17: ESC key to leave insert mode (again)

After replacing first use of the parameter name in the method, I will press the ESC key to leave *insert mode* again. This is where pressing the key brings me: 

![Image](lab4-sc14.png) 

Like stated before, the screen has the same contents as the previous screen, without the *INSERT* text on the bottom. We are now back in the *normal mode*.

## Step 18: Save and exit + <+ < press enter to enter command > 

To save all my changes and exit, I will type in the command `:wq` in the terminal. `:w` saves the file and `q` quits the file. This is what the command looks like in the terminal:

![Image](lab4-sc15.png) 

This is what the screen should look like once the file is exited. I am back to where I started before Vim-ing into the `DocSearchServer` file.

![Image](lab4-sc16.png) 

## Comparing 2 Strategies: Running removely or Vim

In this section of this week's lab report, I will complete the following tasks (these instructions are found on [https://ucsd-cse15l-f22.github.io/week/week7/](https://ucsd-cse15l-f22.github.io/week/week7/)): 

1. " ...Start in Visual Studio Code and make the edit there, then scp the file to the remote server and run it there to confirm it works (you can just run bash test.sh on the remote to test it out). Consider having the appropriate scp command in your command history or easily copy-pasteable! "

2. " Second, start already logged into a ssh session. Then, make the edit for the task you chose in Vim, then exit Vim and run bash test.sh. Report how long it took you to make the edit in seconds in both styles, and any difficulties or details that came up in doing so. "

For task 1, I took approximately 1 minute and 30 seconds to complete all the edits on the *DocSearchServer* file and copy it onto my remote server. Some difficulties include just typing in all the commands to copy using `scp`, logging on using `ssh` and running `bash`; Some of the commands are lengthy so I often mispell. I accidentally pressed an extra letter when running my scp command so that took extra time. 

For task 2, I took approximately 55 seconds to edit and run `bash`. Unlike the first task, I didn't have to copy over any data so I took much less time completeing the tasks. I didn't run into any particular difficulties, especially after being freshly experienced with Vim from this lab report.

*Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?*

I would prefer to use Vim if I was under a time crunch or had to edit something really quickly. I choose Vim in this case because Vim takes significantly less time since `scp`-ing from local to remote isn't necessary. However, if I can time, I will choose local since I can be more precise.

*What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)*

Like I mentioned in the previous question, I would prefer to use Vim under certain time circumstances. A factor that might influence my choice to use local over Vim is whether or not the tasks I have to complete are major. If there are many edits I need to perform and errors are likely to happen, I will use local and just copy it over to remote; I can be more precise this way since I have full control over where my cursor is and where/what I can type. 

# The End (Thank you for reading my Lab 4 Report!)