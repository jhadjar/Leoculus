# LEOCULUS - Automotive Video Interface

## Brief Summary:

Leoculus is an interface to display analog video from a Rear View Camera on monitors found in several make of cars that only display digital video. It only displays the Rear View Camera (RVC) video feed when the car is on reverse and lets the Head Unit display on the monitor otherwise.

Here's a schematic:

![Schematic](https://github.com/jhadjar/Leoculus/blob/master/Doc/leoculus.png)


| Input signals | Output Signals|
| --------------|---------------|
| On-board computer – LVDS HSD connector | Digital video through LVDS to TFT LCD screen – LVDS HSD connector. |
| Rear view camera – RCA connector. | 
| Reverse light + GND – 2 pin connector.|
