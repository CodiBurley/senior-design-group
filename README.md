# O<sup>s</sup>xide: An RTOS for Secure IOT in Rust

This repository serves as a place for the documentation of the O<sup>s</sup>xide Project. O<sup>s</sup>xide is a real time operating system written in Rust that aims create a foundation for secure Internet of Things (IOT) applications. 


1. [Abstract](#abstract)
2. [Project Description](#project-description)
3. [User Stories and Design Diagrams](#user-stories-and-design-diagrams)
   * [User Stories](#user-stories)
   * [Design Diagrams](#design-diagrams)
   * [Diagram Descriptions](#diagram-descriptions)
4. [Tasks and Timeline](#tasks-and-timeline)
   * [Task List](#task-list)
   * [Timeline](#timeline)
   * [Effort Matrix](#effort-matrix)
5. [ABET Concerns](#abet-concerns)
6. [Slideshow](#slideshow)
7. [Self-Assessment](#self-assessment)
8. [Professional Biographies](#professional-biographies)
9. [Budget](#budget)
   * [Expenses](#expenses)
   * [Donated Assets](#donated-assets)
10. [Appendix](#appendix)


## Abstract


## Project Description

#### Team:
- Codi Burley       : burleycj@mail.uc.edu
- Daniel Wendelken  : wendeldr@mail.uc.edu
- Douglas Flick     : flickdm@mail.uc.edu
- Dominic Farolino  : farolidm@mail.uc.edu

#### Advisor: Dr. John Franco

#### Background
Real Time Operating Systems (RTOS) aim to serve as operating systems that satisfy strict time and reliability constraints of some real time applications. Some RTOSs that have been popular in the past include RTLinux, VxWorks, eCos, QNX, etc. These and most RTOSs have historically been built using the C programming language.

While C has been the long time favorite in the types of low-level programming that is often needed for creating an operating system, a new low-level language with the name Rust is gaining popularity. Rust is a modern systems level programming language that promises speed and security. It provides protections against common system level vulnerabilities including use-after-free attacks, buffer overflow attacks, and many more. This makes Rust a good choice to build a modern, secure, RTOS. An area that a secure RTOS may be used is the growing field of internet of things (iOT).

iOT is a movement towards the connection of physical devices in a way that allows information/data to be shared and utilized by all these “things”. These physical devices are often embedded systems that interact with different types of sensors or other means of gathering data, and they often share this data over some network to other physical devices. Because these are embedded systems, they often utilize RTOSs, and because they must share this data with outside devices, security becomes a priority.

#### Problem Statment
As hinted in the background iOT is becoming increasingly widespread.  In the past few years we’ve seen attacks like the Mirai Botnet, TRENDnet security camera vulnerabilities, and countless security issues with many devices.  Many of these vulnerabilities are produced from the rapid development and cutting edge nature of iOT devices; however, they would often be negated if a standard RTOS existed for use across devices.

#### Inadequacy of current solutions to the problem
There are many other RTOSs which exist but only two that utilize Rust, zinc.rs and Tock.  There are issues with these implementations zinc.rs is more of a hardware abstraction layer then a full RTOS and Tock is currently developed specifically for Cortex-M microcontrollers.

#### Background skills/interests applicable to problem
Knowledge of OS kernels, embedded software programming, driver knowledge.

#### Our Teams Approach
We hope to be able to produce a Rust RTOS with some basic drivers (usb, network) which would run on a wider range of chips supporting llvm compilation.




## User Stories and Design Diagrams

### User Stories
1. As a IOT Developer, I want a secure operating system that handles real world events in a known time frame.
2. As a Developer at a Defense Company, we need a real time operating system that would be difficult for enemies of state to penetrate.
3. As a Developer at a conveyer belt company, we need to quickly sort items and ship them to a desired location as quickly as possible.
4. As a Developer at aerospace systems company, we need planes that can handle environmental effects as fast as possible and safer from human programming errors.


### Design Diagrams
The design diagrams are split into three different diagrams, each diagram at a higher level of abstraction than the next.

#### Diagram 1
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/04-user-stories-design-diagrams/D01.png "Design Diagram 1")

#### Diagram 2
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/04-user-stories-design-diagrams/D02.png "Design Diagram 2")

#### Diagram 3
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/04-user-stories-design-diagrams/D03.png "Design Diagram 3")



### Diagram Descriptions
TODO



## Tasks and Timeline

### Task List
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/05-task-list/task-list-img.png "Task List")


### Timeline
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/05-task-list/task-list-img.png "Task List Timeline")

### Effort Matrix
![alt text](https://github.com/CodiBurley/senior-design-group/blob/master/05-task-list/effort-matrix.png "Task Effort Matrix")


## ABET Concerns

#### Social
Information Security is a pressing concern in our technical society in which internet of things (iOT) technology is being used at an exponentially increasing rate. The average consumer of iOT devices could benefit from our operating system that pushes in the direction of secure iOT applications. If iOT devices are built on top of an operating system that promises a more secure foundation, people may be more willing to adopt some iOT applications that could benefit society. If confidence in iOT security is raised, we may see an increase in iOT that is built into infrastructure which could greatly increase the quality of living. It is hard to say in what ways iOT will be used in the future, but it is clear that the possibilities are endless. By creating a real time operating system that attempts to cement a firm foundation for secure iOT, we can help to pave the way for iOT applications to be used to their full potential with a confidence in security.


#### Economic
While our senior design project will rely primarily on self generated code there are some economic limitations that are imposed. To begin we are constrained to the hardware we choose. In this choice we will be required to purchase a microcontroller which fits our projects needs.  This purchase will need to be self funded and more than one microcontroller may be needed to facilitate development.  Another constraint imposed on us is the use of other pre-existing RTOS codebases for reference or code-reuse. Many of these are licensed for free use but care will need to be taken to reference properly.  Overall our project should not have a large economic impact to the team or the users of the created RTOS. 


#### Security
A real time operating system is not designed to be general purpose, such as a phone, laptop, or desktop computer. That being said, a real time operating is designed to provide a deterministic execution pattern. These types of systems may be used by medical devices, wearable technology, assembly lines, power plants, and many more sensitive areas. In all of these cases criminals and foreign agents may attempt to exploit the system to cripple a company or governments infrastructure or do harm to individuals. Our project attempts to provide security by default. The system will be written in the programming language called rust where the focus is on preventing many of the simple errors that are commonly exploited and by preventing segmentation faults and guarantees thread safety. Overall a core part of our project is designing our real time operating system to prevent attacks and data loss.

#### Legal
It is true that when designing any non-trivial piece of software, legal concerns come into play at a regular pace. One such legal concern follows from the idea that we’re only using free and open software, and no intellectual property or copyrighted software in an invalid manner. Given the preliminary research we’ve performed, just about all of the software we’ll be referencing is open-source under an MIT license, which provides us no guarantees regarding the software we’re using in exchange for the ability to use and reproduce it in anyway we’d like. Another legal concern for the project that has the potential of cropping up much later in the future revolves around whether we’d like to provide security guarantees around our software for industry usage. Most modern day operating systems have an EAL (Evaluation Assurance Level) of 2 to 3, which is a security assessment ranking assigned by the NSA after thorough testing. The Real Time Operating Systems in charge of marshalling commands in high-risk situations are often required to have an EAL level of 5 or 6 (7 being the highest) to be considered justified. If one day, we wanted our RTOS to compete on the market for legal industry contracts, it would be in our best interest to shoot for an EAL level of 5 to 6, meaning the core security design in our RTOS would have to be rock solid. This is something to consider in the future if we were looking to have our RTOS be legally involved in high-risk situations, and is for now not a forefront concern.



## Slideshow
This link provides a presentation on the project: https://youtu.be/QamIhC8fg7M

## Self-Assessment


## Professional Biographies

Links to Professional Biographies:
- [Codi Burley](https://github.com/CodiBurley/senior-design-group/blob/master/01-bios/codiburley.md)
- [Dominic Farolino](https://github.com/CodiBurley/senior-design-group/blob/master/01-bios/domfarolino.md)
- [Douglas Flick](https://github.com/CodiBurley/senior-design-group/blob/master/01-bios/douglasflick.md)
- [Daniel Wendelken](https://github.com/CodiBurley/senior-design-group/blob/master/01-bios/wendeldr.md)

## Budget
TODO


### Expenses
TODO


### Donated Assets
TODO

## Appendix

