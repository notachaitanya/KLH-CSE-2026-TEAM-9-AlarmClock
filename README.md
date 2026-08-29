# Alarm Clock System

**Course:** Operating Systems and Systems Programming (25CS2104E)
**Term:** 2026–27, Term-I
**Section:** 9 | **Team No.:** 9

## Team Members

| Roll Number | Student Name |
|---|---|
| 2520030210 | K. Chaitanya |
| 2520030113 | Aakiri Deeraj |
| 2520030357 | K. Abhiram |

## Supervisor

Dr. Harika Devi

## Abstract

Alarm Clock System is a Linux-based Operating Systems project that demonstrates how a program can schedule, track, and respond to time-based events using process and signal management concepts. In conventional program execution, keeping track of elapsed time and triggering an action at a precise future moment can be difficult without a mechanism that lets the operating system notify a process when a specific time has been reached. This project addresses the problem by using Linux timers and signals to let a process set one or more alarms, continue other work, and be asynchronously notified exactly when each alarm expires.

The project focuses on key Operating Systems and system programming concepts such as process creation, process lifecycle management, asynchronous notifications and signal handling, timers, and concurrency and synchronization. System calls and library functions such as fork(), alarm()/setitimer(), signal()/sigaction(), pause(), and POSIX thread functions such as pthread_create() and pthread_mutex_lock() are used to implement scheduling and safe handling of multiple concurrent alarms.

The proposed solution is a Linux-based application in C/C++, where the user sets one or more alarms with a target time or countdown duration, and the system uses timers together with signal handlers (and, where multiple simultaneous alarms are involved, POSIX threads with mutexes for safe access to shared alarm data) to track time and trigger the alarm at the correct moment. The expected outcome is a functional command-line alarm clock that demonstrates asynchronous event handling, accurate timing, and safe concurrent execution.

## Setup Instructions

### Prerequisites
- Linux / Ubuntu (or WSL on Windows)
- GCC / G++ compiler
- POSIX threads library (pthread) — included with glibc on Linux

### Clone the Repository
git clone https://github.com/notachaitanya/KLH-CSE-2026-TEAM-9-AlarmClock.git
cd KLH-CSE-2026-TEAM-9-AlarmClock

### Build
gcc -o alarm_clock alarm_clock.c -lpthread
(Replace alarm_clock.c with the actual source filename once added, and add any additional .c files as the project grows.)

## Execution Instructions

Run the compiled program from the terminal:
./alarm_clock

Typical usage once implemented:
# Set an alarm for a countdown duration (e.g., 30 seconds)
./alarm_clock set 30

# List active alarms
./alarm_clock list

# Cancel an alarm by ID
./alarm_clock cancel <alarm_id>

The program will run in the foreground, print status/countdown updates, and trigger an alert (via a signal handler) when an alarm's timer expires. Multiple alarms can be set concurrently; each is tracked on its own thread.

## Current Phase Status

In Progress — Problem Statement & Design Phase

- [x] Problem statement finalized
- [x] Repository created
- [ ] Core timer/signal logic implementation
- [ ] Multi-alarm threading and synchronization
- [ ] Testing and validation
- [ ] Final report and demo

## Repository

- Project Repository: https://github.com/notachaitanya/KLH-CSE-2026-TEAM-9-AlarmClock
- Team Repository: https://github.com/notachaitanya/Team9_OSSP