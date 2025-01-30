<sup>v1.5 - created \& translated by v1s7, inspired by MrsFolls</sup>

[Версия на русском](https://github.com/v1s7/csv-monsters/tree/main/FAQ.md)

> [!TIP]  
> The contents of this FAQ can be accessed by clicking the ⋮☰ button in the upper right corner. 

> [!NOTE]  
> It is adviced that you read the [README](https://github.com/v1s7/csv-monsters/tree/main/README-en.md) first before you start reading this FAQ.

# Mundane

### How do I remove mods or resource patch files?
This is useful to know in advance. The menu for removing mods can be accessed at http://files.dnull.xyz/mods.html.

The advanced menu, where you can remove the resource patch files, can be accessed by clearing the game data in the settings. Don't worry, the data itself shouldn't be cleared right away. 

### How to install a mod on iOS?
> [!CAUTION]  
> The current maintainer has no idea about the integrity of this answer, as the maintainer does not own any iOS device. Take this information with caution and intelligence.

1. Download the latest version of Null's Brawl and install the game via [Sideloadly](https://sideloadly.io) with file sharing enabled (or unzip the IPA file and add the UISupportsDocumentBrowser (bool) key with a value of TRUE to Info.plist, then unzip back, sign and install, it will be the same). 
2. Log into the game at least once. 
3. Download the .NullsBrawlAssets file, extract it as a ZIP archive (for example, with [Filza](https://www.tigisoftware.com/default/?page_id=78)) and put all the contents in the path `/var/mobile/Containers/Data/Application/NB v58.279/Documents/updated/mods/`.

### How to install a signed mod (.NullsBrawlAssets) on Android?
Download and open the mod file (.NullsBrawlAssets) directly from Telegram and select Null's Brawl in the list of apps. Check the box and click install. And that's it.

> [!NOTE]  
> If for some reason Telegram doesn't open the file, click on "⋮", then "Save to Downloads", open a file explorer, go to Download/Telegram folder (for people with certain third-party clients the folder might be Download/AyuGram or similar) and open the mod file from there.

> [!NOTE]  
> Please note that some file managers do not see some intent filters, and because of that they don't see Null's Brawl supporting this file format. You can try another file manager in this case, such as:
> - [MT Manager](https://mt2.cn) ([4PDA topic](https://4pda.to/forum/index.php?showtopic=548542)),
> - [Solid Explorer](https://neatbytes.com/solidexplorer/index.php/about) ([4PDA topic](https://4pda.to/forum/index.php?showtopic=325553)),
> - [MiXplorer](https://www.mixplorer.com) ([4PDA topic](https://4pda.to/forum/index.php?showtopic=318294)), 
> - [ZArchiver](https://zdevs.ru) ([4PDA topic](https://4pda.to/forum/index.php?showtopic=305019)).

### How to install mod zip file (unsigned) on Android?   
Just paste the folder (the name of which needs to be a UUID (generate [here](https://uuidgenerator.net)) and nothing else) containing the mod to the path
`/data/data/daniillnull.nulls.brawlstars/mods/`. This can be done in several ways:
1. Using root privileges or a virtual machine with Magisk support (such as [Virtual Master](https://drive.google.com/file/d/1M15zazz8sEhC2wWzl0igFNghTtAvkt6U/view)). The virtual machine will need 6GB of free space. Video tutorial: [YouTube](https://youtu.be/4Bzl8jt57qc) | [Odysee](https://odysee.com/@visthj:f/nb-zip-rootvm-method:4) (English coming soon)
2. Modifying the Null's Brawl apk file to open access to hidden app data to the document provider and to remove apk signature verification. Keep in mind that this way you risk catching a ban on your account. Video tutorial: [YouTube](https://youtu.be/Jqq-g_-TLhU) | [Odysee](https://odysee.com/@visthj:f/nb-zip-apktool-method:c) (English coming soon)

### When installing a signed mod (.NullsBrawlAssets) it gives me an error, why? 
Perhaps it has an expired signature (signatures made by the bot only last 3 days) and/or it's not compatible with the current version of the game. Or the mod itself is broken, which is highly unlikely for a signed one. 

### Why when I open the ZIP Null's Brawl does not appear?
This can and will only work with .NullsBrawlAssets.

The reason Null's Brawl doesn't show up in the app selection menu when you try to open a ZIP is because unsigned mods were never intended to be installed in the first place. And also because the app selection menu would be cluttered – ZIPs are everywhere, for example APKs are also an embellished ZIP archives.

# Community

### How to make mods?  
Everything is described in the [official manual](https://github.com/v1s7/csv-monsters/tree/main/MANUAL-en.md) written in Russian (it'll be available in English someday). Be sure to read it from cover to cover!

> [!NOTE]  
> To create and modify text files (.json and .toml among others) on Android, you can either use the editors that are built into your file manager, or use [QuickEdit](https://xdaforums.com/t/app-4-0-3-quickedit-text-editor.2899385/) for Android, [Runestone Text Editor](https://apps.apple.com/us/app/runestone-text-editor/id1548193893) for iOS, or [Notepad++](https://notepad-plus-plus.org/) for Windows.

> [!TIP]  
> There is also a website for simplified creation process of "small" scripted mods for Null's Brawl: https://nb-mods.vercel.app

> [!TIP]  
> And I should mention the unofficial [tutorial on creating mods in JSON](https://telegra.ph/Tutor-po-dzhsonu-dlya-modov-nulya-bravla-11-12) (use auto-translation to read it in your language).

### About modpacks and the lack of sense in them
As of version 59.197, the game now has an updated modloader and it's possible to install several mods at a time.[²](https://t.me/nb_mods_for_kids/13) Making modpacks is a long, tedious and pointless endeavor now, because you can just install the mods you want and that's it. This won't save time, neither for your nor for others. 

#### How do I sign a mod?
Do it with [official bot](https://t.me/nulls_mods_bot) by sending it a script with the /sign command in one message. And yes, you can submit to the bot both "small" and "large" mods, but you can also submit to [Signing Requests Pro](https://t.me/nb_mods/3) if your mod requires additional resources, or if you want to sign your mod with a stricter and longer term signature. Trash mods and old classic mods with modified CSVs in them are no longer welcome there.[³](https://t.me/nb_mods/3/4525)

> [!NOTE]  
> The format of the signature request is as follows: a ZIP archive that includes a content.json file and optionally additional resources. You can leave author information either in content.json, with "@author" and in the game. 

### Where can I download mods from other people? 
In the official [channel](https://t.me/nb_mods_for_kids) with mods and [chat](https://t.me/nb_mods) of modders:
- For simple scripts, see `Signing Reqiests Lite`, 
- for signed mods in `Mods v## (Signed)`, 
- for unsigned mods in `Signing Requests Pro`, 
- for modding updates, check out `Updates`, 
- and `General` is for questions, suggestions, ideas and other kinds of support.

> [!IMPORTANT]  
> Before making a request like "send me a mod for China Nulls", try to find the mod you need in the chat room mentioned above. You can do this by turning on "Unified Chat" in "⋮" and going to "Search" in the same menu. 

#### Why is there a 5 minute delay on messages?  
This chat is made for modders to ask questions and get help in making mods, not for offtopic. You can go to [@dnclserv_chat](https://t.me/dnclserv_chat) or [@nulls_ru](https://t.me/nulls_ru) to chat about something else. 

### Are there rules in the chat? 
Yes. [Here](https://telegra.ph/Pravila-chata-Nulls-04-24) they are. 

### Where can I spend my boosts?
You can boost the [@nulls_ru](https://t.me/nulls_ru) group, in return you will be given 1,750 trophies each week and 250 trophies inclusive for each boost.[⁴](https://t.me/nulls_ru/811).

#### I found an annoying bug in a mod.
If the problematic mod was not taken from this repository (otherwise see [README](https://github.com/v1s7/csv-monsters)), you can post in [this](https://t.me/nb_mods/1) thread, mentioning the author of the mod by @username beforehand (DM-ing them is strongly discouraged).

# Normalization of context

### How do I check the contents of .NullsBrawlAssets?
Just change the file extension from .NullsBrawlAssets to .zip by renaming the file and look inside of it. Most archival apps and programs can do this even without changing the extension. 

### What is ZIP?
https://github.com/v1s7/csv-monsters/blob/main/FILETYPES-en.md#zip

### Can I open a ZIP archive without a computer?
Of course you can, any file manager should work with archives, both on phones, and on computers, and on TVs. The only thing that makes WinRAR stand out is that it can archive files in their proprietary RAR format (but anything can unpack it), which nobody needs nowadays (except for the 4PDA people, although they are forced by forum restrictions).

### What is root?
Ever noticed that all files in Android are located in the `/storage/emulated/0/` path? This is called the internal directory or internal storage and contains all the user's files. But there is also a root directory - just `/`. Root access allows programs to interact with this directory, which means they can access every single file on the device, including system ones, as well as private application storage.
> [!WARNING]  
> This opens up many possibilities for customization, as well as security risks.

The owner of these permissions is called a superuser and exists in all UNIX-like systems. For example, in Linux, the internal directory is the home directory - `/home/username/`.

Some of the features of root access include:  
- uninstalling any pre-installed applications, 
- creating full backups, 
- controlling CPU frequency, 
- installing third-party modules to change the appearance or to introduce new functionality. 

### How to get root access? 
> [!CAUTION]  
> This is an extremely dangerous, long and difficult process where you can not only make the system less stable, but also completely brick your device and, sometimes, with no way back.

In the traditional way, you will need to unlock the bootloader of the system (and therefore clear all the data on the device), which by the way may already be impossible without a certain physical intervention on some devices (for such a service usually charge $75, so it will be more profitable to buy a used Redmi 6a for $25), install a custom recovery and flash Magisk. 

It will be easiest for Google Pixel owners, in which bootloader unlocking is extremely simple and with the system that most developers of such software rely on and support. For such purposes there are threads for each model of different devices with instructions on Russian-speaking 4PDA and English-speaking XDA forums.

<!--Переведено с помощью DeepL https://www.deepl.com/app/-->