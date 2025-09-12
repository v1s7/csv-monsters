<sup>created \& translated by v1s7, inspired by MrsFolls</sup>  
[Версия на русском 🇷🇺](/FAQ.md) | [用中文阅读（很快）🇨🇳](/FAQ-cn.md)  

The contents of this FAQ can be accessed by clicking the ⋮☰ button in the upper right corner. 
-----
-----
# Mundane

### How to remove/enable/disable mods?
#### On iOS <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Apple.svg" height="16rem">
Remove all files (or just `fingerprint.json`) from the `updated` folder – here's its path:
```
/var/mobile/Containers/Data/Application/NB v##.###/Documents/updated
```  
It won't affect any critical data – the game will re-download the missing files by itself.
#### On Android <img src="https://github.com/gui-bus/TechIcons/raw/refs/heads/main/Dark/Android.svg" alt="Android" height="16rem">
<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/manage-mods-menu.webp" width="100%"/>
This mod management menu can be opened in several ways: 

##### 1. Straight from the game
<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/manage-mods-ingame-button.webp" alt="1. Go to the in-game settings. 2. Tap the button with purple text «Manage mods…»." width="100%"/>
There is no need to download a separate mod for this button anymore – this functionality has been added to the vanilla game!

##### 2. By a URL
http://files.dnull.xyz/mods.html

##### 3. Via "App info" menu
<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/manage-mods-settings-method-24fps.avifs" alt="1. Clear the game data. Don't worry, the data itself will not be cleared. 2. In the opened menu, select «Manage modifications»." width="260em"/>

### How to install a mod on iOS?
> [!important]  
 > <details>  
 > 
 > <summary>The maintainer doesn't have any iOS device!</summary>  
 > The current maintainer doesn't own any iOS device and can't verify the information in practice, so proceed with caution. If you own one – please share your experience by posting it in <a href="https://github.com/v1s7/csv-monsters/issues">Issues</a>!  
 > 
 > </details>  
 > 
 > -----
 > <details>  
 > 
 > <summary>There's no modloader on iOS!</summary>  
 > Exactly. Everything is done by putting files in the `updated` folder, just like in v58 on Android. Have you noticed that CSV files are generated inside NullsBrawlAssets upon signing? They exist only for the sake of iOS users. Android modloader completely ignores them.  
 > </details>  

