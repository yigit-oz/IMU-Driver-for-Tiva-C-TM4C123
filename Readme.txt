# IMU Driver for Tiva C TM4C123

This project implements a bare-metal IMU sensor driver for the Tiva C TM4C123.  
It communicates with a BMX160 IMU over I2C and streams gyroscope data over UART.

## Features
- Low-level I2C driver (register read/write, address scan)
- UART driver for serial data output
- BMX160 gyroscope initialization, configuration, and self-test
- Raw sensor data parsing and scaling to physical units

## How It Works
1. System clock, UART, and I2C peripherals are initialized
2. BMX160 is reset and set to normal operating mode
3. Gyroscope is configured (ODR, bandwidth, measurement range)
4. Raw gyro data is read via I2C
5. Data is scaled and transmitted over UART
