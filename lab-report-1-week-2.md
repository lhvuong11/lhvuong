# **LAB REPORT 1**

![Image](gears.jpg)

Hello incoming 15L students!
This blog post will be a tutorial about how to log into your course-speical account on `ieng6` (the UCSD basement server). 

---

## Step 1: *Installing VScode*
Go to [Visual Studio Code](https://code.visualstudio.com/) and download and install it on your device.

> It should look something like this (may differ depending on system/ display settings).

![Image](vscode.jpg)



## Step 2: *Remotely Connecting*
Here we will be connecting VScode to a remote device over the Internet!

Since I'm operating on Windows, I'll be giving instructions for Window users (my apologies to other users reading this). 

1. Install [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) using the link attached.
2. Look up your course-specific account for CSE15L : [CSE15L-Account](https://sdacs.ucsd.edu/~icc/index.php)
3. Open your terminal in VSCode using the Terminal menu and type in a `ssh` command replacing my account with your own.

    ``` $ ssh cs15lwi22akz@ieng6.ucsd.edu```

    Continue connecting by pressing "yes", enter your password and you should get something like this
    > ![Image](terminal.jpg)

Congrats! Your terminal is now connected to a computer in the UCSD CSE basement! 



## Step 3: *Trying Some Commands*
Now that everything's set up, let's try running some commands!
Here are some commands to try:
- `cd`
- `cd ~`
- `ls` 
- `ls -lat`
- `pwd`
- `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`
- `cat /home/linux/ieng6/cs15lwi22/public/hello.txt`

> Here's an example of how mine looks:
![Image](commands.jpg)



## Step 4: *Moving Files with scp*
 *A key step in working remotely is being able to copy files between computers.*

 We'll be copying a file from our computer to a remote computer in this exercise by using a command called `scp`, which stands for secure copy.

 1. Create a file on your computer called `WhereAmI.java` with the following contents in it:
     ```
     class WhereAmI { 
         public static void main(String[] args) {
             System.out.println(System.getProperty("os.name"));
             System.out.println(System.getProperty("user.name"));
             System.out.println(System.getProperty("user.home"));
              System.out.println(System.getProperty("user.dir"));
            }
        }
    ```
    2. In the terminal from the directory where `WhereAmI.java` was made, run the command using: (but with your username)
    ``` scp WhereAmI.java cs15lwi22zakz@ieng6.ucsd.edu:~```
    3. Enter your password!
    Now, log into `ieng6` again using the `ssh` command and use `ls`.
        > You should see something along these lines!
        ![Image](scp.jpg)



## Step 5: *Setting an SSH Key*




## Step 6: *Optimizing Remote Running*

