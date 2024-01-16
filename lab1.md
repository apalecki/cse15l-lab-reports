# Lab Report 1

## `cd` command

Using the command without arguments:
![Image](lab1-1.jpeg)
* Working directory was `/home`
* Having no arguments with the `cd` command lead to nothing happening. A new command line opened with there being no changes to anything related to the directory.
* The output was not an error.


Using the command with a path to a directory as an argument: 
![Image](lab1-2.jpg)
* Working directory was `/home`
* Having a directory as the argument for the `cd` command lead to the working directory being changed from `/home` to `/home/lecture1`.
* The output was not an error.


Using the command with a path to a file as an argument:
![image](lab1-3.jpg)
* Working directory was `/home/lecture1`
* Having a file as an argument for the `cd` command lead to the terminal spitting out the error `bash: cd: Hello.java: Not a directory`.
* The output was an error because the `cd` command only works on changing directory so if we attempt to put in a file as the argument it will get upset with us.

## `ls` command

Using the command without arguments:
![Image](lab1-4.jpg)
* Working directory was `/home`
* Having no arguments with the `ls` command lead to the all the files and folders in the `/home` directory being printed (in this case there was only the `lecture1` folder).
* The output was not an error


Using the command with a path to a directory as an argument:
![Image](lab1-5.jpg)
* Working directory was `/home`
* Having a directory as the argument for the `ls` command lead to all the contents of the directory being printed out.
* The output was not an error.

Using the command with a path to a file as an argument:
![Image](lab1-6.jpg)
* Working directory was `/home/lecture1`
* Having a file as the argument for the `ls` command lead to the file we used as the argument being printed out (in this case the `Hello.java` was printed out).
* The output was not an error.
