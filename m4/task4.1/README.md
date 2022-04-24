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
![screen6](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.1/screen/screen6.png)
