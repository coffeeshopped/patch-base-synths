# Kawai K5000W

Does everything the K5000S/R do, but also has PCM wave-based patches, and Drum Kits.

The sysex implementation can be found in the [K5000W/S/R MIDI Implementation from Kawai](https://kawaius.com/wp-content/uploads/2019/04/Kawai-K5000-MIDI-Manual.pdf).

## Tone Structures

### Single ADD patch

= Single Tone Data + (ADD Wave Kit Data * Num sources)

Single Tone Data

* Effect Data
* Common Data
* (Source Data * Num srcs)

ADD Wave Kit Data:

* HC Kit Data
* HC code1 Data
* HC code 2 Data
* Formant Filter Data
* Harmonic Env Data
* Loudness Sens Select

### Single PCM patch

= Single Tone Data


## Editor Sections

TODO

## Voice Patch

TODO

## Multi Patch

TODO.

## Fetch Requests

TODO.
