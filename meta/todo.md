# Tending that needs to be done
A list of things I'd like to do. This list is kept in the garden so I can link back to it and so it's kept close, always.

### Software things ToDo

#### {{Parser/Generator | https://github.com/gennyble/pingling}}
- Automatic recent change detection using `mtime`. This will *not* work if {!wikarden} is cloned through git. Rsyncing it is less steps, so maybe that's better. I can even setup a little script to rsync and run the generator. It'd be a lower barrier than pushing, sshing, pulling+generatoring. Hmm.
- Actual list support instead of hyphens and softbreaks. It's bad for accessibility.
- A refactor is sorely needed. Don't be afraid to do a two pass. An actual lexer and then parser is fine. Parse to an AST and then pattern match to form objects and things. You- me, that is. *she turns to herself*- You tried to avoid doing multiple passes but now you have *three*, so look where that got you.

[wikarden]: https://github.com/gennyble/wikarden

### Writings
- Most of {image processing} left
