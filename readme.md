A RTOS for Secure IOT in Rust
=============================

## Team Members
### Team:
- Codi Burley       : burleycj@mail.uc.edu
- Daniel Wendelken  : wendeldr@mail.uc.edu
- Douglas Flick     : flickdm@mail.uc.edu
- Dominic Farolino  : farolidm@mail.uc.edu

### Advisor:
- ???????

## Background
Real Time Operating Systems (RTOS) aim to serve as operating systems that satisfy strict time and reliability constraints of some real time applications. Some RTOSs that have been popular in the past include RTLinux, VxWorks, eCos, QNX, etc. These and most RTOSs have historically been built using the C programming language.

While C has been the long time favorite in the types of low-level programming that is often needed for creating an operating system, a new low-level language with the name Rust is gaining popularity. Rust is a modern systems level programming language that promises speed and security. It’s provides protections against common system level vulnerabilities including use-after-free attacks, buffer overflow attacks, and many more. This makes Rust a good choice a modern, secure, RTOS. An area that a secure RTOS may be used is the growing field of internet of things (iOT).

iOT is a movement towards the connection of physical devices in a way that allows information/data to be shared and utilized by all these “things”. These physical devices are often embedded systems that interact with different types of sensors or other means of gathering data, and they often share this data over some network to other physical devices. Because these are embedded systems, they often utilize RTOSs, and because they have must share this data with outside devices, security becomes a priority.

## Problem Statment
As hinted in the background iOT is becoming increasingly widespread.  In the past few years we’ve seen attacks like the Mirai Botnet, TRENDnet security camera vulnerabilities, and countless security issues with many devices.  Many of these vulnerabilities are produced from the rapid development and cutting edge nature of iOT devices; however, they would often be negated if a standard RTOS existed for use across devices.

## Inadequacy of current solutions to the problem
There are many other RTOSs which exist but only two that utilize Rust, zinc.rs and Tock.  There are issues with these implementations zinc.rs is more of a hardware abstraction layer then a full RTOS and Tock is currently developed specifically for Cortex-M microcontrollers.

## Background skills/interests applicable to problem
Knowledge of OS kernels, embedded software programming, driver knowledge.

## Teams Approach
We hope to be able to produce a Rust RTOS with some basic drivers (usb, network) which would run on a wider range of chips supporting llvm compilation.
