# Useful programs with small codebases
A lot of these I made because I couldn't find something out there to do it for me.

## {!towebp}
A very simple program leveraging the power of the webp ({!lib.rs | webp-lrs}) and image ({!lib.rs | image-lrs}) crates to convert "standard" formats, like png and jpeg, to webp images.

`-l`, `--lossless` a flag for lossless quality
`-q`, `--quality` an optarg to select the quality of the lossy compression. Floats 0-100

[towebp]: https://github.com/gennyble/towebp
[webp-lrs]: https://lib.rs/crates/webp
[image-lrs]: https://lib.rs/crates/image
