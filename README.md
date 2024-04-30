# Lock-free data structures

## What's the issue?

When developing a multithreaded low-latency application, 
opting for traditional synchronization primitives like semaphores,mutexes (binary semaphores), and conditional variables may not be the most efficient choice.
Their usage can lead to heightened latencies due to avoidable context switches. 
It is imperative to actively minimize these switches to uphold optimal performance standards

## What is a lock-free algorithm?  

A lock-free algorithm is a concurrent algorithm designed to enable progress by multiple threads without the need for traditional locks or blocking synchronization mechanisms like mutexes or semaphores.
In a lock-free algorithm, threads can continue making forward progress even in the presence of contention, without any thread being blocked indefinitely by another

## Why lock free? 

- No Global Locks: Lock-free algorithms do not rely on global locks for synchronization to prevent data races.
- Non-Blocking: Threads in a lock-free algorithm do not prevent each other from making progress, even during contention.
- Guaranteed Progress: Every thread running a lock-free algorithm will eventually complete its operation, regardless of other thread activities.
- Data Structure Safety: Lock-free algorithms ensure the integrity of shared data structures in a concurrent environment.
- Scalability: Lock-free algorithms often exhibit better scalability than lock-based approaches in highly concurrent scenarios.
