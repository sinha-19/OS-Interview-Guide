# 6. File Systems (File Concepts, Allocation, Directory Structure, Access Control)

---

## What is a File System?

- A **file system** organizes and manages files and directories on storage devices.
- Provides operations like create, read, write, delete, and manage access permissions.

---

## File Concepts

- **File:** Named collection of related data stored on secondary storage.
- **File Attributes:** Name, type, size, location, protection, time/date, owner.
- **File Operations:** Create, open, close, read, write, delete, seek, append, truncate.

---

## File Types

- Text files, binary files, executable files, directories, special files (device files).

---

## File Access Methods

- **Sequential Access:** Data accessed in order (e.g., magnetic tapes).
- **Direct (Random) Access:** Data can be read/written in any order (e.g., hard disks).
- **Indexed Access:** Uses an index to access blocks/records.

---

## Directory Structure

- **Single-Level Directory:** One directory for all users/files.
- **Two-Level Directory:** Separate directory per user.
- **Tree-Structured Directory:** Hierarchical (most common; allows subdirectories).
- **Acyclic/General Graph Directory:** Allows shared subdirectories/files (links).

---

## File Allocation Methods

| Method         | Description                                            | Pros/Cons                  |
|----------------|--------------------------------------------------------|----------------------------|
| Contiguous     | Each file occupies a set of contiguous blocks          | Fast, simple; fragmentation|
| Linked         | Each file is a linked list of blocks                   | No fragmentation; slow access|
| Indexed        | Uses an index block to keep track of file blocks       | Fast direct access; overhead|

---

## Free Space Management

- **Bit Vector:** 1 bit per block (0 = free, 1 = occupied)
- **Linked List:** Free blocks linked together
- **Grouping, Counting:** Store free block numbers in special blocks

---

## Access Control

- **File Protection:** Prevent unauthorized access/modification
- **Access Control List (ACL):** Specifies users and their permissions (read, write, execute)
- **User Classes:** Owner, group, others (UNIX model: rwxr-xr--)

---

## Mounting File Systems

- Attaching a file system to a directory structure so it is accessible.

---

## Interview Tips

- Be able to draw and explain directory structures and allocation methods.
- Know how access control works in UNIX vs. Windows.
- Explain advantages/disadvantages of allocation techniques.

---

## Possible Follow-Up Questions

- How does indexed allocation work? What are its pros/cons?
- What is an inode in UNIX file systems?
- Explain the difference between sequential and direct access.
- How does the OS keep track of free disk space?