1. Download the latest .ipa file of Null's Brawl and install the game via [Sideloadly](https://sideloadly.io) (requires having a computer and an Apple ID), beforehand enabling File Sharing in advanced settings.
> [!tip]  
> Alternatively you can unzip the IPA file and add the UISupportsDocumentBrowser (bool) key with a value of TRUE into Info.plist, then archive it back, sign and install, you should get the same result. 
2. Open the game at least once. 
3. Download any .NullsBrawlAssets file, extract it as a ZIP archive (for example, with [Filza](https://www.tigisoftware.com/default/?page_id=78)) and put all the contents in the path `/var/mobile/Containers/Data/Application/NB v##.###/Documents/updated/`.

> [!tip]  
> - If you need to – rename the .NullsBrawlAssets file extension to .zip  
> - If an overwriting confirmation screen appears – choose to overwrite all files

### How to install a signed mod (.NullsBrawlAssets) on Android?
Download and open a mod file (.NullsBrawlAssets) directly from Telegram and select Null's Brawl in the list of apps. Check the box and click install. And that's it.

> [!NOTE]  
> If for some reason Telegram doesn't open the file, click on "⋮", then "Save to Downloads" (do it twice just for sure), open a file explorer, go to Download/Telegram folder (for people with certain third-party clients the folder might be called Download/AyuGram or similar) and open the mod file from there.

> [!NOTE]  
> Some file managers may not see Null's Brawl supporting its file format. You can try opening the file with [another file manager](/PROGRAMS-en.md#-explorers) in this case.

### How to install mod zip file (unsigned) on Android?   

> [!IMPORTANT]  
> <details>  
> 
> <summary><h4>HIGHLIGHTS FOR V61</h4></summary>  
> 
> 1. All unsigned mods are disabled by default since v60. So after installing one you need to manually enable it in the mod manager.
> 
> 2. If the ENABLE button is pale, then it means the mod is incompatible with v61 – however, this can be bypassed by adding the following line in `content.json` after `@description`:
> ```json
> "@gv": 61,
> ```
> </details>

Just paste the folder (the name of which needs to be a UUID (generate [here](https://uuidgenerator.net)) and nothing else) containing the mod to the path
`/data/data/daniillnull.nulls.brawlstars/mods/`. This can be done in two ways:
#### 1. Using ROOT / a virtual machine
Using superuser privileges or a virtual machine with Magisk support (such as [Virtual Master](https://drive.google.com/file/d/1M15zazz8sEhC2wWzl0igFNghTtAvkt6U/view)). The virtual machine will need 6GB of free space. 
Video tutorial: [YouTube](https://youtu.be/4Bzl8jt57qc) | [Odysee](https://odysee.com/@visthj:f/nb-zip-rootvm-method:4)  
(English coming *very* soon)
#### 2. Patching apk of Null's Brawl
More specifically to open access the app's private storage to DocumentProvider and to remove apk signature verification. Keep in mind that this way you risk getting your account banned (a special flag is set when a modified apk is detected), the maintainer still didn't receive this punishment though.  
Video tutorial: [YouTube](https://youtu.be/Jqq-g_-TLhU) | [Odysee](https://odysee.com/@visthj:f/nb-zip-apktool-method:c)  
(English coming *very* soon)

> [!TIP]  
> Private storage of Null's Brawl can be accessed by [other file managers](/PROGRAMS-en.md#-explorers) as well:
> <details>  
> <summary>Material Files</summary>  
> <img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/documents-provider-in-materialfiles.avifs" alt="Left slideout menu \> Add storage \> External storage \> Left slideout menu \> Null\'s Brawl \> Use this folder \> Grant \> daniillnull.nulls.nullsbrawl \> data \> mods" width="260em"/>  
> </details><details>  
> <summary>MT Manager</summary>  
> <img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/documents-provider-in-mtmanager.avifs" alt="Left slideout menu \> Three dots on top center \> Add local storage \> Left slideout menu \> Null\'s Brawl \> Use this folder \> Grant \> Null\'s Brawl \> data \> mods" width="260em"/>  
> </details>

### When installing a signed mod (.NullsBrawlAssets) gives me an error? 
There can be several reasons:  
1. The signature has expired (signatures made by the bot only last 3 days, the manually singed mods last 90 days) – if that's the case, ask the mod's author to sign it again (or ask the moderators to do it if it was signed manually in Signing Requests Pro).  
2. The archive is either improper or damaged – you can't really do anything about this besides downloading the file again, that usually helps.  
3. There's not enough space on your device left – have mercy on your phone, clean it out of random junk! It's probably also extremely slow just because of that.  
4. IOException – same as the one above, but usually happens on rooted devices with a custom ROM when there's not enough space in the Root partition. Instances may vary, look for the exact error in logcat. Your system might be flawed and needs to be properly re-installed if the issue isn't the lack of space.

### Why when I open the ZIP Null's Brawl does not appear?
This can and will only work with .NullsBrawlAssets.

The reason Null's Brawl doesn't show up in the app selection menu when you try to open a ZIP is because unsigned mods were never intended to be installed in the first place. And also because the app selection menu would be cluttered – ZIPs are everywhere, for example APKs are also an embellished ZIP archives.

# Community

### How to make mods?  
Everything is described in the [official manual](/MANUAL-en.md) (this one is localized to English). Be sure to read it from cover to cover!

> [!NOTE]  
> To create and modify text files (.json and .toml among others) on Android, you can either use the text editor that's built into your [file manager](/PROGRAMS-en.md#-explorers), or use a [separate code editor](/PROGRAMS-en.md#-editors). <!--[QuickEdit](https://xdaforums.com/t/app-4-0-3-quickedit-text-editor.2899385/) for Android, [Runestone Text Editor](https://apps.apple.com/us/app/runestone-text-editor/id1548193893) for iOS, or [Notepad++](https://notepad-plus-plus.org/) for Windows.-->

> [!TIP]  
> There is also a website for simplified creation process of "small" mods for Null's Brawl: https://nb-mods.vercel.app

> [!TIP]  
> And I should mention the unofficial [tutorial on creating mods in JSON](https://telegra.ph/Tutor-po-dzhsonu-dlya-modov-nulya-bravla-11-12) (use auto-translation to read it in your language). It should be noted, however, that v58 was the latest version at the time it was written and a lot of currently crucial information isn't mentioned (such as the requirement to enter "@title" and "@description").

### About modpacks and their futility, unless you're on iOS
As of v59 the game got an updated modloader, which made it possible to install several mods at a time.[²](https://t.me/nb_mods_for_kids/13) Making modpacks is a long, tedious and pointless endeavor now, because you can just install the mods you want and that's it. This won't save time, neither for your nor for others. 

However, there's one case where modpacks are still needed – iOS, because there mods work by extracting modified assemblies into the `updated` folder, i.e. there is no mod loader on iOS at all. Have you noticed that within NullsBrawlAssets, CSV files are also generated when signed? They exist only for the sake of iOS players, while they are completely ignored by the Android modloader.

### How do I sign a mod?
Do it with [official bot](https://t.me/nulls_mods_bot) by sending it your JSON file with the /sign command in one message (you can also send this command as a reply to the attached file in a separate message).  
> [!important]  
> The bot only accepts "small" mods – that are made out of a single JSON file, meaning you can't sign "large" mods in a ZIP archive. Read further to learn how to sign them.

You may also send your mod to [Signing Requests Pro](https://t.me/nb_mods/3) if it got additional resources (a .zip mod), or if you want to sign your mod with a stricter and longer term signature. Litter mods and old classic mods with modified CSVs in them are no longer welcome there.[³](https://t.me/nb_mods/3/4525)

> [!NOTE]  
> The format of the signature request is as follows: a ZIP archive that includes a content.json file and all the additional resources, if any. You can leave author information in content.json with "@author" and the request itself. 

### Where can I download mods from other people? 
In the official (stagnant) [channel](https://t.me/nb_mods_for_kids) with mods, the Library inside of the mod manager (Android only) and [chat](https://t.me/nb_mods) of modders:
- For simple scripts, see `Signing Reqiests Lite`, 
- for signed mods in `Mods v## (Signed)`, 
- for unsigned mods in `Signing Requests Pro`, 
- for modding updates, check out `Updates`, 
- and `General` is for questions, suggestions, ideas and other kinds of support,
- you can ignore the other topics – you'll see for yourself what they're for if you need them.

> [!IMPORTANT]  
> Before making a request like "send me a mod for China Nulls", try to find the mod you need in the chat room mentioned above. You can do this by turning on "Unified Chat" in "⋮" and going to "Search" in the same menu. 

### Why is there a 5 minute delay on messages?  
That chat was made for modders to ask questions and get help in making mods, not for off-toping (although it's still not enforced). You can go to [@dnclserv_chat](https://t.me/dnclserv_chat) or [@nulls_ru](https://t.me/nulls_ru) to chat about something else. 

### Are there rules in the chat? 
Yes. [Here](https://telegra.ph/Pravila-chata-Nulls-04-24) they are. 

### Where can I spend my boosts?
Firstly you need to link your Null's Connect account to Telegram and boost the official channel [@nulls_ru](t.me/boost/nulls_ru). You can do it in the additional settings in Null's Connect itself.  
For a boost you will receive **2000 trophies** for a random character **every Friday**. For each additional boost you'll receive 250 trophies more. If you boost for the first time, you'll also receive extra 3000 trophies.[⁴](https://t.me/nulls_ru_faq/5).

### I found a bug in a mod
You can write a message about it in [this](https://t.me/nb_mods/1) thread, mentioning the author of the mod by @username beforehand (DM-ing them is strongly discouraged).

# Normalization of context

### How do I check the contents of .NullsBrawlAssets?
Just change the file extension from .NullsBrawlAssets to .zip by renaming the file and look inside of it. Most file managers can do this even without changing the extension. 

### What is a ZIP?
[Read here](/FILETYPES-en.md#zip)

### Can I open a ZIP archive without a computer?
Of course you can, any file manager should work with archives, both on phones, and on computers, even on TVs. The only thing that makes WinRAR stand out is that it can archive files in its proprietary RAR format (but anything can unpack it), which nowadays isn't very popular.

### What is root?
Ever noticed that all files in Android are located in the `/storage/emulated/0/` path? This is called the internal directory or internal storage and contains all the user's files. But there is also a root directory - just `/`. Root access allows programs to interact with this directory, which means they can access every single file on the device, including system ones, as well as private application storage.
> [!WARNING]  
> This opens up many possibilities for customization, as well as security risks.

The owner of these permissions is called a superuser and exists in all UNIX-like systems. For example, in Linux, the internal directory is the home directory – `/home/username/`.

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