# Multi-threaded File Server & Client

Due to academic integrity, the project source code and detailed report are private. This public summary outlines the core objectives, challenges, and achievements. Code/reports cannot be shared, even on request.

## Project Overview

This project involved designing and implementing a scalable, multi-threaded file server and client system in C, using sockets and POSIX threads. The system is based on a custom, HTTP-like protocol for transferring files between a server and multiple clients. The goal was to build robust, concurrent networked applications that efficiently handle multiple simultaneous file transfer requests.

## Problem Statement

- Develop a server that can serve static files to clients over a network using a custom protocol.
- Implement a client capable of requesting and downloading files from the server.
- Extend both server and client to support concurrent operations using a boss-worker (thread pool) model.
- Ensure correctness, efficiency, and robustness in the presence of multiple simultaneous requests.

## High-Level Design

- **Socket Programming:** Both server and client use low-level TCP sockets for communication.
- **Custom Protocol:** The GetFile protocol defines request/response formats for file transfer, including error handling for invalid requests or missing files.
- **Concurrency:** The server employs a thread pool (worker threads) to handle multiple client requests in parallel, coordinated by a boss thread that accepts connections and dispatches work.
- **Synchronization:** Shared resources (such as the work queue) are protected using mutexes and condition variables to prevent race conditions and ensure thread safety.
- **Modular Design:** The project is structured into reusable libraries for client and server logic, with clear interfaces and callback mechanisms for extensibility.

## Project Resposibilities

- Designed and implemented both the single-threaded and multi-threaded versions of the server and client.
- Developed thread-safe work queues and integrated POSIX thread synchronization primitives.
- Ensured robust error handling and resource management (e.g., proper socket/file closure, memory management).
- Extensively tested the system for correctness, concurrency, and edge cases (e.g., malformed requests, large files, simultaneous connections).
- Documented design decisions and testing strategies.

## Skills & Technologies Used

- C programming (systems-level)
- POSIX sockets (TCP/IP networking)
- POSIX threads (pthreads)
- Synchronization (mutexes, condition variables)
- Protocol design and parsing
- Debugging concurrent networked applications
- Linux development environment

## Outcomes & Impact

- Built a scalable file server capable of handling multiple concurrent clients with high reliability.
- Gained hands-on experience with core distributed systems concepts: concurrency, synchronization, and network programming.
- Demonstrated ability to design, implement, and test complex systems software in C.

## Learning Highlights

- Deepened understanding of thread safety and synchronization challenges in concurrent systems.
- Improved proficiency in socket programming and custom protocol implementation.
- Developed strategies for debugging and testing multi-threaded networked applications.
