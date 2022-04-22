# DOOR SENSOR

## INTRODUCTION

Door sensors are an essential component of your home security system: they let you know when someone is entering your home. These devices are made up of two parts, which form a circuit when they’re kept parallel to each other.

![DOOR](https://user-images.githubusercontent.com/80033796/164703686-8815a90f-977b-47db-b221-b9b15b206054.jpg)

## OBJECTIVE

* To let us know whenever a person enters the door
* To safeguard important things

## SOFTWARE USED

* SimulIDE
* ATMEL STUDIO 7.0

## COMPONENTS USED

* ATmega328
* Switch
* LED
* Voltmeter
* Resister

## STEPS TO BUILD THE CODE

- Including required libraries.
- Then in main function assign pinB1 as input to do this we have to set logic = 0.
- To assign logic 0 in port B, we have to use DDRB (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 1 to other pins by using -DDRB=DDRB&0b11111101 command which is binary representation of HEX value which represents second bit as low and others as high.
- To assign pinC6 as output to do this we have to set logic = 1.
- To assign logic 1 in port C ,we have to use DDRC (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 0 to other pins by using DDRC=DDRC|0b01000000 command which is binary representation of HEX value which represents sixth bit as high and others as low.
- Then in while loop we have to continuosly monitor and compare value of pinB with given input and if switch is open the pinB will receive 0b00000010 input thus making the LED connected to port C high and glowing it.
- if switch is closed the pinB will not receive any input thus LED connected to port C gets low and it will not glow.

## STEPS TO RUN THE CIRCUIT

- After compiling the code many files will be generated in the debug folder.
- After building the setup, load firmware and upload the hex file and it will burn the hex file as the microcontroller only knows 1's and 0's.
- After loading it,run the circuit .
- To run the circuit turn on the voltage
- Then on opening the switch,the LED blinks and on closing the switch the LED turns off.
- Finally stop the circuit .

## WORKING

https://user-images.githubusercontent.com/80033796/164705797-1092932c-f6df-430c-baf6-a92b10f6a596.mp4

## BEHAVIORAL DIAGRAM

![Behavioral diagram ](https://user-images.githubusercontent.com/80033796/164675157-1f8a6e20-5042-4c0e-b4d4-1df6f00ac6d9.png)

## STRUCTURAL DIAGRAM

![Structural diagram](https://user-images.githubusercontent.com/80033796/164657236-a3ede462-0d96-4a0a-baec-a290d8869764.png)

## OUTPUT

### DOOR OPEN

![door open-out](https://user-images.githubusercontent.com/80033796/164676514-71e4c141-c69f-44dd-88af-d3b536c8e349.png)

### DOOR CLOSE

![door close-out](https://user-images.githubusercontent.com/80033796/164676490-c761e002-9c3f-41bc-af76-2d1046114fa5.png)



