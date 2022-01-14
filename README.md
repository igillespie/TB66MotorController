# Welcome

Simple c++ and header file written for use in Arduino projects to control motors using the TB6612 motor driver. Code originally came from the SparkFun example.



## How to use

Put the c++ and h files into your Arduino project. 
Add the #include "TB66MotorController.h" to your .ino Arduino sketch.

Here is how you initialize the motor controller:

Paste this code (be sure to map your pin numbers to pins you are using in your project):
~~~
//Define the Pins for Motors
//Motor 1
int pinAIN1 = 11; //Direction
int pinAIN2 = 8; //Direction
int pinPWMA = 3; //Speed

//Motor 2
int pinBIN1 = 12; //Direction
int pinBIN2 = 13; //Direction
int pinPWMB = 5; //Speed

//Standby
int pinSTBY = 7;


TB66MotorController motorController(pinAIN1, pinAIN2, pinPWMA, pinBIN1, pinBIN2, pinPWMB, pinSTBY);
~~~
Here is how to drive the motors:

~~~
//Drive both motors CW, full speed
motorController.motorDrive(MOTOR_A, MOTOR_FORWARD, 255);
motorController.motorDrive(MOTOR_B, MOTOR_FORWARD, 255);
~~~
