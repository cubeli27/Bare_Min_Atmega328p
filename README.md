# Bare_Min_Atmega328p
Custom PCB made for available in-house parts. Made just for testing the fab house and lab capabilities.

# *Disclaimer*

This board has no defined purpose it was made for testing the ordering process and the lab assembly capabilities. 
Additionally, it was designed for the preexisting available components that were lying around the lab. Hence the part selection is suboptimal.

![FD85354D-6141-4799-AFD3-7899771D79AB](https://github.com/cubeli27/Bare_Min_Atmega328p/assets/134604815/310bae56-21a8-453f-970b-b6daa55a1d49)

# Assembly

Silkscreen is simplified for hand assembly so;
 ```ignore
 |   R      |   C          |   L
 |----------|--------------|------------------|
 | R1 = 1k  | C1 = 100nF   |  L1 = 10uH
 | R2 = 470 | C2 = 22pF    |
 | R3 = 10k | C3 = 10uF    |

 ```

R1 = 1k   |   C1 = 100nF  |  L1 = 10uH
R2 = 470  |  C2 = 22pF    |
R3 = 10k  |  C3 = 10uF    |


LED's labels:
R --> RED

G --> GREEN

B --> BLUE

TX/RX --> ORANGE

PWR --> WHITE 

Tip: 
R1 next to the PWR led should be more than 1k unless you want it to always be too bright, I recommend 1k8 or 2k2.
