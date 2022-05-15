# Task 4.3 
## Part1
#### 1) How many states could has a process in Linux?
- R  running or runnable (on run queue)
- D  uninterruptible sleep (usually IO)
- S  interruptible sleep (waiting for an event to complete)
- T  stopped, either by a job control signal or because it is being traced
- Z  defunct/zombie, terminated but not reaped by its parent

![screen1](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen1.png)
#### 2) Examine the pstree command. Make output (highlight) the chain (ancestors) of the current process.
```
The pstree command shows running processes as a tree.
```
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen2.png)
![screen3](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen3.png)
#### 3) What is a proc file system?
```
/proc is very special in that it is also a virtual filesystem. It's sometimes referred to as a process information pseudo-file system. It doesn't contain 'real' files but runtime system information (e.g. system memory, devices mounted, hardware configuration, etc). 
```
![screen4](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen4.png)
#### 4) Print information about the processor (its type, supported technologies, etc.).
![screen5](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen5.png)
#### 5) Use the ps command to get information about the process. The information should be asfollows: the owner of the process, the arguments with which the process was launched forexecution, the group owner of this process, etc.
![screen6](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen6.png)
#### 6) How to define kernel processes and user processes?
```
For this task, we use the following command:
- ps -N --ppid 2 -p 2  - to display only user processes;
- ps --ppid 2 -p 2 - to display only kernel processes;
```
![screen7](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen7.png)
![screen8](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen8.png)
#### 7) Print the list of processes to the terminal. Briefly describe the statuses of the processes.What condition are they in, or can they be arriving in?
```
For this task, we use the following command:
ps -aux, where:
-a: Shows information about all users
-x: Shows information about processes without terminals
-u: Shows additional information like -f option
So, we will see a column called STAT that displays the process’s status.
Here is a list of the various process statuses and what they mean:

D – Uninterruptible sleep (usually a critical system process, a process that cannot be killed without rebooting)
R – Running or runable (on run queue)
S – Interruptible sleep (waiting for an event to complete)
T – Stopped, either by a job control signal or because it is being traced.
Z – Defunct (“zombie”) process, terminated but not closed by the parent process that created it
W – Ppaging (not valid since the 2.6.xx kernel)
X – Dead (should never be seen)

Additional characters may be seen if in a BSD environment or when using the “stat” modifier with ps:

W – has no resident pages
< – high-priority process
N – low-priority task
L – has pages locked into memory (for real-time and custom IO)
+ – is in the foreground process group
l – is multi-threaded (using Clone_thread, like NPTL pthreads do)
```
![screen9](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen9.jpg)
#### 8) Display only the processes of a specific user.
> Used command: ps -u [username]
![screen10](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen10.png)
#### 9) What utilities can be used to analyze existing running tasks (by analyzing the help for the pscommand)?
![screen11](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen11.png)
#### 10) 
