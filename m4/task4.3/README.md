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
- The pstree command shows running processes as a tree.
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen2.png)
![screen3](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen3.png)
#### 3) What is a proc file system?
```
/proc is very special in that it is also a virtual filesystem. It's sometimes referred to as a process information pseudo-file system. It doesn't contain 'real' files but runtime system information (e.g. system memory, devices mounted, hardware configuration, etc). 
```
![screen4](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m4/task4.3/screen/screen4.png)
#### 4) 
