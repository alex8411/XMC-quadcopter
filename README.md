# XMC quadcopter
DIY Infineon XMC4500 Microcontroller based flight controller and quadcopter full assembly.

This tutorial is based on the original work of jherkenhoff, see the link: https://github.com/jherkenhoff/XMC_Cleanflight_Doc
Whereas the original GIT / tutorial was focusing on the Flight Controller bringup, this GIT is focused on the whole drone assembly incl. flight controller, from scratch. 

The flight controller Cleanflight was ported for the Infineon XMC4500 MCU (ARM Cortex M4 based) on the "Cerasus" PCB.

For those unfamiliar with Cleanflight. It is an open source flight-controller firmware which is used on a broad range of commercial and open source flight-controllers. Since it is targeted towards 32 bit MCU's it provides a perfect base for the Cerasus board / XMC4500 MCU.

1st Bringup DONE: Hardware and motors simple control
- build and/or flash the Flight Controller software using Infineon DAVE Eclipse based IDE OR the SEGGER JFLASH Lite tool, AND an Infineon MiniWriggler or XMCFLasher Hardware debugger. CAUTION: the Debug/Flash is done via SWD pins, not the USB (Communication with PC / Cleanflight Appl SW Config later only)

![image](https://github.com/alex8411/XMC-quadcopter/assets/53020923/f170a32b-48b3-456b-baf6-34ddf2fa9139)

- download and start the Cleanflight web browser plugin to see if you can connect to the flight controller board via USB
- if you can connect properly, you wil be able to see the gyro based moves of your board int the web browser
- mount the flight controller board and motors driver board on the chassis and test if the motors are turning when operated from the Browser Cleanflight GUI
WARNING : 
- do not put any propeller or nut on the motors axis for now, maybe just a tape to see in which direction they are moving
- do not connect the 4S (14,7V) battery at first, just test the flight controller board via USB. Once done you can connect the motors driver board as below to the flight controller and supply 14,7V with an external supply where you can control the max current, limit it to a low value such as 200mA at first, to manage if any shortcut (too high current) happens, only after checking that the motor turn slowly, you can increase the max current limit on you ext supply.


![full_schematics](https://user-images.githubusercontent.com/53020923/225000396-94c44e37-3880-45eb-9cef-276a054b6754.png)

![supply_Cable_for_current_limit_bringup](https://user-images.githubusercontent.com/53020923/223108909-fee6594b-b4fb-4649-b664-825c47fc2b5e.png)

![drone_first_bringup_20230304](https://user-images.githubusercontent.com/53020923/223107001-305f6b54-2690-4eec-adb0-e4f18266bb32.jpg)

![4motors_bringup](https://user-images.githubusercontent.com/53020923/223109392-92ddcfb7-16fa-41e9-be3a-3f8d52831f3d.png)


 
![boards_stackup_and_assembly](https://user-images.githubusercontent.com/53020923/224997301-727d79b6-fb10-402d-8ecc-ec976826d33b.jpg)

![boards_stackup_and_assembly_2](https://user-images.githubusercontent.com/53020923/224997340-fd0a70fd-cba3-4bd5-bc68-5fe2686f5797.jpg)

...

2nd Bringup UNDER WORK: Remote control :
- bring up of the physical remote control instead of the PC Cleanflight GUI drone control
- optional : connect remote receiver pins to osci to see any signal when changing remote commands

NEXT STEPS:

3rd Bringup: Calibration of the Inertial Measurement Unit (e.g. Gyroscope) UNDER WORK
- after fixing the flight controller and brushless motors driver board on the drone structure you can now configure the gyroscope in the Cleanflight GUI
...

4th Bringup: Remote control : 
- build or buy a platform under the bench to calibrate the drone internal SW PID and the remote control commands range and sensitivity in cleanflight


