**Logging Into a Course-Specific Account on ieng6 Server**

The bullet points below indicate topics that will be covered in properly setting up on an ieng6 server
* Installing VSCode

1. Click the link to download [VSCode](https://code.visualstudio.com/)

When VSCode is downloaded successfully, a screen like the image below should popup

![VSCode Homepage](VSCodeHomepage.png)


You are allowed to use any other IDE's, however, VSCode is probably the easiest and best IDE to use.
* Remotely Connecting

Before connecting to the server, you will need a username.

You can find your own personal username for CSE15L from the link below:

[Course-Specific Username](https://sdacs.ucsd.edu/~icc/index.php)

Open VSCode, and open a new Terminal(Ctrl or Command + `, or use the Terminal → New Terminal menu option)

When the Terminal opened up, there should be a '$' after your directory

Writing the command to connect to the ssh server
![ssh](ssh.png)

Replace the zz with your own course-specific username. It should be 3 letters, for example cs15lwi22abc. Once, you click enter, it will prompt you to enter a password. This password is the same password that you use to log in to Canvas or mytritonlink.

When you logged in successfully, it will show you a cluster status such as the image below.
![Terminal](TerminalLogIn.png)

Once you have this on your terminal, you have successfully connect to the ieng6 server. The next steps will be running some basic command lines inside the server by using the terminal.
* Basic Command Lines

Some basic command lines:

1. cd = change directory
2. ls = list directory
3. pwd = prints working directory
4. mkdir = make directory
5. cp = copy

There are other command lines that are more advanced
1. cd ~ = open the home directory
2. ls -a =
3. ls -lat =

Below is an example of running the basic command line on the server

![basicCommand](BasicCommand.png)
As you can see, I used ls to list the directories in the home directories, but there's only perl5 so I created a direcotry called "Lab" by using the mkdir command line. Now, when I used ls again, it showed both Lab and perl5.

* Moving Files with scp
* Setting an ssh key
* Optimizing Remote Running