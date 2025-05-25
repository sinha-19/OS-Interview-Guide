# 5. Memory Management (Paging, Segmentation, Virtual Memory)

---

## Memory Management Overview

- **Goal:** Efficiently allocate and manage main memory for processes.
- Ensures processes have enough memory, protects memory spaces, and maximizes CPU/memory utilization.

---

## Contiguous vs. Non-Contiguous Allocation

- **Contiguous:** Each process occupies a single, continuous memory block.
    - Simple but causes fragmentation.
- **Non-Contiguous:** Memory is divided into fixed (paging) or variable (segmentation) blocks.

---

## Paging

- **Paging:** Memory is divided into fixed-size blocks (**frames** in RAM, **pages** in process).
- **Page Table:** Maps logical (virtual) pages to physical frames.
- **Address Translation:** CPU generates logical address → page number + offset → translated to physical address.

**Pros:** Eliminates external fragmentation  
**Cons:** Page table overhead, internal fragmentation possible

---

## Segmentation

- **Segmentation:** Memory divided into variable-size segments (code, data, stack, etc.).
- **Segment Table:** Maps segment numbers to physical memory locations.
- Logical address = (segment number, offset).

**Pros:** Better models user's view, less internal fragmentation  
**Cons:** External fragmentation, complex allocation

---

## Virtual Memory

- **Virtual Memory:** Processes can use more memory than physically available by swapping pages/segments in/out from secondary storage (disk).
- **Demand Paging:** Load pages into memory only when needed (page fault triggers load).
- **Page Replacement Algorithms:**
    - **FIFO:** Oldest page replaced
    - **LRU:** Least recently used page replaced
    - **Optimal:** Replace page that won’t be used for the longest time
    - **Clock/Second Chance:** Circular buffer with reference bits

---

## Thrashing

- **Thrashing:** Excessive paging/swapping causing CPU to spend more time swapping than executing processes.
- Caused by too little memory or poor page replacement.

---

## Fragmentation

- **Internal Fragmentation:** Wasted space within allocated memory blocks (paging).
- **External Fragmentation:** Free memory exists but is not contiguous (segmentation, contiguous allocation).

---

## Interview Tips

- Draw paging/segmentation diagrams; explain address translation.
- Work through page replacement algorithm examples.
- Know difference between internal/external fragmentation.
- Explain how virtual memory enables multiprogramming.

---

## Possible Follow-Up Questions

- What is the difference between paging and segmentation?
- How does the LRU page replacement algorithm work?
- What is a page fault?
- How does virtual memory improve system performance?
