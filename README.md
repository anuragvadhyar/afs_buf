# afs_buf
A high-performance user-space buffer cache with an adaptive read-ahead engine and O_DIRECT scatter-gather I/O.

This is an educational project aimed at improving my understanding and expertise of storage subsystems like the buffer cache in DRAM which serves file data in nanoseconds without having to perform operations on the backing SSD/RAID storage, and the Read-Ahead Engine which aims to reduce read latency drastically for sequential read worklaods.
