# AwesomeChasm
Chasm: The Rift PC game resource collection.

## Links
- [Chasm: The Rift Archive](https://www.chasm3d.com/)
- [Shikadi Modding Wiki](https://moddingwiki.shikadi.net/wiki/Chasm:_The_Rift)
- [The Shadow Zone](https://discord.com/channels/768103789411434586/1374778669612007527)
- [moddb - Chasm: The Rift](https://www.moddb.com/games/chasm-the-rift)
- [Chasm: The Rift at Moby Games](https://www.mobygames.com/game/2691/chasm-the-rift/)

## Inactive/Archived
- [Chasm: The Rift - Website Recreation by Effektus](https://web.archive.org/web/20251022090715/http://chasm.atspace.eu/)

## Releases
- [Chasm: The Rift Portable Staging including bin/cue image](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-portable-staging)
- [Chasm: The Rift Patch 3298](https://www.chasm3d.com/files/patches/csmtcpip.zip)
- [Chasm: The Rift Patch 1.05 with DOSBox P10fix](https://image.dosgamesarchive.com/games/chasm105.zip)
- [Chasm: The Rift Pack](https://steamcommunity.com/sharedfiles/filedetails/?id=3128742113)
- [Chasm: The Rift - 3OVIEW.EXE DOS model viewer](https://www.chasm3d.com/files/dump/CDEMOf.zip)
- [Chasm: The Rift - FLAC OST music](https://www.chasm3d.com/files/music/flac/)
- [Zrift Chasm in Doom - Legacy Edition](https://www.moddb.com/mods/zrift-chasm-in-doom-legacy-edition/downloads/zrift-chasm-in-doom-legacy-edition-v11)
- [Chasm-Reverse Panzerchasm](https://github.com/Panzerschrek/Chasm-Reverse)
- [OpenChasm](https://github.com/alexey-lysiuk/OpenChasm)

## Installation
- DOS Release Version
  - get [Chasm: The Rift Portable Staging](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-portable-staging) and unpack it to `.`
  - replace `FILE "CHASM.BIN"` with `FILE "chasm.bin"` in `Chasm\ Portable\ Staging/Chasm/music/Chasm.cue` and copy to `chasm.cue`
  - copy `Chasm\ Portable\ Staging/Chasm/music/chasm.bin` to `chasm.bin`
  - install and run [DOSBox Staging](https://www.dosbox-staging.org/)
    ```bat
    mount c <absolute cwd>
    C:
    imgmount d -t cdrom <absolute cwd>/chasm.cue
    dossetup.exe
    exit
    ```
  - get [Chasm: The Rift Patch 3298](https://www.chasm3d.com/files/patches/csmtcpip.zip) and unpack to `CHASM`
  - get [Chasm: The Rift Patch 1.05 with DOSBox P10fix](https://image.dosgamesarchive.com/games/chasm105.zip) and unpack `P10fix.zip` to `CHASM`
  - get [Chasm: The Rift Music Loop Fix](https://www.moddb.com/games/chasm-the-rift/downloads/chasm-music-loop) and unpack to `CHASM`
  - see [DOSBOX Staging wiki Game Issues](https://github.com/dosbox-staging/dosbox-staging/wiki/Game-issues#chasm-the-rift) for another explanation

- Windows Remastered Support
  - get [Chasm: The Rift Remastered Demo for Windows](https://steamdb.info/sub/766094/)
    - copy the `csm.bin` to `CHASM/csm.tar`
  - get [Chasm: The Rift Remastered for Windows](https://steamdb.info/sub/736338/)
    - copy the `csm.bin` to `CHASM/csm.tar`

## Modding
- [The Shadow Zone: Chasm Modding Toolkit Package](https://discord.com/channels/768103789411434586/1374842906002718803)
- [The Shadow Zone: OpenSesame](https://discord.com/channels/768103789411434586/1374929171263918080)
- [glcar3o](https://github.com/joneqdaniel/glcar3o/wiki)
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

### [Vivisector: Beast Within](https://www.mobygames.com/game/21823/vivisector-beast-within/)
### [Perilous Warp](https://crystice.com/perilous-warp/)
