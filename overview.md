# Overview
The basic ideas of this project is following:
* Do not waste time on hardware
* Use as many digital components as possible, to eliminate design concerns on analog
* Make it easy to develop
* Use mixed C/C++
* Use FreeRTOS for task managing and resource management

To observe the ideas above, the micromouse features:

* STM32F446RET 32-bit ARM Cortex-M Microcontroller @180MHz
  * 512kB of Flash, 128kB of SRAM
  * One of the fastest microcontroller for 64-pin package
* VL6180X ToF Range sensor \*3 (or \*4)
  * Eliminates analog concern of Infrad LEDs/Phototransistors combo
  * Use PCA9546A I2C multiplexer to communicate between 4 indentical sensors
* MAX14871 full-bridge DC motor driver \*2
  * Avoids electrical and timing issues on H-bridge and MOFSET design
* Micro SD card reader
  * Easy to log and read data for designers, instead of use of SPI memory
* 4 Character LED display
* MPU9250 digital Inertial Measurement Unit (IMU)
* 5:1 Micro Metal Gearmotor HP by Polou *2
  * AS5304B magnetic encoder & AS5000-MR20-44 magnetic ring combo for rotary encoder of each motors