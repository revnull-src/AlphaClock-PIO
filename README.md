# AlphaClock FW (For PlatformIO)

Software for the [Alpha Clock Five](https://shop.evilmadscientist.com/tinykitlist/589) from [Evil Mad Scientist Laboratories](https://www.evilmadscientist.com/).

Complete documentation here: <http://wiki.evilmadscientist.com/Alpha_Clock_Five>

## PlatformIO

This fork of the AlphaClock firmware was modified to efficiently compile and upload using the [PlatformIO](https://platformio.org/platformio-ide) build environment. All build dependencies and required libraries should be automatically satisfied without installing additional software. The PlatformIO config includes several PIO project tasks that should cover the most common [bootloader baud rates](https://wiki.evilmadscientist.com/Alpha_Clock_Firmware_v2?section=5#Setting_the_upload_baud_rate), 57200 is the default. Please select the appropriate project task for your bootloader. If you are uncertain which to choose, try each until you get an upload response.

**NOTE:** This fork only contains the functional clock program. PlatformIO will download the AlphaClock library components as one of the build dependencies at compile time.

## Changes

* Renamed original AlphaClock.ino sketch to main.cpp following PlatformIO standards.
* Re-ordered functions to resolve compile-time errors.
* Small change to some functions to resolve String to Char conversion warnings at compile time.
* Removed "SYNC'D" display message after serial time sync. IMHO, this message becomes distracting when the time is updated regularly via the serial port.
