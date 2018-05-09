# JoyCon-Driver
A vJoy feeder / Driver for the Nintendo Switch JoyCons and Pro Controller on Windows with analog stick support and motion controls

## How to build
### Build wxWidgets-3.0.3
1. Download wxWidgets-3.0.3.7z sources here: https://github.com/wxWidgets/wxWidgets/releases/tag/v3.0.3
2. Extract content somewhere (Example: C:\dev\c++\wx\3.0.3)
3. Open C:\dev\c++\wx\3.0.3\build\msw\wx_vc11.sln with Visual Studio 2017 Community
4. Visual Studio will prompt for an update of the source files. Choose update to vc141.
5. After updating choose "Build > Build solution (F6)"

### Include wxWidgets-3.0.3
1. After building the project it can be included in the JoyCon-Driver project like this:
2. Open the JoyCon-Driver project in Visual Studio
3. Go to "Project > Properties"
4. Click on C/C++
6. Add C:\dev\c++\wx\3.0.3\include\msvc and C:\dev\c++\wx\3.0.3\include to the Additional Include Directories (in this order)
7. Click on Linker
8. Add C:\dev\c++\wx\3.0.3\lib\vc_lib to the Additional Library Directories
9. wxWidgets-3.0.3 is now included in the project.

## How to use
1. Install vJoy, here: http://vjoystick.sourceforge.net/site/

2. Setup your vJoy Devices to look like this (search for configure vJoy in Windows search):
    * ![Imgur](http://i.imgur.com/nXQDFPK.png)
    * Add a device for every controller you have, so if you have 4 JoyCons and 1 Pro Controller, enable 5 devices

3. Pair the JoyCon(s) / Pro Controller(s) to your PC

4. Run the Application, if it doesn't detect your JoyCon(s) / Pro Controller, make sure they are fully paired / connected and restart the program.
	* For the latest features and updates, just click check for updates, updating is (mostly) automatic

5. Once the program is running vJoy should register the input from the JoyCon(s) / Pro Controller.
    * To verify it's working you can use the vJoy monitor that comes with vJoy, it should look something like this: http://i.imgur.com/x4Fn7Cq.png
    * To re-pair the JoyCon(s) / Pro Controller go into Settings and remove them and then pair them again.
    * You'll likely want to use this with something like x360ce (http://www.x360ce.com), which will let you map the vJoy device to a virtual xbox controller for games that support them.

6. Here's a screenshot of the actual program:
	* ![Imgur](https://i.imgur.com/ihK9WNf.png)

## Settings and features (some settings are only in the config file!)
* Combine JoyCons
	* Combines a pair of JoyCons into a single vJoy device
* Reverse Stick X/Y
	* Reverses the X/Y direction(s) for both sticks
* Gyro Controls
	* Enables controlling the mouse with a JoyCon like a WiiMote
* Prefer Left JoyCon
	* By default, the right JoyCon is used (if found), this forces the program to use the left JoyCon (if found)
* Gyro Controls Sensitivity X/Y
	* Controls the sensitivity -> higher = more sensitive
	* The X sensitivity also controls the gyro sensitivity for Rz/sl0/sl1 in vJoy
* Gyroscope Combo Code
	* A number that tells the program which button or set of buttons to use to toggle gyro controls
	* To figure out what number to put in the config, look at the Gyro Combo Code when you press your desired keycombo
* Quick Toggle Gyro
	* Changes the behavior of the Gyro toggle from a standard switch, to a "always off unless keycombo is pressed" mode
* Invert Quick Toggle
	* Changes the behavior of the quick toggle from always off unless keycombo is pressed to always on unless keycombo is pressed
* Gyro Window
	* Opens up a visualizer for the JoyCon's gyroscope
* Dolphin Mode
	* Makes it so that the Rz/sl0/sl1 sliders in vJoy don't reset back to 0 when the JoyCon stops moving
* Mario Theme
	* Plays the Mario theme on the first connected JoyCon at startup
* Debug Mode
	* Prints debug info to the console
* Write Debug to File
	* Writes the debug info to a file
* Force Poll Update
	* Don't use this, probably
* Broadcast mode
	* Don't use this, probably

## Important Notes
* The JoyCons need to be re-paired anytime after they've reconnected to the switch

## Contact
* If you have any questions about anything the fastest way to reach me is probably my discord [server](https://discord.gg/jmcfdeS) or (fosse#0430) or twitter (@fosseisanerd) or even my email matt.cfosse@gmail.com
* If you find a bug please don't hesitate to make an issue, I'll try to respond within 24 hours if possible

## Donate
* If you like the project and would like to donate:
* https://paypal.me/matthewfosse
* BTC Address: 17hDC2X7a1SWjsqBJRt9mJb9fJjqLCwgzG
* ETH Address: 0xFdcA914e1213af24fD20fB6855E89141DF8caF96

## Thanks
* Thanks to everyone at: https://github.com/dekuNukem/Nintendo_Switch_Reverse_Engineering/
