# STM32-USB-Target

## Introduction

We will check and test STM32 series development kit to inspect USB target connectivity of Windows.

Target boards:
- NUCLEO-L552ZE-Q: STM32 Nucleo-144 for STM32L552 ultra-lowpower MCUs
- STM32F746G-DISCO: STM32F746 Discovery kit
- STM32 Nucleo-F411RE Nucleo-64 development board with STM32F411RE MCU
- and some other boards

Notice:
- STM32CubeMX
  STM32CubeMX is a source code generator.

- STM32CubeF7
  STM32CubeMX is a source code library.

Most of STM32 boards support support one of these.

- STM32CubeIDE:
  Delevopment Environment.

### Important Notice
The source of the confusion is that even though MX does not support F7 boards and F7 libraries, the **Embedded Software Packages Manager** that comes with MX supports their installation and management.
In particular, using the "Embedded Software Packages Manager" is important for putting the source code in the "where it should be". 


x At first, we will challenge to investigate STM32F746G-DISCO with STM32CubeMX.
  -- STM32CubeMX doesn't support STM32F746G-DISCO. Use STM32CubeF7 with extarnal tool.

@ At first, we will challenge to investigate STM32F746 with STM32F746G-DISCO.

## NUCLEO-L552ZE-Q
STM32 Nucleo-144 for STM32L552 ultra-lowpower 

### information Page

STM32 Nucleo-144 development board with STM32L552ZE MCU, SMPS, supports Arduino, ST Zio and morpho connectivity 

https://www.st.com/ja/evaluation-tools/nucleo-l552ze-q.html

This product may be for STM32Cube.

### Supported USB Device Function
NUCLEO-L552ZE-Q
    - CDC_Standalone CubeMX
    - DFU_Standalone CubeMX
    - HID_Standalone CubeMX

### How to start

Provide USB **micro-B** cable

If you connect to PC USB port with this, you can check the board works properly.

- Install STM32 CubeIDE
Integrated Development Environment for STM32
https://www.st.com/ja/development-tools/stm32cubeide.html

- Install STM32 CubeMX
STM32Cube initialization code generator
https://www.st.com/ja/development-tools/stm32cubemx.html

- Start STM32 CubeMX

- Install **STM32Cube MCU Package for STM32L5 Series** from STM32Cube **Embedded Software Packages Manager**.

- Click **ACCESS TO EXAMPLE SELECTOR** of Start My project from Example on STM32 CubeMX main manu.

- Search with Keyword of "USB_Device" on left pain and you can find berow sample projects for Nucleo L552ZE-Q.

    - CDC_Standalone
    - DFU_Standalone
    - HID_Standalone

Now we will try HID_Standalone.

- Select and double click HID_Standalone

- Enable ICACHE to enable Instaruction cache

- Select and double click HID_Standalone

Generated
C:\Users\Tom\STM32Cube\Example\HID_Standalone

Select 
Start new project from an existing STM32CibeMX configuration file (.ioc)
from STM32CubeIDE Home menu 

Choose
C:\Users\Tom\STM32Cube\Example\HID_Standalone

Run

Not worked...

Thren try DFU_Standalone
without enable cache

C:\Users\Tom\STM32Cube\Example\DFU_Standalone

Run

Not worked...

Thren try CDC_Standalone
without enable cache

C:\Users\Tom\STM32Cube\Example\CDC_Standalone

Run

Not worked...

Gave up to use STM32 CubeMX code generator.

Try samples...



## STM32F746G-DISCO
STM32F746 Discovery kit

### information Page

- Development Kit
https://www.st.com/ja/evaluation-tools/32f746gdiscovery.html

- Software tools (STM32CubeF7)
https://www.st.com/content/st_com/ja/products/embedded-software/mcu-mpu-embedded-software/stm32-embedded-software/stm32cube-mcu-mpu-packages/stm32cubef7.html

Getting started with STM32CubeF7
dm00180213-getting-started-with-stm32cubef7-mcu-package-for-stm32f7-series-stmicroelectronics.pdf P17

### Supported USB Device Function
STM32F746G-DISCO
- AUDIO_Standalone 
- DFU_Standalone 
- DualCore_Standalone 
- HID_LPM_Standalone 
- HID_Standalone 
- MSC_Standalone 


**IMPORTANT**

This product is not supported by STM32Cube.

### How to start

Provide USB **mini-B** cable

Install STM32 CubeIDE
*link

Install STM32 CubeMX
*link



