# AwesomeChasm
Chasm: The Rift PC game resource collection.

## Releases
- [Chasm: The Rift Archive](https://www.chasm3d.com/)
- [Chasm: The Rift Pack](https://steamcommunity.com/sharedfiles/filedetails/?id=3128742113)
- [Chasm: The Rift at Moby Games](https://www.mobygames.com/game/2691/chasm-the-rift/)
- [Chasm: The Rift Portable Staging including bin/cue image](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-portable-staging)
- [Zrift Chasm in Doom - Legacy Edition](https://www.moddb.com/mods/zrift-chasm-in-doom-legacy-edition/downloads/zrift-chasm-in-doom-legacy-edition-v11)
- [Chasm-Reverse Panzerchasm](https://github.com/Panzerschrek/Chasm-Reverse)
- [OpenChasm](https://github.com/alexey-lysiuk/OpenChasm)
- [Chasm: The Rift - 3OVIEW.EXE DOS model viewer](https://www.chasm3d.com/files/dump/CDEMOf.zip)
- [Chasm: The Rift - FLAC OST music](https://www.chasm3d.com/files/music/flac/)
## Historical
- [Chasm: The Rift - Website Recreation by Effektus](http://chasm.atspace.eu/)
## Installation
- get [Chasm: The Rift Portable Staging](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-portable-staging) and unpack it to `.`
- move the bin/cue image in `Chasm\ Portable\ Staging/Chasm/music/` to `.`
- run dosbox
```bat
mount c <CWD>
C:
imgmount d -t cdrom chasm.cue
dossetup.exe
exit
```
- get [Chasm: The Rift Patch 3298](https://www.chasm3d.com/files/patches/csmtcpip.zip) and unpack to `CHASM`
- use an hex editor to modify `PS10.EXE` at offset `0x14030` from `f7 f3` to `90 90`
- run `dosbox fix.exe`
- get [Chasm: The Rift Music Loop Fix](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-music-loop) and unpack to `CHASM`
- get [Chasm: The Rift Windows](https://steamdb.info/sub/736338/) or [Chasm: The Rift Windows Demo](https://steamdb.info/sub/766094/) and copy the `csm.tar` to `CHASM`

## Formats
- [glcar3o](https://github.com/jopadan/glcar3o/wiki)
- [Shikadi Modding Wiki](https://moddingwiki.shikadi.net/wiki/Chasm:_The_Rift)
- [The Shadow Zone](https://discord.com/channels/768103789411434586/1374778669612007527)
  - [Chasm Modding Toolkit Package](https://discord.com/channels/768103789411434586/1374842906002718803)

## Modding
- [The Shadow Zone Invite](https://discord.gg/f85Cz4FaXP/)
- [The Shadow Zone](https://discord.com/channels/768103789411434586/1374778669612007527)
  - [OpenSesame](https://discord.com/channels/768103789411434586/1374929171263918080)
- [moddb](https://www.moddb.com/games/chasm-the-rift)
- [Autodesk Animator](https://github.com/AnimatorPro)
- [Noesis .3O/.CAR 3D model viewer/converter](https://richwhitehouse.com/index.php?content=inc_stream.php)

## Reverse Engineering
- [Peganza Pascal Analyzer](https://www.peganza.com/)
- [A Deep Dive into the Turbo Pascal Compiled Code](https://github.com/daelsepara/turbo-pascal-assembly)
- [Awesome Pascal](https://github.com/Fr0sT-Brutal/awesome-pascal)
- [TDInfo Parser for IDA](https://github.com/ramikg/tdinfo-parser)
- [Duncan Murdoch's Programs](https://www.murdoch-sutherland.com/programs/index.htm)
- [Rebuild of Turbo Pascal exe missing TPU modules](https://comp.lang.pascal.borland.narkive.com/1B3WeJkX/rebuild-of-turbo-pascal-exe-missing-tpu-modules)
- [Reverse Engineering Delphi Binaries in Ghidra with Dhrake](https://blag.nullteilerfrei.de/2019/12/23/reverse-engineering-delphi-binaries-in-ghidra-with-dhrake/)
- [Hachoir is a Python library to view and edit a binary stream field by field](https://github.com/vstinner/hachoir)
- [Kaitai Struct: declarative language to generate binary data parsers](https://github.com/kaitai-io/kaitai_struct)
- [0xeb/TurboPascal: TP7P5FIX](https://github.com/0xeb/TurboPascal)

## Similiar Pascal Games

### [HROT](https://en.wikipedia.org/wiki/Hrot)
- [HROT Demo](https://www.gog.com/en/game/hrot_demo)
- [HROT CLI Tools](https://github.com/joshuaskelly/hrot-cli-tools)
```cpp
/* HROT .PAK FILE FORMAT */
namespace hrot::pak
{
struct header
{
    c8<4> magic = "HROT"
    u32   names;
    u32   count; // 128 is file count
};

struct entry
{
    c8<120> name; // terminated with 0x00
    u32 pos;
    u32 len;
};
};
```
## Similiar C++ Games

### [Perilous Warp](https://crystice.com/perilous-warp/)
