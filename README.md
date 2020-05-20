# Patch Base Synths

A repository of technical information about synthesizers that Patch Base supports, or will support.

If you'd like to contribute information to this repo, please find the synth(s) that you're interested in helping with, and see if they are complete yet or not. If not, shoot me an email first just in case someone is already working on the synth you're considering (so as not to repeat work between people).

## Patch Structure Spreadsheets

Some of the most important info for creating patch editors is the data structure of the patches themselves. This structure document lists all of the parameters associated with a patch (or performance, etc), along with the numerical ID of each parameter, its minimum/maximum values, and more. The information that goes into this spreadsheet is most often found in the Owner's Manual for a synthesizer, or possibly a separate data sheet published by the manufacturer. Sometimes it was never fully documented, but maybe some searching on the internet can yield 3rd-party documentation.

This structure can vary from synth to synth, but here are the typical columns in a Patch Structure Spreadsheet:

### Parameter Name

The human-readable name of the parameter (e.g. "Oscillator 1 Wave")

### Param #

The ID for this parameter, when transmitted to the synth. This is the ID used for sending individual parameter changes to the synth.

### Byte #

This is the byte location for the parameter within a patch. In other words, if you have a blob of binary data from the synth representing a patch, this is the location in that blob that holds the value for this parameter.

The location starts at 0 for the first byte of patch information (so, ignoring any header bytes in the patch). The manual will often document this and you can transcribe it as-is.

For many synths, the Param # and Byte # for a parameter will be identical (e.g. most Roland synths, and many Yamaha FM synths). But for others (e.g. most DSI synths) they're different. If they're identical, just say so, don't bother copying everything twice.

### Min Val, Max Val

The minimum and maximum values for the parameter. If the parameter has Options (see below), then you can leave these blank.

### Display Offset

The amount that is added to the value when it is displayed to the user, if any. For example, the Transpose parameter on the DX21 has an internal range of 0 to 48. But the values are shown to the user as -24 to 24. So the Display Offset is -24 in this case.

### Options

Some parameters are shown to the user as text rather than numbers. The DX21's LFO waveshape has a range of 0 to 3, but the options shown to the user are *Saw Up, Square, Triangle, S/Hold*. For parameters like this, enter those text options in the Options column, ordered by their numerical value (e.g. for the DX21 example 0 = Saw Up, 1 = Square, etc).

If there is a long list of options, it is probably easier to instead list the options in a separate file, then just reference them in the Options column.


### Path

This column is internal to Patch Base. Patch Base uses a vocabulary (limited to a specific set of terms) to internally refer to each parameter. For example, in a 2 oscillator synth, the parameter for the wave shape of oscillator 1 might have the path:

`osc, i(0), wave`

"osc" is for oscillator, and "wave" is for waveshape. Whenever a number is used in a parameter name (because there are multiples of something), you put "i(X)" to denote the number, where X is a zero-based count (because programming). Hence the "i(0)" for Oscillator 1. Oscillator 2's wave shape would be `osc, i(1), wave`.

More on this soon.
