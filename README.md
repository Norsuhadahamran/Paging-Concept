# Paging-Concept

## Core Concepts of Paging
1) Paging as a memory management scheme:

- A technique that allows processes to use more memory than physically available

- Enables efficient memory allocation by dividing memory into fixed-size units

2) Virtual memory division:

- Virtual address space is divided into fixed-size pages (typically 4KB)

- Provides each process with the illusion of a large, contiguous memory space

3) Physical memory division:

- Physical RAM is divided into frames of the same size as pages

- Frames hold the actual data that pages map to

4) Page table role:

- Data structure that maps virtual page numbers to physical frame numbers

- Maintained by the operating system for each process

- May include additional information (permissions, dirty bits, etc.)

5) Address translation:

- Converts logical (virtual) addresses to physical addresses

- CPU's Memory Management Unit (MMU) handles this translation

- Involves splitting addresses into page number and offset components

6) Page faults and handling:

- Occur when a requested page isn't in physical memory

- Triggers an interrupt that the OS handles by:
  - Locating the page on disk
  - Loading it into a free frame
  - Updating the page table
  - Restarting the interrupted instruction
