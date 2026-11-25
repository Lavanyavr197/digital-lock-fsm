# digital-lock-fsm
A finite state machine based digital lock with a failed-attempt counter that restricts access after three consecutive incorrect password attempts.
Digital Lock with Failed-Attempt Counter using FSM

Project Overview

This project focuses on designing a simple digital security lock using a Finite State Machine (FSM).

The system checks the password entered by the user and controls access based on whether the entered password is correct or incorrect. To improve security, the design includes a failed-attempt counter that keeps track of consecutive incorrect password entries.

If the user enters an incorrect password three times consecutively, the system enters a locked state and prevents further access until the system is reset.

The main objective of this project is to understand how FSMs can be used to design sequential digital systems with controlled state transitions.

Objectives

- Design a digital lock using a Finite State Machine.
- Verify the entered password against the predefined password.
- Maintain a counter for consecutive incorrect attempts.
- Restrict access after three consecutive incorrect attempts.
- Understand state transitions and sequential circuit behaviour.
- Implement and examine the hardware design using the selected design tool.

Working Principle

The digital lock operates based on password verification and the number of failed attempts.

1. Initially, the system remains in the idle state.
2. When a password is entered, the FSM checks whether it matches the predefined password.
3. If the password is correct, access is granted.
4. If the password is incorrect, the failed-attempt counter is incremented.
5. The system allows another attempt if the number of incorrect attempts is below three.
6. After three consecutive incorrect attempts, the FSM moves to the locked state.
7. Once locked, the system does not accept further access attempts until reset.

A successful password entry before the third failure resets the consecutive failed-attempt count.

FSM State Description

The FSM can be described using the following conceptual states:

State| Description
IDLE| Waits for password entry
CHECK| Checks the entered password
UNLOCK| Grants access when the password is correct
ERROR| Handles an incorrect password
LOCKED| Disables access after three consecutive failures

Note: The state names and transitions should be adjusted to match the actual RTL implementation.

Design Flow

The project follows these general digital design steps:

1. Understand the problem statement.
2. Define the FSM states and transitions.
3. Develop the RTL design.
4. Verify the design through simulation, if applicable.
5. Perform design elaboration.
6. Examine the implementation design.
7. Analyse the resulting design.

Design Screenshots

1. Implementation Design

The following image shows the implementation design generated during the design process.

"Implementation Design" (images/implementation_design.png)

2. Elaborated Design

The elaborated design provides a structural view of the RTL design and its components.

"Elaborated Design" (images/elaborated_design.png)

3. Additional Design Results

Additional screenshots, such as simulation waveforms, synthesis results or other relevant design views, can be added below.

"Additional Design Screenshot" (images/additional_design.png)

Results and Observations

The FSM-based digital lock is designed to provide controlled access through password verification.

The failed-attempt counter introduces an additional security mechanism by restricting access after three consecutive incorrect attempts.

The project demonstrates the application of finite state machines, counters and sequential logic in a basic digital security system.

Conclusion

This project helped me understand the practical application of Finite State Machines in digital system design.

Through this assignment, I explored how state transitions, password verification and counters can work together to implement a basic digital locking mechanism. It also provided an opportunity to understand the design flow and examine the generated hardware design.

Tools and Technologies

- Hardware Description Language: [Verilog / VHDL]
- Design Tool: [Vivado / Quartus / Other]
- Concept: Finite State Machine (FSM)
- Digital Design Concepts: Sequential Logic, State Transitions and Counters

Repository Structure

digital-lock-fsm/
│
├── README.md
│
├── src/
│   └── digital_lock.v
│
├── images/
│   ├── implementation_design.png
│   ├── elaborated_design.png
│   └── additional_design.png
│
└── simulation/
    └── testbench.v

The folder structure can be modified according to the files included in the actual project.
