---
parent: Harmony 3 driver and system service application examples for SAM D21/DA1 family
title: Console Debug System Service using USB 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# Console Debug System Service using USB

This example application demonstrates the USB based console and debug system service.

## Description

- The application example demonstrates console and debug system service using two instances of console, each connected to an instance of the USB CDC function driver
- These will appear as two COM ports on the host PC
- The example first demonstrates the various debug system service APIs/macros.
- It then demonstrates the console related APIs.
- The application asks the user to enter a character on one console which is echoed back on the second console (and vice-versa), using the console system service read/write APIs.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/core_apps_sam_d21_da1) and then click Clone button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/system/console_debug/sys_console_debug_usb_read_write/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| sam_d21_xpro.X | MPLABX project for [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
| sam_d21_xpro_freertos.X | MPLABX project for [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
| sam_da1_xpro.X | MPLABX project for [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| sam_d21_xpro.X <br> sam_d21_xpro_freertos.X | [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
| sam_da1_xpro.X | [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) |
|||

### Setting up [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro)

- Connect the Debug USB port on the board to the computer using a micro USB cable
- Connect the Target USB port on the board to the computer using a micro USB cable

### Setting up [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO)

- Connect the Debug USB port on the board to the computer using a micro USB cable
- Connect the Target USB port on the board to the computer using a micro USB cable

## Running the Application

1. Build and program the application using its IDE
2. Attach the device to the host. If the host is a personal computer and this is the first time you have plugged this device into the computer, you may be prompted for a .inf file.

    ![found_new_hardware](images/found_new_hardware.png)

3. Select the "Install from a list or specific location (Advanced)" option. Specify the \<install-dir\>/core_apps_pic32mz_ef/apps/system/console_debug/sys_console_debug_usb_read_write/inf directory.

    ![select_inf_location](images/select_inf_location.png)

    **Note:**
    - As an option, to specify the driver, you may open the device manager and expand the Ports (COM & LPT) tab, and right click on "Update Driver Software..."

        ![cdc_d1a](images/cdc_d1a.png)

    - Verify that the enumerated USB device is seen as a virtual USB serial comport in Device Manager.

        ![cdc_d2](images/cdc_d2.png)

4. Once the device is successfully installed, open up two instances of a terminal program, such as Tera Term. Select the appropriate COM port for each of these terminal instances. The following screen shot shows the COM port selection for the Tera Term terminal program.

    ![com_port_selection](images/com_port_selection.png)

5. Once the USB is enumerated
    - The LED on the demonstration board will be turned on.
    - Press the swtich on the development board and observe the following output on the terminals
    - The output on the console instance 0 prints the messages using the debug system service
    - It then prints the size of the receive buffer and asks the user to enter 10 characters on the terminal

    ![usb_console_output_1](images/usb_console_output_1.png)

6. Once, 10 characters are entered on console instance 0
    - The demonstration prints the free space available in the receive and transmit buffers
    - Since the receive buffer contains 10 unread characters, its free space will be reduced by 10
    - The received characters are read and echoed on the terminal
    - After this, the demonstration enters in echo test mode, where a character entered on console instance 0 will be echoed on console instance 1 and vice-versa

    ![usb_console_output_2](images/usb_console_output_2.png)

7. Enter a character on console instance 0 terminal and observe it getting echoed on console instance 1 terminal and vice-versa

    ![usb_console_output_3](images/usb_console_output_3.png)

Refer to the following table for LED and Switch name:

| Board | LED Name | Switch Name |
| ----- | -------- | ----------- |
|  [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) | LED0 | SW0 |
|  [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) | LED0 | SW0 |
|||
