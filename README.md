gcc-arm-embedded for STM32L1 Discovery Kit

Runs blinky example from http://www.st.com/web/en/catalog/tools/PF259096

1. Download & install gcc-arm-embedded toolchain-
https://launchpad.net/gcc-arm-embedded/4.7/4.7-2013-q3-update/+download/gcc-arm-none-eabi-4_7-2013q3-20130916-win32.exe

2. Add the bin directory to your Path.
For me, this is C:\Program Files (x86)\GNU Tools ARM Embedded\4.7 2013q3\bin

3. Install codeblocks-
http://www.codeblocks.org/downloads/26

4. Run codeblocks, and configure compiler executables-
Go to Settings->Compiler..., select "GNU ARM GCC Compiler" in the dropdown.
Select the "Toolchain executables" tab and set the installation directory to the bin directory for the gcc-arm tools.
Also set the C compiler to "arm-none-eabi-gcc.exe" (sans quotes of course), and both linkers to arm-none-eabi-gcc.exe (same).

5. Open the codeblocks project file, stm32l100.cbp, and rebuild all (ctrl+f11).
Assuming that works, there should be a brand-new output file:
default/stm32l100.hex
You may need to tweak the path for the newlib-nano, under-
Project->Build Options->Search directories
