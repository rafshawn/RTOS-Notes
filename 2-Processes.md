# Processes
- **Memory Allocation**: Running programs need memory for code, global variables (`.bss`), the stack, and the heap.
- **Virtual address**: Address used directly by software
- Processses are *unprivileged*

# Privilege
- **Supervisor mode**: Access to privileged instructions
- **User mode**: No privileged instructions
	- Attempting to execute a privileged instruction fromm user mode results in a *trap* (type of interupt)
- Mode indicated by bits in *status register*
- Mode changes on interrupt handling, system calls, or other traps

# Privilege Rings

# Unprivileged processes
**System calls**:
- How unprivileged processes perform privileged operations
- Privileged system (*kernel*) code called by unprivileged (*user*) process
- Note called like ordinary functions:
	1. Set arguments (including syscall #) in registers or memroy
	2. Invoke interrupt or syscall instruction
