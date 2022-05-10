# Task 4.2 
#### 1) Analyze the structure of the /etc/passwd and /etc/group file
![screen1](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen1.png)
```
'cat /etc/passwd' - we are see all users accounts in system, for example, we took the one entry from the command output.
'ubuntu:x:1000:1000:Ubuntu:/home/ubuntu:/bin/bash'
where: 
- ubuntu - login(username);
- x - password;
- 1000 - UID (user ID);
- 1000 - GID (group ID);
- Ubuntu - gecos field (It is typically used to record general information about the account or its user(s) such as their real name and phone number.)
- /home/ubuntu - home directory;
- /bin/bash - default shell.
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
```
- what users exist on the system? 
* Superuser: root;
* Ordinary users: Standard users have limited permissions to the operating system;
* Pseudo user.
Specify several pseudo-users, howto define them?
Pseudo user: To facilitate system management, meets the requirements of the owner of the corresponding system process file, Pseudo user cannot log in, UID value 1 - 499
```
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen2.png)
```
The /etc/group is a stores group information or defines the user groups i.e. it defines the groups to which users belong. There is one entry per line, and each line has the following format (all fields are separated by a colon (:).
For example, we can take one entry in our file, 
'cat /etc/group' where:
'adm:x:4:syslog,ubuntu'
- adm - group_name;
- x - Password;
- 4 - Group ID (GID);
- syslog,ubuntu - Group List.
```
#### 2) What are the uid ranges? What is UID? How to define it?
```
Unix-like operating systems identify a user by a value called a user identifier (UID).
A UID (user identifier) is a number assigned by Linux to each user on the system. This number is used to identify the user to the system and to determine which system resources the user can access.
The 'id' command in Linux will display the UID, GID and groups current user belongs to;
```
#### 3) What is GID? How to define it?
```
GID - unique identifier of the group within the system to which the user belongs.
The 'id' command in Linux will display the UID, GID and groups current user belongs to;
```
#### 4) How to determine belonging of user to the specific group?
```
We can use file /etc/passwd and also we can determine usergroups with command "groups", for example:
ubuntu@ip-172-31-24-52:~$ groups ubuntu
ubuntu : ubuntu adm dialout cdrom floppy sudo audio dip video plugdev netdev lxd
```
#### 5) What are the commands for adding a user to the system? What are the basic parameters required to create a user?
![screen3](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen3.png)
#### 6) How do I change the name (account name) of an existing user?
> For change the name (account name) of an existing user we can use next command: **usermod -l user3 user2**; 
#### 7) What is skell_dir? What is its structure?
```
Directory /etc/skel/ (skel is derived from the “skeleton”) is used to initiate home directory when a user is first created.
```
![screen4](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen4.png)
#### 8) How to remove a user from the system (including his mailbox)?
```
Use next command: 'userdel -r user4':
where 
-r : Remove Linux user account including home directory and mail spool;
```
![screen5](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen5.png)
#### 9) What commands and keys should be used to lock and unlock a user account?
```
lock users account:
Use the command “passwd -l username”.
or
Use the command “usermod -L username”.

unlock users account:
Use the command “passwd -u username”.
or
Use the command “usermod -U username”.
```
#### 10) How to remove a user's password and provide him with a password-free login for subsequent password change?
![screen6](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen6.png)

