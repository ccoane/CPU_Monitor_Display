# CPU_Monitor_Display

![JIF](ReadmeImages/Example.gif?raw=true "JIF")

## Hardware:
* TTGO TDisplay (Arduino-based Microcontroller)
  * [Example Link](https://www.aliexpress.com/item/33048962331.html)
* USB C cable
* 3D Printed Case for the TTGO TDisplay
  * I modified [this model](https://www.thingiverse.com/thing:4501444) and filled in the face buttons

## Setup:
* Install Visual Studio Code (VS Code)
* Install the PlatformIO Extension in VS Code
* Install [HWInfo v6.4.2](https://www.fosshub.com/HWiNFO-old.html?dwl=hwi_642.exe)
* Download and install the [CP210x USB to UART Driver](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
* Open the project in VS Code and Build the project.
* Navigate to the TFT_eSPI Library folder in your Project directory
  * Example: \CPU_Monitor_Display\\.pio\libdeps\esp32dev\TFT_eSPI
* Make the following changes to the User_Setup_Select.h file:
  * Comment out "#include <User_Setup.h>"
  * Uncomment "#include <User_Setups/Setup25_TTGO_T_Display.h>"
  * Save Settings
* Download my modified version of [RemoteHWInfo](https://github.com/ccoane/remotehwinfo/releases)
  * Update the sensors.txt file as noted in the **Setup** section of the [Readme](https://github.com/ccoane/remotehwinfo/blob/master/README.md)
* Connect the TTGO T-Display and Upload the sketch.
* Start RemoteHWInfo
