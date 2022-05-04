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
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.2/screen/screen2.png)
