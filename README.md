# EW270 Pulser GUI

## Installation Instructions

1. Ensure that you have MATLAB installed and an active license. I'm running 2024a.
2. Install the driver for whichever Serial to RS232 adapter you are using. The FTDI one for Windows is [here](https://ftdichip.com/wp-content/uploads/2025/03/CDM2123620_Setup.zip).
3. Download all of the files from this repository.
4. Run EW270_GUI.mlappinstall to install the application
5. Open MATLAB, ensure that the working directory is NOT the same location as the installer, and go to apps -> EW270_GUI

## Using the GUI

1. Open the device manager in Windows and figure out which COM port the device is attached to.
2. Open the GUI and select the correct COM port from the dropdown box, click connect, and wait for the device ID to be displayed.
3. Click "Read Configuration" to read the current config of the pulser. The config will only update when you click this button.
4. Changing any of the settings automatically sends commands to the device, so changes are made immediately.
5. Setups can be saved to or recalled from any of 16 profiles using the box in the bottom right. Select a profile and click save or recall. Profile 0 is automatically recalled when the pulser is powered on.

Note: All of the settings have limits that are defined in the pulser rather than by the GUI, so you will be able to enter values outside of this range. After changing a setting the pulser will do its best to give you what you wanted, and you can see if you have hit a limit by reading the configuration and checking that the required settings have been applied.

## Editing the GUI

If you want to add to or modify the GUI you can do so by downloading EW270_GUI.mlapp in the repository and opening it in MATLAB App Designer (requires a MATLAB license). You will also need to recompile the app into a binary, which will give you a new installer for the modified application. 
