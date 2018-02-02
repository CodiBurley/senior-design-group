# User Manual

> Warning: Practical usage and functionality is limited

This document is meant to guide the user when using the OSxide RTOS. Seeing as how
the project is primarily exploratory for the team members involved, the practical usage
and overall functionality of the operating system is extremely limited, due to the complexity
of the project. Consequently, the user guide this document describes is extremely *bare-bones*
and largely aimed at a technical audience.

# Installation and Execution

This section describes how to flash the OS and a binary compatible with the ARM architecture
to your Nordic Semiconductor board.

 1. Plug in the board via micro usb
 1. In the operating system directory, run `make flash` from shell or command prompt.
 1. At this point, the operating system will install correctly. To verify the binary you've
    uploaded to the device has executed or is executing successfully, see the
    [Interpreting Outputs](#interpreting-outputs) section listed below.

# Pairing the OS with a Bluetooth device

Steps to pair

1. Hold button 1 on Nordic device until all 4 leds flash
2. While flashing press pair button on bluetooth device
3. Wait for leds to stop flashing
4. Devices should be paired

# How to load a binary program on the operating system
To load binary

1. run `$make flash binary`. Substitute 'binary' with either path to single binary or directory of binaries. 

# Interpreting Outputs

Interpreting the output of the execution of a process in the operating system is crucial. The RTOS
provided has the ability to run `3` number of processes on the provided Nordic Semiconductor
board. The specific process (program) number (id) that is currently executing on the board will be
represented in binary (big-endian) on the LEDs present on the Nordic board. The fourth LED is used
to represent the state of the current process. If the fourth LED is solid, the running process is in
an OK execution state. If the LED is consistently blinking, the process was not able to be run correctly.

TODO(): determine whether this is the functionality we want or not
