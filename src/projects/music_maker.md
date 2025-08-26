# Music Maker

## Problem Statement

Sounds are formed by waves propagating through the air
at various frequencies. When sound enters your ear [it vibrates your eardrum](https://www.nidcd.nih.gov/health/how-do-we-hear) which in turn vibrates other parts of your ear ultimately culminating
in your brain perceiving a sound. The frequencies
of sound determine in what way your eardrum will vibrate and therefore are what determine how you
will percieve any given sound.

If you want to recreate a sound you need to in some way record what that sound was.
The oldest example we have of someone doing this dates back [to a thousands of years old stone tablet.](https://www.youtube.com/watch?v=KElPnD-dbkk) The idea being that if someone could read that tablet
and knew what the symbols on it meant, they could use an instrument of some kind to reproduce the song.

While stone tablets were awesome and paper acceptable for the task, writing down what someone else
should play only lets you record music. Writing down words similarly doesn't help record
the sound of someone's voice.[^lincoln]

The first of recording of someone's voice was done [in 1860 in Paris by Édouard-Léon Scott de Martinville](https://www.firstsounds.org/sounds/scott.php). He would later have his glory stolen by Thomas Edison; a common occurrence for the time.

Nowadays computers are generally more convenient for sharing music and recordings than other
methods, if sometimes of lower quality than something like a [vinyl record](https://victrola.com/blogs/articles/does-music-really-sound-better-on-vinyl)[^debate].

Storing audio on a computer requires translating audio information into a form
that a computer can store. We call this translation step "digitization."
It requires in some manner storing what frequencies of sounds
and in what proportion need to be produced to "play back" a sound.


## Your Goal

Make a program that produces a WAV file that, when played,
will sound like an instrumental version of [Three Blind Mice](https://en.wikipedia.org/wiki/Three_Blind_Mice)[^haloreach].

As a hint: `byte` and `short` can be helpful when representing "binary formats" like WAV.
Reading comprehension as well as reading stamina will also be useful for figuring out
how a WAV file works. You will need to learn a lot about audio.

## Future Goals

When you learn enough to do the following, come back to this project and expand it.

* Make the program produce other songs.
* Expand the program to take as input a text file that in some way describes a song and produce a WAV file
in turn.
* Make a "virtual keyboard" where somebody can play notes by typing and whatever they played can
be "exported" as a WAV file.
* Support a file format other than WAV as the output.

[^lincoln]: Abraham Lincoln had a really high pitched trill voice apparently. It is a real bummer we don't have recordings.

[^debate]: This is a subject of much debate.

[^haloreach]: When Halo Reach came out there was a lot of internet fighting about the "reticle bloom"
on a weapon called the DMR. This meant that if you fired it too quickly it would get
less and less accurate. The advice I heard around that time was to pull the trigger to the tune
of "three blind mice" and that would be about the right timing.