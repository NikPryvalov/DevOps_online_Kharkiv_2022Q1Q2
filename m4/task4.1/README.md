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
1) 
