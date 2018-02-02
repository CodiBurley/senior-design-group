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
 1. At this point, the operating system will install correctly, but to verify the binary
    you've uploaded to run on the device is running in an OK state, check to see the if you
    see a single LED light constantly lit up. If you see a single LED light consistently blinking,
    the application binary you've uploaded could not be run successfully.

# Pairing the OS with a Bluetooth device

# How to load a binary program on the operating system

# Interpreting outputs
