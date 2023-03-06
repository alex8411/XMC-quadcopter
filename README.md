# XMC quadcopter
DIY Infineon XMC4500 Microcontroller based flight controller and quadcopter full assembly.

This tutorial is based on the original work of jherkenhoff, see the link: https://github.com/jherkenhoff/XMC_Cleanflight_Doc
Whereas the original GIT / tutorial was focusing on the Flight Controller bringup, this GIT is focused on the whole drone assembly incl. flight controller, from scratch. 

The flight controller Cleanflight was ported for the Infineon XMC4500 MCU (ARM Cortex M4 based) on the "Cerasus" PCB.

For those unfamiliar with Cleanflight. It is an open source flight-controller firmware which is used on a broad range of commercial and open source flight-controllers. Since it is targeted towards 32 bit MCU's it provides a perfect base for the Cerasus board / XMC4500 MCU.

First Bringup:
- flash the Flight Controller software using Infineon DAVE Eclipse based IDE and an Infineon MiniWriggler or XMCFLasher tool
- download and start the Cleanflight web browser plugin to see if you can connect to the flight controller board via USB
- if you can connect properly, you wil be able to see the gyro based moves of your board int the web browser
- mount the flight controller board and motors driver board on the chassis and test if the motors are turning when operated from the Browser Cleanflight GUI
WARNING : 
- do not put any propeller or nut on the motors axis for now, maybe just a tape to see in which direction they are moving
- do not connect the 4S (14,7V) battery at first, just test the flight controller board via USB. Once done you can connect the motors driver board as below to the flight controller and supply 14,7V with an external supply where you can control the max current, limit it to a low value such as 200mA at first, to manage if any shortcut (too high current) happens, only after checking that the motor turn slowly, you can increase the max current limit on you ext supply.


![full_schematics](https://user-images.githubusercontent.com/53020923/223108481-814bab0e-bc21-4113-b43a-16c47adb46a4.png)



![bringup_connector_to_ExtSupply_not_battery_to_limit_current_in_case_of_shortcut](https://user-images.githubusercontent.com/53020923/223106977-fccb53e2-6074-4c39-b3ed-4e173cd35fe9.jpg)


![drone_first_bringup_20230304](https://user-images.githubusercontent.com/53020923/223107001-305f6b54-2690-4eec-adb0-e4f18266bb32.jpg)
