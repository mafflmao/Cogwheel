# BUILDMAN - What is it?
"buildman" seems to just be a block type in the Goliath Engine PAKFILES.

## BLOCK IDENTIFIER
This Block's Identifier is 17.
# DATA
It has a lot of information about when the files were built and how they were built.
So far, what I have is this:

| Name | Offset | Size |
|--------|---------|------
| File Identifier | 0x00 | 0x04 |
| Unknown | 0x04 | 0x0F |
| Date and Time | 0x13 | 0x18 |
| Unknown | 0x2B | 0x5D |
| GS Version | 0x88 | 0x15 |
| Unknown | 0x9D | 0x6B |

Example `Date and Time`

`Fri Jun 26 08:21:18 2015`

Example `GS Version` (Goliath Studio)

`GS version 9.0.170764` - "Skylanders Superchargers Racing (Alpha) [Wii]"

`GS version 9.0.175008` - "Skylanders Superchargers Racing (Retail) [Wii]"

`GS version 8.20.98473` - "The Amazing Spider-Man 2 (Retail) [PS3]"
