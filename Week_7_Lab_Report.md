# Lab Report 4
This lab report revolves around Lab 7 of week 7's competition.  
It's the competition's step 4-9.
## Step 4
I used ssh cs15lwi23auu@ieng6.ucsd.edu in order to login to the remote server.  
This is done without needing a password.  
## Step 4.1
In order to do this without the password you need to first type in ssh-keygen, which should look like
![](https://i.imgur.com/EAL5r9Q.png)
Remember where your public key is saved. Mine is saved in /Users/hallushination/.ssh/id_rsa.pub
## Step 4.2
Log in to the remote ieng6 course account.
![](https://i.imgur.com/yukijno.png)
## Step 4.3
Type in `mkdir .ssh` to create a ssh directory.
![](https://i.imgur.com/znn8B8t.png)
It was already made on my mac so it had no new effect.
## Step 4.4
Exit the remote server via the command `exit`.
## Step 4.5
You create a new file and save it to authorized_keys.txt by using  
`cat /Users/hallushination/.ssh/id_rsa.pub >  authorized_keys.txt`
## Step 4.6
You then run `scp <path to your public SSH key> cs15lwi23__@ieng6.ucsd.edu:~/.ssh/authorized_keys` on your local computer.  
For me it would be
![](https://i.imgur.com/3oP2B60.png)
Now I can log-in without my password on my local computer.
## Step 4.7
Now I ran `cat /Users/hallushination/.ssh/id_rsa.pub` and <ctrl+c> my ssh key in order to later connect my github and local computer. 
## Step 4.8
You have to go to [github](https://github.com) and enter your settings.  
![](https://i.imgur.com/nyMXco6.png)
## Step 4.9
In the settings there should be a button that looks like the following
![](https://i.imgur.com/uptC8PF.png)
## Step 4.91
You create a new key with any title with the key type of Authentification Key and add your ssh-key like the following
![](https://i.imgur.com/T4ky6t5.png)
## Step 4.92
You can now type in `ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts` and `ssh -T git@github.com` to see your connection to the account on the remote server
![](https://i.imgur.com/tsZKlLS.png)
## Step 5
Now the actual competion steps.  
It starts off with `git clone git@github.com:JacksonYangUCSD/lab7.git` instead of the https link.  
This only works bcause the ssh key connects my github to the remote server.
## Step 6
To test the files legitimacy I used junit.  
First I had to get to the directory, using `cd lab7` then 
I pressed <up> 8 times and pressed <enter>
Then I pressed <up> 8 times again and pressed <enter>
  In order to get  
  ![](https://i.imgur.com/KLJ5XzD.png)
## Step 7
  Now to fix the file I typed in `ls` to make sure I was in the right directory and proceeded to type in `nano ListExamples.java`.  
  Which brought me in a screen like this.  
  ![](https://i.imgur.com/BgUFaQK.png)
  I then pressed <down> 42 times and <right> 12 times to get to the issue.  
  Then I fixed the type with <delete><insert 2><ctrl+x><y><enter> 
## Step 8
  To run the tests again I pressed <up> 11 times to get to `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and pressed <enter>.  
  Then I pressed <up> 11 times again to get `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTest` 
  and pressed <enter>. Which then showed up as
  ![](https://i.imgur.com/ZTCKgyy.png)
 ## Step 9
  I first used `git add ListExamples.java`.  
  Followed by a `git commit`
  Which brought up a screen like ![](https://i.imgur.com/JsY5bmV.png)
  Where I had typed "Replaced index1 with index2 to fix the infinite loop."  
  Then I got out of the screen by pressed <shift+z> <shift+z>.  
  Then it was followed with a `git push`.  Which looks like
  ![](https://i.imgur.com/5aOc7Be.png)
  
  
