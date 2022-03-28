# The Pocketbook is where things go to be remembered
Ideas that have yet to be realized or articles not-yet written. The pocketbook preserves them in memory so they can be later recalled. If an idea feels large or otherwise to-me-significant it likely has a page of its own.

## A 2D Spatial Image Sorter
I take a lot of photos and I have trouble sorting through them. So what if I could open my camera's SD card in a a little 2D plane and sort, using a graphics tablet for input (or a mouse, I suppose) literal small photos (like Polaroids, thumbnails) into cute little boxes. I can use the idea below for naming directories and creating new tags for photos. Oh, right, I want a tagging system, too.

---

## Gif Sequencer
My D3200 can capture images in a sequence at around 4-5 fps and sometimes I get some very pleasing pictures that I'd very much like to make into an animated gif. So, the idea:
A Rust program that uses gifed and the algorithm in colorsquash to quantize the image and then make the gif. It should be a very simple interface. You can crop the image to known values or some random free-form thing. Another rectangle selection will be used to pick the area the colors are taken from; a kind of subject indication. Use all the colors for the subject, and a few for the background. Maybe allow indicating what colors you want for the background, too?

---

## Flipnote
A lo-fi raster editor and animator designed to mimic the DSiWare Flipnote Studio.

I wrote here once "could also have an online service similar to Hatena but it seems I was beat to it (unsurprising!) by {!Sudomemo}! Figure out how Flipnote Studio talks to Flipnote Hatena and maybe we can directly integrate with them!

[Sudomemo]: https://www.sudomemo.net/

---

## Conversion Clipboard
A dear friend told me they convert heic files to a format that most other computers can read by taking a screenshot of the image in OSX's image viewer. This disturbed me.

A clipboard that reads the mime type and, upon some key combination (configurable, default to a variation fo ctrl+v), opens a menu that allows you to choose how to paste it. Whether that's as it is or converting an image to png/jpep/webp or an audio file to mp3/wav.