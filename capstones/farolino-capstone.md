# Capstone Essay

## Description of project

The goal of this project is to create a real time operating system (RTOS) in the modern systems programming language,
Rust. Historically, real time operating systems are used to satisfy strict time and reliability constraints on embedded 
systems by implementing effective prioritization and security capabilities. In this project, we’ll be constructing a simple
RTOS aimed at providing a secure platform for embedded systems and IOT devices. The project will require in-depth knowledge
of the design of computer architecture and operating systems. Building an OS will require building a bootloader, basic kernel,
process scheduler, and a few essential drivers. Security is the main goal of the basic RTOS we’ll be building, so beyond functionality,
our operating system should be inherently more secure than RTOSs built with the C programing language.

## Application of academic coursework

The content provided in several courses throughout our academic career will become relevant in a practical setting. Specifically
these courses are:

 - Introduction to Computing Systems
 - Data structures
 - Operating System Concepts

Understanding how the CPU processes instructions is extremely important for the low-level programming required at the operating system
level. Furthermore, the kernel will need to implement many basic data structures from scratch that higher-level processes can take advantage
of. All of this should happen while providing a process scheduling model that is secure by default. In other words, it should be impossible
for application code to have the level of control over the computer hardware that the kernel has.

## Application of co-op experience

My first two co-ops at Interactive Intelligence did very little to provide a practical environment for me to practice some
of the low-level theory I had gained in the classroom. Luckily my third co-op with Mozilla provided me with a great opportunity
to grow in this area! While I personally have very little real world operating systems experience on my own, the co-op at Mozilla
has taught me much about low-level programming that I had not experienced in the classroom. Firefox must be efficient, and therefore
interfaces directly with the OS API required to build efficient applications that interface directly with the OS API. I learned a lot
about the general compilation process of software, how to write multiprocess applications in C++, and how system calls work within the
kernel while providing application security. Besides allowing me to both practice and gain real world experience in this area, this co-op
experience gave me the hunger for more of this experience that drives much of the passion I have for this senior design project.

## Motivation for project

There is plenty of motivation for the type of project we’re undertaking. Chief among many OS concerns is security, which operating systems
written in the C programming language traditionally have many issues with by default. Rust is a systems programming language that promises
a higher level of security than C does, leading to inherently secure programs by default. We intend to put the Rust programming language to
the test by attempting to create an operating system free of many of the security vulnerabilities that C-based operating systems have out of
the box, and verifying the supposed security features that Rust promises.

Furthermore, the IOT community lacks a standard RTOS operating system built in a secure language like Rust. Many of the current implementations
are more of hardware abstraction layers with a limited target architecture, than even simple multi-architecture platforms, suggesting that
experimentation in this realm may result in a valuable contribution to the IOT and embedded systems security.

## How we intend to accomplish the project and validate its success

To accomplish this ambitious task, adequate research on the current implementations in the market is necessary. Once enough data is collected,
we’ll then shift our focus on building a minimal bootable program in Rust that compiles to several target architectures. At this point most of
the kernel development will take place, allowing us to develop a very small lightweight kernel that supports basic process scheduling. Finally
we’ll focus on writing simple USB and networking drivers so that external applications can interface with our kernel.

Evaluating our project’s success will consist of running several security test suites on our operating system to validate that applications running
in user space processes cannot by default affect or interrupt tasks running in kernel space. With Rust’s inherent security features, things such as
buffer-overflow errors common in C programs should be eliminated by default, thus providing a more secure platform for applications to run on.

