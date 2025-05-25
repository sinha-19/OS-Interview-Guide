# 7. I/O Management & Disk Scheduling

---

## I/O Management Overview

- **Goal:** Manage all input/output devices (disks, printers, network, etc.) and coordinate data transfer between hardware and processes.
- **Device Drivers:** Software modules that control hardware devices and provide a standard interface to the OS.

---

## I/O Techniques

- **Programmed I/O:** CPU actively waits and controls I/O operation (busy waiting).
- **Interrupt-Driven I/O:** Devices interrupt the CPU when they are ready, freeing the CPU for other work.
- **Direct Memory Access (DMA):** Data transferred directly between memory and device, bypassing CPU for bulk transfers.

---

## Disk Structure

- **Disk:** Consists of platters, tracks, sectors, and cylinders.
- **Seek Time:** Time to move the disk arm to the desired track.
- **Rotational Latency:** Time waiting for the disk to rotate to the right sector.
- **Transfer Time:** Time to transfer data.

---

## Disk Scheduling Algorithms

| Algorithm      | Description                                                      | Performance   |
|----------------|------------------------------------------------------------------|---------------|
| FCFS           | First-Come, First-Served; simple but not always efficient        | Poor          |
| SSTF           | Shortest Seek Time First; closest request next                   | Better, can starve far requests |
| SCAN           | Elevator algorithm; moves in one direction, services requests, then reverses | Good, fair   |
| C-SCAN         | Circular SCAN; services in one direction, jumps to start         | Uniform wait  |
| LOOK/C-LOOK    | Like SCAN/C-SCAN but only goes as far as the last request        | Optimized     |

---

## Example: SCAN (Elevator Algorithm)

- Disk arm moves back and forth, servicing all requests in one direction before reversing.

---

## RAID (Redundant Array of Independent Disks)

- **RAID:** Combines multiple disks to improve performance and/or reliability.
- **Common Levels:**
    - **RAID 0:** Striping, no redundancy, high performance.
    - **RAID 1:** Mirroring, high reliability.
    - **RAID 5:** Block-level striping with distributed parity (balance of performance and fault-tolerance).

---

## Buffering, Caching, Spooling

- **Buffering:** Temporary storage for data being transferred.
- **Caching:** Storing frequently accessed data for fast access.
- **Spooling:** Staging data for devices that cannot accept interleaved data streams (e.g., printers).

---

## Interview Tips

- Be able to draw and explain disk scheduling (with seek sequences).
- Know trade-offs between different scheduling algorithms.
- Explain DMA vs. interrupt-driven I/O.
- Discuss RAID levels and their use-cases.

---

## Possible Follow-Up Questions

- What is the difference between buffering and caching?
- How does SSTF differ from FCFS?
- Explain the working of DMA.
- What are the advantages of RAID 5?
