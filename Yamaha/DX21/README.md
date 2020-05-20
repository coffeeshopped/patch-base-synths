# Yamaha DX21

## Editor Sections

* Voice
* Voice Bank

## Voice Patch

Structure in voice-patch.csv.
Name is stored in bytes 77-86.

## Voice Bank

Voice banks are typical Yamaha compact format, where the byte structure is different (more compact) than the single patch format. Still needs to be specified in a separate CSV.

## Fetch Requests

To fetch the current patch, send:

`0xf0, 0x43, 0x20 + channel, 0x03, 0xf7`

To fetch voice bank:

`0xf0, 0x43, 0x20 + channel, 0x04, 0xf7`
