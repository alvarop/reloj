# Reloj v1.2 Assembly Instructions

## Gather Materials
![Materials](pictures/IMG_2826.jpg)

Check the BOM and make sure you have all the required components.

**NOTE:** The IC sockets are optional, but do make debugging, repair, etc. much simpler in the end. You will have to modify the sockets for U19-U22 to fit the 7-segment LED footprints.

## Start Soldering!

![Bare board](pictures/IMG_6934.jpg)

I usually start with the lowest profile components so that I can flip the board over before soldering and they don't fall out as easily. In this case, start with R3.

![R3](pictures/IMG_6937.jpg)

I usually put all the components I plan on soldering in a particular stage and bend the leads on the other side to hold them in place while flipping the board over.

![Bent leads example](pictures/IMG_2829.jpg)

Continue with R2.

![R2](pictures/IMG_6938.jpg)

Next place R4, R5, R6, R7.

![R4-R7](pictures/IMG_6940.jpg)

The LED resistors come next. R8-R35. I did them in four stages to give myself room to solder. You could also do every other column at a time.

![LED Resistors 1](pictures/IMG_6941.jpg)

![LED Resistors 2](pictures/IMG_6942.jpg)

![LED Resistors 3](pictures/IMG_6943.jpg)

![LED Resistors 4](pictures/IMG_6944.jpg)

That's all the resistors. Next place C9 and C10.

![C9, C10](pictures/IMG_6945.jpg)

Now come the rest of the capacitors. (C1,C2,C3,C4,C5,C6,C7,C8,C11,C12,C13,C14,C15,C16,C17,C18,C21)

![C1,C2,C3,C4,C5,C6,C7,C8,C11,C12,C13,C14,C15,C16,C17,C18,C21](pictures/IMG_6946.jpg)

Time to install the IC sockets!

![IC Sockets](pictures/IMG_6947.jpg)

Before installing the sockets for U19-U22, cut off the extra leads so they fit in the socket.

![Socket before modification](pictures/IMG_2814.jpg)

![Socket modification](pictures/IMG_2815.jpg)

![Socket after modification](pictures/IMG_2816.jpg)

![Socket in place](pictures/IMG_2817.jpg)

Time to install the two buttons.

![Buttons](pictures/IMG_6948.jpg)

Next comes the tiny crystal Y1. I also forgot to take a picture in between but after the crystal install the pin headers J1.
![Y1, J1](pictures/IMG_6950.jpg)

Now comes the potentiometer RV1.
![RV1](pictures/IMG_6951.jpg)

Finally, the last component on this side, the electrolytic capacitor C22. Make sure the shorter lead goes in the negative side (filled in white silkscreen).

![C22](pictures/IMG_6953.jpg)

Before soldering the USB connector J2, make sure you flip the board! The footprint can go on both ways, which is unfortunate.

![USB Footprint](pictures/IMG_2832.jpg)

![USB Connector](pictures/IMG_2833.jpg)

![Finished!](pictures/IMG_6956.jpg)

Time to put in the jumper on J1 to select your clock. You can use the full 7400-series path with the 555 timer as the clock source or the "Alt" clock that uses the crystal oscillator for much lower drift.

That's it! If you happen to have a current-limited power supply, use that to power it up first.

## Adjusting the clock
Potentiometer RV1 can be used to adjust the 10kHz clock source. You'll need a frequency counter, oscilloscope, or other equipment to monitor this while you adjust.

To increment the minute count, press SW1. To increment the hours, press SW2. There's no button debouncing, so sometimes the value will go up by more than one.

When you first power it up, the clocks might read impossible times like **75:89**. That's ok. Just use the buttons to increment them until they reset back to 0.

## Troubleshooting
If things aren't working, first make sure all the IC's are inserted correctly. Notch up and no bent pins. Make sure the clock select jumper is in place as well.
