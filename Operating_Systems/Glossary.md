
| Term | Concise Definition and Function |
| :--- | :--- |
| **Abstraction** | The simplification process: the OS provides users and programmers with **easy-to-use models** (e.g., the concept of a *File*, *Process*, or *Virtual Memory*) by hiding underlying hardware complexity. |
| **Concurrency** | The set of challenges arising when multiple **threads** or **processes** try to access and modify the same shared resource simultaneously (e.g., a variable in memory). |
| **File System** | The OS component that manages the organization, storage, retrieval, and protection of data on **persistent storage devices**. |
| **Kernel Mode** | The **privileged** CPU operating mode where OS code is executed. It has unlimited access to all hardware resources and instructions. |
| **Multiprogramming** | A historical technique where multiple processes resided in main memory and the CPU switched rapidly between them to improve processor utilization. |
| **Operating System (OS)** | Software that **manages and coordinates all resources** (CPU, memory, I/O) to ensure the computer system is efficient and user-friendly. |
| **Overhead** | The cost in terms of time and resources (e.g., CPU cycles or memory) introduced by the OS itself to perform its management, scheduling, and virtualization functions. |
| **Persistence** | The system's ability to **store data** (via the File System) so that it survives power loss, using non-volatile memory (disks, SSDs). |
| **PID** | PID stands for Process ID—a unique integer the OS assigns to each running process. |
| **Pipe** | A pipe is a one-way in-memory channel that connects one process’s stdout to another process’s stdin, enabling composition of tools without temporary files. |
| **POSIX** | Functions exposed by the operating system that a process can invoke. |
| **Process** | **The instance executing a program** with its execution context: memory (stack/heap), registers, file descriptors, environment variables, permissions, state, etc. |
| **Shell** | **Textual interface and orchestrator (parsing, variables, pipes, redirections, process launching). |
| **System Call** | The interface or mechanism through which a program in **User Mode** can request a service from the kernel in **Kernel Mode**. |
| **UNIX** | UNIX is a family of operating systems (and a system design philosophy) born in the 1970s at Bell Labs. |
| **User Mode** | The **non-privileged** operating mode where user program code runs. It is restricted from direct hardware access to ensure **protection** and isolation. |
| **Virtualization** | The core technique by which the OS transforms a physical resource (e.g., one CPU) into a **virtual resource** that can be used simultaneously by multiple programs (**multi-tasking**). |
| **Kernel** | It is the only software that has full control over the computer's hardware and acts as a translator and manager between user programs (such as applications and the Shell) and the machine's physical resources. |
