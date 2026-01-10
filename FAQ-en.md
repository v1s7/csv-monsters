<sup>created \& translated by v1s7 with the help of [DeepL](https://www.deepl.com/) and [Kagi](https://translate.kagi.com/), inspired by MrsFolls</sup>  
[Версия на русском 🇷🇺](/FAQ.md)

The contents of this FAQ can be accessed by clicking the ⋮☰ button in the upper right corner. 
-----
-----
# Mundane

### How to remove/enable/disable mods?
#### On iOS <img src="/static/icons/Dark/Apple.svg" height="16rem">
Remove all files (or just `fingerprint.json`) from the `updated` folder – here's its path:
```
/var/mobile/Containers/Data/Application/NB v##.###/Documents/updated
```  
It won't affect any critical data – the game will re-download the missing files by itself.
#### On Android <img src="/static/icons/Dark/Android.svg" height="16rem">
<img src="/static/faq/mm/Menu.webp" width="100%"/>
This mod management menu can be opened in several ways: 

##### 1. Straight from the game
<img src="/static/faq/mm/Ingame.webp" width="100%"/>
1. Go to the in-game settings.  
2. Tap the button with purple text «Manage mods…».

There is no need to download a separate mod for this button anymore – this functionality has been added to the vanilla game!

##### 2. By a URL
http://files.dnull.xyz/mods.html

##### 3. Via "App info" menu
<img src="/static/faq/mm/AppInfo.avif" width="260em"/>
1. Clear the game data. Don't worry, the data itself will not be cleared.  
2. In the opened menu, select «Manage modifications».  

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
> <summary><h4>About incompatibilities and "gv"</h4></summary>  
> 
> 1. All unsigned mods are disabled by default since v60. So after installing one you need to manually enable it in the mod manager.
> 
> 2. If the ENABLE button is pale, then it means the mod is incompatible with v60 – it happens because the mod has .sc files, however, this can be bypassed by adding the following line in `content.json` (e.g. after `@description`):
> ```json
> "@gv": 60,
> ```  
> where:
> - \@gv – "game version" meta-tag;
> - 60 – current version (now it's different, of course)
> </details>

#### New method (for v65 or later)
<details>  

<summary>daniillnull: (translated)</summary>  
Small announcements regarding the testing of unsigned modifications ("installing zip").  

As you've probably [seen in the main chat](https://t.me/nb_mods/1/110889), this feature will appear in the next update.  
Now, more details about how it will work: to unlock this feature, you'll need to install a special client of Null's Brawl. It'll be fully compatible with the regular client, having the same signature and package name.  
It's something like an "APK for modders", but now **official**, **reliable** and **safe**.  
In this regard, I'd like to remind you again that from now on, the use of third-party APKs will be much more strictly controlled. Don't take risks and don't download malware from the internet. And if you've created it yourself — it's time to consider making mods in our format instead of APKs.
</details>

Starting with v65, an official method for installing unsigned mods for testing purposes has been introduced[⁶](https://t.me/nb_mods/16782/112860). A section called "Libraries & sources" has appeared in the mod manager, where you can select a folder (preferably a new one) to load mods from it. These mods will appear in the list alongside all the others and you'll be able to start testing.  
<img src="/static/faq/mm/FolderUnavailable.webp" width="100%"/>
However, the button to add a custom folder in the mod manager isn't available to everyone. It needs to be unlocked. To do this, you need to download the game's APK again, but from a different URL. It'll be provided below.

>[!IMPORTANT]  
>By using this APK you accept all the rules and conditions for creating modifications. You must not use it to install modifications that you are not involved in developing or testing. In case of rule violations, your account in the game and Null's Connect may be permanently suspended.

**Link to the APK with the ability to test modifications:**  
- v65: https://tempweb.nullsusercontent.com/fpapk/nb_65.165_release_412b740e.apk?allowUnsignedMods=1  
<img src="/static/faq/mm/FolderAdded.webp" width="100%"/>
Structure of the mod folders looks like this:  
```
{mods folder}/{uuid}/content.json
```  
<details>  

<summary>Visual example</summary>  

```
└── 📂mods/
    ├── 📂a026ca56-807c-5605-9f29-73c3d34a0c81/
    │   └── 📄content.json
    ├── 📂263ca6f6-2689-46b8-8830-86f458c8b87b/
    │   ├── 📄content.json
    │   ├── 🖼️icon.png
    │   └── 📂sc/
    │       └── 💾level.sc
    ├── 📂8a59e795-ae15-4622-9460-a931b98e0502/
    │   ├── 📄content.json
    │   └── 🖼️icon.png
    └── 📂d4530d00-a021-4d32-b04f-6933538732de/
         ├── 📄content.json
         ├── 🖼️icon.png
         ├── 📂sfx/
         │   └── 💾supercell_jingle.ogg
         ├── 📂music/
         │   ├── 💾power_of_neo.ogg
         │   ├── 💾no_more_deals.ogg
         │   ├── 💾mus_menu7.ogg
         │   ├── 💾mus_f.ogg
         │   └── 💾lunar_brawl_menu_01.ogg
         └── 📂sc/
             ├── 💾background_waterfall.sc
             └── 💾background_waterfall_tex.sc
```  

</details>

- The {uuid} folder names must contain only the UUID and nothing else. **Check if there're any spaces at the end/beginning of the name – this is the most common issue**.  
- Only folders with a UUID as their name can be inside the mods folder.  
- The rest of mod's files, if there're any, are stored beside `content.json`.
> [!TIP]  
> As you know from the [manual](/MANUAL-en.md), a UUID can be generated on https://uuidgenerator.net/ so you shouldn't have any problems with that (you've already read it, right?)  

#### Old methods (for v64 or sooner)
>[!IMPORTANT]  
>This section serves an archival purpose and should not be used. It's better to use the [new method](#new-method-for-v65-or-later).  

Just paste the folder (the name of which needs to be a UUID (generate [here](https://uuidgenerator.net)) and nothing else) containing the mod to the path
`/data/data/daniillnull.nulls.brawlstars/mods/`. This can be done in two ways:
#### 1. Using ROOT / a virtual machine
Using superuser privileges or a virtual machine with Magisk support (such as [Virtual Master](https://drive.google.com/file/d/1M15zazz8sEhC2wWzl0igFNghTtAvkt6U/view)). The virtual machine will need 6GB of free space.  
>[!TIP]  
>Despite this method remaining functional, starting with v65 a [more convenient alternative](#new-method-for-v65-or-later) has been made.

Video tutorial: ~~[YouTube](https://youtu.be/4Bzl8jt57qc)~~ (removed by Suреrсеll :c) | [Odysee](https://odysee.com/@visthj:f/nb-zip-rootvm-method:4)  
(English coming ~~very soon~~ never)
#### 2. Patching apk of Null's Brawl
>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

More specifically to open access the app's private storage to DocumentProvider and to remove apk signature verification. Keep in mind that this way you risk getting your account banned (a special flag is set when a modified apk is detected), ~~the maintainer still didn't receive this punishment though.~~  
>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

Video tutorial: [YouTube (READ THE WARNINGS)](https://youtu.be/Jqq-g_-TLhU) | [Odysee (READ THE WARNINGS)](https://odysee.com/@visthj:f/nb-zip-apktool-method:c)  
(English coming ~~very soon~~ never)
>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

>[!CAUTION]  
> THIS METHOD NO LONGER WORKS AND WILL RESULT IN YOUR ACCOUNT GETTING BANNED. PLEASE USE THE [ALTERNATIVE](#new-method-for-v65-or-later).

> [!TIP]  
> Private storage of Null's Brawl can be accessed by [other file managers](/PROGRAMS-en.md#-explorers) as well:
> <details>  
> <summary>Material Files</summary>  
> [MaterialFiles.webm](/static/faq/dp/MaterialFiles.webm)  
> Left slideout menu → Add storage → External storage → Left slideout menu → Null\'s Brawl → Use this folder → Grant → daniillnull.nulls.nullsbrawl → data → mods
> </details><details>  
> <summary>MT Manager</summary>  
> [MT.webm](/static/faq/dp/MT.webm)    
> Left slideout menu → Three dots on top center → Add local storage = Left slideout menu → Null\'s Brawl → Use this folder → Grant → Null\'s Brawl → data → mods
> </details><details>  
> <summary>MiXplorer</summary>
> [MiX.webm](/static/faq/dp/MiX.webm)  
> </details><details>  
> <summary>Total Commander</summary>
> [TotalCommander.webm](/static/faq/dp/TotalCommander.webm)    
> </details>

### When installing a signed mod (.NullsBrawlAssets) gives me an error? 
There can be several reasons:  
1. The signature has expired (signatures made by the bot only last 3 days, the manually singed mods last 90 days) – if that's the case, ask the mod's author to sign it again (or ask the moderators to do it if it was signed manually in Signing Requests Pro).  
2. The archive is either improper or damaged – you can't really do anything about this besides downloading the file again, that usually helps.  
3. There's not enough space on your device left – have mercy on your phone, clean it out of random junk! It's probably also extremely slow just because of that.  
4. IOException – same as the one above, but usually happens on rooted devices with a custom ROM when there's not enough space in the Root partition. Instances may vary, look for the exact error in logcat. Your system might be flawed and needs to be properly re-installed if the issue isn't the lack of space.

### Why when I open the ZIP Null's Brawl does not appear?
This can and will only work with .NullsBrawlAssets

The reason Null's Brawl doesn't show up in the app selection menu when you try to open a ZIP is because unsigned mods were never intended to be installed in the first place

# Community

### How to make mods?  
Everything is described in the [official manual](/MANUAL-en.md) (this one is localized to English). Be sure to read it from cover to cover!

> [!NOTE]  
> To create and modify text files (.json and .toml among others) on Android, you can either use the text editor that's built into your [file manager](/PROGRAMS-en.md#-explorers), or use a [separate code editor](/PROGRAMS-en.md#-editors).

> [!TIP]  
> There is also a website for simplified creation process of "small" mods for Null's Brawl: https://darkmean-dev.github.io/nullsmod

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
> Before making a request like "send me China skins mod pls", try to find the mod you need in the chat room mentioned above. You can do this by turning on "Unified Chat" in "⋮" and going to "Search" in the same menu. 

### Why is there a 5 minute delay on messages?  
That chat was made for modders to ask questions and get help in making mods, not for off-toping (although it's still not enforced). You can go to [@dnclserv_chat](https://t.me/dnclserv_chat) or [@nulls_ru](https://t.me/nulls_ru) to chat about something else. 

### Are there rules in the chat? 
Yes. [Here](https://telegra.ph/Pravila-chata-Nulls-04-24) they are. 

### Where can I spend my boosts?
С ноября 2025 забустив чат мододелов ([@nb_mods](https://t.me/nb_mods)) можно будет писать в нём без медленного режима в 5 минут.  
Помимо чата мододелов, вы можете получить трофеи на аккаунт за буст другого чата. Firstly you need to link your Null's Connect account to Telegram and boost the official channel [@nulls_ru](t.me/boost/nulls_ru). You can do it in the additional settings in Null's Connect itself.  
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
Ever noticed that all files in Android are located in the `/storage/emulated/0/` path? This is called the internal directory or internal storage and contains all the user's files. But there is also a root directory - just `/`. Root access allows apps to interact with this directory, which means they can access every single file on the device, including system ones, as well as private application storage.

The owner of these permissions is called a superuser and exists in all UNIX-like systems. For example, in Linux, the internal directory is the home directory – `/home/username/`.

### How to get root access? 
> [!CAUTION]  
> This is an extremely dangerous, long and difficult process where you can not only make the system less stable, but also completely brick your device and, sometimes, with no way back. Think thrice if you really need it (most likely not).

In the traditional way, you will need to unlock the bootloader of the system (and therefore clear all the data on the device), which by the way may already be impossible without a certain physical intervention on some devices, install a custom recovery and flash Magisk. 

It will be easiest for Google Pixel owners, in which bootloader unlocking is extremely simple and with the system that most developers of such software rely on and support. For such purposes there are threads for each model of different devices with instructions on Russian-speaking 4PDA and English-speaking XDA forums.