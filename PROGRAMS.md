<sup>написал v1s7, особые благодарности [Daniil-SV](https://github.com/Daniil-SV) и сообществу [SC Workshop](https://discord.gg/spFcna3xFJ)</sup>
<!--
Techicons by gui-bus
Linux <img src="/static/icons/Dark/Linux.svg" height="16rem"> --
Android <img src="/static/icons/Dark/Android.svg" alt="Android" height="16rem"> --
Windows <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem"> https://icons8.com/icon/108792/windows-10
Animate <img src="/static/icons/Dark/Animate.svg" alt="Adobe Animate" height="16rem"> https://icons8.com/icons/set/adobe-animate--animated
MacOS <img src="/static/icons/Dark/Apple.svg" height="16rem"> https://icons8.com/icons/set/macos
Bash <img src="/static/icons/Dark/Bash.svg" height="16rem"> https://icons8.com/icon/9MJf0ngDwS8z/bash
Python <img src="/static/icons/Dark/Python.svg" height="16rem"> https://icons8.com/icon/13441/python
Java <img src="/static/icons/Dark/Java.svg" height="16rem"> https://icons8.com/icon/13679/java
C++ <img src="/static/icons/Dark/C++.svg" height="16rem"> https://icons8.com/icon/40669/c%2B%2B
Discord <img src="/static/icons/Dark/Discord.svg" height="16rem"> https://icons8.com/icon/M725CLW4L7wE/discord-new
Telegram <img src="/static/icons/Dark/Telegram.svg" height="16rem"> https://icons8.com/icon/25n4hOEoY7ss/telegram-app
-->

[Switch to English 🇬🇧](/PROGRAMS-en.md)  

> [!TIP]  
> Список программ можно открыть, нажав на кнопку ⋮☰ в правом верхнем углу.  

**Здесь описаны все конвертеры, боты, скрипты, чаты и прочие полезные ресурсы для моддинга. Заметка была создана для удобного единого обновления описаний и ссылок.**

-----
# 📱Сообщества и боты

### [EscavunBot](https://t.me/escavun_chat) <img src="/static/icons/Dark/Telegram.svg" height="16rem"> 
Бот в Телеграме с гибкими возможностями загрузки игровых файлов:
- поддержка поиска по RegEx,
- смена игры и её версии из которой требуется загрузить ассеты,
- загрузка сразу нескольких файлов (не ограничен 10 МБ как Дискорд),
- автоматически разжимает CSV-файлы,
- и многое другое.

### [Null's Brawl Mods Bot](https://t.me/nb_mods/4827) <img src="/static/icons/Dark/Telegram.svg" height="16rem"> 
Название говорит само за себя. Используется для временной подписи в NullsBrawlAssets файлов JSON (и только их), а именно на 3 дня. Находится в официальном чате мододелов Null's Brawl, в котором:
- создаются заявки на долгосрочную подпись мода (90 дней),
- выкладывается новейшая информация об обновлениях механизма модов и игры,
- запрашиваются публикации модов в библиотеку модов из управления модами.

> [!note]  
> Чтобы начать использовать бота необходимо присоединиться к чату мододелов и находиться в нём как минимум 10 минут. Это все условия.

Также боту можно отправлять файлы на подпись в личные сообщения, но между успешными запросами на подпись будет задержка в 120 секунд до следующей возможности запроса. Впрочем, это всё равно лучше 5-минутной задержки чата мододелов.  

### [ScwBot](https://discord.gg/dbD8erDDmF) <img src="/static/icons/Dark/Discord.svg" height="16rem"> 
Бот в Дискорде, в котором собраны почти все конвертеры форматов для моддинга, есть моментальный поиск/скачивание игровых файлов и множество прочих интересных функций по типу `img2map`. 
Этот бот – спасение для людей с телефона, так как почти для всех конвертеров требуется компьютер. Но не всё так радужно: благодаря Дискорду все отправляемые файлы ограничены 10 МБ, а также он не постоянно онлайн.  
Сам сервер также полезен обилием туториалов на использование конвертеров – советую взглянуть.

### [SC Workshop](https://discord.gg/spFcna3xFJ) <img src="/static/icons/Dark/Discord.svg" height="16rem"> 
Сообщество, благодаря которому моддинг ресурсов игры сейчас не является кошмаром или вовсе выдумкой.

<!--# 🌐 Сайты-конвертеры
## GLB ←→ DAE ←→ FBX ←→ BLEND ←→ OBJ ←→ (...)
скоро
## KTX ←→ PNG
скоро
## OGG ←→ MP3 ←→ (...) ← MP4
скоро-->
# 🧱 Базовые
## 📁 Проводники
Достаточно выбрать один.
### На Android
Все из них поддерживают подключение внешних хранилищ – в нашем случае, хранилища игры.
#### MiXplorer
[Сайт](https://mixplorer.com) | [4PDA](https://4pda.to/forum/index.php?showtopic=318294) | Google Play – [платно💲](https://play.google.com/store/apps/details?id=com.mixplorer.silver)  
Самый кастомизируемый и с богатым функционалом. Есть доступ к Android/data при наличии Shizuku (включается в настройках).
#### Material Files
[GitHub](https://github.com/zhanghai/MaterialFiles) | [4PDA](https://4pda.to/forum/index.php?showtopic=957950) | [Google Play](https://play.google.com/store/apps/details?id=me.zhanghai.android.files)  
Лучший среди доступных в Google Play бесплатных менеджеров с открытым кодом.
#### MT Manager
[Сайт](https://mt2.cn) | [4PDA](https://4pda.to/forum/index.php?showtopic=548542) | Google Play – никогда❌  
Самый напичканный функциями менеджер, некоторые из которых платные. Есть доступ к Android/data при наличии Shizuku (запрашивается при старте и в настройках).

### На iOS
> [!warning]  
> У автора нет устройства на iOS, требуется дополнение информации. Не стесняйтесь делиться ею постами в [Issues](https://github.com/v1s7/csv-monsters/issues)!
#### Filza File Manager
[Сайт](https://www.tigisoftware.com/default/?page_id=78) | [BigBoss Repo](http://cydia.saurik.com/package/com.tigisoftware.filza) | [TrollStore](https://www.tigisoftware.com/default/?p=439)  
Сказать нечего ¯\\\_(ツ)\_/¯
## 👨‍💻 Редакторы кода
На случай, если вы недовольны редактором от файлового менеджера или системным блокнотом – пользоваться именно ими **необязательно**, это всё вопрос удобства.
### На компьютере
Варианты должны подойти под любые ОС.
#### VS Code
[Сайт](https://code.visualstudio.com/download)  
Самый популярный IDE с массой плагинов и с кучей форков, по типу [VSCodium](https://vscodium.com) (вырезана телеметрия майкрософт), [Cursor](https://cursor.com) (прикручены нейросети) и прочих.
#### Kate  
[Сайт](https://kate-editor.org/get-it/)  
Менее требовательный к мощности компьютера редактор.

### На Android
Здесь функционал у всех скудноват, но для наших целей они подойдут
#### ACode
[Github](https://github.com/Acode-Foundation/Acode?tab=readme-ov-file#-installation) | [F-Droid](https://f-droid.org/repo/com.foxdebug.acode) | [Google Play](https://play.google.com/store/apps/details?id=com.foxdebug.acode)   
Буквально копия VS Code, но портом не является.

#### Xed Editor
[Github](https://github.com/Xed-Editor/Xed-Editor) | [Izzy](https://apt.izzysoft.de/fdroid/repo/com.rk.xededitor) | Google Play – нет❌  
Редактор со своим подходом к папкам и приятным интерфейсом. Можно выдать доступ к папке `mods` через DocumentsUI (только если вы [патчили apk игры через ApkTool M](/FAQ.md#2-патч-apk-от-nulls-brawl)) и иметь удобный способ редактировать все JSON-файлы установленных модов!

#### QuickEdit
[Сайт](https://rhmsoft.com/?p=283) | [4PDA](https://4pda.to/forum/index.php?showtopic=625901) | [Google Play](https://play.google.com/store/apps/details?id=com.rhmsoft.edit)  
Классика

### На iOS
> [!warning]  
> У автора нет устройства на iOS, требуется дополнение информации. Не стесняйтесь делиться ею постами в [Issues](https://github.com/v1s7/csv-monsters/issues)!
#### Runespace Text Editor
[Сайт](https://runestone.app) | [Github](https://github.com/simonbs/runestone) | [App Store](https://apps.apple.com/us/app/runestone-editor/id1548193893)  
Сказать нечего ¯\\\_(ツ)\_/¯

## 📑 Редакторы таблиц
CSV-таблицы могут открывать любые редакторы кода и текста, но они отображают её в сыром виде. Удобнее всего их открывать через редакторы электронных таблиц. Чуть ли не все из них опираются на максимальную кроссплатформенность, поэтому разделения по ОС здесь нет.

#### Google Sheets
[Сайт](https://workspace.google.com/products/sheets) | [App Store](https://apps.apple.com/us/app/google-sheets/id842849113) | [Google Play](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets)

#### Microsoft Excel
[Сайт](https://www.microsoft.com/en-us/microsoft-365/excel) | [App Store](https://apps.apple.com/us/app/microsoft-excel/id586683407) | [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.office.excel)

#### WPS Office
[Сайт](https://wps.com/download) | [App Store](https://apps.apple.com/us/app/wps-office-pdf-docs-sheets/id1491101673) | [Google Play](https://play.google.com/store/apps/details?id=cn.wps.moffice_eng)

# 🚪Конвертеры форматов Supercell
## ♻️ Специализированные 
### [Flat Converter](https://github.com/Daniil-SV/Supercell-Flat-Converter) <img src="/static/icons/Dark/Python.svg" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
Конвертирует в обе стороны обычный GLB с оптимизированным GLB во FlatBuffers.

### [SCTX Converter](https://github.com/Daniil-SV/SCTX-Converter) <img src="/static/icons/Dark/Python.svg" height="16rem"> |  <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">
Конвертирует в обе стороны SCTX и PNG.

### [SCW by Opegit Studio](https://github.com/OpegitStudio/SCW) <img src="/static/icons/Dark/Java.svg" height="16rem">  
Конвертирует в обе стороны SCW и DAE.

<!--### [XCoder by Lexa]()
нашёлся, скоро будет :)
-->

<!--### [010 Editor]()
пока не изучал что это
-->

<!--## 🫡 Устаревшее, но имело значение
### [SC Editor by ToxicLand]

### [XCoder от кого-то ещё]()

### вряд-ли это выйдет из комментариев

### так то устаревших программ немало, но 90% из них это XCoder
-->
## 🛠️ Универсальные
### [SC Editor](https://github.com/danila-schelkov/sc-editor) <img src="/static/icons/Dark/Java.svg" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem"> <img src="/static/icons/Dark/Apple.svg" height="16rem"> <img src="/static/icons/Dark/Linux.svg" height="16rem">  
Позволяет открывать и просматривать файлы SC (и v1, и v2) и SCTX. Есть возможность сохранять разные файлы игры в формате SC v1. Может использоваться для проверки работоспособности пользовательских изменений в SC-файлах. Также он может отрендерить объект в картинку или видео, что может быть полезно для контент-мейкеров.  
SC Editor собран модульно, а значит эти модули можно взять и использовать их в своих целях. Например, можно написать приложение, открывающее файлы SC2 и сохраняющее их в старом формате SC. У такой идеи как раз имеется [демо](https://github.com/danila-schelkov/sc-reassembler).  
> [!important]  
> Для его работы дополнительно потребуется скачать [KTX Tools](https://github.com/KhronosGroup/KTX-Software) и в установщике добавить его в PATH.

*Не путать с уже неактульным SC Editor by ToxicLand*
### [SimpleTexToolGUI](https://github.com/ARHCOS/SimpleTexToolGUI) <img src="/static/icons/Dark/Python.svg" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
Простой конвертер текстур из игр Supercell с графическим интерфейсом. Основан на PVRTexTool и SCTX Converter. Умеет конвертировать:
- KTX ←→ PNG
- PVR → PNG
- SCTX ←→ PNG

## 🖌️ Для работы в Adobe Animate
### [ScDowngrade](https://github.com/Daniil-SV/ScDowngrade) <img src="/static/icons/Dark/C++.svg" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
Понижает версию SC-файлов с v2 до v1 или v0.5. Используется ради совместимости с программой ниже.

### [SC2FLA](https://discord.com/channels/751042695698579457/751056303123857509/1288796520199487532) <img src="/static/icons/Dark/Python.svg" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
Конвертирует SC-файлы версий v0.5 и v1 в документ FLA – файл проекта Adobe Animate. 

### [SupercellSWF Animate](https://github.com/sc-workshop/SupercellSWF-Animate) <img src="/static/icons/Dark/Animate.svg" alt="Adobe Animate" height="16rem"> | <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
Плагин для Adobe Animate, позволяющий экспортировать проект в SC-файл. Должен работать на версиях выше Animate 2022, но рекомендуемая и самая стабильная из них – Animate 2023.

# 🥣 Прочие полезности
### FFmpeg <img src="/static/icons/Dark/Bash.svg" height="16rem"> | <img src="/static/icons/Dark/Android.svg" alt="Android" height="16rem"> <img src="/static/icons/Dark/Linux.svg" height="16rem"> <img src="/static/icons/Dark/Apple.svg" height="16rem"> <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">
Конвертер вообще любых медиафайлов с громадным набором параметров. Подвох в том, что утилиту можно полноценно использовать только в командной строке – пользовательского интерфейса нет.

Полезна она будет способностью массово конвертировать аудио и даже видео в предпочитаемый игрой формат OGG. На разных платформах это делается по-разному:
#### Termux <img src="/static/icons/Dark/Android.svg" alt="Android" height="16rem"> / Bash <img src="/static/icons/Dark/Linux.svg" height="16rem">  
```bash
shopt -s nullglob
mkdir Converted
for FILE in *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac;
    do ffmpeg -hide_banner -i "$FILE" -c:a libvorbis -vn -q:a 0 "Converted/`echo ${FILE%.*}.ogg`"
done
shopt -u nullglob
```
<details>  

<summary>Разъяснение</summary>  

- `shopt -s nullglob` нужен, чтобы при провальной попытке найти файлы, подходящие под, например, условие `*.avi`, система вернула пустой ответ. Без этой команды условие интерпретируется, как буквальное название файла, и FFmpeg будет делать лишние действия с несуществующими файлами, попутно заполняя терминал горой ошибок.
- `mkdir Converted` создаёт папку "Converted".
- `for FILE in *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac;    do` сначала задаёт переменную "FILE", которая включает в себя текст, соответствующий одному из популярных форматов аудио и видео, а потом выполняет следующую команду.
- ffmpeg -hide_banner -i "$FILE" -c:a libvorbis -vn -q:a 0 "Converted/\`echo ${FILE%.\*}.ogg\`" – сама команда для конвертации:
    - `-hide_banner` убирает мусорную информацию о параметрах команды.
    - `-i "$FILE"` задаёт исходный файл, в котором ищутся все файлы, соответствующие одному из условий из переменной "FILE".
    - `-c:a libvorbis` на всякий случай задаёт кодек конечного результата на нужный нам. Без этого OGG может восприниматься программой, как видео, и весь файл испортится.
    - `-vn` убирает видео с конечного результата – благодаря нему существуют всякие YouTube to MP3! Это включает в себя и обложки трека – приятный бонус для экономии места.
    - `-q:a 0` задаёт уровень так называемого качества трека на ноль. Другими словами это **переменный битрейт** где-то между 48 и 80 кбит/с – такой же используется в игре.
    - "Converted/\`echo ${FILE%.\*}.ogg\`" – название конечного результата и путь его сохранения:
        - `Converted/` – внутри созданной ранее папки.
        - \`echo ${FILE%.}.ogg\` – копирует названия исходных файлов, исключая весь текст после последней точки (то есть расширение файла), и приписывает новое – OGG.
- `done` завершает цикл for…in.
- `shopt -u nullglob` снимает действие самой первой команды.
</details>

#### PowerShell <img src="/static/icons/Dark/Windows.svg" alt="Windows" height="16rem">  
> [!warning]  
> На работоспособность не проверялось – похожий скрипт можно найти на просторах интернета.

```powershell
Get-ChildItem *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac { 
    ffmpeg -hide_banner -i $_.FullName -vn -c:a libvorbis -q:a 0 ("Converted" + "\" + $_.Name + ".ogg") 
}
```
<details>  

<summary>Разъяснение</summary>  

- В отличии от предыдущего способа, в PowerShell не нужно задавать подобие `shopt -s nullglob`, так как у него такое поведение уже стоит по умолчанию.
- `Get-ChildItem *.mp3 *.mp4 *.webm *.aac *.m4a *.avi *.ogg *.opus *.oga *.wav *.flac {…}` ищет соответствующие одному из популярных форматов аудио и видео в текущей директории, а потом выполняет команду внутри фигурных скобок.
- `ffmpeg -hide_banner -i $_.FullName -vn -c:a libvorbis -q:a 0 ("Converted" + "\" +$_.Name)`– сама команда для конвертации:
    - `-hide_banner` убирает мусорную информацию о параметрах команды.
    - `-i $_.FullName` задаёт исходный файл, в котором содержатся все файлы, предоставленные `Get-ChildItem` с учётом расширения.
    - `-c:a libvorbis` на всякий случай задаёт кодек конечного результата на нужный нам. Без этого OGG может восприниматься программой, как видео, и весь файл испортится.
    - `-vn` убирает видео с конечного результата – благодаря нему существуют всякие YouTube to MP3! Это включает в себя и обложки трека – приятный бонус для экономии места.
    - `-q:a 0` задаёт уровень так называемого качества трека на ноль. Другими словами это **переменный битрейт** где-то между 48 и 80 кбит/с – такой же используется в игре.
    - `("Converted" + "\" + $_.Name + ".ogg")` – скопированное название (без расширения) конечного результата "\$\_.Name", новое расширение файлов ".ogg" и путь его сохранения – папка "Converted":
        - Примечание: в отличии от любых других операционных систем, где директории разделяются обычным слешом «/», в Windows они разделяются обратным слешом «\\», который одновременно является **делимитером** – спец. символом, предотвращяющим свойства следующего спец. символа. Внутри кавычек любые спец. символы теряют свои свойства, но у этого поавила есть свои подводные камни. Поэтому обратный слеш вынесли в отдельный блок кавычек, дабы предотвратить возможные ошибки.
</details>