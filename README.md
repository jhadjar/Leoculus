# LEOCULUS - Automotive Video Interface

## Brief Summary:

&nbsp;

### What:

Leoculus is an interface to display analog video from a Rear View Camera on car monitors that only display digital video (Peugeot S.A., Tesla Motors, etc.). 


### Why:

There are after-market interfaces with many features for these cars, but they are expensive and most people want the RVC option the most. They're paying for things they don't really want. 


### How:
The interface transmits the camera feed when it's on reverse, and the on-board computer's feed otherwise. It's a 2 to 1 mux. It has to decode and serialize the input video signal first.

Here's a schematic:

![Schematic](https://github.com/jhadjar/Leoculus/blob/master/Doc/leoculus.png)

&nbsp;

* The camera's output/interface input is analog video, CVBS (Composite, Video, Blanking, Sync). 
* CVBS injected into processor/decoder for chroma/luma separation. Output is 8 bit BT656 / YCbCr video. 
* Serialization of YCbCr/BT656 for transmission over LVDS (Low-Voltage Differential Signaling).
* Injected into a multiplexer. Input selected when the car is on "reverse".
* The other multiplexer's input is active otherwise and relays what the head-unit normally shows.

| Input signal | Connector | Output Signal | Connector |
| --------------|-----------|----------------|-----------|
| On-board computer | LVDS-HSD | Digital video to LCD screen | LVDS HSD|
| RVC CVBS| RCA connector|
| Reverse light + GND | 2 pin connector|

&nbsp;

&nbsp;

### Details:

![CamSpecs](https://github.com/jhadjar/Leoculus/blob/master/Doc/cam.jpg)
