# Task 4.1 
### Part 1.
#### 1) Log in to the system as root (or sudo-er). Command used -- ' sudo su '
![screen1](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen1.png)
#### 2) Used the _"passwd"_ command to change the password.
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen2.png)
> With "passwd" command we can change/delete passwords for users, set expiration date/checked the status of passwords.

> Files used by _"passwd"_:
 ```
- /etc/passwd - User account information.
- /etc/shadow - Secure user account information.
- /etc/pam.d/passwd - PAM configuration for passwd.
```
![screen3](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen3.png)
#### 3)For determine the users registered in the system, as well as what commands they execute -- will be used next commands:  
```
- who - shows who is currently logged into the system;
- w - shows who is currently in the system and what he is doing;
- whoami - Prints out the user's UID( the name of the user executing this command.)
- id - prints extended user information (group, uid, gid);
- finger - displays information about the user;
- last - displays a list of all users logged in (and out) the system;
- cat /etc/passwd - displays user accounts information;
- sed 's/:.*//' /etc/passwd - displays only usernames list who logged in the system.
```
##### Let's start practicing::
![screen4](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen4.png)
![screen5](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen5.png)
#### 4) Let's start change personal information about yourself, using for that next comands:
```
chfn - change personal information displayed by 'finger' comand;
```
![screen6](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen6.png)
#### 5) Linux help system. We used "man" command for get help:
```
For examples, used command 'passwd' with some options 
- man passwd
- passwd -aS - This option can be used only with -S and causes show status for all users.
- passwd -S - Display account status information.
```
![screen7](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen7.png)
![screen8](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen8.png)
![screen9](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen9.png)
#### 6) View the contents of files .bash* using commands 'more' and 'less':
![screen10](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen10.png)
![screen11](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen11.png)
![screen12](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen12.png)
![screen13](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen13.png)
#### 7) Last  logon  time  for  all  users. Used the documentation for the finger command.
![screen14](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen14.png)
![screen15](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen15.png)
#### 8) List the contents of the home directory using the 'ls' command.
![screen16](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen16.png)
### Part2
#### 1) The 'tree' command.
![screen17](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen17.png)
#### 2) For determining file type we use following command  '*file*'.
![screen18](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen18.png)
#### 3) Navigating the file system
![screen19](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen19.png)
#### 4) The 'ls' command. Using different keys -- the -l and -a
```
- ls -a will list all files including hidden files (files with names beginning with a dot).
- ls -l gives a long listing of all files.
```
![screen20](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen20.png)
#### 5) For performe the  sequence of operations in this task used next commands:
![screen21](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen21.png)
#### 6) For performe the  sequence of operations in this task used next commands:
![screen22](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen22.png)
![screen23](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen23.png)
```
A hard link is a file that points to the same underlying inode, as another file. In case we delete one file, it removes one link to the underlying inode. 
* command: 'ln file hardlink'
A soft link, is a special kind of file that points to another file. Unlike a hard link, a symbolic link does not contain the data in the target file. It simply points to another entry somewhere in the file system.
* command: 'ln -s file1 symlink1'
So, Hard link contains data in the target file, while soft link doesn’t contain the data and also, when we delete a target file, symbolic links to that file become unusable, whereas hard links preserve the contents of the file.
```
#### 7) Using "locate" utility for find all files that contain the squid and traceroute sequence.
![screen24](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen24.png)
#### 8) We determined which partitions are mounted in the system, as well as the types of these partitions.
![screen25](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen25.png)
#### 9) So next task and let's count the number lines in our file:
![screen26](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen26.png)
#### 10) Next task and we will using the 'find' command for find all files in the /etc directory containing the 'host' character sequence.
![screen27](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen27.png)
#### 11) Listed all objects in /etc that contain the ss character sequence, we also used 'grep' command.
![screen28](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen28.png)
#### 12) Organized a screen-by-screen print of the contents of the /etc directory, used -- 'ls -la /etc | less'
![screen29](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen29.png)
#### 13) 
![screen30](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen30.png)
#### 14) To Identify File Types in Linux we using next:
File types and their symbols in Linux:
```
+--------------+------------------------+
|    Symbol    |      File Types        |
+--------------+------------------------+
|      -       | Regular File           |
|      d       | Directory              |
|      l       | Link File              |
|      c       | Character Device File  |
|      s       | Local Socket File      |
|      p       | Named Pipe File        |
|      b       | Block Device File      |
+--------------+------------------------+
```
###### Method-1:
```
- ls -la | grep ^-
- ls -la | grep ^d
- ls -la | grep ^l
- ls -la | grep ^c
- ls -la | grep ^s
- ls -la | grep ^p
- ls -la | grep ^b
```
![screen31](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen31.png)
###### Method-2:
```
The 'file' command allows to determine various file types in Linux.
```
![screen32](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen32.png)
###### Method-3:
```
The 'stat' command allow us to check file types or file system status.
```
![screen33](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen33.png)
#### 15)
![screen34](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen34.png)
