# GIF, However You Pronounce It
GIF stands for Graphics Interchange Format. It's a useful little thing for storing images and animations 

*This page is a still young and very incomplete, but it's on the {todo} and being worked on actively. Check back later <3*

## Structure of a GIF: Block by Block
Gif is a block based file format which, in my opinion at least, makes parsing it a bunch easier. There are two specifications, 87a and 89a. 87a could be called the base while 89a extends that and adds some functionality.

An important thing to note: Where relevant, like with 16-bit ints, **gifs are little endian**. This troubled me for some time because I apparently cannot read, but I now understand and my GIFs are displayable!

### Identifying a GIF: The Header
Identifying a gif is one of the easier things you'll do. If you don't trust the `.gif` file extension, or it doesn't have one, look for `GIF87a` or `GIF89a` as the first six bytes of the file.

The first three bytes mark it as a gif and the latter three indicate which version it is.

**Length:** 6 Bytes
*Required in 87a and 89a as the first six bytes*

### Your GIFs Profile: Logical Screen Descriptor
The Logical Screen Descriptor gives decoder the size of the canvas your gif will draw to as well as a few other important pieces of information.

**Logical Screen Width**: 16bit unsigned integer
**Logical Screen Height**: 16bit unsigned integer
The width and height of the canvas you can draw images on.

**Packed Field**: 1 Byte
*Bit 1*: Global Color Table Flag
Whether or not a color table follows this block.

*Bits 2-4*: Color Resolution
The number of bits per primary color available to the original image, minus one. That is, if this field is 7, the original image had 8bits available for the Red, Green, and Blue channels of the original image.

*Bit 5*: Sort flag (89a) or Reserved (87a)
For 87a, this bit should be set to 0 while encoding and ignore for decoding.
For 89a, indicates to the decoder that the Global Color Table is sorted with the most frequent color appearing first.

*Bits 6-8*: Size of Global Color Table


**Background Color Index**: 1 Byte
**Pixel Aspect Ratio**: 1 Byte

**Length**: 7 Bytes
*Required in 87a and 89a directly after the header*

- {!gif87a}
- {!gif89a}
- {!Netscape Looping Extension | netscape}

[gif87a]: https://www.w3.org/Graphics/GIF/spec-gif87.txt
[gif89a]: https://www.w3.org/Graphics/GIF/spec-gif89a.txt
[netscape]: http://www.vurdalakov.net/misc/gif/netscape-looping-application-extension