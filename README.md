This repository contains my implementation of the Pintos operating system, developed as part of my Operating Systems course at Galatasaray University.

Pintos is a simple operating system framework for the 80x80x architecture. The goal of this project was to dive deep into the kernel level and understand how threads, synchronization, and system calls actually work under the hood. It was a challenging but incredibly rewarding experience in low-level C programming

Key Accomplishments
Thread Management: Implemented core threading features, including a priority-based scheduler. I had to ensure that threads with higher priority always run first and handle priority donation to avoid priority inversion.

Synchronization: Heavily used and implemented synchronization primitives like semaphores, locks, and condition variables. Dealing with race conditions and deadlocks was a major part of the debugging process.

Passing the Tests: I successfully passed 27 out of 27 required system tests. Reaching that 100% pass rate involved a lot of late-night debugging sessions and kernel logs analysis.

The Debugging Journey: Bochs vs. Qemu
One of the biggest hurdles during this project was the simulation environment. Initially, I struggled with execution failures on the Bochs simulator. After some troubleshooting, I decided to switch the local execution environment to Qemu on a Linux Mint VM. This change was a game-changer; it provided more stable execution and better debugging tools, which allowed me to finally pass the remaining tests.

Tech Stack
Language: C (Kernel-level programming)

Environment: Linux Mint VM

Simulator: Qemu

Version Control: Git (Used for collaboration and tracking progress with my project partner)

 Project Structure
Plaintext
├── src/
│   ├── threads/     # Thread management and synchronization logic
│   ├── devices/     # Hardware device drivers (timer, keyboard, etc.)
│   ├── lib/         # Standard C library functions for the kernel
│   └── tests/       # The 27 tests I had to pass
└── README.md

How to Run
Note: This project is designed to run in a specific Unix-like environment with the Pintos toolchain installed.

Clone the repository.
Navigate to the threads directory:

cd src/threads

Compile the kernel:

make

Run the tests using Qemu:

pintos --qemu -- run [test_name]

This project was a collaborative effort with my project partner. We managed our workflow through Git, ensuring consistent commits and clear design documentation.
