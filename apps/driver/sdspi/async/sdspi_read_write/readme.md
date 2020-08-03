[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SDSPI driver asynchronous - SDSPI Read Write

This example application shows how to use the SDSPI driver in asynchronous mode to perform non-blocking operations on the SD Card Media

## Description

- The asynchronous mode of the SDSPI driver is configured to use DMA and performs non-blocking read and write operations
- This application writes 4KB (4096 bytes) of data starting at the SD Card memory location 0x2000, using the SDSPI driver.
- The application then reads and verifies the written data.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_sam_d21_da1) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/sdspi/async/sdspi_read_write/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| sam_d21_xpro.X | MPLABX project for [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| sam_d21_xpro.X | [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
|||

### Setting up [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro)

- To run the demo, the following additional hardware are required:
  - [IO1 Xplained PRO Extension Kit](https://www.microchip.com/developmenttools/ProductDetails/ATIO1-XPRO)
  - One micro-sd card
- Connect the [IO1 Xplained PRO Extension Kit](https://www.microchip.com/developmenttools/ProductDetails/ATIO1-XPRO) to the EXT1 header
- Insert the micro-SD Card in the [IO1 Xplained PRO Extension Kit](https://www.microchip.com/developmenttools/ProductDetails/ATIO1-XPRO)
- Connect the Debug USB port on the board to the computer using a micro USB cable

## Running the Application

1. Build and program the application using its IDE
2. The LED is turned ON when the read data from the SD card matches with the written data

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) | LED0 |
|||
