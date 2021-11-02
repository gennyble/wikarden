# Algorithms for changing the colors in images
A set of algorithms for processing images. These algorithms assume your color components are floats where 0 is no value and 1 is full value.
This research was done for rawproc and easyraw.

Still a seedling. See notes under Writings in {todo}.

## Raw Images
A raw image is produced by certain cameras when in their raw mode. It might have a file extension like `nef`, `dng`, or `heic`. When you shoot in raw, the camera does minimal processing to the image so it's something you *must* do later to get a usable image.

### Black Level

### White Balance

### Exposure

### Demosaicing

### Color Correction

### Brightness

### Saturation

### Contrast
The algorithm for a global contrast applied to the whole image. For the RGB color model.
`adjustment * ( value - 0.5 ) + 0.5`

You can see how the contrast algorithm works to move values away from the center and make them more extreme. The subtraction of half-max essentially makes the sign an indicator of whether or not `value` is above/below the middle-gray. `adjustment` then, if >1, moves it further from that gray, increasing the darkest-lightest difference.

 - {{Algorithms to increase or decrease the contrast of an image | https://math.stackexchange.com/a/906280}}