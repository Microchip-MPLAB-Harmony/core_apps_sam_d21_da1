---
parent: Harmony 3 driver and system service application examples for SAM D21/DA1 family
title: USART driver asynchronous - USART multi instance 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# USART driver asynchronous - USART multi instance

This example echoes the received characters over the two consoles using the USART driver in asynchronous mode.

## Description

This example uses the USART driver in asynchronous mode in both Bare-Metal and RTOS environments to communicate over two consoles. It receives and echoes back the characters entered by the user on the respective console.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_sam_d21_da1) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/driver/usart/async/usart_multi_instance/firmware** .

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

- To run the application, following additional hardware are required
  - [mikroBUS Xplained Pro board](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO)
  - [USB UART click board](https://www.mikroe.com/usb-uart-click)

- Connect the [mikroBUS Xplained Pro board](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO) to the EXT1 header
- Install an [USB UART click board](https://www.mikroe.com/usb-uart-click) on to the [mikroBUS Xplained Pro board](https://www.microchip.com/developmenttools/ProductDetails/ATMBUSADAPTER-XPRO)
- Connect the Debug USB port on the board to the computer using a micro USB cable (This will enumerate as a COM port)
- Connect mini USB cable to the [USB UART click board](https://www.mikroe.com/usb-uart-click) (This will enumerate the second port)

## Running the Application

1. Open the Terminal application (Ex.:Tera term) on the computer.
2. Connect to the EDBG/Jlink Virtual COM port and configure the serial settings as follows:
    - Baud : 115200
    - Data : 8 Bits
    - Parity : None
    - Stop : 1 Bit
    - Flow Control : None
3. Build and program the application using its IDE
4. Type a character and observe the output on the two consoles as shown below:
    - If success the character typed echoes back and an LED toggles on each time the character is echoed
    - **Console 1**

    ![output_async_usart_multi_instance_console_1](./images/output_async_usart_multi_instance_console_1.png)

    - **Console 2**

    ![output_async_usart_multi_instance_console_2](./images/output_async_usart_multi_instance_console_2.png)

Refer to the following table for LED name:

| Board | LED Name |
| ----- | -------- |
|  [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) | LED0 |
|||