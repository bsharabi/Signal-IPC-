# Signal-IPC-

>Signals are standardized messages sent to a running program to trigger specific behavior, such as quitting or error handling. They are a limited form of inter-process communication (IPC), typically used in Unix, Unix-like, and other POSIX-compliant operating systems.

>A signal is an asynchronous notification sent to a process or to a specific thread within the same process to notify it of an event. Common uses of signals are to interrupt, suspend, terminate or kill a process. Signals originated in 1970s Bell Labs Unix and were later specified in the POSIX standard.

>When a signal is sent, the operating system interrupts the target process' normal flow of execution to deliver the signal. Execution can be interrupted during any non-atomic instruction. If the process has previously registered a signal handler, that routine is executed. Otherwise, the default signal handler is executed.

>Embedded programs may find signals useful for inter-process communications, as signals are notable for their Algorithmic efficiency.

>Signals are similar to interrupts, the difference being that interrupts are mediated by the CPU and handled by the kernel while signals are mediated by the kernel (possibly via system calls) and handled by individual processes. The kernel may pass an interrupt as a signal to the process that caused it (typical examples are SIGSEGV, SIGBUS, SIGILL and SIGFPE).

# POSIX signals

Signal    | Portable number             | Default action        | Description 
---       |             :---:           |         ---           |        ---                                        |
SIGABRT   |  6	                        | Terminate (core dump) | Process abort signal                              | 
SIGALRM   |  14	                        | Terminate	            | Alarm clock                                       | 
SIGBUS    |  N/A	                    | Terminate (core dump) | Access to an undefined portion of a memory object | 
SIGCHLD   |  N/A	                    | Ignore	            | Child process terminated, stopped, or continued   | 
SIGCONT   |  N/A	                    | Continue	            | Continue executing, if stopped                    | 
SIGFPE    |  8                          | Terminate (core dump) | Erroneous arithmetic operation                    | 
SIGHUP    |  1                          | Terminate	            | Hangup                                            | 
SIGILL    |  4                          | Terminate (core dump) | Illegal instruction                               | 
SIGINT    |  2                          | Terminate	            | Terminal interrupt signal                         | 
SIGKILL   |  9                          | Terminate	            | Kill (cannot be caught or ignored)                | 
SIGPIPE   |  13	                        | Terminate	            | Write on a pipe with no one to read it            | 
SIGPOLL   |  N/A	                    | Terminate	            | Pollable event                                    | 
SIGPROF   |  N/A	                    | Terminate	            | Profiling timer expired                           | 
SIGQUIT   |  3                          | =Terminate (core dump | )	Terminal quit signal                            | 
SIGSEGV   |  11	                        | Terminate (core dump) | Invalid memory reference                          | 
SIGSTOP   |  N/A	                    | Stop	                | Stop executing (cannot be caught or ignored)      | 
SIGSYS    |  N/A	                    | Terminate (core dump) | Bad system call                                   | 
SIGTERM   |  15	                        | Terminate	            | Termination signal                                | 
SIGTRAP   |  5                          | Terminate (core dump) | Trace/breakpoint trap                             | 
SIGTSTP   |  N/A	                    | Stop	                | Terminal stop signal                              | 
SIGTTIN   |  N/A	                    | Stop	                | Background process attempting read                | 
SIGTTOU   |  N/A	                    | Stop	                | Background process attempting write               | 
SIGUSR1   |  N/A	                    | Terminate	            | User-defined signal 1                             | 
SIGUSR2   |  N/A	                    | Terminate	            | User-defined signal 2                             | 
SIGURG    |  N/A	                    | Ignore	            | Out-of-band data is available at a socket         | 
SIGVTALRM |  N/A	                    | Terminate	            | Virtual timer expired                             | 
SIGXCPU   |  N/A	                    | Terminate (core dump) | CPU time limit exceeded                           | 
SIGXFSZ   |  N/A	                    | Terminate (core dump) | File size limit exceeded                          | 
SIGWINCH  |  N/A	                    | Ignore	            | Terminal window size changed                      | 


