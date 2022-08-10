# Fork Notes
My motivation for forking this was in wanting a far more verbose version of infgen. I wanted to understand what each bit in the bitstream reperesented (with color coding). An initialy mistake of mine was in adding this functionality to an old copy I had of infgen (2.4), when Adler literally added the bit functionality in a more recent version. Adlers 3.0 version now has a license where I can fork & modify, but I will need to reprogram and re-add the features that I had for this new version

Features (added back in so far)
--------
-t table: When in dynamic huffman mode, actually print the huffman tables. Look at oversubscribed.png for a good visualization on what a 'huffman table' looks like when you only give each symbol one bit, of course you get an error.

# Synopsis

_infgen_ is a deflate stream disassembler. It will read a gzip, zlib, or raw
deflate stream, and output a readable description of the contents.

# Motivation

_infgen_ permits the examination of deflate compressed data for instructional
purposes, to see how the data is compressed, and for debugging deflate
compressors.

# Installation

Simply compile `infgen.c`, and provide the compressed data to stdin. The
disassembled output will be written to stdout.

## Test

    gzip < infgen.c | ./infgen

will display the disassembled result of compressing the _infgen_ source code.

Use:

    infgen -h

to see the command options.

# License

This code is under the zlib license, found in the source file and LICENSE.
