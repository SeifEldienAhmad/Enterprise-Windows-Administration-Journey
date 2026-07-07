# Windows Processes and Threads

## Objectives:
> Understand how Windows executes a program and the relationship between Programs, Processes, and Threads.

## Topics Covered:
  - Program VS Process VS Thread
  - Windows Process Creation
  - Virtual Address Space
  - Primary Thread
  - Windows Scheduler (Overview)
  - Resource Monitor
## Practical Lab

  ### Environment

    - Windows 10 VM
    - Resource Monitor
  ### Top Memory Consuming Processes
  | Process | Working Set |
  |----------|------------:|
  | MsMpEng.exe | 113.64 MB |
  | SearchUI.exe | 65.05 MB |
  | svchost.exe (LocalSystemNetwork) | 31 MB |
  | backgroundTaskHost.exe | 28.94 MB |
  | explorer.exe | 27.3 MB |
  | dwm.exe | 26.7 MB |
  | ShellExperenceHost.exe | 23.9 MB |
  | perfmon.exe | 21.54 MB |
  | svchost.exe (LocalServiceNetwork) | 19.58 MB |
  | svchost.exe (netsvcs) | 13.08 MB |

  > Note: Processes are explaind in Notes.md

  ## Observations

  - Windows creates isolated virtual memory for every process.
  - Multiple svchost.exe instances are expected.
  - Memory usage differs between Working Set and Private Bytes.
  ``` 
  Working Set measures physical memory (RAM) currently active for a process, while Private Bytes measures virtual memory allocated exclusively to that process, regardless of whether it sits in RAM or has been swapped to the pagefile on your hard drive.
  ```
  
## What I Learned

- A Program is a static executable.
- A Process is a running instance with its own memory and resources (like virtual address space, Process ID, Security Token, Handle Table, Environment Variables, at least one Thread, and Loaded DLLS).
- Threads are the execution units scheduled by Windows.

## Challenges

Initially I confused Windows process creation with thread pools. After reviewing the Windows architecture, I understood that thread pools belong to applications rather than the operating system process creation mechanism. I explained it in the following process starting after double-clicking notepad.exe:
```
  1- CMD calls CreateProcess()
  
  ↓
  
  2- Windows Kernel checks the file
  
  ↓
  
  3- Generate the  EPROCESS Object
  
  ↓
  
  4- Allocate Virtual Address Space
  
  ↓
  
  5- Install EXE
  
  ↓
  
  6- Install DLLs
  
  ↓
  
  7- Generate the Primary Thread
  
  ↓
  
  8- Create Security Token
  
  ↓
  
  9- Place the thread in the Ready Queue
  
  ↓
  
  10- Scheduler selects the thread
  
  ↓
  
  11- CPU begins executing the first instruction
  
  ↓
  
  12- Notepad Window appears
```
