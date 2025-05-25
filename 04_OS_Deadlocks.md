# 4. Deadlocks (Detection, Prevention, Avoidance, Recovery)

---

## What is a Deadlock?

- **Deadlock:** A situation where two or more processes are unable to proceed because each is waiting for a resource held by another.

---

## Necessary Conditions for Deadlock

1. **Mutual Exclusion:** At least one resource is non-sharable.
2. **Hold and Wait:** A process holding at least one resource is waiting for more.
3. **No Preemption:** Resources cannot be forcibly removed from a process.
4. **Circular Wait:** A set of processes are waiting for each other in a circular chain.

---

## Deadlock Handling Strategies

### 1. Deadlock Prevention

- Ensure that at least one of the necessary conditions cannot occur.
    - **Mutual Exclusion:** Not always possible.
    - **Hold and Wait:** Require all resources at once.
    - **No Preemption:** Allow resource preemption.
    - **Circular Wait:** Impose resource ordering.

### 2. Deadlock Avoidance

- System dynamically checks whether allocating a resource leads to deadlock.
- **Banker’s Algorithm:** Checks for safe states before granting resources.
- **Safe State:** System can allocate resources to each process in some order without deadlock.

### 3. Deadlock Detection

- Allow deadlocks to occur, but detect and recover.
- **Resource Allocation Graph (RAG):**
    - Detects cycles in the graph; cycle implies deadlock (for single instance per resource).
- **Detection Algorithm:** For multiple instances, uses matrices (similar to Banker’s algorithm).

### 4. Deadlock Recovery

- **Process Termination:** Abort one or more processes to break the deadlock.
- **Resource Preemption:** Take resources from some processes and give to others.

---

## Example: Resource Allocation Graph

- Nodes: Processes (circles) and resources (squares).
- Edges:
    - Resource → Process: Assignment
    - Process → Resource: Request

---

## Interview Tips

- Be able to define and illustrate all four necessary conditions.
- Know Banker’s algorithm and be able to walk through an example.
- Explain RAG and how cycles mean deadlock.
- Discuss trade-offs between prevention, avoidance, detection, and recovery.

---

## Possible Follow-Up Questions

- Explain the difference between deadlock prevention and avoidance.
- What is a safe state in Banker’s algorithm?
- How can you recover from a deadlock?
- Give a real-world example of deadlock.
  
