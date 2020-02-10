### Scheduling Algorithms
**Out:** February 10, 2020    
**Due:** February 24, 2020, at 11:59pm

This project involves implementing several different process scheduling algorithms. 
The scheduler will be assigned a predefined set of tasks and will schedule the tasks based on the selected scheduling 
algorithm. Each task is assigned a priority and CPU burst. The following scheduling algorithms will be implemented:

* First-come, first-served (FCFS), which schedules tasks in the order in which they request the CPU.
* Shortest-job-first (SJF), which schedules tasks in order of the length of the tasks’ next CPU burst.
* Priority scheduling, which schedules tasks based on priority. 
* Round-robin (RR) scheduling, where each task is run for a time quantum (or for the remainder of its CPU burst).
* Priority with round-robin, which schedules tasks in order of priority and uses round-robin scheduling for tasks with equal priority.

Priorities range from 1 to 10, where a higher numeric value indicates a higher relative priority. 
For round-robin scheduling, the length of a time quantum is 10 milliseconds.

## Implementation
The implementation of this project may be completed in C and program files supporting the project are 
provided in the `StartKit-Code` folder. These supporting files read in the schedule of tasks, 
insert the tasks into a list, and invoke the scheduler. The schedule of tasks has the form 
`[task name][priority][CPU burst]`, with the following example format:
    T1, 4, 20 
    T2, 2, 25 
    T3, 3, 25 
    T4, 3, 15 
    T5, 10, 10
Thus, task T1 has priority 4 and a CPU burst of 20 milliseconds, and so forth. It is assumed that all tasks arrive at 
the same time, so your scheduler algorithms do not have to support higher-priority processes preempting processes with 
lower priorities. In addition, tasks do not have to be placed into a queue or list in any particular order.





Completing this project will require writing the following C files:

schedule_fcfs.c
schedule_sjf.c
schedule_rr.c
schedule_priority.c
schedule_priority_rr.c

The supporting files invoke the appropriate scheduling algorithm. 

For example, to build the FCFS scheduler, enter

make fcfs

which builds the fcfs executable file.