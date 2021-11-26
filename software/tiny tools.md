# Useful programs with small codebases
A lot of these I made because I couldn't find something out there to do it for me.

## {!towebp}
A very simple program leveraging the power of the webp ({!lib.rs | webp-lrs}) and image ({!lib.rs | image-lrs}) crates to convert from classic formats, like png and jpeg, to webp.

Your output file will be in the same place and with the same name as your input, but with a `.webp` extension. If you don't give any options, `-q 80` is assumed.

`towebp FILE [options]`
`-l`, `--lossless` a flag for lossless quality
`-q`, `--quality` an optarg to select the quality of the lossy compression. Floats 0-100

[towebp]: https://github.com/gennyble/towebp
[webp-lrs]: https://lib.rs/crates/webp
[image-lrs]: https://lib.rs/crates/image

## {!neam}
A small, little program to scale PNGs using Nearest Neighbor. PNG encoding/decoding provided by the png ({!lib.rs | png-lrs}) crate.

`neam FILE [options]`
`-s`,`--size` the output image size. Use an x or coma to separate the width and height, like `width`x`height`.
`-o`,`--output` name of the output file. Defaults to the input name with `_widthxheight` appended.

[neam]: https://github.com/gennyble/neam
[png-lrs]: https://lib.rs/crates/png