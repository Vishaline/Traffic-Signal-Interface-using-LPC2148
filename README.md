# Traffic-Signal-Interface-using-LPC2148
A simple working model of a Traffic Light with LPC2148 using KEIL and simulation using Proteus


The Traffic light controller section consists of 12 LEDs arranged in 4 Lanes in LPC2148 Primer Board. Each lane has Go(Green),  Listen(Yellow)  and  Stop(Red)  LED is being placed.
#Algorithm:
1. Configure P0.0 to 0.15 as GPIO
PINSEL0 = 0X00000000
2. Configure P0.0 to P0.15 as output ports
IO0DIR = 0X0000FFF0
[The simulation starts with the green light at the East and red lights in the other directions]
WHILE(1)
3. The green light on the EAST, connected to P0.12, and all the other red lights are turned on
IO0SET=0x00003090
4. The green light is turned off
IO0CLR=0x00001000
5. The yellow light is turned on in the east direction, while the red lights continue to be unaffected
IO0SET=0x00002890
6. The yellow light is turned off and the green light on the SOUTH, connected to P0.15, and all the other red lights are turned on
IO0SET=0x00008490
7. The green light is turned off
IO0CLR=0x00008000
8. The yellow light is turned on in the south direction, while the red lights continue to be unaffected
IO0SET=0x00004490
9. The yellow light is turned off and the green light on the WEST, connected to P0.6, and all the other red lights are turned on
IO0SET=0x000024C0
10. The green light is turned off
IO0CLR=0x00000040
11. The yellow light is turned on in the west direction, while the red lights continue to be unaffected
IO0SET=0x000024A0
12. The yellow light is turned off and the green light on the NORTH, connected to P0.9, and all the other red lights are turned on
IO0SET=0x00002610
13. The green light is turned off
IO0CLR=0x00000200
14. The yellow light is turned on in the north direction, while the red lights continue to be unaffected
IO0SET=0x00002510
15. The yellow light is turned off.

Note: Delays are included to ensure the proper functioning of traffic lights.
