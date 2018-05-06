## Purpose:

This is to document the ongoing progress of building and training an RC car to drive itself using the open source Donkeycar platform. The Donkeycar repo is located [here](https://github.com/wroscoe/donkey).

## Origin: 

I originally wanted to start this project for 2 reasons.
- I have always been interested in robotics, so I felt this would be a great project to experiment with.

- I really enjoyed the behavioral cloning project I completed as part of my Udacity nanodegree program, and thought it would
be cool to work with the same theory on a tangible project. My behavioral cloning project can be found [here](https://github.com/DavidG1011/Udacity-Behavioral-Cloning---P3).

## Electronic Parts:

- 1/16 2.4Ghz Exceed RC Blaze.
- Raspberry Pi 3 Model B.
- SunFounder PCA9685 16 Channel 12 Bit PWM Servo Driver.
- SainSmart Wide Angle Fish-Eye RPi Camera.
- Maxmoral 10cm Dupont Female to Female Jumper Wire.
- 6700mAh Anker Astro E1 Power Bank.

## Structural Parts:

- Masonite.
- Velcro Cable Ties.
- Shell cover from D-Link KVM switch.
- RC car chassis.

## General Behavior Theory:

- Car driven manually to record desired behavior for the vehicle.
- Images and actuator values synced to more powerful system for training model. 
- Images and actuator values used to train a model for inferencing.
- Model is synced back to Raspberry Pi.
- Model is used to inference frames from camera for autonomous operation. 


## Specific System Functionality And Design:

- 1/16 2.4Ghz Exceed RC Blaze: The basis for the whole project. This model of RC car was specifically picked due to it having a separable reciever and ESC (Electronic Speed Control).  This means that it's easy to bypass the reciever, so it can be controlled by other means. 

- Raspberry Pi 3 Model B: The brain for the RC car. Handles: sending signals for actuation, recording behavior during manual operation, transfering images, inferencing for autonomous operation.

- SunFounder PCA9685 16 Channel 12 Bit PWM Servo Driver: Recieves commands from the Raspberry Pi. Handles actuation of the RC car motor and steering servo.

- SainSmart Wide Angle Fish-Eye RPi Camera: Eyes of the system. Connects to the Raspberry Pi. Records images to use for model training, as well as observing car postion for autonomous inferencing. The wide angle lens provides sufficient coverage of the driving surface.  

- Maxmoral 10cm Dupont Female to Female Jumper Wire: Connects the Raspberry Pi to the servo driver to provide power and actuation commands. 

- 6700mAh Anker Astro E1 Power Bank: Used to power the Raspberry Pi, and by extention, the servo driver. 

## The Journey:

### Prototyping:
First, the car chassis needed to be modified so that the components needed would fit on the car. The first design was simple, just a piece of masonite fitted over the existing pegs that held the original car shell. A backboard was also added for fitting the camera, but this was ultimately too small to see the entire driving surface. 






