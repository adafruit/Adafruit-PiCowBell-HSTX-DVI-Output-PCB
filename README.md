## Adafruit PiCowBell HSTX DVI Output for Pico - Works with HDMI Displays PCB

<a href="http://www.adafruit.com/products/6363"><img src="assets/6363.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit PiCowBell HSTX DVI Output for Pico - Works with HDMI Displays. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/6363

### Description

Ding dong! Hear that? It's the PiCowbell ringing, letting you know that the new Adafruit PiCowbell HSTX DVI Output for Pico is in stock and ready to display images and graphics from a microcontroller directly to an HDMI monitor or television! Note that it doesn't do audio, just graphics.

The PiCowbell is the same size and shape as a Pico and is intended to socket underneath to make your next video output project super easy. Mini HDMI connector for use with standard HDMI cables? Yes! STEMMA QT / Qwiic connector for fast I2C? Indeed. Reset button & extra switch for restarting code or changing configuration? Bien sur.

[Compared to the original DVI PiCowbell](http://www.adafruit.com/product/5745), this board has very similar setup:

* Uses the HSTX-specific pins for RP2350 usage, thats GPIO 12-19
* Has a slimmer slide-switch
* Adds 4 'USB host port' pads that can be used with PIO-USB to add a peripheral. We recommend a USB A socket cable for adding a proper USB host port.

You can use this board with either a Pico 1 (RP2040, using PIO-DVI) or Pico 2 (RP2350, using PIO-DVI or HSTX-DVI) . However, we recommend using the Pico 2 or Pico 2W with this board since you can use the improved HSTX peripheral which means you can save a PIO and processor time when generating video.

The PiCowbell provides you with:

* Right angle JST SH connector for I2C / Stemma QT / Qwiic connection. Provides 3V, GND, IO4 (SDA), and IO5 (SCL). Also connected through to the HDMI sink (monitor) with level shifting, so the EDID can be read.
* Mini HDMI connector for DVI output to any HDMI display or monitor.
	* GPIO12: D0+
	* GPIO13: D0-
	* GPIO14: Clock +
	* GPIO15: Clock -
	* GPIO16: D2+
	* GPIO17: D2-
	* GPIO18: D1+
	* GPIO19: D1-
* Pin breakout for HDMI extras: Utility, CEC, and HotPlug pins
* Reset button - Press to restart your program
* Slide switch - On GPIO #3 for whatever purpose you wish.
* USB host port pads - that can be used with PIO-USB to add a peripheral. We recommend a USB A socket cable for adding a proper USB host port.
* Many pads on the 'Bell have a duplicate hole pad next to it for solder-jumpering
* The ground pads have white silkscreen rectangles to easily identify
* Gold-plated pads for easy soldering

In Arduino, [we use our fork of PicoDVI (RP2040 or RP235)](https://github.com/adafruit/PicoDVI) or [Adafruit_DVI_HSTX (RP2350 only)](https://github.com/adafruit/Adafruit-DVI-HSTX) to create an internal framebuffer of 320x240 or 400x240 16-bit pixels that is then continuously blitted out as pixel-doubled 640x480 or 800x480 digital video. Whatever you 'draw' to the internal memory framebuffer appears instantly on the digital display in crisp color. Since the library is a subclass of AdafruitGFX, it'll be familiar to folks who have used our TFT or OLED displays before. 

[There's also DVI output support in CircuitPython](https://docs.circuitpython.org/en/latest/shared-bindings/picodvi/) - but note that it uses a lot of memory, so in particular if you want to use Pico with WiFi support, you should go with a Pico 2 since it has more SRAM.

We also connected the HDMI-connectors I2C pins to the SDA/SCL of the Pico (through a safe level shifter) so you can read the EDID EEPROM of displays, and have broken out the CEC and Utility pads. The Hot Plug Detect pin is also available. Read this pin to know when a display has been connected!

Each order comes with an assembled PCB and header. You will need to solder in the header yourself, but it's a quick task.

Please Note! There are numerous possible configurations, and we stock various headers depending on how you want to solder and attach. Especially if you want the Pico on top so that the BOOTSEL button and LED are accessible.

* Use the Pico Stacking Headers if you want to be able to plug into a breadboard or other accessory with sockets.
* Use the Pico Socket Headers if you want to plug directly in and have a nice solid connection that doesn't have any poking-out-bits.
* Use the Short Socket Headers for a very slim but pluggable design; note that you'll want to trim down the Pico's headers or use the short plug headers on the Pico to have a skinny sandwich.
* Solder the PCB directly to the Pico headers - of course, this is very compact and inexpensive, but you won't be able to remove the PiCowbell.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
