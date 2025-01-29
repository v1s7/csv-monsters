<sup>Manual's version: 3.1 (25.12.2024), written by <b>данянул \<3</b> / Original source: https://t.me/nb_mods/16782/21399 / Translated by v1s7 (11.01.2025)</sup>

[Прочитать на русском](https://github.com/v1s7/csv-monsters/blob/main/MANUAL.md)

-----
**This manual provides the basic information you need to create your own mods for Null's Brawl.**

Contents:
```table-of-contents
title: 
style: nestedList # (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 
maxLevel: 0 
includeLinks: true 
hideWhenEmpty: false 
debugInConsole: false 
```
# I. Generic rules
But let's start with... the rules. They are quite simple, but, unfortunately, are not obvious to everyone.
- The title and description of the mod must be meaningful and understandable (without any spelling mistakes)
- Foul language in the title and description are forbidden (in the mod itself is allowed, if appropriate)
- The description should describe the changes made as verbosely as possible  (including side effects, if any)
- In case of borrowing content from other mods or sources, it is recommended to specify them (either in the authorship or in the description)
- You should not modify game texts for the purpose of authorship or advertising (authorship is specified separately in the mod itself)

Also it is exceptionally and **strictly forbidden** to:
- disrupt the game experience
- make changes that are not expected from the description

In case of deliberate development or distribution of mods that violate the rules, the administration may completely restrict the violators' ability to create mods and/or apply other measures at its discretion.

# II. Game files and their structure
Mods are aimed primarily at altering the game files. Therefore, let's take a look at their structure.

## Overall structure of the game folders and files
All basic (necessary for the game) textures, sounds, tables and other files are stored in the assets folder in the APK, or in the res folder in the IPA file. In turn, they are also organized into folders:
- **csv_logic** : tables in csv format describing the behavior of both the client and the server
- **csv_client** : csv tables relating to client behavior only
- **localizations** : csv tables containing all texts in the game for various languages
- **sc** : 2D textures and animations in proprietary format (there are open-source editors of varying quality)
- **sc3d** : 3D textures, models and animations in various formats (glb, scw, png, etc.)
- **json** : files describing some physical aspects of character models
- **music** : background music
- **sfx** : sounds and sound effects
- **fingerprint.json** : necessary to download files from the server (more on this below)

There are also other folders and files that are rarely relevant to modding.

### Tables 
As for tables, it is worth to talk about them in detail. They are stored in **.csv** format (values are separated by commas), one table in each file.

In most cases, the tables describe a separate type of objects. For example, **projectiles.csv** describes all projectiles existing in the game. The first column of the table, **Name** , defines the name of the object, all subsequent columns define its inherent values.

These values can have the following data types:
- Numeric (int)
- Logical (boolean)
- String
- Reference: a special case when a string is the name of an object from the same or another table (for example: "CocoonerCocoon" in the SpawnCharacter column).
- Paths: special case when the string is the path or name of a file (e.g. "sc/effects.sc" in the FileName column).

Moreover, some tables support lists as a value. In such a case, the list is written vertically, each new element on a new unnamed row. A prime example of this would be the **color_gradients.csv** file:

| Name      | Colors   | Speed | Scale |
| --------- | -------- | ----- | ----- |
| String    | String   | int   | int   |
| FreeOffer | FF9FFF72 | 40    | 100   |
|           | FF68E524 |       |       |
|           | FF68E524 |       |       |
|           | FF9FFF72 |       |       |
|           | FFE0FFA0 |       |       |
| ...       | ...      | ...   | ...   |

In this case the **FreeOffer** object will have these values:
- Colors = \[FF9FFF72, FF68E524, FF68E524, FF9FFF72, FFE0FFA0\] (string array)
- Speed = 40 (int)
- Scale = 100 (int)

Now, I recommend that you take a look at all the tables in the game – and familiarize yourself with what useful (or not) data they hold. It'll be interesting, trust me :)

### Game resources
Textures, music, models... here we will not cover how they are organized, because it would require a separate huge manual.
> [!NOTE]  
> [Here it is](https://github.com/v1s7/csv-monsters/blob/main/FILETYPES-en.md) by the way.

It is important to know the following: the tables contain paths to these resources. This means that we can safely add our own files – the key is to specify the path to them in the corresponding tables.

### Server-side patches 
One more thing that's important to keep in mind: the game has a mechanism where it can download some files from the server and use them **instead** of the ones in the APK (IPA).

The algorithm, in a nutshell, is as follows:
1. the game reads the **fingerprint.json** file by reading the **sha** and **version** fields
2. When logging into the server, the game sends the **sha** field to the server
3. If it has an outdated value, the server sends the game a new **fingerprint.json** file and the address of the server from which the files can be downloaded
4. The game checks the **sha** values for each file, and if it has changed, downloads a new version of the file

All files are saved to the separate **update** folder in the process, which is usually located at the following path on Android: /data/data/{package name}/update.

# III. Mods and their structure
Starting with the version 59.197, Null's Brawl has a separate modloader, which introduces several of its own concepts for handling files.

## NullsBrawlAssets 
Mods are distributed in special files, the format of which can be described as follows:
1. The file has the **NullsBrawlAssets** extension
2. The file itself is a Java Archive, i.e. a regular ZIP-archive with META-INF folder

Furthermore, this archive may contain the following files:
1. **META-INF/MANIFEST.MF** : mandatory (according to JAR specifications), contains information about the archive, and requires the mandatory field **mod-Id** - UUID of the mod
2. **content.json** : mandatory, describes meta-information (title, description, authorship) as well as table mods (more details below)
3. **icon.png** : an optional square png icon that is displayed during installation and in the mods list.
4. Various resources that should be available to the game (for example: **sc3d/colette_rabbit.scw** )

## The most important: content.json 
Almost always a mod involves changing values in tables in one way or another. A fairly simple way could be to edit **.csv** files and pack them inside the mod - but this solution has a significant number of drawbacks and potential compatibility issues. After all, it's unknown what to do if multiple mods want to modify a single table.

That's why the modloader **does not accept** table files directly, but requires a description of the changes in the **content.json** file. In fact, all these changes will be applied when the game is launched, taking into account all installed mods as well as the server-side patch.

Now, now let's take a look at the structure of the file itself:
```json
{
	"@title": "Mod's title",
	"@description": "Mod's description",
	"@author": "Mod's author",
	"{table}": {
		"{line}": {
			"{column}": "{value}"
		}
	}
}
```
This may look a bit intimidating, but let's get into it.

The first three lines contain meta-information: they do not affect the game files. They are necessary to display information about the mod to the user: "@title" and "@description" contain the title and description of the mod, and "@author" - the name of the developer. These fields also support HTML tags and URLs.

Next comes the description of the changes. It is best to show it by example:
1. You decided to edit the **alliance_roles.csv** file - then "{table}" will be = "alliance_roles" (without the .csv extension).
2. In this file, you found a line with called **Elder** - then "{line}" will = "Elder"
3. You want to change the value in the **CanSendMail** column - then "{column}" will = "CanSendMail"
4. You want the new value to be **true** - then "{value}" will = true

So, we have got the following:
```json
{
	"alliance_roles": {
		"Elder": {
			"CanSendMail": true
		}
	}
}
```
Don't forget about covering string values in quotation marks! But in numeric values or flags (true / false) they are unnecessary.

Let's take a look at a more complex mod:
```json
{
	"@title": "Test mod",
	"@description": "This mod fills the mega pig and allows to visually...",
	"@author": "NB modding legend",
	"club_piggy_levels": {
		"PiggyLevel_0_0": {
			"State": 6,
			"ShownLevelInCounter": 5
		}
	},
	"alliance_roles": {
		"Elder": {
			"CanSendMail": true,
			"CanChangeAllianceSettings": true,
			"CanBePromotedToLeader": true,
			"PromoteSkill": 2
		},
		"Member": {
			"CanInvite": true,
			"CanSendMail": true,
			"CanChangeAllianceSettings": true,
			"CanAcceptJoinRequest": true,
			"CanKick": true,
			"CanBePromotedToLeader": true,
			"PromoteSkill": 2
		}
	}
}
```
As you can see, a few rows in several tables have already been changed here. I hope the general idea of the format is now clear!

The format also supports adding new rows to tables. In that case, just describe the new row with a new name! You can't delete rows, unfortunately.

To write mods in the JSON format, I recommend using a special code editor that supports this format (for example, Notepad++). To validate the syntax you can use the following website: https://jsonlint.com.

Moreover, the format also supports lists as values. There is more information about it in this message in the chat room: https://t.me/nb_mods/1/

## UUID, huh? 
Yes, a mandatory field is required in the **MANIFEST.MF** file: **mod-Id** , containing a unique identifier in UUID format: https://en.wikipedia.org/wiki/UUID#Format.

Why is it needed? For now only for one purpose: if a user already had a mod with the same UUID when installing another mod, the older one will be deleted. This simplifies the process of updating mods for users.

As an example you can generate a UUID here: https://www.uuidgenerator.net.

## Making your own mod 
It is highly recommended to familiarize yourself with the rules first.

So you have a content.json file, maybe some additional resources (textures or music). Now how do you package it all up?

Each mod must be signed. You can do this in two ways:

### Automatic signature
In case your mod consists of just a json file, without textures and sounds, you can use our Telegram bot.

To do this, send the /sign@nulls_brawl_bot command to the \#Signing Requests Lite channel, attaching your file beforehand. In a few seconds you will receive a complete and signed mod!

If you don't want to write messages in a public topic, you can also use the command from the bot in private messages: @nulls_brawl_bot.

In addition to the lack of support for additional resources, there are some other limitations:
1. A file signed in this way will be valid only for three days (after that it will be impossible to install it)
2. The "@author" field will be assigned automatically (and will always contain your username and Telegram ID)
3. UUID will be generated automatically (it will be unique and constant for the "@author" + "@title" field combination)
4. You cannot change the mod icon

This method is not recommended if you want to distribute your mod in the future.

### Manual signature
This method will work for you if you are ready to distribute your mod to the community, or if you are not satisfied with the limitations of automatic signature.

To do this, send your mod to the \#Signing Requests Pro channel in a ZIP archive. This archive should contain the **content.json** file as well as all necessary game resources.

The archive can also contain **icon.png** file according to the requirements.

In the message you can specify various comments and preferences. It is also desirable to specify UUID - it must be new and unique for new mods, or must match the UUID of the previous version for new versions of existing mods. It is not allowed to release updates on other people's mods (without the author's consent).

Unfortunately, manual signing can take a long time - up to several days. Moreover, we may not sign your mod if it contains errors or questionable content.

## Server-side mods
At this time, mods are neither loaded nor supported on the server side. Any server-side behavior will remain the same as it was without them.

You should not change values that are used by both client and server. This can cause the game to mishandle server behavior. In the worst case scenario, it can cause the game to crash.

# IV. Additional info

## More about modloader operation
When installing a mod, the loader extracts its files to the following path: /data/data/{package name}/mods/{uuid}.

Each time the game runs, it loads all the unpacked mods, merges all the changes in the tables, and updates the values in them as needed.

When the game accesses any file, the loader checks if this file is not in the installed mods. If it is, it redirects the call to the file from the mod. This does not apply to **.csv** files – they will be ignored by the loader (as there is a separate mechanism for tables).

If several mods contain a file with the same name, the behavior of the loader is undefined, redirection can happen to any of them. Therefore, if possible, it is recommended to name files so that they do not conflict with other mods.

## Icon requirements (icon.png)
PNG format only, square-shaped, no larger than 640x640. It can be any suitable image, as long as it is NSFW-free.

## Alternative format for mods (toml)
Perhaps in the future there will be support for mod descriptions not only in json format (**content.json**), but also in TOML. The concept is exactly the same, just with a more simplistic syntax:
```toml
[club_piggy_levels.PiggyLevel_0_0]
State = 6
ShownLevelInCounter = 5

[alliance_roles.Elder]
CanSendMail = true
CanChangeAllianceSettings = true
CanBePromotedToLeader = true
PromoteSkill = 2

[alliance_roles.Member]
CanInvite = true
CanSendMail = true
CanChangeAllianceSettings = true
CanAcceptJoinRequest = true
CanKick = true
CanBePromotedToLeader = true
PromoteSkill = 2
```
