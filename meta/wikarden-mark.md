# Wikarden-Mark

This markup language is inspired by the {!Oscean Markup}, {!GemText}, and of course {!Markdown}.

[Oscean Markup]: https://wiki.xxiivv.com/site/meta.html
[GemText]: https://gemini.circumlunar.space/docs/cheatsheet.gmi
[Markdown]: https://commonmark.org/

# # Title
## ## subtitle
### ### section
#### #### subsection

How many heading levels do you really need? I guess I decided it was four.

### A Quick Note On Linebreaks

In Markdown, linebreaks are seen as kind of wibbly-wobbly, and I don't like that. If you break a line in Markdown, the next line will blow into the previous with a space added between. Instead of that, a line break is respected here. If you, for example...
break once! then you get a soft break, a `<br>` if we're generating HTML. It keeps it in the same paragraph but breaks the line. It's representative of how the text appears in the original file.

If you break twice, like I just did, you get a new paragraph. This is, again, representative of how the original file looks. It's kind of What You See Is What You Get, see, but not in a rich editor of some sort. Just vim'd do you well.

### *Inline Elements*

Interlinks
{meta}
`{meta}`

Reference Links
{!the homepage}
`{!the homepage}`
`[the homepage]: https://nyble.dev`

[the homepage]: https://nyble.dev

Absolute Links
{{https://nyble.dev}}
`{{https://nyble.dev}}`

You can name any kind of link- so that the text differs from what is displayed, like a reference link- with a pipe `|`. If I wanted to link you back to the {meta} but I wanted to proper-noun it and everything, I might do {The Meta | meta}. In the source that's `{The Meta | meta}`.

*Italic and also a bit of **bold** thrown in there. Without ending the italic, can we do **another bold?***

This derivative-of-markdown is designed to be as readable as possible when it's in-writing or unprocessed, and to be easily parseable. The hardest thing, I think, will be the internal linking. It hasn't been properly described yet, so let's get to that.

### Internal Linking
It isn't *too* complex. Imagine this directory structure:
`/digital/audio/formats/mp3`
`/digital/visual/formats/gif`

Now, you encounter a link to `{formats}`. Oh right, so internal links are designed to be as short as possible, normally only requiring the final name and none of the path. Anyway, `{formats}` is ambiguous; is it linking the audio or visual formats? Well, that's exactly what you have to specify. Just add the parent to the link so, it looks like `{audio/formats}`, and you're good!

What does that require of the parser? Well, I'd probably create a tree of the garden in memory, but you could, in theory, look through it on every internal link. I mean, I wouldn't recommend it, but if you're really tight on RAM then it could be necessary.

### Block Elements
Except for headings, there are a few block level elements that are useful and I would not leave home without. One really, and image, which are next.

```langauge
Honestly, give me a monospaced code block any day.
It's so great
and preserves
line breaks
```

### Images
Alt-text is first class and required to get your image to be one and not just a link. You link an image like anything else, by using any kind of link, but it will only become some kind of `<img>`- to use HTML as an example- if you write alt for it. The syntax for which is to put, on the line directly below it, a paragraph leading with a carrot. You may pad it away from the carrot with a space; whitespace is trimmed. Here's an example:

{not_really_an_image_link}
^ An image that does not exist. The link is invalid and therefore nothing is shown

{!Figure 1}
^ Again, not a valid image.

[Figure 1]: not_really_an_image_link