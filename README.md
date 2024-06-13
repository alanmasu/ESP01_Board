# ESP01 Board
## Description
This board is inspired from the classic ESP01 Relay board. 
In the large case of Relay boards, you can find the same problems like the relay is driven LOW end when the ESP boots up, the relay is triggered since the ESP boot reaches the end of the setup function when the GPIO pin is set to LOW.

The ESP01 Board is designed to solve these problems, but also to provide a more stable and flexible solution for your projects.

## Features
- ESP01/ESP01-S Module
- 1x Relay 5V or 3.3V (hardware configurable whit a jumper)
- 4x NMOS Ouput Stage, with 2 of them driven LOW but in a safe way
- 4x Input Stage, with 2 of them pulled up to 3.3V with a 10K resistor
- 1x 3.3V LDO Regulator
- 1x fuse for the 5V input
- USB Type-C Connector for power supply (or a classic pin header)

## Note
> If you need the UART pins, you can use the I1 and I3 pins but you need to remove the 10K resistor (R2 and R3) and the NMOS (Q1 and Q2) from the board.