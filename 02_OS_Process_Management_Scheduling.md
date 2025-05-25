# 2. Process Management & Scheduling

---

## What is a Process?

- **Process:** A program in execution (not just code, but code + data + resources + state).
- **Process Control Block (PCB):** Data structure storing process information (PID, state, registers, etc.).

---

## Process States

| State        | Description                         |
|--------------|-------------------------------------|
| New          | Being created                       |
| Ready        | Waiting to be assigned to CPU       |
| Running      | Instructions being executed         |
| Waiting      | Waiting for some event (I/O, etc.)  |
| Terminated   | Finished execution                  |

**State Transition Diagram:**
```
New → Ready → Running → (Waiting ↔ Ready) → Terminated
```

---

## Process vs. Thread

- **Process:** Independent, own memory space.
- **Thread:** Lightweight process, shares memory with parent process, faster context switching.

---

## Context Switching

- The process of saving the state of a running process and loading the state of another.
- Necessary for multitasking and CPU sharing.
- Involves overhead.

---

## Scheduling

### Scheduling Queues

- **Job Queue:** All processes in the system.
- **Ready Queue:** Processes in memory, ready to execute.
- **Device Queue:** Waiting for I/O device.

---

### CPU Scheduling Algorithms

| Algorithm              | Description & Characteristics                                      |
|------------------------|--------------------------------------------------------------------|
| FCFS (First-Come, First-Served) | Simple, non-preemptive, may lead to convoy effect         |
| SJF (Shortest Job First)| Shortest process first, optimal for minimal average waiting time  |
| Priority Scheduling    | Each process assigned priority; higher runs first                  |
| Round Robin (RR)       | Each process gets a time quantum, preemptive                      |
| Multilevel Queue       | Multiple queues by process type                                    |
| Multilevel Feedback Queue | Processes can move between queues                               |

---

### Scheduling Criteria

- **CPU Utilization:** Percent of time CPU is busy.
- **Throughput:** No. of processes completed per unit time.
- **Turnaround Time:** Time from submission to completion.
- **Waiting Time:** Total time a process spends in ready queue.
- **Response Time:** Time from request to first response.

---

## Interview Tips

- Draw and explain process state diagrams.
- Know difference between process/thread.
- Practice scheduling algorithm problems (Gantt charts, waiting time, etc.).
- Be able to compare algorithms on starvation, fairness, and overhead.

---

## Possible Follow-Up Questions

- What is context switching? Why is it expensive?
- Which scheduling algorithm is used in Linux?
- What is starvation? How to avoid it?
- How is preemptive scheduling different from non-preemptive?
