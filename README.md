musthe
======

Music theory implemented in Python. Notes, scales and chords. It was made as an experiment to test Python3 and magic methods.

Feel free to read the code, fork and make pull requests! They are welcome!


How to use
==========

It is very simple, everything is coded in a object-oriented style, for example:

    $ python 
    >>> a = Note('A4')
    >>> a
    <__main__.Note object at 0x7f981b1ba9b0>
    >>> str(a)
    'A'


Suppose you want to create tension, so you want the perfect fifth or the minor seventh of that A, so you do:

    >>> fifth = Interval('P5')
    >>> seventh = Interval('m7')
    >>> a+fifth
    <__main__.Note object at 0x7f981b1baac8>
    >>> str(a+fifth)
    'E'
    >>> str(a+seventh)
    'G'

Though it is important to see that the octaves of those notes are different:

    >>> a.octave
    4
    >>> (a+seventh).octave
    5

Now lets try scales:

    >>> b.scale('major')
    [<__main__.Note object at 0x7f981b1bafd0>, <__main__.Note object at 0x7f981aa43208>, <__main__.Note object at 0x7f981aa43240>, <__main__.Note object at 0x7f981aa430b8>, <__main__.Note object at 0x7f981aa43320>, <__main__.Note object at 0x7f981aa433c8>, <__main__.Note object at 0x7f981aa43400>, <__main__.Note object at 0x7f981aa432e8>]

wat

It return a list of Note instances, so you should do something like:

    >>> list(map(str, b.scale('major')))
    ['B', 'C#', 'D#', 'E', 'F#', 'G#', 'A#', 'B']
    
Fair enough. Chords are yet to be implemented.


If you have lilypond installed, you can make little melodies using this program, an example is given in 'lilypond_example.py'

