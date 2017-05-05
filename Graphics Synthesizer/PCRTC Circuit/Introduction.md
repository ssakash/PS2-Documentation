# PCRTC Circuit

The PCRTC (cathode ray tube controller) embedded in the Graphics synthesizer is responsible for all the video-signal generation and video output.

![img](https://snag.gy/61aAPu.jpg)

The PCRTC Circuit mainly consists of the following components,

* Memory Controller
* Sync Generator
* Two output circuits
* Merge Circuit
* Input Circuit
* Digital to Analog converter

## How it works:

* The memory controller reads the data from the framebuffer and passes it on to the two output circuits.

* The Sync Generator provides the necessary vertical and horizontal synchronization signals necessary for keeping the system in perfect synchronization. The signal is generated with the help of a Phase-locked loop.

* The data from the two output circuits are then passed to the merge circuit and the merge circuit merges the two contexts of output into a single one.

* The input circuit is capable of reading a specific rectangular area from the CRT output image and writing it to the framebuffer with the help of the memory controller. (This function is known as feedback write)

* The data from the merge circuit is then passed to a ``Digital to Analog converter (DAC)`` which finally transmits the analog data to the CRT.
