# Week 1 Lab Report
## Must do
 Install [Visual Studio Code](https://code.visualstudio.com/)
 - Press the download button
 - ![](https://i.imgur.com/wQpju15.png)
 - After downloading the ZIP File you can unzip and install from there
## Steps to access remote server
- Open Visual Studio Code
- Click the terminal button -> Click the new Terminal button
- Obtain your [Course Specific Account](https://sdacs.ucsd.edu/~icc/index.php) (It will be your login-username), you will need your student username and id
- It should look like this 
- ![](https://i.imgur.com/xdt3yPX.png)
- You are looking for the something like looks like this
![Image](https://i.imgur.com/waVaDXR.png)
- While you are searching for your account reset your course-specific password
- In Visual Studio Code type in the terminal `ssh` (your [Course Specific Account](https://sdacs.ucsd.edu/~icc/index.php))ieng6.ucsd.edu 
- ex. cs15lwi23zz@ieng6.ucsd.edu
- When logged in the terminal should end with "Are you sure you want to continue connecting" in where you should say yes
- Your terminal should post this
![Image](https://i.imgur.com/Xxynvvz.png)
- Type in your new course-specific password
- Don't fret, it may seem like your password isn't being typed but it is
- Your terminal should look like this
![Image](https://i.imgur.com/GmEkOMR.png)
# 🎉 Congratulations you have entetered the remote server! 🎉 
Here are some commands you can run for fun!
- `pwd` (Prints your directory)
- `ls -lat` (Gives all the folders in the directory)
- `cat /home/linux/ieng6/cs15lwi23/public/hello.txt` (Prints the hello.txt file)
- `cat /home/linux/ieng6/cs15lwi23/public/hello.txt /home/linux/ieng6/cs15lwi23/public/hello.txt` (Prints the hello.txt twice)
