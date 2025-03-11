[Версия на русском 🇷🇺](/TUTORIAL.md)

> [!WARNING]  
> THIS ENTIRE TUTORIAL WAS MACHINE TRANSLATED FROM A VERY JARGON RUSSIAN. EXPECT A LOT OF MISTAKES. I'LL IMPROVE THIS SOON WHEN I GET MORE TIME. FOR NOW I ONLY FIXED VITAL MARKUP ERRORS.
> DEEPL DID THE BEST IT COULD.

# json tutorial for zero bravl mods
@DenysDt & @sakupen_ppppp - November 12, 2024 - [Original source](https://telegra.ph/Tutor-po-dzhsonu-dlya-modov-nulya-bravla-11-12)

-----
So, this is probably a detailed tutorial on how to learn how to write mods on json (only on it so far).

Let's get started.

If you see this telegraph, then you have obviously seen the topic: "Signing request", there you will throw your "mods" to sign in the future, but now not about that....

In this thread you may have seen files with the .json extension and clicking on it, wanted to see what was there and saw this:

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj1.webp" width="400em" />  
*Crow Thanksgiving.*

Or something like that, so that's exactly how mods are written for zero. 

Here DenysDt and I will try to explain how to write it all and what is better to resort to first.

In order to start with something at all, then personally from myself (Vadi) I advise you to dig into the assemblies of zero to understand how the .csv files are organized, and to start doing something to understand how everything is organized.

  

Now let's get down to the json itself and take apart one screenshot:

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj2.webp" width="100%" />  
*Done code.*

For convenience, we will write each step step step by step to understand how to write the code correctly

  

Let's look at the first line and see that it starts with "{" You should always write this bracket as soon as you start writing json for the mod.
```json
{
```
Press "Enter", and the next thing we see is "ru".

This is the name of our csv file. Exactly .csv do not need to write, just enough of what is written before it, and it must be written in quotes.
```json
{
    "ru"
```
After the quotation marks, we write: ": {" and press "Enter". If you are writing from some code editor, selecting JSON syntax will automatically indent the space for the next line.
```json
{
    "ru": {
```
Next we see: "TID_TITLE_MASTERY_GRAY", this is the very first column in the csv file: 

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj3.webp" width="100%" />  
*On the very left under TID.*

They are different in each csv, in the screenshot below it's "PiggyLevel0", in the screenshot even lower it's "TitleMasteryJessie" and everything below it.

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj4.webp" width="100%" />  
*csv file which is responsible for how full the mega piggy bank is.*

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj5.webp" width="100%" />  
*csv file which is responsible for titles*

Everything is closed in quotes and written ": {" and then press "Enter".
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
```
The next line in our json file is:
```json.
    "RU": "I love Gray"
```
"RU" is already a column, as with the string, each csv file has its own columns, for example color_gradients has these: "Colors", "Speed", "Scale". "Name" is also a column, but it is highly undesirable to change it

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj6.webp" width="100%" />  
*What's underlined in red are the columns.*

And it is under those columns, on the line you want, that you write what you need in jsone, I'll show you again:  
"RU": "I love Gray."
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
```
Then press "Enter" and put 3 brackets like this: "}" (each on a line closer to the beginning of the code).

The first one closes the line, the second one closes the bracket after the file name and the third one closes the very first bracket (IMPORTANT, the last closing bracket also means the end of the code, it is strictly forbidden to write after it).
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        }
    }
}
```
What if I want to change another line, do I have to write it all over again?

If you want to add a new line (e.g. change Lily's title to "I love Lily"), all you have to do is do the same thing, but starting from the step where we explained how to define a line.

If it is not clear, here is an example to illustrate:
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
```
**VERY IMPORTANT,** if you want to continue writing code, don't forget to put a comma after the last closed brackets when opening new brackets.

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj7.webp" width="100%" />  
*Blue is the comma that should be there when opening new brackets*.

The next step is much simpler, you repeat the same thing you did with Gray (specify the column and write what you want to replace).
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
    },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
```
And then close the 3 open brackets (IMPORTANT! The bracket that is responsible for Gray is already closed!!!! So you need to close exactly 3 brackets!!!).

You close the bracket that changed the text to lily, then the bracket that stood next to "ru", and at the end the bracket that shows the end of the code.
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
        }
    }
}
```
What if you need to change a line in another file?

You can do that too! In fact it will work almost the same way as when we changed Lily's title, the difference is that you will open the new brackets not after the brackets where we changed the text to Gray, but after the brackets that close "ru".

Here is an example of how it should look like:
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
        }
    },
"your file name"
```
DON'T FORGET THE COMMA AFTER THE BRACKET!!!

Let's change "alliance_roles.csv" for example, so that the member can visually send letters to the club!

First we specify the name of the file and open the brackets as usual.
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
        }
    },
    "alliance_roles": {
```
Now we need to see which row and column we are going to change, in our case it will be the "Member" row and the "CanSendMail" column.

<img src="https://github.com/v1s7/csv-monsters/raw/refs/heads/media/tj8.webp" width="100%" />  
*This is what the entire alliance_roles.csv csv file looks like.*

It can be noticed that by default (or so the developers put it) a member can NOT send letters to the club, because of which the cell says "false". On the other hand, the club president can do it, that's why he has "true" in the cell.

Our task is to give the member an opportunity to see (albeit visually) the button for creating a club letter.

To do this we will change the value in the "Member" row and "CanSendMail" column to "true", it will look like this:
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
        }
    },
    "alliance_roles": {
        "member": {
            "CanSendMail": "true"
```
And at the end we close all our previously opened brackets as usual.
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": "I love Lily"
        }
    },
    "alliance_roles": {
        "member": {
            "CanSendMail": "true"
        }
    }
}
```
This way we get a small and quite cool mod!

  

If you have easily gone through all the points of this tutorial, there are some more interesting things that can make it easier for you to write code.

If you want to have absolutely nothing in the cell, you should write null WITHOUT QUOTES instead of text, it will look like this:
```json
{
    "ru": {
        "TID_TITLE_MASTERY_GRAY": {
            "RU": "I love Gray"
        },
        "TID_TITLE_MASTERY_LILY": {
            "RU": null
        }
    }
}
```
This is where we changed the lily title to . nothing.

**WARNING, it's not advisable to do this with text, but you might need it someday.**

  

One more cool little hack is the ability to change all values in one column to whatever you write, to do this you will have to do something like this:
```json
{
    "ru": {
        "*": {
             "RU": "I love nulls"
        }
    }
}
```
Instead of a string you should specify "\*", this means that every string should be affected, so absolutely everything in the "RU" column (which is basically all the text) will be replaced with "I love nulls".

  

  

This is approximately the whole tutorial! I hope you can find yourself as a mod creator and have a lot of cool ideas!

  

*from @DenysDt and @sakupen_ppppp, thanks for watching!*