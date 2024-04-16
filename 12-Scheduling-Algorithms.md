```TODO: FINISH THIS CHAPTER```
# Dispatching Algorithms
Determines task execution order and efficiency

## First Come First Served (FCFS)
- Processes chose from the fron of the ready queue in order of arrival
- Better for long processes, but may lead to poor turnaroud due to *convoy effect*
- Not ideal for short processes, as it can cause delays in execution

## Shortest Process Next (SPN)
- Also known as *Shortest Job First (SJF)*
- Selects shortest job in the ready queue for execution
- Optimal average Turnaround Time (TAT) **if all jobs arrive together**...
- ...but risk of starvation for long processes
- **Assumes** knowledge of job lengths

## Shortest Remaining Time (SRT)
- Preemptive version of SPN
- Prioritises process with shortest remaining process time
- Good turnaround time
- Avvoids bias to longer processes
- Low overhead
- Need estimate of required processing time

## Round Robin
- Also known as time slicing
- FCFS with clock based preemption
- Each process gets a time slice (quantum) to execute
	- Smaller quantum reduces response time
	- Too small can increase overhead
- Favours processor-bound processes

## Virtual Round Robin
- Involves multiple process queues
- I/O queues feed into aux queue
	- Aux queue is prioritised over ready queue for process execution
- i.e., Helps manage process priorities efficiently in a multi-process environment

## Highest Response Ratio Next
$R = \frac{w+s}{s}$

$w=$ Time spent waiting

$s=$ Expected service time
- Selects the ready process with the largest value of response ratio, $R$
- Favours shorter jobs and brings lognger jobs to the top based on age
- i.e., Helps minimise waiting time by prioritising processes with a higher expected service time

## Fair-Share Scheduling
- Ensures each user or process group get as a fair share of processor time
- **up to now**: homogenous pool of processes
- **multi-user environment**: groups of user processos
- Ensure each user gets "fair share" of processor time
- Dynamic priority adjustments on usage within group
- **Networking**: *Weighted fair queueing*
- Implemented in Linux with the Completely Fair Scheduler (CFS) to maintain fairnes sin resources allocation

# Multiprocessor Scheduling