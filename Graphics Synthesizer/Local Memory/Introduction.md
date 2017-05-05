# GS Local Memory


The local memory of the Graphics Synthesizer is a 4MB memory space which consists of the following buffers,

* Frame buffer ``(Stores RGBA values of drawing result)``
* Z buffer ``(Stores Z value of the drawing result)``
* Texture buffer ``(Stores texture image data)``
* CLUT buffer ``(Stores the CLUT used when texture is an index colour)``

![buffer](https://snag.gy/MbaSjE.jpg)

## Memory

On the local memory, there are three different types of memory access units, they vary according to the type of processing being done.

* Memory access units
  - Page (8 kilobytes) ``(FBP/ZBP point to pages)``
  - Block (256 bytes) ``(TBP/SBP/DBP point to blocks)``
  - Column (64 bytes)

The GS local memory consists of 512 pages, 16,384 blocks and 65,536 columns.

Where,
* total memory = 512 pages (4MB)
* 1 page = 32 blocks
* 1 block = 4 columns
