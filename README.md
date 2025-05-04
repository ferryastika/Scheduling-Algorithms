# [Scheduling Algorithms](https://github.com/PrakharPipersania/Scheduling-Algorithms)

![Language](https://img.shields.io/badge/Language-C-255fcc.svg)&nbsp;
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE)&nbsp;
![Total Tests](https://img.shields.io/badge/Total%20Tests-58%20(All%20Passed)-purple.svg)&nbsp;
![Progress](https://img.shields.io/badge/Progress-100%25-brightgreen.svg)&nbsp;

## Important Variables in Scheduling Algorithm
* Arrival Time (AT): The time when the process arrives in the ready queue
* Burst Time (BT): The CPU time required to finish the process. 
* Completion Time (CT): The time at which the  process finished its execution
* Turn Around Time (TAT): CT - AT
* Waiting Time (WT) = TAT - BT
* 
## Some Popular Process Scheduling Algorithms are:-
* First Come First Served (FCFS) Scheduling
* Shortest Job First (SJN) Scheduling
* Priority Scheduling
* Round Robin(RR) Scheduling
* Highest Response Ratio Next(HRRN) Scheduling

### First Come First Served Scheduling:
In this Algorithm, the Process that requests CPU first is allocated CPU first, i.e., the algorithm is known as first-come, first-served. It is based on the FIFO (First in First Out) queue data structure. When a process is entered in the ready queue, its Process Control Block (PCB) is added to the end of the Queue. When the CPU gets free after a process execution, a new process from the head of the queue is removed and enters the running state.
* Criteria: Arrival Time
* Mode: Non-Preemptive
* Convoy Effect OR Starvation (When the CPU first entertains the process with the highest burst time)

### Shortest Job First Scheduling:
SJF is a preemptive and Non-Preemptive algorithm. It is based on the length of the latter’s next CPU burst. If a process acquired the CPU and execution is going on, a new process with a small CPU burst enters. The CPU is preempted from the current process and will be given to a further process. If two processes have the same length next CPU burst, FCFS scheduling breaks the tie. Shortest Next CPU burst is also an appropriate term for the SJF algorithm because the scheduler continuously examines the next CPU burst's length.
* Criteria: Burst Time
* Mode(Shortest Job First): Non-Preemptive
* Mode(Shortest Remaining Time First ): Preemptive

### Priority Scheduling:
SJF is a simple priority algorithm. We do not consider the smallest next CPU burst; the scheduler considers the priority of processes. The priority is assigned to each process, and the CPU is allocated to the highest priority process. Equal-priority processes are scheduled in FCFS order. Priority can be discussed regarding Lower and higher priorities. Numbers denote it. We can use 0 for lower priority as well as higher priority. There is no hard-and-fast rule to assign numbers to preferences.
* Criteria: Priority
* Mode: Non-Preemptive OR Preemptive

### Round Robin Scheduling
Round Robin Scheduling is an algorithm designed for time-sharing systems. It is similar to FCFS scheduling but adds preemption to switch the processes after a small unit of time, called a time quantum. A time quantum might be 10 to 100 milliseconds.
* How the RR algorithm works: Ready queue is a FIFO queue. The new process will add to the tail of the ready queue and process is removed from the head of queue.The CPU selects a process from the ready queue and sets a timer. After the completion of the time quantum, the process will be preempted, regardless of whether it is completed or not. IF the process is not finished, it will be added to the tail of the queue, and the CPU will select a new process. In this way, the process is going on.
* Criteria: Time Quantum
* Mode: Preemptive
* No Starvation

### Highest Response Ratio Next Scheduling
Highest Response Ratio Next (HRNN) is one of the most optimal scheduling algorithms. This non-preemptive algorithm schedules based on an extra parameter called Response Ratio. A Response Ratio is calculated for each of the available jobs, and the Job with the highest response ratio is given priority over the others.
* Criteria: Response Ratio
* Mode: Non-Preemptive
