# Frame_GFX_Compatible
A simple flexible frame buffer that is compatible with the adafruit GFX library

Adafruit provide some nice kit and useful libraries ... (see https://github.com/adafruit)

But I'm building my own hardware all the time to do all sorts of display stuff ...

So I decided to start saving some time and use their graphics library but I need a flexible way to define my frame buffer that matches my hardware not their examples.

This frame buffer provide an intermediate bit of RAM in which I can draw and 'print' and manipulate then then I write my own routines to squirt this out to the hardware I'm working with. this makes drawing images and text easy and hardware independent (size restrictions aside)

So far I've adapted this to use:

1. VFD dot matrix boards I designed (7 dot tubes IV26 large and IV25 small)
2. Flip-Dot bus sign I salvaged (96x16 flip dot array)
3. RGB matrix boards of WS2812 (various snake layout also working on being able to combine tiles)
4. Nixie tubes of various sorts

These are connected by serial, SPI, I2C, or some sort of GPIO

some more projects I'm working on will include

1. VFD matric display e.g. GU7000 series
2. some electromechanical displays I'm looking at (old score board/ petrol station as massive display elements)
3. more Nixie tubes maybe even a mega sized array?


Options for the frame buffer include:
- Width
- Height
- Window Width   (view able window allows fast pan/scan/scroll) 
- Window Height
- Bit depth      (anything from single bit to 16 bit for colours)
- Row ordered
- Col ordered
- LSB endian
- MSB endian

For some targets I've written some optimised functions for drawing, and split area select to allow mixed scrolling
Best of all I can now start making my application code more generic and common between the device I design and so reduce my design cycle time (I need to get round to upload some of these projects)

I'm in process of tidying up the code and sorting out a few Arduino issues then I'll be uploading the source
