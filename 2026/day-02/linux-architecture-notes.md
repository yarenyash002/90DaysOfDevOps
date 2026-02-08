# Core components of linux

**Kernel**
- Kernel is heart of linux
- Provides bridge between hardware and software
- Written mainly in **C language**
- Manages critical system resources: CPU,Memory,DISK,Processes

**Hardware**  
Physical component where OS is installed

**Shell**  
Interactive way to talk through kernel using commands

**Gui**  
It provides visual interaction

**System libraries**  
Collection of pre written functions that application use to request service from kernel.

**System utlities**  
system utilities are built in tools that helps users manage, configure and maintain the OS. 
Used for tasks like software installation, user management and monitoring.

# systemd (use)
- Systemd is the modern init system and service manager  
- It’s the very first process that starts after the kernel boots (PID 1), and from there it manages all other processes and services.
  - Boots the system
  - Manages services:systemctll start/stop/status
  - Monitors processes: Restarts services automatically if they fail.
 
# Processes in Linux
* A **process** is a running program
* A new process is created when a program starts another program
* Each process has:

  * Its own memory
  * Its own Process ID (PID)
## Process states 
 - Running: The process is actively using the CPU or is ready to run.
 - Sleeping : The process is waiting for an event (like user input, network data, or disk I/O). It can be interrupted by signals.
 - zoombie : Process has terminated but its entry in the process table still exists because its parent process has not read its exit status

# 5 commands daily used
- df-h: To check the mount space  
- chmod: change the permission  
 -  top,sar: Check the cpu utilization  
- ps: Process monitor provide process id, command name which is curucial for monitoring, system performance and troubleshooting  
- ls: list the file  
