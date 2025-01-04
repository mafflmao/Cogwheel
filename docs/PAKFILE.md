PAKFILE (.PKZ) documentation
# GS VERSION 8 OR HIGHER.
Other versions of the PAKFILE Format might be different.
All SSCR PKZ Files are NOT compressed, and this is different on other games.
# What are they?
PKZ Files are the main file type used in Beenox's Goliath Engine, and are made up of several blocks, some being sub-blocks. There isn't actually much online about these files, so all of my information either comes from the 
[Beenox Spider-Man Modding Server](https://discord.gg/EvwSfyQz9Z) or [Skylanders Reverse Engineering](https://discord.gg/ZmZshRs5m3). 
# Block Header
So the blocks have a Unique 4-byte Identifier, then 8 bytes which I have no idea what they do, then the length of the block starting after this section.

| Offset    | Length | Usage |
| -------- | ------- | ----- |
| 0x00  | 0x04    | Unique Identifier |
| 0x04 | 0x02     | Unknown Bytes |
| 0x06 | 0x02     | Has Sub-Blocks? |
| 0x08 | 0x04     | Unknown Bytes |
| 0x0C    | 0x04    | Block Length |

## Unique Identifier
The first 2 bytes are actually useless really, but I use them to check if the next section is actually a block header. It's always going to start with 0x8000 (Big Endian), then it would have the actual identifier as the next 2 bytes.

## Unknown Section
WIP, once I know what this is, I'll update it.

## Length
This is probably one of the most simple parts of the PKZ files, it's just the length of the block data, starting right after this header.

## Sub-Blocks
I don't actually think I can explain in words how much I hate these "Sub-Blocks". Currently Cogwheel can only detect Sub-Blocks which are at the start of a block's data, and not later in the data, which is a HUGE issue. I really hope that unknown section in the Block Header can fix this problem, but I doubt it

# GS VERSION 7 OR BELOW.
Other versions of the PAKFILE Format might be different.
All SSCR PKZ Files are NOT compressed, and this is different on other games.
# What are they?
PKZ Files are the main file type used in Beenox's Goliath Engine, and are made up of several blocks, some being sub-blocks. There isn't actually much online about these files, so all of my information either comes from the 
[Beenox Spider-Man Modding Server](https://discord.gg/EvwSfyQz9Z) or [Skylanders Reverse Engineering](https://discord.gg/ZmZshRs5m3). 
## Block Header
So the blocks have a Unique 4-byte Identifier, then 8 bytes which I have no idea what they do, then the length of the block starting after this section.

| Offset    | Length | Usage |
| -------- | ------- | ----- |
| 0x00  | 0x04    | Unique Identifier |
| 0x04 | 0x02     | Unknown Bytes |
| 0x06 | 0x02     | Has Sub-Blocks? |
| 0x0C    | 0x04    | Block Length |

## Unique Identifier
The first 2 bytes are actually useless really, but I use them to check if the next section is actually a block header. This identifier would use all 4 bytes, unlike GS 6+

## Unknown Section
WIP, once I know what this is, I'll update it.

## Length
This is probably one of the most simple parts of the PKZ files, it's just the length of the block data, starting right after this header.

## Sub-Blocks
WIP? Until more is here, just assume that Sub-Blocks still exist lol
