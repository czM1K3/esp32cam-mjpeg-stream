# ESP32CAM-mjpeg-stream

This code is originally from [RandomNerdTutorials.com](https://RandomNerdTutorials.com/esp32-cam-video-streaming-web-server-camera-home-assistant/)

## Requirements

* ESP32-CAM
  * Support list:
    * AI THINKER (tested and fully working)
    * M5STACK WITH PSRAM
    * M5STACK WITHOUT PSRAM
    * WROVER KIT (not tested)
* Programmer (I used [CP2102](https://www.aliexpress.com/item/33039615015.html))
* Dupont female to female cables (at least 5)
* IDE that supports PlatformIO (VSCode, Atom and [more](https://docs.platformio.org/en/latest/integration/ide/index.html?highlight=ide#desktop-ide)) or only PlatformIO Core

## Installation

1. Wire ESP with programmer like so: 
![Wire diagram](https://i1.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/12/ESP32-CAM-FTDI-programmer-5V-supply.png?w=750&ssl=1)
1. After that connect it to PC (**Otherwise you can fry your ESP**).
1. Clone this repository to your PC and open it with your favorite IDE.
1. If you open it with VSCode it will prompt you in bottom right corner to install PlatformIO. Otherwise go to plugin manager and download it from there.
1. Open configuration.h and change your WiFi details, uncomment your ESP type (mostly AI THINKER) and resolution (I recommend to use 800x600 or 1024x768 for AI THINKER) If you want to get messages from Serial connection (IP, errors) uncomment ```#define EnableDebug```.
1. Click on Upload button (in VSCode it is in left bottom corner).
1. Wait for upload (**Do not disconnect while uploading!**)
1. Unplug from USB, disconnect wire between GND and IO0 and re plug it to PC.
1. If you enabled Debug open serial monitor (In VSCode it is also located in left bottom corner).
1. Go to IP address of ESP and you should see stream.
1. If you have AI THINKER you can enter address followed by ```/flash``` and it will turn flash on or off (You can't have stream opened).