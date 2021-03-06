                                     pc2abc
                                    =========

This will eventually be a Python program to take music files written using the Personal Composer 
application and convert them to abc notation.

Command line invocation:
  pc2abc <filename>

where <filename> is something like myfile.PC

The program will generate two output files:

- myfile.abc is the resulting abc notation file
- myfile.log is a debugging file showing how the program has parsed the binary data of the .PC file.

Current progress
=================

Things that work:
- single line of music per staff
- multiple staves (one voice per staff)
- chords (not fully tested)
- translation of basic notes and rests
- note range (abc notation) from C,,, to b'''
- ordinary barlines
- treble, alto, bass clefs
- changes of clef within the tune 
- keys: major and minor from 6 flats to 5 sharps
- changes of key withing the tune (not fully tested)
- time signatures (n/m format)
- changes of time signature in the tune (not fully tested)
- ties
- beams
- titles (partial)
- accidentals
- repeats
- first and second time endings

Things that don't work:
- anything other than 'type 12' .PC files
- multiple voices per staff
- double barlines, dotted barlines, invisible barlines
- clefs other than treble, alto, bass
- C and C| time signatures
- dynamic markings etc
- pedal notation
- guitar chords
- song lyrics
- slurs
- midi instruments (though some basic defaults are chosen by the program)
- stem-up and stem-down (these are encoded for every note in .PC files but not usually in abc)
- tablature
- tempo markings
- ornaments
- page formatting
- xml conversion (planned)
- everything else

Mostly, PC files that contain 'things that don't work' will still be converted but 
unrecognised stuff is ignored. In some cases, the unrecognisable stuff may prevent 
the program from doing a conversion at all.
