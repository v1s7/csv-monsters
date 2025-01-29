<!--Coming soon, will contain info about file extensions that you'll encounter on your way when modding Null's Brawl.-->
<sup>v1.0 – written \& translated by v1s7, special thanks to [Daniill-SV](https://github.com/Daniil-SV) and [SC Workshop](https://discord.gg/spFcna3xFJ) community</sup> 

[Прочесть на русском](https://github.com/v1s7/csv-monsters/tree/main/FILETYPES.md)

> [!TIP]  
> The contents of this guide can be accessed by clicking the ⋮☰ button in the upper right corner.

> [!NOTE]  
> Before reading on it's recommended to first read the [manual](https://github.com/v1s7/csv-monsters/tree/main/MANUAL-en.md).

-----
# Introduction
A few simple terms should be clarified before reading on: 

**Filename** - any file must be named. It is displayed next to each file when you open the file folder in file manager (explorer). 

**File extension** is the set of characters after the last dot in the file name. For example, content.json has the extension "json". If there are multiple dots in a file name, the extension is often taken after the last dot. So "content.txt.md.json" will still have the extension "json". There are rare exceptions to this rule, such as .tar.xz, .zip.001 and others, but you are not likely to ever encounter them. 

**Compression/compression** is the process of encoding data so that it takes up less space in the device's storage. Usually slows down the opening speed of compressed files. Each format has its own complex methods, they will not be explained here.

**Archive** - A set of multiple folders and/or files presented as one monolithic.

**Texture** - a picture superimposed on some object.

**MIP-mapping** (from Latin: multum in parvo - "much in little") - a texturing method that uses several copies of the same texture with different details. What is the point of rendering a texture in its full 1024x1024 resolution, if it will occupy 70-80 pixels on the device screen because of its remoteness (or because of the low resolution of the display)? That's what mipmapping solves - it duplicates textures in different resolutions to waste less GPU resources.

**FlatBuffers** is a cool library from Google designed to make it easier to optimize speed and RAM consumption of games and heavy programs.

**Library** - in this context, this is a piece code that can be embedded into other pieces of code to make it not only shorter, more functional and simpler, but also to prevent programmers from reinventing the wheel.

[**ScwBot**](https://discord.gg/spFcna3xFJ) is a Discord bot that contains almost all format converters for modding, instant search/downloading of game files and many other interesting features like `img2map`. This bot is a lifesaver for people on a phone, since almost all converters require a computer. But not everything is so rosy: thanks to Discord, all files sent are limited to 10 MB, and it's not always online. 

**Converter** is a program that allows you to properly replace file formats.

# Basic
## .glb / .gltf
In short, GLB is a version of the GLTF format, with data converted to binary format. In its turn, glTF is a JSON-based (not the one used by mods) simple, efficient and fast-loading 3D texture format with excellent compression, nicknamed "the JPEG of the 3D world". Read more: https://simple.wikipedia.org/wiki/GlTF

GLB-files used in Supercell game are optimized with FlatBuffers, so to open GLB in 3D-editors (like Blender) you should first convert it to a format without FlatBuffers (for example, using [Flat-Converter](https://github.com/Daniil-SV/Supercell-Flat-Converter) or the same ScwBot), and when adding it to the mod - convert it back (optional, but desirable).

## .scw
Proprietary format of 3D models from Supercell with exactly the same purpose of use as GLB, and in its structure SCW is very similar to DAE, from which there are converters of these formats (for example, the same ScwBot). As a format, SCW has long been abandoned in favor of GLB, which supports quite a lot of extensions, compression methods, and it is banally more convenient to use, from which it becomes very flexible.

## .sctx
Proprietary texture format from Supercell, customized for their Titan engine. It contains either sprite sheets or 3D model unwraps. It also has such features as MIP-mapping and texture streaming.

[SCTX Converter](https://github.com/Daniil-SV/SCTX-Converter) will do a great job by pulling two files from one file: PNG and JSON. To convert back, you will need both of these files.

ScwBot can also convert via `s! sctx2png`. But you can't get JSON from it, so when converting back (`s! png2sctx`) you may lose important data, and the game may display the edited file incorrectly. But this is still the best option for quick texture preview.

## .sc
Proprietary Supercell texture format, which can contain both simple textures (if the file name ends with \_tex.sc) and 2D animations. The most difficult to edit and decompile, because files of this type have the largest sizes, like emoji.sc, which occupies as much as 64 MB. 

The format has several versions, popularly known as v0.5, v1 and v2:
- v0.5 - stored regular textures in "\_tex.sc"
- v1 - each texture was moved to its own separate ZKTX
- v2 - SC was rewritten, after which everything was stored in one file (in fact in the same KTX), namely inside FlatBuffers.

It should be clarified that at least v0.5 and v1.0 were invented by the modders themselves purely for the sake of convenience - until 2024 Supercell used the approach with tags, as in the original SWF since the days of Adobe Flash. Thus, to update something, they just needed to add a new tag, so all these versions are just a rough set of tags that they used for a long time.
And about v2, since Supersell started to use FlatBuffer actively, .sc was also affected, thus SC2 was created. As a result SC2 is the same good old SC, but it was stuffed into FlatBuffer.

The fastest way to convert files with this extension is with the command `s! sc2png` in the channel with ScwBot. But remember, this method is limited to files up to 10 MB, and given the compression from SC, then 5-6 MB.

To get acquainted with SC-file internals you can use [SC Editor (the one in Java)](https://github.com/danila-schelkov/sc-editor), in which you can visually look at all resources contained in it. However, SC2 is not supported by it, and you will have to run SC through [ScDowngrade](https://github.com/Daniil-SV/ScDowngrade) first. You will also need to download [KTX Tools](https://github.com/KhronosGroup/KTX-Software) and add it to the PATH in the installer.

If you are not satisfied with both of the previous options, or if you want a more flexible option for editing (namely Adobe Animate), the last option is [SC2FLA](https://discord.com/channels/751042695698579457/751056303123857509/1288796520199487532) (FLA is the project format in Animate). It doesn't support SC2 either, the file will need to be degraded first. To convert FLA back to SC you will need to install the [SupercellSWF-Animate](https://github.com/sc-workshop/SupercellSWF-Animate) plugin.

## Extras
## .dae
One of the standard formats for 3D models that can be opened in any 3D editor. Can be obtained by converting an SCW file. Read more: https://wikipedia.org/wiki/COLLADA

## .ktx / .zktx
KTX ([Khronos TeXture](https://www.khronos.org/ktx/)) - It is an efficient and performant container format for reliable distribution of GPU textures across multiple platforms and applications. The contents of a KTX file can range from a simple 2D texture to a cubemap array texture with mipmaps. KTX files contain all the parameters needed to efficiently load textures into 3D interfaces such as OpenGL and Vulkan, including access to individual levels of MIP mapping.
ZKTX is the same KTX file, but compressed using Zstandard.
Both options, as of game version v58, are no longer accepted by the game. You will need to convert either to PNG first and then to SCTX (for example, by the same ScwBot), or to SC if you opt to edit via Adobe Animate.

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
The most common format for music and effects in the game industry is OGG (Vorbis), which not only beats MP3 and AAC in compression level, but also does not have the problems that the previous two suffer from - AAC from closed code and royalties (usage fees), MP3 from the 0.5 second playback delay when looping (unless crutches are applied) and poor compression with more damage to CPU efficiency (although these days it's almost unnoticeable, in games it's important to squeeze every percent of performance out of the player's hardware).
There's also the WAV format, which is audio without any compression at all and therefore with a huge file size (30 times larger than the average MP3 track). Its advantage is maximum performance and instant startup on any hardware, so it is suitable only for repetitive sound effects lasting less than a second. It has no use in Null's Brawl, as OGG is still a reasonable candidate for such purposes.
The characteristics of all sounds in Null's Brawl are as follows:
- Format: OGG Vorbis
- Frequency (sampling): 44.1 kHz (44100 Hz)
- Bitrate: 48-80 kbps (64 kbps on average)
- Stereo sound
Adherence to this standard is desirable, but not required. Null's Brawl will play any format with any characteristics.

## Fonts
Among them there are only 2 basic formats: .ttf and .otf, in Null's Brawl only the first one is used, so the second one is hardly supported by the game. You can read more about their differences here: https://old.reddit.com/r/typography/comments/ci4nwk/otf_vs_ttf/.
More information is required on the availability of .otf compatibility in the game.

## Literature
## .png
Image format, has lossless compression. Very flexible, used in many places. Base for any textures.

## .json
Regular text file, just with a different extension. Seriously, you can just create a TXT file and rename it to JSON later. Designed to use the markup language of the same name in it. It's what mods are written in for nulls, myncroft poorrock, and many other games.

## .zip
ZIP is the most popular format for lossless data compression and archiving. A ZIP file contains one or more files that have been joined together in order to reduce file size, preserve the original quality of media content, and/or send multiple files in one. In our case, ZIP archives are used to join the mod files into one, and are further manually validated and signed.

## .jar / .NullsBrawlAssets
JAR - Java ARchive, roughly speaking it's a ZIP archive with a META-INF folder inside. NullsBrawlAssets is just a JAR archive with a different extension. You can find more information about it in the [manual](https://github.com/v1s7/csv-monsters/tree/main/MANUAL-en.md#NullsBrawlAssets).