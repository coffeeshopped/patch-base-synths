# Kawai K1r

The sysex implementation can be found in the [K1 Wave List from Kawai](https://kawaius.com/wp-content/uploads/2019/04/Kawai-K1-Wave-List.pdf).

But Kawai lists this info as being for the K1 and K1m. Is it the same for the K1r?

## Editor Sections

TODO

## Voice Patch

Name is in bytes 0-9 of the patch.

## Multi Patch

Name is in bytes 0-9 of the dump.

Multi Block, including header, is 85 bytes. Each single parameter edit results in a complete block send.

Header of SysEx Messages: F0 40 00 20 00 03 00 40

Checksum value (M75) is sum of A5H and M0-M74, bit 7 clear

## Fetch Requests

Can you fetch the edit buffer of the current patch? Or just fetch the saved sounds?

TODO.
