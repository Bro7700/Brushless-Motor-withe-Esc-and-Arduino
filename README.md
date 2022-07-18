# Brushless-Motor-withe-Esc-and-Arduino
Task 3



 ## Introduction

A brushless motor is a direct current (DC) electric motor that operates without the mechanical brushes and commutator of a traditional brush motor. It has distinct advantages over a brush motor and is more economical in the long run, although the initial costs are higher. Brushless motors are used in various aspects of trenchless construction. 


 
 
 ## Technologies
 
 
 Arduino IDE 1.8.19 [To Download](https://www.arduino.cc/en/software)
  
 Fritzing [ To Download ](https://fritzing.org/download/)

 
 
 ## Components required
 

1. Arduino UNO
2. ESC 30A Module
3. jumper wirs
4. Potentiometer
5. bettrey   12 volt 
6. Brushless Motor
 


## Connections

connecting  to  in  Ardunio
connecting  to  in  Ardunio
connecting  to  in  Ardunio
connecting  to  in  Ardunio
connecting 
connecting  



 
 ## Block diagram & simulation
 
 
 
 
 
 ![BRUSHLESS MOTOR](https://user-images.githubusercontent.com/109243989/179446233-27f0d198-cee1-4421-b39e-78b97c612de3.JPG)

 
 
 
 
 ### The Code 
 
 
 #include <Servo.h>


Servo esc;  //Creating a servo class with name as esc

void setup()

{

esc.attach(8); //Specify the esc signal pin,Here as D8

esc.writeMicroseconds(1000); //initialize the signal to 1000

Serial.begin(9600);

}

void loop()

{

int val; //Creating a variable val

val= analogRead(A0); //Read input from analog pin a0 and store in val

val= map(val, 0, 1023,1000,2000); //mapping val to minimum and maximum(Change if needed)

esc.writeMicroseconds(val); //using val as the signal to esc

}
 
 
