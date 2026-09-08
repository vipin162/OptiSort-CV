# Overview 
This project is aimed at segregating objects like screws, nuts and other miscellaneous objects accurately with
almost no human intervention using computer vision and ESP32.

#### Sources 
https://blog.roboflow.com/automated-sorting-with-computer-vision/

https://www.researchgate.net/publication/399110003_Development_of_Vision_Based_Sorting_System_Using_Machine_Learning_for_Automated_Material_Classification

# Components 
- Microcontroller : ESP32
- IR Sensor Array : FC-51 obstacle avoidance sensor
  - used to detect the entry and exit of the object inside the inspection
- Stepper Motor : NEMA 17 stepper motor
  - Stepper driver : A4988 driver
  - To rotate the conveyor
- 12V DC power supply
- Servo Motor : SG90 micro servos
- 5V step-down buck converter

# How does it work ?
- Box containing screws, nuts, bolts and other miscellaneous object is placed completely on the feeding mechanism
-  The feeding mechanism makes sure that the only object at a time enters the inspection area
-  The inspection area is black box inside the box there are 2 IR sensors to detect the entry and exit of the objects.The box is illuminated by a white led light
-  The phone camera placed above the black box using captures the images of the objects using an IP camera app in a mobile phone these pictures are recognised by the laptop using openCV
-  The conveyor consists of 2 arms which are connected to the servo motors. As the objects moves if it is identified as a screw for example then conveyor stops near the box assigned to screw and the servo arm pushes the screw to the box and this process continues.
  
