# ESP01 Board
## Description
This board is inspired from the classic ESP01 Relay board. 
In the large case of Relay boards, you can find the same problems like the relay is driven LOW end when the ESP boots up, the relay is triggered since the ESP boot reaches the end of the setup function when the GPIO pin is set to LOW.

The ESP01 Board is designed to solve these problems, but also to provide a more stable and flexible solution for your projects.

The output stage of strapping pins is latched and modifyng the time constant of the RC (R12-C7 and R13-C8) you can change the time of the latching. The default latched time is about 210ms for certain, but the latces become transparent after 545ms due to the $V_{IL}$ of the Latch is $0,9V$ so the latch is completally transparent when the RC circuit reaches $0,9V$; in the range of $2V - 0,9V$ the behavior of the latch is unpredictable.


## Features
- ESP01/ESP01-S Module
- 1x Relay 5V or 3.3V (hardware configurable whit a jumper)
- 2x NMOS Output Stage, 
- 2x NMOS Latched Output Stage,
- 4x Input Stage, with 2 of them pulled up to 3.3V with a 10K resistor,
- 1x 3.3V LDO Regulator,
- 1x fuse for the 5V input,
- USB Type-C Connector for power supply (or a classic pin header).

## Note
> If you need the UART pins, you can use the I1 and I3 pins but you need to remove the 10K resistor (R2 and R3) and the NMOS (Q1 and Q2) from the board.