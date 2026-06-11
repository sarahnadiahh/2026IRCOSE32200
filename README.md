# 2026IRCOSE32200 - OPTIONAL PROJECT

## INFORMATION
-Name: SARAH NADIAH BINTI MUHAMMAD KHADZIR (사라 나디아)
-StudentID: 2023320142
-Department: Computer Science and Engineering

## ENVIRONMENT SPECS
-VM: Ubuntu 22.04.5 LTS
-Kernel Version: 5.15.0-176-generic

## BASIC LINUX COMMANDS
### pwd
-To display current working directory

### ls
-List files and directories

### cd
-Change current directory

### mkdir
-Create new directory

### rm
-Remove files or directories.

## Linux Filesystem Structure
/
|- bin
|- root
|- dev
|- etc
|- home
|- lib
|- proc
|- tmp
|- usr

/bin:essential commands
/etc:configuration files
/home:user files
/proc:process information
/tmp:temporary files

## File Permissions
r = read
w = write
x = execute

Eg:
-rwxr-xr-x

Owner:rwx
Group:r-x
Others:r-x

### Common commands
ls -l:view permissions
chmod 755 filename:change permissions
chmod +x script.sh:make a script executable
chown username filename:change file owner

## Process  Management
Process - program that is currently being executed

When a program runs, os creates a process and allocates resources
-CPU time
-Memory
-File descriptors
-Process ID(PID)

Each process has a unique PID that identifies it within the system

### Process States
#### Running
currently executing in CPU

#### Ready
waiting for CPU time

#### Waiting(Blocked)
waiting for an event such as user input or disk I/O

#### Terminated
finished execution

### Viewing Processes
```bash 
ps
```
-display currently running processes

```bash
ps -aux
```
-display detailed process info

```bash
top
```
-display processes in real time

### Terminating Processes
```bash
kill PID
``` 
-Kill a process using its PID

```bash
kill -9 PID
```
-Force termination

```bash
killall process_name
```
-Terminate processes by name

## Memory Management
The goal is to use available memory efficiently while preventing processes from interfering with each other.

### Memory Layout of a process
A typical process memory layout consists of:
+------------------+
|     Stack        |   -stores function parameters, local variables, return addresses
+------------------+
|                  |
|       Free       |
|      Memory      |
|                  |
+------------------+
|      Heap        |   -for dynamic memory allocation
+------------------+
|   Data Segment   |   -stores global and static variables
+------------------+
|   Text Segment   |   -contains executable instructions a program
+------------------+