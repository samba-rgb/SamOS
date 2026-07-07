# samOS

> A 64-bit operating system written in Rust, built from scratch to
> deeply understand how computers work.

## Vision

samOS is a long-term operating system project focused on learning by
building.

The goal is **not** to follow tutorials and copy existing kernels.
Instead, every subsystem is implemented incrementally, understanding the
concepts only when they become necessary.

By the end of this project, the operating system will include its own
boot process, memory management, scheduler, filesystem, networking
stack, and user-mode programs.

------------------------------------------------------------------------

## Philosophy

This project follows one simple rule:

> **Learn by implementing.**

Instead of learning operating system theory first, every concept is
introduced naturally while building the next feature.

For example:

-   Need keyboard input? → Learn interrupts.
-   Need dynamic memory? → Build a heap allocator.
-   Need multitasking? → Implement context switching.
-   Need applications? → Build system calls and an ELF loader.

Theory always follows implementation.

------------------------------------------------------------------------

## Goals

The long-term objective is to build an operating system capable of:

-   Booting on x86_64
-   Running a Rust kernel
-   Memory management
-   Heap allocation
-   Virtual memory and paging
-   Interrupt handling
-   Timer subsystem
-   Keyboard driver
-   Text console
-   Interactive shell
-   Process scheduler
-   User mode
-   System calls
-   ELF executable loading
-   File system
-   Disk drivers
-   Networking
-   Basic user applications

------------------------------------------------------------------------

## Project Roadmap

### Phase 0 --- Boot

-   Project setup
-   Build system
-   Bootloader
-   Boot in QEMU
-   Print `Hello samOS`

### Phase 1 --- Console

-   `println!`
-   Screen clearing
-   Colors
-   Cursor
-   Scrolling
-   Panic screen

### Phase 2 --- Keyboard

-   Keyboard interrupts
-   Scan code decoding
-   Input handling
-   Backspace
-   Enter

### Phase 3 --- Shell

Commands:

-   help
-   clear
-   echo
-   version
-   reboot
-   shutdown

### Phase 4 --- Memory

-   Physical frame allocator
-   Virtual memory mapping
-   Paging primitives
-   Heap allocator
-   Bump allocator
-   Arena allocator
-   Free-list allocator
-   Global allocator
-   `Box`
-   `Vec`
-   `String`
-   Allocation tests and debugging

### Phase 5 --- Timer

-   Timer interrupts
-   Sleep
-   Uptime
-   Kernel clock

### Phase 6 --- Scheduler

-   Kernel tasks
-   Context switching
-   Round-robin scheduler

### Phase 7 --- User Mode

-   Ring 3 execution
-   System calls
-   ELF loading

### Phase 8 --- File System

-   RAM filesystem
-   Disk-backed filesystem

### Phase 9 --- Drivers

-   Serial
-   VGA / Framebuffer
-   Disk
-   PCI
-   Mouse
-   USB (future)

### Phase 10 --- Networking

-   Ethernet
-   IPv4
-   ICMP
-   UDP
-   TCP (basic)
-   Simple HTTP server

------------------------------------------------------------------------

## Repository Structure

``` text
samOS/
├── kernel/
├── bootloader/
├── memory/
├── scheduler/
├── drivers/
├── filesystem/
├── shell/
├── userland/
├── tests/
└── docs/
```

------------------------------------------------------------------------

## Development Principles

-   Build one feature at a time.
-   Every phase must produce a runnable system.
-   Keep commits small and meaningful.
-   Prefer understanding over speed.
-   Avoid unnecessary abstractions.
-   Document important design decisions.

------------------------------------------------------------------------

## Current Milestone

**Phase 0 --- Boot**

Goal:

``` text
Hello samOS
```

Boot samOS in QEMU and print the message above.

------------------------------------------------------------------------

## Long-Term Vision

samOS is more than an operating system project.

It is a journey to understand:

-   How a computer boots
-   How CPUs execute code
-   How memory is managed
-   How interrupts work
-   How kernels schedule tasks
-   How filesystems store data
-   How operating systems communicate with hardware
-   How networks are implemented from the ground up

The destination is a working operating system.

The real goal is becoming a better systems engineer by understanding
every layer that makes modern computers work.
# SamOS
