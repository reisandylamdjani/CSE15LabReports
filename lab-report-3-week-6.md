# **Lab Report 3**
# Streamlining ssh Configuration
For this part of the assignment, I have to open the config files using any text editor. In my case, I used vim to edit the file. Below is an image of the finished file after adding the Host and alias.

![configFile](configFile.png)

I used the alias `ieng6` for my example.

Once I have edited and saved my config file. I ran the `ssh` command using the `ieng6`. The image below will give an example of that.

![sshLogging](sshLogging.png)

From this, I just have to create a new file on my computer so that I can copy it using the `scp` command to my account using the alias `ieng6`. Below is an example of what the correct output would be if everything is done correctly.

![scpCommand](scpCommand.png)

Based on the image above, you can see that the `helloWorld.java` file wasn't listed in the home directory yet, but once I copied it into the account, it showed up.

# Setup Github Acces from ieng6
For this part of the Group Choice, we want to understand that we can also `commit` and `push` from the command line. However, in order for us to do that, we need to use a token-based mechanism such as SSH keys.

Some things that we will be doing is creating an SSH keys, if you don't already have one, and putting the public key in our GitHub account.

We will create an SSH keys in our `ieng6` server so that we can also run the command lines while we are logged in into the server. Creating the key is the same as usual, using `ssh-keygen`.

I wanna show images of where the public key is stored on Github and my user account

![sshGit](sshGit.png)

![sshPubPri](sshPubPri.png)

The public key is under the name `id_rsa.pub` and the private key is under the name `id_rsa`.

The image below will show the result of successfully adding, committing, and pushing the changes in the file.

![successPush](successPush.png)

This is the link for the [successful commit](https://github.com/reisandylamdjani/markdown-parser/commit/94a7ac6ba20e167c41cd0f1f0b777c6aea73f5cc).


# Copy Whole Directories with `scp -r`
The first image that I will show is when I copied the whole markdown-parser directory to my `ieng6` account.

![scpWhole](scpWhole.png)

Once I have copied the whole directory, I was able to compile and run the test successfully on the ssh server.

![sshOutput](sshOutput.png)

The last step of this process is showing the process of running the whole command in one line.

![oneLineFirst](oneLineFirst.png)

![oneLineSecond](oneLineSecond.png)
