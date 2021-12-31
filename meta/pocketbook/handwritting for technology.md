# Inputting Text With a Graphics Tablet
Instead of a clunky on-screen keyboard where you have to "peck" the letters in, what if you could just write them? Not OCR, that is hard and wasteful and doesn't work all that great. 

## The Surface
A 5x5 grid where you write. If you cross a cell with your pen, it's considered to be a part of the pattern. You draw here and not in Latin letters. It's a new writing system meant specific for interacting with your computer.

The grid need not be uniform either. It can have more detection in the middle as that's likely where you'll be writing. It need not even be square. Could it have hexagons or triangles? What is the best shape for non-straight lines?

### Other Bits
Some kind of selection mode so you can go back and edit text. It'd be nice if this could happen on the main surface. Some kind of stroke to initiate it and then tracking the current position of the pen, maybe, and moving the selection using arrow key inputs.

Capital letters, in languages where required, could be a stroke going across the bottom of the surface as if you're underlining it andsaying "You're important, get bigger!"

Common letter combinations can have patterns, too. English's th-, ch-, -ing, -tion. Can we get a symbol for every Toki Pona word? There aren't many. That would make it so you're normally inputting whole words and would only have to stop to write letters for a name or the like.

#### English
At first it can have a few patterns for letters. A way to detect errors? H(o|u)ffman? You can set patterns? How? A percentage of the cell hit, maybe? Detecting user-defined patterns would be harder than programmed ones, I imagine, but maybe not? Why would it be?

#### Toki Pona
I've yet to learn this lovely language, but I do seem to remember that it has less symbols than english. This is a good thing indeed. I think it's fit for this task.

Toki Pona doesn't use capitals except for unofficial words, which would mean we might be able to assign it a longer stroke as they're not input often.

#### Stenography
While this seemed promising at first, it seems stenotype requires pressing multiple keys at once which doesn't do well here as there is presumably only one pen.