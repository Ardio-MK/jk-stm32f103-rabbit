/******************** (C) COPYRIGHT 2010 STMicroelectronics ********************
* File Name          : readme.txt
* Author             : MCD Application Team
* Version            : V3.2.1
* Date               : 07/05/2010
* Description        : Description of the USB JoyStickMouse Demo.
********************************************************************************
* THE PRESENT FIRMWARE WHICH IS FOR GUIDANCE ONLY AIMS AT PROVIDING CUSTOMERS
* WITH CODING INFORMATION REGARDING THEIR PRODUCTS IN ORDER FOR THEM TO SAVE TIME.
* AS A RESULT, STMICROELECTRONICS SHALL NOT BE HELD LIABLE FOR ANY DIRECT,
* INDIRECT OR CONSEQUENTIAL DAMAGES WITH RESPECT TO ANY CLAIMS ARISING FROM THE
* CONTENT OF SUCH FIRMWARE AND/OR THE USE MADE BY CUSTOMERS OF THE CODING
* INFORMATION CONTAINED HEREIN IN CONNECTION WITH THEIR PRODUCTS.
*******************************************************************************/

Example description
===================
This Demo provides a description of how to use the USB-FS-Device on the STM32F10x 
devices.
The STM32F10x device is enumerated as an USB-FS-Device Joystick Mouse, that uses 
the native PC Host USB-FS-Device HID driver.
The Joystick mounted on the STM3210B-EVAL, STM3210C-EVAL and STM3210E-EVAL boards 
is used to emulate the Mouse directions.

More details about this Demo implementation is given in the User manual 
"UM0424 STM32F10xxx USB development kit", available for download from the ST
microcontrollers website: www.st.com/stm32


Directory contents
==================
 + \inc: contains the Demo firmware header files
 + \EWARMv5: contains pre-configured projects for EWARM5 toolchain
 + \RIDE: contains pre-configured projects for RIDE toolchain
 + \MDK-ARM: contains pre-configured projects for MDK-ARM toolchain
 + \HiTOP: contains pre-configured projects for HiTOP toolchain
 + \TrueSTUDIO: contains pre-configured projects for TrueSTUDIO toolchain           
 + \src: contains the Demo firmware source files


Hardware environment
====================
This example runs on STMicroelectronics STM3210B-EVAL, STM3210C-EVAL and 
STM3210E-EVAL evaluation boards and can be easily tailored to any other hardware.
To select the STMicroelectronics evaluation board used to run the example, uncomment
the corresponding line in platform_config.h file.

  - STM3210B-EVAL Set-up 
     - Jumper JP1 (USB disconnect) should be connected in position 2-3.

  - STM3210E-EVAL Set-up 
     - Jumper JP14 (USB disconnect) should be connected in position 2-3.

  - STM3210C-EVAL Set-up 
     - Jumper JP17 (I2C_SCK) should be connected.


How to use it
=============
 + MDK-ARM
    - Open the JoyStickMouse.uvproj project
    - In the build toolbar select the project config:
        - STM3210B-EVAL: to configure the project for STM32 Medium-density devices
        - STM3210C-EVAL: to configure the project for STM32 Connectivity-Line devices
        - STM3210E-EVAL: to configure the project for STM32 High-density devices
        - STM3210E-EVAL_XL: to configure the project for STM32 XL-density devices
    - Rebuild all files: Project->Rebuild all target files
    - Load project image: Debug->Start/Stop Debug Session
    - Run program: Debug->Run (F5)
    Note: The intialization file "STM32DBG.ini" is used to allow debugging in stop 
    mode.     

 + EWARM5
    - Open the JoyStickMouse.eww workspace.
    - In the workspace toolbar select the project config:
        - STM3210B-EVAL: to configure the project for STM32 Medium-density devices
        - STM3210C-EVAL: to configure the project for STM32 Connectivity-Line devices
        - STM3210E-EVAL: to configure the project for STM32 High-density devices
        - STM3210E-EVAL_XL: to configure the project for STM32 XL-density devices
    - Rebuild all files: Project->Rebuild all
    - Load project image: Project->Debug
    - Run program: Debug->Go(F5)

 + RIDE
    - Open the JoyStickMouse.rprj project.
    - In the configuration toolbar(Project->properties) select the project config:
        - STM3210B-EVAL: to configure the project for STM32 Medium-density devices
        - STM3210C-EVAL: to configure the project for STM32 Connectivity-Line devices
        - STM3210E-EVAL: to configure the project for STM32 High-density devices
        - STM3210E-EVAL_XL: to configure the project for STM32 XL-density devices
    - Rebuild all files: Project->build project
    - Load project image: Debug->start(ctrl+D)
    - Run program: Debug->Run(ctrl+F9) 

 + HiTOP
    - Open the HiTOP toolchain, a "using projects in HiTOP" window appears.
    - Select open an existing project.
    - Browse to open the JoyStickMouse.htp:
        - under STM32F10B_EVAL directory: to select the project for STM32 Medium-density devices.
        - under STM32F10C_EVAL directory: to select the project for STM32 Connectivity-Line devices.
        - under STM32F10E_EVAL directory: to select the project for STM32 High-density devices
        - under STM32F10E_EVAL_XL directory: to select the project for STM32 XL-density devices
    - "Download application" window is displayed, click "cancel".
    - Rebuild all files: Project->Rebuild all
    - Click on ok in the "download project" window.
    - Run program: Debug->Go(F5). 

 + TrueSTUDIO
    - Open the TrueSTUDIO toolchain.
    - Click on File->Switch Workspace->Other and browse to TrueSTUDIO workspace 
      directory.
    - Click on File->Import, select General->'Existing Projects into Workspace' 
      and then click "Next". 
    - Browse to the TrueSTUDIO workspace directory and select the project:  
        - STM3210B-EVAL: to load the project for STM32 Medium-density devices
        - STM3210C-EVAL: to load the project for STM32 Connectivity line devices
        - STM3210E-EVAL: to load the project for STM32 High-density devices
        - STM3210E_EVAL_XL: to load the project for STM32 XL-density devices
    - Rebuild all project files: Select the project in the "Project explorer" 
      window then click 
      on Project->build project menu.
    - Run program: Select the project in the "Project explorer" window then click 
      Run->Debug (F11)

NOTE:
 - Low-density devices are STM32F101xx, STM32F102xx and STM32F103xx 
   microcontrollers where the Flash memory density ranges between 16 and 32 Kbytes.
 - Medium-density devices are STM32F101xx, STM32F102xx and STM32F103xx 
   microcontrollers where the Flash memory density ranges between 64 and 128 Kbytes.
 - High-density devices are STM32F101xx and STM32F103xx microcontrollers where
   the Flash memory density ranges between 256 and 512 Kbytes.
 - XL-density devices are STM32F101xx and STM32F103xx microcontrollers where
   the Flash memory density ranges between 512 and 1024 Kbytes.
 - Connectivity line devices are STM32F105xx and STM32F107xx microcontrollers.

******************* (C) COPYRIGHT 2010 STMicroelectronics *****END OF FILE******
