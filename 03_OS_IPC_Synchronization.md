# 3. Inter-Process Communication (IPC) & Synchronization

---

## What is IPC?

- **Inter-Process Communication (IPC):** Mechanisms that allow processes to communicate and synchronize their actions when running concurrently.

---

## IPC Mechanisms

| Mechanism       | Description                                       | Example Use                        |
|-----------------|---------------------------------------------------|-------------------------------------|
| Shared Memory   | Two+ processes access common memory region        | Fast, but needs synchronization     |
| Message Passing | Processes exchange messages (send/receive)        | Pipe, mailbox, sockets             |
| Pipes           | Unidirectional (or bidirectional) byte stream     | UNIX `|` operator, parent-child     |
| Sockets         | Communication over a network                      | Client-server, web apps            |
| Semaphores      | Signaling mechanism for synchronization           | Producer-consumer, resource access |
| Signals         | Software interrupts to notify a process           | Termination, alarms                |
| Message Queues  | Queue structure for message passing               | Print spooling, job scheduling     |
| Monitors        | High-level synchronization construct              | Used in Java, high-level languages |

---

## Synchronization

- **Goal:** Coordinate access to shared resources to avoid inconsistency (race conditions).

### Race Condition

- Occurs when two+ processes access shared data concurrently and the final result depends on the order of execution.

---

## Critical Section Problem

- **Critical Section:** Code segment where shared resources are accessed.
- **Problem:** Ensure that when one process is in its critical section, no other process is.

### Requirements

1. **Mutual Exclusion:** Only one process in critical section at a time.
2. **Progress:** If no process is in the critical section, others can enter.
3. **Bounded Waiting:** Limit on number of times others can enter before a waiting process.

---

## Synchronization Tools

### 1. Semaphores

- **Binary Semaphore:** Only 0 or 1; similar to a mutex.
- **Counting Semaphore:** Allow arbitrary resource count.
- **Operations:** `wait(P)`, `signal(V)`

### 2. Mutex Locks

- Used to provide mutual exclusion.

### 3. Monitors

- High-level abstraction, encapsulates shared data + procedures.

### 4. Spinlocks

- Busy-waiting lock, avoids context switch but wastes CPU.

---

## Classical Problems

- **Producer-Consumer Problem**
- **Readers-Writers Problem**
- **Dining Philosophers Problem**

---

## Interview Tips

- Be able to explain each IPC mechanism and when to use them.
- Draw/read synchronization code (semaphores, monitors, etc.).
- Explain race conditions and critical section requirements.
- Discuss real-world synchronization bugs.

---

## Possible Follow-Up Questions

- What is the difference between a semaphore and a mutex?
- How does shared memory IPC work? What are its pros/cons?
- Give an example of a race condition.
- How do you avoid deadlock in synchronization?

---

Say "yes" to continue to **4. Deadlocks (Detection, Prevention, Avoidance, Recovery)**!
