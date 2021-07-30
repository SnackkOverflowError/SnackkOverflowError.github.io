---
title: "Hornet Motor Controller"
date: 2021-07-30T01:12:52-04:00
draft: false
---
[link to project](https://github.com/sahil-kale/MotorController)
### tldr 
Developing of a motor controller for brushed and brushless motors with features such as built-in PIDF feedback control, triangle, trapezoidal, and s-curve motion profile generation, and encoder feedback. It can interface with other devices using UART and CAN, and can be controlled via CAN or PWM.
### Purpose
The purpose of this project was to create a motor controller that can be used to drive both brushed and brushless motors, perform PIDF feedback control, generate motion profiles and interface over CAN, PWM, and UART. We wanted to replicate and build on features that we used in FRC with controllers like the Spark MAX and the CTRE Talon.
### Features
This project is still in development, however so far, from a hardware perspective, the motor controller supports UART and CAN communication, can take input via PWM, can be connected directly to a quad encoder, can accept up to 24V and output that to both brushed and brushless motors, and it can “brake” the motors as well. From a software perspective, the built in PIDF is supported, motion profile generators for trapezoidal and triangular profiles are supported, drivers for quad encoders, CAN, UART, and PWM input and output is also written. The driver for brushed motor output is also written.
This project makes use of a stm32f4 as its core, which was chosen as it meets our requirements for speed, has the necessary amount of timers, has support for CAN and for FreeRTOS.
### Future Features
Software features that we need to implement include the brushless driver and the state machine that controls the motor and makes use of the drivers. Another software improvement is support for S-curve motion profiles, the algorithm for which is currently in development
Hardware updates that we are looking into for version 2, include using a lower cost chip and adding another CAN line to the board so that the controller can be daisy chained over can.
