# afs_buf
A high-performance user-space buffer cache with an adaptive read-ahead engine and O_DIRECT scatter-gather I/O.

This is an educational project aimed at improving my understanding and expertise of storage subsystems like the buffer cache in DRAM which serves file data in nanoseconds without having to perform operations on the backing SSD/RAID storage, and the Read-Ahead Engine which aims to reduce read latency drastically for sequential read worklaods.


afs_buf is a lightweight, high-throughput user-space buffer cache and adaptive read-ahead engine written in C/C++. Designed for kernel-bypass and O_DIRECT storage workloads, it manages fixed 4 KB memory slabs carved from a contiguous pre-allocated arena, eliminating dynamic allocation latency and heap fragmentation. It features a lock-sharded hash table, concurrent per-buffer state synchronization, and an access-pattern detector that dynamically scales prefetch windows to hide storage latency on streaming reads while avoiding cache pollution during random I/O.

