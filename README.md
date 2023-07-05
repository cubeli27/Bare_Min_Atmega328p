# Bare_Min_Atmega328p
Custom PCB made for available in-house parts. Made just for testing the fab house and lab capabilities.

# *Disclaimer*

This board has no defined purpose it was made for testing the ordering process and the lab assembly capabilities. 
Additionally, it was designed for the preexisting available components that were lying around the lab. Hence the part selection is suboptimal.

![FD85354D-6141-4799-AFD3-7899771D79AB](https://github.com/cubeli27/Bare_Min_Atmega328p/assets/134604815/310bae56-21a8-453f-970b-b6daa55a1d49 = 100x100)

# Assembly

Silkscreen is simplified for hand assembly so;
 ```ignore
 | Resistor |  Capacitor   | Inductor    |    LED                  |
 |----------|--------------|-------------|-------------------------|
 | R1 = 1k  | C1 = 100nF   |  L1 = 10uH  | PWR = White             |
 | R2 = 470 | C2 = 22pF    |             | R/G/B = Red/Green/Blue  |
 | R3 = 10k | C3 = 10uF    |             | RX/TX = Orange          |

 ```


Tip: 
R1 next to the PWR led should be more than 1k unless you want it to always be too bright, I recommend 1k8 or 2k2.

# Programming
1. Open in Arduino IDE File/Examples/11.ArduinoISP/ArduinoISP
2. Uncomment line 81 (// #define USE_OLD_STYLE_WIRING).

![Capture](https://github.com/cubeli27/Bare_Min_Atmega328p/assets/134604815/28f24a41-0049-4fdf-ba29-87c680bc72ed)

3. Upload the code to your Arduino Uno with Board: Arduino Uno, Programmer: AVRISP mkII.
4. Connect Arduino Uno with the custom board like so:
 ```ignore
 | Uno      |  Custom Board| 
 |----------|--------------|
 | 10       | RESET        |  
 | 11       | MOSI         | 
 | 12       | MISO         |  
 | 13       | SCK          |
 | 5v       | 5v           |
 | GND      | GND          |
 ```
![IMG-0519](https://github.com/cubeli27/Bare_Min_Atmega328p/assets/134604815/d84351ba-188d-4cdd-98d3-a7fc82aea7c9)

5. Burning the bootloader steps. In Tools set Board: Breadboard Arduino/ ATmega328p, Programmer: Arduino as ISP, then click Burn Bootloader.
6. You should see "Done Burning Bootloader". Now you're set and can unplug your jumper wires and store your Arduino Uno you won't need it anymore.

![Capture](https://github.com/cubeli27/Bare_Min_Atmega328p/assets/134604815/60ea35dd-088a-4fe0-80df-bdbf18407586)

7. Connect your custom board to your PC through a USB cable.
8. In order to upload any code just select in Tools Board: Arduino AVR Board/ Arduino Duemilanove or Diecimila and click Upload (arrow pointing right). You should see the orange LEDs flashing.
9. If you want to start with the blink sketch make sure to use pins 5,6 or 7 because built-in LED's are on those pins.
 ```ignore
 | PIN      |  LED        | 
 |----------|-------------|
 | PD7      | RED         |  
 | PD6      | GREEN       | 
 | PD5      | BLUE        |  
 ```












