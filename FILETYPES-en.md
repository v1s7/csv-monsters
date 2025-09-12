<sup>written \& translated by v1s7, special thanks to [Daniil-SV](https://github.com/Daniil-SV) and [SC Workshop](https://discord.gg/spFcna3xFJ) community</sup> 

[Версия на русском 🇷🇺](/FILETYPES.md) | [用中文阅读（很快）🇨🇳](/FILETYPES-cn.md)

The contents of this guide can be accessed by clicking the ⋮☰ button in the upper right corner.
-----

> [!NOTE]  
> Before reading on it's recommended to first read the [manual](/MANUAL-en.md).

-----
# Introduction
A few simple and less simple terms should be clarified before reading on: 

**File name**. Any file must be named. It's displayed next to each file in a file explorer when you open the folder it is inside of.

**File extension** is the set of characters after the last dot in the file name. For example, content.json has the extension "json". If there are multiple dots in a file name, the extension is often taken after the last dot. So "content.txt.md.json" would still have the extension "json". There're rare exceptions to this rule, such as .tar.xz, .zip.001 and others, but you're not likely to ever encounter them. 

**Compression** is the process of encoding data in such a way so it takes up less storage space. Usually slows down the opening speed of compressed files. Each format has its own complex methods, those won't be explained here.

**Archive** is a set of multiple folders and/or files presented as one monolithic.

**Texture** is a picture superimposed on some object.

**MIP-mapping** (from Latin: multum in parvo - "much in little") - a texturing method that uses several copies of the same texture with different details. What is the point of rendering a texture in its full 1024x1024 resolution, if it will occupy around 80 pixels on the device's screen because of its remoteness (or because of the low resolution of the display)? That's what mipmapping solves - it duplicates textures in different resolutions to waste less GPU resources.

**FlatBuffers** is a cool library from Google designed to make it easier to optimize speed and RAM consumption rate in games and heavy programs.

**Library** - in this context, a piece of code that can be embedded into other pieces of code to prevent programmers from reinventing the wheel, making code simpler and more functional.

**Converter** is a program that allows you to properly replace file formats.

# General
## .glb / .gltf – modern 3D models and their animations
In short, GLB is a version of GLTF with its data converted to a binary format. In turn, glTF is a JSON-based (not the one used by mods) 3D texture format with excellent compression. Read more: https://simple.wikipedia.org/wiki/GlTF
##### How to convert
Most of GLB files used in Supercell games are optimized with FlatBuffers, so to open them in 3D editors (like Blender) you should convert it to a format without FlatBuffers first:
- [Flat Converter](/PROGRAMS-en.md#flat-converter---)
- [ScwBot](/PROGRAMS-en.md#scwbot-) by sending `s!flat2glb`

When adding the new model in a mod, there's no need to convert it back.

## .scw – Supercell's legacy 3D model format
Proprietary format of 3D models from Supercell with exactly the same purpose of use as GLB. As a format, SCW has long been abandoned in favor of GLB, which supports quite a lot of extensions, compression methods, and it's just more convenient to use, from which it becomes very flexible.
##### How to convert
By its structure SCW is extremely similar to DAE, that's also the reason there're simple converters out there.
- [SCW by Opegit Studio](/PROGRAMS-en.md#scw-by-opegit-studio-)
- [ScwBot](/PROGRAMS-en.md#scwbot-) by sending `s!scw2dae`, and back into SCW by sending `s!dae2scw`. Outside of DAE it's possible to convert to other 3D formats, such as:
    - FBX: `s!scw2fbx`, vice versa: `s!fbx2scw`
    - OBJ: `s!scw2obj`, vice versa: `s!obj2scw`
    - BLEND: `s!blend2fbx`, vice versa: `s!blend2scw`

## .sctx – textures and unwarps
Proprietary texture format from Supercell, tailored for their Titan engine. It contains either sprite sheets or unwraps of 3D models. It also has such features as mipmapping and texture streaming.
##### How to convert
- [SCTX Converter](/PROGRAMS-en.md#sctx-converter----)
- [SC Editor](/PROGRAMS-en.md#sc-editor-----) – great option for exploring the internals of such files.
- [ScwBot](/PROGRAMS-en.md#scwbot-) by sending `s!sctx2png`. Keep in mind that you can't get JSON from it, so some important data can be lost when converting back (`s!png2sctx`), and the game may display the edited file incorrectly. This is still the best way to quickly view textures nonetheless.

## .sc – sets of diverse interface elements
Proprietary Supercell texture format, which can contain both simple textures (if the file name ends with \_tex.sc) and 2D animations. The format has several versions, popularly reffered as v0.5, v1 and v2:
- v0.5 - stored regular textures in "\_tex.sc"
- v1 - each texture was moved to its own separate ZKTX
- v2 - SC was rewritten, after which everything was stored in one file (still in the same KTX), namely inside of FlatBuffers. Compression algorithm was updated as well to version 5, thus it can sometimes get wrongly called as "SC v5".

It should be clarified that at least v0.5 and v1.0 were named so by the modders themselves for the sake of convenience – up until 2024 Supercell used the approach with tags, as in the original SWF since the days of Adobe Flash. Thus, to update something, they just needed to add a new tag, so all these versions are a rough set of tags that they used for a long time.
As for v2, since Supersell started to actively use FlatBuffers, .sc was also affected, thus SC2 was created. As a result, SC2 is still the same good old SC, but the one that was put into FlatBuffers.
##### How to convert
The most difficult format to convert due to its frequent updates, closed code and general complexity.  
- [ScwBot](/PROGRAMS-en.md#scwbot-) by sending `s!sc2png`. Keep in mind that this method is limited by files up to 10MB in size, and SC files generally aren't very small. This is still the best way to quickly view textures nonetheless.
- [SC Editor](/PROGRAMS-en.md#sc-editor-----) will let you view every resource integrated into SC.
- If you wish to edit SC, then the best option would be to use Adobe Animate 2023[😉](https://rutor.info/torrent/908269/adobe-animate-2023-23.0.2.103-2023-pc-repack-by-kpojiuk) with [«Three horsemen of SC»](/PROGRAMS-en.md#%EF%B8%8F-three-horsemen-of-sc).

## Extras
## .dae – format SCW is based on
One of the standard formats for 3D models that can be opened in any 3D editor. Can be obtained by converting an SCW file. Read more: https://wikipedia.org/wiki/COLLADA

## .ktx / .zktx – compresses textures, is used in SC, unsupported by the game as a standalone format
KTX ([Khronos TeXture](https://www.khronos.org/ktx/)) is a lightweight container format for distributing GPU textures to various platforms and applications built on OpenGL or Vulkan. The contents of a KTX file can range from a simple base-level 2D texture to a cubemap array texture with mipmaps.  
ZKTX is a KTX file compressed using Zstandard.
##### How to convert
For both options the game, as of v58, can no longer open them without firstly wrapping it in SCTX, or just extracting the PNG. Converting is possible with any specialized website and the same good [ScwBot](/PROGRAMS-en.md#scwbot-) by sending `s!ktx2png`. 

<!--
## .pvr
[PVR](https://docs.imgtec.com/specifications/pvr-file-format-specification/html/topics/pvr-introduction.html) is a texture container format used for storing textures in graphics applications. It has been around since the Sega Dreamcast and is now used mostly in mobile games.

It is not used in the game itself.
-->

<!-- # Shaders
## .shader

## .fsh

## .vsh

-->
## Sounds
The most common format for music and sound effects in the gaming industry is OGG (Vorbis), which not only beats MP3 and AAC in compression level, but also does not have the problems that the previous two suffer from - AAC from its closed code and royalties (usage fees), MP3 from the 0.5 second playback delay when looping (unless some hacks are applied) and poor compression with bigger penalty to CPU performance (although these days it's almost unnoticeable, in games it's important to squeeze every percent of performance out of the player's hardware).  
There's also the WAV format, which is audio without any compression at all and therefore with a huge file size (30 times larger than an average MP3 track). Th advantage of using it is getting the maximum performance and instantaneous startup on any hardware, so it's suitable only for overlapping and repetitive sound effects lasting less than a second. It has no use in Null's Brawl, as OGG is still a reasonable candidate for such purposes.
##### How to convert
The specs of all sounds in Null's Brawl are as follows:
- Format: OGG Vorbis
- Frequency (sampling): 44.1 kHz (44100 Hz)
- Bitrate: 48-80 kbps (64 kbps on average)
- Stereo sound

Adherence to this standard is desirable, but not required. Null's Brawl will play any format with any specs. However, soon conversion to OGG will be mandatory for a mod to get signed.
- If there aren't many tracks to convert (about 1-3), any conversion website will do the job. Just google "mp3 to ogg". If it'll have a choice of OGG quality - set it below average.
- If there're a lot of tracks, or you just want a more authentic way of converting – [FFmpeg](/PROGRAMS-en.md#ffmpeg------) is the perfect solution for you (see the link for commands and scripts for mass conversion).

## Fonts
Among fonts there're only 2 mainstream formats: .ttf and .otf, both of which are supported by the game, so it doesn't really matter which one you choose. You can read about their differences more here: https://old.reddit.com/r/typography/comments/ci4nwk/otf_vs_ttf/

The main game font (LilitaOne Regular) isn't always replaceable, and may not display the custom font at all (there will literally be spaces instead of any characters). The exact cause of this behaviour is unknown.

# Basic
## .png
Image format, has lossless compression. Very flexible, used in many places. The base for any textures.

## .json
Regular text file, just with a different extension. Seriously, you can just create a TXT file and rename it to JSON later. Designed to use the markup language of the same name in it. It's what mods are written in for Null's Brawl, Minecraft Bedrock and many other games.

## .zip
ZIP is a popular format for compressing and archiving data in a lossless manner. A ZIP file contains one or more files that have been joined together in order to reduce file size, preserve the original quality of media content, and/or send multiple files in one. In our case, ZIP archives are used to pack several mod files into one, and are further manually verified and signed.

## .jar / .NullsBrawlAssets
JAR - Java ARchive, basically it's a ZIP archive with a META-INF folder inside. NullsBrawlAssets is just a JAR archive with a different extension. You can find more information about it in the [manual](/MANUAL-en.md#NullsBrawlAssets). Haven't you read it yet? >:( 