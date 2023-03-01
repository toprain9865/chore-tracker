<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a>

# Chore Tracker

A device to track up to 5 chores around the house. I am currently tracking my clothes washer, clothes dryer, dishwasher, trash, and recycling. The indicators are WS2812 LEDs, allowing customization of the indicator colors, patterns, etc.

I have additionally included a DHT22 temperature and humidity sensor.

## Code

I used ESPHome and Home Assistant to do all the heavy lifting. You can find the basic code to get everything on the PCB into an ESPHome configuration.

## Body

The body is deep enough to comfortably hold all the components as well as a generous amount of extra wire, in case you don't want to deal with getting everything the perfect length and just so. The hole in the model for the USB cord will fit a cord, but won't fit a terminated cord. You'll have to pull it through and then add the JST connector.

## PCB

When soldering the PCB, don't skimp out on the pin sockets. Both the ground and power planes are directly under the antenna, which isn't a performance issue if you use the pin sockets to get enough of a separation. I don't know how it might work if you solder it directly to the board.

I also designed the PCB to include a potentiometer to control the brightness of the LEDs. I ended up not using it, and instead just programming a fixed brightness that works well for me. Optional components for the potentiometer are listed below *in italics*.

## BOM

|Qty|Description|P/N|
|-|-|-|
|1|PCB|
1|Printed case
1|USB power cable|
|2|JST connector, 1x3, 2.54mm pitch
|2|JST PCB header, 1x3, 2.54mm pitch
6|JST connector, 1x2, 2.54mm pitch
6|JST PCB header, 1x2, 2.54mm pitch
1|esp8266 microcontroller|WeMos D1 mini
1|I<sup>2</sup>C I/O expander|MCP23008
1|DIP18 IC socket
2|10k resistor, 1/4 W, axial, len: 9.0mm, dia: 3.2mm
5|SPST momentary push button, 6mm cap, 6.9mm thread
5|WS2812B 5050 neopixel LEDs with PCB|
1|DHT22 compatible temperature & humidity sensor|AM2302
1|*JST connector, 1x3, 2.54mm pitch*
1|*JST PCB header, 1x3, 2.54mm pitch*
1|*Potentiometer*