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
![screen11](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen11.jpg)
#### 10) What information does top command display?
```
The top command (table of processes) displays the processor activity of your Linux box and also displays tasks managed by the kernel in real-time.
PID: Process ID.
USER: The owner of the process.
PR: Process priority.
NI: The nice value of the process.
VIRT: Amount of virtual memory used by the process.
RES: Amount of resident memory used by the process.
SHR: Amount of shared memory used by the process.
S: Status of the process. (See the list below for the values this field can take).
%CPU: The share of CPU time used by the process since the last update.
%MEM: The share of physical memory used.
TIME+: Total CPU time used by the task in hundredths of a second.
COMMAND: The command name or command line (name + options).
```
#### 11) Display the processes of the specific user using the top command.
> used command: top -u ubuntu
![screen12](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen12.png)
#### 12) What interactive commands can be used to control the top command? Give a couple of examples.
```
The 'TOP' utilite have a many keys for interactive commands, we briefly describe some one:
n - set max number of tasks displayed
w - write current  settings to the config file
ESC - update
k - kill process
u - filter by user
h - help
```
#### 13) Sort the contents of the processes window using various parameters (for example, theamount of processor time taken up, etc.)
> So, when we stert 'top' command we can press 'f' to enter the interactive menu and we can interactively choose which column to sort on:
![screen13](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen13.png)
![screen14](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen14.png)
#### 14) Concept of priority, what commands are used to set priority?
> We can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority. Renice command will modify the scheduling priority of a running process. A nice value of -20 represents highest priority, and a nice value of 19 represent least priority for a process, for decrease the priority we can use a regular user, but for increase - we must have a superuser rights.
- Example: nice -n 19 top
![screen15](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen15.png)
- Example: sudo renice -n -12 -p 4621
![screen16](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen16.png)
![screen17](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen17.png)
![screen18](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen18.png)
#### 15) Can I change the priority of a process using the top command?If so, how?
> If we wiil use 'top' command with key 'r' we can make changes the priority of a process. When 'top' command start press f and enter PID after that enter new value of priority.
- Example: 
![screen19](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen19.png)
![screen20](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen20.png)
![screen21](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen21.png)
#### 16) Examine the kill command. How to send with the kill commandprocess control signal? Give an example of commonly used signals.
![screen22](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen22.png)
- kill -l :To display all the available signals we can use below command option:
![screen23](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen23.png)
- Example:
```
SIGINT - Interrupt (request termination) of the process.
SIGKILL - Force termination of the process 
SIGTERM - Request Termination of the process.
SIGCONT - continue process.
SIGTSTP - Stop (suspend) the process.
```
![screen24](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen24.png)
#### 17) Commands jobs, fg, bg, nohup. What are they for? Use the sleep, yes command todemonstrate the process control mechanism with fg, bg.
- jobs: Display a list of the jobs with their status
- fg: Move a background job into the foreground
- bg: Resume suspended jobs by running them as background jobs
- nohup: let to save started process after closing terminal session.
![screen26](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen26.png)

## Part2
#### 1) Check the implementability of the most frequently used OPENSSH commands in the MSWindows operating system. (Description of the expected result of the commands +screenshots: command –result should be presented)
![screen27](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen27.png)
![screen28](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen28.png)
![screen29](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen29.png)
```
Using SCP
SCP uses the same security mechanism as SSH, but rather than running commands, it is most commonly used to securely copy files from one system to another:
scp source user@host:/location
```
![screen30](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen30.png)
#### 2)  Implement basic SSH settings to increase the security of the client-server connection (at least)
![screen31](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen31.png)
#### 3) List the options for choosing keys for encryption in SSH. Implement 3 of them.
```
Choosing an Algorithm and Key Size
ssh-keygen -t rsa -b 4096
ssh-keygen -t dsa 
ssh-keygen -t ecdsa -b 521
ssh-keygen -t ed25519
```
![screen32](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen32.png)
#### 4) Implement port forwarding for the SSH client from the host machine to the guest Linuxvirtual machine behind NAT.
![screen33](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen33.png)
![screen34](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen34.png)
#### 5*) Intercept (capture) traffic (tcpdump, wireshark) while authorizing the remote client on theserver using ssh, telnet, rlogin. Analyze the result.
![screen35](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen35.png)
