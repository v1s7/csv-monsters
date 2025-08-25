<sup>v1.991 – written by v1s7, special thanks to [Daniil-SV](https://github.com/Daniil-SV) and [SC Workshop](https://discord.gg/spFcna3xFJ) community</sup>
<!--
Techicons by gui-bus
Linux <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Linux.svg" height="16rem">
Android <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Android.svg" alt="Android" height="16rem">
Windows <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">
Animate <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Animate.svg" alt="Adobe Animate" height="16rem">
MacOS <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Apple.svg" height="16rem">
Bash <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Bash.svg" height="16rem">
Python <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Python.svg" height="16rem">
Java <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Java.svg" height="16rem">
C++ <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/C++.svg" height="16rem">
Discord <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Discord.svg" height="16rem">
Telegram <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Telegram.svg" height="16rem">
-->

[Версия на русском 🇷🇺](/PROGRAMS.md)  

> [!TIP]  
> The list of programs can be opened by pressing the ⋮☰ button in upper right corner.  

**All converters, bots, scripts, chat rooms and other useful resources for modding are described here. This note was created for convenient unified updating of descriptions and links.**

-----
# Bots and communities📱

### [EscavunBot](https://t.me/escavun_chat) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Telegram.svg" height="16rem"> 
Telegram bot with flexible options for downloading game files:
- RegEx search support,
- allows you to change the game and its version from which you want to download assets,
- download multiple files at once (isn't limited to 10 MB unlike Discord),
- automatically decompresses CSV files,
- and much more.

### [Null's Brawl Mods Bot](https://t.me/nb_mods/4827) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Telegram.svg" height="16rem"> 
The name speaks for itself. It's used to temporarily sign JSON files (and only them) into NullsBrawlAssets for exactly for 3 days. It's located in the official chat room of Null's Brawl modders from which:
- long term mod signing requests (for 90 days) are created,
- the latest information about updates to the modding engine and the game is posted,
- publications to the mod library from mod manager are requested.

> [!note]  
> To start using the bot you need to join the chat room and be in it for at least 10 minutes. That is all the requirements.

You can also send files to the bot for signing in PMs, but there will be a 120 second delay between successful signature requests until the next one becomes available. Though it's still better than the 5 minute delay of the chat room.

### [ScwBot](https://discord.gg/dbD8erDDmF) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Discord.svg" height="16rem"> 
A Discord bot that contains almost every single converter needed for modding, has instant searching/downloading of game files and many other interesting features like `img2map`. 
This bot is a lifesaver for people without a computer under hand, as almost all converters require one. But it's not all sunshine and rainbows: because to Discord, every file that has been sent is limited to 10MB, and the bot isn't constantly online.  
The server itself also got plenty of tutorials on how to use convertion programs – I recommend everyone to take a look.

### [SC Workshop](https://discord.gg/spFcna3xFJ) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Discord.svg" height="16rem"> 
A community that makes modding game's resources not be a nightmare or a fantasy at all.

<!--# 🌐 Web-converters
## GLB ←→ DAE ←→ FBX ←→ BLEND ←→ OBJ ←→ (...)
Wip
## KTX ←→ PNG
Wip
## OGG ←→ MP3 ←→ (...) ← MP4
Wip-->
# 🧱 Fundamentals
## 📁 File explorers
Just pick one.
### On Android
All of them support mounting external storage – in our case, the game's storage.
#### MiXplorer
[Website](https://mixplorer.com) | [4PDA](https://4pda.to/forum/index.php?showtopic=318294) | Google Play – [paid💲](https://play.google.com/store/apps/details?id=com.mixplorer.silver)  
The most customisable and has a plenty of features. You can access Android/data if you have Shizuku installed (needs to be enabled in the settings).
#### Material Files
[GitHub](https://github.com/zhanghai/MaterialFiles) | [4PDA](https://4pda.to/forum/index.php?showtopic=957950) | [Google Play](https://play.google.com/store/apps/details?id=me.zhanghai.android.files)  
The best among free and open source managers available on Google Play.
#### MT Manager
[Website](https://mt2.cn) | [4PDA](https://4pda.to/forum/index.php?showtopic=548542) | Google Play – never❌  
The most feature-rich manager, some parts of which are paid. You can access Android/data if you have Shizuku installed (requested at startup and can be toggled in the settings).

### On iOS
> [!warning]  
> The current maintainer doesn't own any iOS device, additional information is needed. Don't hesitate to share some by posting on [Issues](https://github.com/v1s7/csv-monsters/issues)!
#### Filza File Manager
[Website](https://www.tigisoftware.com/default/?page_id=78) | [BigBoss Repo](http://cydia.saurik.com/package/com.tigisoftware.filza) | [TrollStore](https://www.tigisoftware.com/default/?p=439)  
Nothing to say here ¯\\\_(ツ)\_/¯
## 👨‍💻 Code editors
Just in case you're not happy with the editor from the file manager or the system notepad – you don't **have** to use them, it's all a matter of convenience.
### On a computer
These options should fit any OS.
#### VS Code
[Website](https://code.visualstudio.com/download)  
The most popular IDE with a ton of plugins and a bunch of forks like [VSCodium](https://vscodium.com/) (removed microsoft telemetry), [Cursor](https://cursor.com/) (integrated AI) and others.
#### Kate  
[Website](https://kate-editor.org/get-it/)  
A way less resource-demanding editor.

### On Android
Here the functionality of all of them is a bit lacking, but for our purposes they're fine
#### ACode
[Github](https://github.com/Acode-Foundation/Acode?tab=readme-ov-file#-installation) | [F-Droid](https://f-droid.org/repo/com.foxdebug.acode) | [Google Play](https://play.google.com/store/apps/details?id=com.foxdebug.acode)   
Literal copy of VS Code, though it's not a port.

#### Xed Editor
[Github](https://github.com/Xed-Editor/Xed-Editor) | [Izzy](https://apt.izzysoft.de/fdroid/repo/com.rk.xededitor) | Google Play – not❌  
An editor with its own approach to folders with a nice UI. You can give access to the `mods` folder via DocumentsUI (only if you've [patched the game's .apk file with ApkTool M](/FAQ-en.md#2-patching-apk-of-nulls-brawl)) and have a convenient way to edit all JSON files of installed mods!

#### QuickEdit
[Website](https://rhmsoft.com/?p=283) | [4PDA](https://4pda.to/forum/index.php?showtopic=625901) | [Google Play](https://play.google.com/store/apps/details?id=com.rhmsoft.edit)  
The classic

### On iOS
> [!warning]  
> The current maintainer doesn't own any iOS device, additional information is needed. Don't hesitate to share some by posting on [Issues](https://github.com/v1s7/csv-monsters/issues)!
#### Runespace Text Editor
[Website](https://runestone.app) | [Github](https://github.com/simonbs/runestone) | [App Store](https://apps.apple.com/us/app/runestone-editor/id1548193893)  
Nothing to say here ¯\\\_(ツ)\_/¯

## 📑 Table editors
CSV tables can be opened by any text editor, but they'll display it in raw form. The most convenient way to open them is through spreadsheet editors. Almost all of them are built with cross-platform in mind, so there's not really a point in OS division here.

#### Google Sheets
[Website](https://workspace.google.com/products/sheets) | [App Store](https://apps.apple.com/us/app/google-sheets/id842849113) | [Google Play](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets)

#### Microsoft Excel
[Website](https://www.microsoft.com/en-us/microsoft-365/excel) | [App Store](https://apps.apple.com/us/app/microsoft-excel/id586683407) | [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.office.excel)

#### WPS Office
[Website](https://wps.com/download) | [App Store](https://apps.apple.com/us/app/wps-office-pdf-docs-sheets/id1491101673) | [Google Play](https://play.google.com/store/apps/details?id=cn.wps.moffice_eng)
# 🚪Converters of Supercell's formats
## ♻️ Specialized  
### [Flat Converter](https://github.com/Daniil-SV/Supercell-Flat-Converter) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Python.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">  
Can convert between regular GLB and FlatBuffered GLB.

### [SCTX Converter](https://github.com/Daniil-SV/SCTX-Converter) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Python.svg" height="16rem"> |  <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">
Can convert between SCTX and PNG.

### [SCW by Opegit Studio](https://github.com/OpegitStudio/SCW) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Java.svg" height="16rem">  
Can convert between SCW and DAE.

<!--### [XCoder by Lexa]()
Find urself
-->

<!--## 🫡 Aged poorly, but was important
### [SC Editor by ToxicLand]

### [another XCoder]()

### вряд-ли это выйдет из комментариев

### так то устаревших программ немало, но 90% из них это XCoder
-->
## 🛠️ Universal
### [SC Editor](https://github.com/danila-schelkov/sc-editor) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Java.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem"> <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Apple.svg" height="16rem"> <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Linux.svg" height="16rem">  
Allows you to open and view SC (both v1 and v2) and SCTX files. It can be used to save different game files in SC v1 format and to test the functionality of custom changes to SC files. It can also render an object into a picture or video, which can be useful for content creators.  
SC Editor is built modularly, which means these modules can be taken and used for your own purposes. For example, you could write an application that opens SC2 files and saves them in the old SC format. Such idea already has [demo](https://github.com/danila-schelkov/sc-reassembler).  
> [!important]  
> [KTX Tools](https://github.com/KhronosGroup/KTX-Software) are required for the program to function properly. Don't forget to «Add it to PATH» in the installer!

*Not to be confused with outdated SC Editor by ToxicLand*
### [SimpleTexToolGUI](https://github.com/ARHCOS/SimpleTexToolGUI) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Python.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">  
A simple texture conversion tool with a GUI for SC games. Based on PVRTexTool and SCTX Converter. Can convert:
- KTX ←→ PNG
- PVR → PNG
- SCTX ←→ PNG

## 🖌️ For working in Adobe Animate
### [ScDowngrade](https://github.com/Daniil-SV/ScDowngrade) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/C++.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem"> 
Downgrades SC files from v2 to v1 or v0.5. Used for the sake of compatibility with the program below.

### [SC2FLA](https://discord.com/channels/751042695698579457/751056303123857509/1288796520199487532) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Python.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">
Converts SC v0.5 and v1 files into an FLA document – Adobe Animate project file.

### [SupercellSWF Animate](https://github.com/sc-workshop/SupercellSWF-Animate) <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Animate.svg" alt="Adobe Animate" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">  
A plugin for Adobe Animate that allows you to export the project to an SC file. Should work on versions greater than Animate 2022, but the recommended and most stable version is Animate 2023.

# 🥣 Miscellaneous
### FFmpeg <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Bash.svg" height="16rem"> | <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Android.svg" alt="Android" height="16rem"> <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Linux.svg" height="16rem"> <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Apple.svg" height="16rem"> <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">
Converter of any kind of media files with a huge set of parameters. The catch is that the utility can be fully used only in the command line - there is no GUI.

It'll be useful for its ability to mass convert audios and even videos to the preferred by the game OGG format. This is done differently depending on the platform:
#### Termux <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Android.svg" alt="Android" height="16rem"> / Bash <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Linux.svg" height="16rem">  
```bash
shopt -s nullglob
mkdir Converted
for FILE in *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac;
    do ffmpeg -hide_banner -i "$FILE" -c:a libvorbis -vn -q:a 0 "Converted/`echo ${FILE%.*}.ogg`"
done
shopt -u nullglob
```
<details>  

<summary>Elaboration</summary>  

- `shopt -s nullglob` is needed so that when the system fails to find files matching, for example, the `*.avi` condition, it will return an empty response. Without this command, the condition is interpreted as a literal file name, and FFmpeg will do unnecessary actions with non-existent files, flooding the terminal with errors along the way.
- `mkdir Converted` creates a folder named "Converted".
- `for FILE in *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac; do` sets the variable "FILE" to include the text corresponding to one of the popular audio and video formats first, and then executes the following command.
- ffmpeg -hide_banner -i "$FILE" -c:a libvorbis -vn -q:a 0 "Converted/\`echo ${FILE%.\*}.ogg\`" – the convertion command itself:
    - `-hide_banner` removes unnecessary information about preset command parameters.
    - `-i "$FILE"` specifies the source file, which searches for all files matching one of the conditions from the "FILE" variable.
    - `-c:a libvorbis` sets the codec of the final result to the one we want, just in case. Without this, OGG may be treated as video by the program and the whole file may be corrupted.
    - `-vn` removes the video from the final result – all the YouTube to MP3 stuff exists thanks to it! This includes the track's album art – a nice bonus for saving space.
    - `-q:a 0` sets the so-called track quality level to zero. In other words it's a **variable bitrate** somewhere between 48 and 80 kbps – the same one used in the game.
    - "Converted/\`echo ${FILE%.\*}.ogg\`" – the name of the final result and the path to save it:
        - `Converted/` – inside the previously created folder.
        - \`echo ${FILE%.}.ogg\` – copies the names of the source files, excluding all text after the last dot (i.e. file extension), and attributes a new one - OGG.
- `done` ends the for...in loop.
- `shopt -u nullglob` removes the effect of the very first command.
</details>

#### PowerShell <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Windows.svg" alt="Windows" height="16rem">  
> [!warning]  
> It hasn't been tested for workability - a similar script can be found on the internet.

```powershell
Get-ChildItem *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac { 
    ffmpeg -hide_banner -i $_.FullName -vn -c:a libvorbis -q:a 0 ("Converted" + "\" + $_.Name + ".ogg") 
}
```
<details>  

<summary>Elaboration</summary>  

- Unlike the previous method, you don't need to specify the `shopt -s nullglob` semblance, as PowerShell already has this behaviour by default.
- `Get-ChildItem *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac {...}` searches media files for matching one of the popular audio and video formats in the current directory, and then executes the command inside curly braces.
- `ffmpeg -hide_banner -i $_.FullName -vn -c:a libvorbis -q:a 0 ("Converted" + "\" +$_.Name)`- the command itself to convert:
    - `-hide_banner` removes unnecessary information about preset command parameters.
    - `-i "$FILE"` specifies the source file, which searches for all files matching one of the conditions from the "FILE" variable.
    - `-c:a libvorbis` sets the codec of the final result to the one we want, just in case. Without this, OGG may be treated as video by the program and the whole file may be corrupted.
    - `-vn` removes the video from the final result – all the YouTube to MP3 stuff exists thanks to it! This includes the track's album art – a nice bonus for saving space.
    - `-q:a 0` sets the so-called track quality level to zero. In other words it's a **variable bitrate** somewhere between 48 and 80 kbps – the same one used in the game.
    - `("Converted" + "\" + $_.Name + ".ogg")` – the copied name (without extension) of the final result "\$\_.Name", new file extension ".ogg" and path of its saving – the "Converted" folder:
         - Note: unlike any other operating system where directories are separated by regular slashes "/", in Windows they are separated by backslashes "\\", which are also **delimiters** – special characters that prevent the properties of the next special character. Inside of quotes any special character loses their properties, but this rule has its pitfalls. That's why the backslash is placed in a separate block of quotes to prevent possible errors.
</details>