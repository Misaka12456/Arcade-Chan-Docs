# Arcade-Chan Special System Developing Document

Arcade-Chan adds a new special effects system 「Special」 on 1.2.0 Update.  
You can use special system do whatever you want!  
Tip: All special statement are only take effects in the `FullPlay Mode` (which is started by clicking the Right-Buttom `Play!` button in the editor scene), and **will clear all special effects** when quitting `FullPlay Mode` (by manually stopping or by automatically switching to the result screen after finishing playing the song).  
Caution: We will use placeholder `%varName%` to replace the corresponding value that should be filled in by yourself.

#### 1. Show/Hide Texts

Updated on: 1.2.0 (5.17.2022)

This statement can dynamically show/hide tutorial text on the top-center of the window.

Usage:

```cs
special(%time%, text, in, %textId%); // Show a tutorial text by the given time and the text id. (Fade-In Duration: 0.3s)
special(%time%, text, out); // Hide a tutorial text which was shown before by the given time. (Fade-Out Duration: 0.3s)
```

> Wait, I know what is %time% - the execute time of the statement, but **what is %textId% (text id)?**

Due to the consideration to the principle that *insert less Arcade-Chan exclusived statements into the raw aff file*, we moved the real text data to a JSON file called `spStrTable.json`(in the root folder of the Arcade Project (which contains several raw aff files, audio file and so on)), whose contents are like the format below:

```json
{
	"first": "Hello world!", // Define a text id-data pair
	"second": "Welcome to Arcade-Chan\nSpecial System!" // Use \n to switch to the new line
}
```

The format of all key-value pair in the spStrTable.json should be like this:

```json
"text id": "text data"
```

**Now you can use id starts with alphabets and contains numbers**, but you can use all displayable Unicode Characters in the data. (Use `\n` to switch to the new line)  
Then, you should only use the id of the text in the final aff file, like this:

```cs
special(0,text,in,first); // Show "Hello world!"
special(1495,text,out); // Hide "Hello world!"
special(6174,text,in,second); // Show "Welcome to Arcade-Chan<New Line>Special System!"
special(15626,text,out); // Hide "Welcome to Arcade-Chan<New Line>Special System!"
```

**REMEMBER: Every `out` statement should have the corresponding `in` statement, or may occurr something which is unexpected.**

#### 2. Show/Hide UI (Pause Button & Score+Progress+Song Info Bar)

Updated on: 1.2.0 (5.17.2022)

This statement can dynamically show/hide the game UI, which includes Left-Top Pause Button and Right-Top Song Info Bar.  
Tip: Hide the UI will **not remove** the Left-Top Pause Button, actually, it just **changes the alpha of the button to `0`**. (So you can pause playing like usual by clicking the Left-Top space which was the location of the Pause Button before.)  

Usage:

```cs
special(%time%, ui, out, <type>, <duration>); // Hide Game UI.
special(%time%, ui, in, <type>, <duration>); // Show Game UI.
```

``type``: The type of the UI Component, could be one of the following values:

- `0`: Pause Button

* `1`: All Components
* `2`: All Components except Difficulty Indicator (for hide)
  Difficulty Indicator Only (for show)

``duration``: The duration of the fade-in/out animation, in seconds. (Default: 0.3s)

**For this type of effects, you must put the `out` statement before the first `in` statement, or may occurr something which is unexpected.**  
(This is because the default state of the UI is shown.)

#### **3. Show/Hide Blacken Overlay**

Updated on: 1.2.0 (5.17.2022)

This statement can show/hide a pure-black overlay on the whole window, which is usually used in chart special performances.

Usage:

```cs
special(%time%, overlay, in); // Show the pure-black overlay. (Fade-In Duration: 0.1s)
special(%time%, overlay, out); // Hide the pure-black overlay which was shown before. (Fade-Out Duration: 0.5s)
```

You are able to use only one `in` statement. The overlay will **automatically hide** when returning from the result scene to the editor scene.

#### **4. Show/Hide Images**

Updated on 2.0.0 (7.12.2022)

This statement can show/hide images on the whole window, which is usually used in chart special performances.

Images will be scaled in 1280x720 resolution (all positions are based on this resolution).

Usage:

```cs
special(%time%, image, in, <imgId>, <startX>, <startY>);
special(%time%, image, in, <imgId>, <startX>, <startY>, <width>, <height>);
special(%time%, image, in, <imgId>, <startX>, <startY>, <width>, <height>, <isInstantly>);
special(%time%, image, in, <imgId>, <startX>, <startY>, <width>, <height>, <isInstantly>, <duration>);

special(%time%, image, out, <imgId>);
special(%time%, image, out, <imgId>, <duration>);
```

``imgId``(string): The id of the image, which is the name of the image file in the `Arcade/Special/Images` folder of the Arcade Project. (Supported jpg/png/bmp)

``startX``(int): The x left-top position of the image, in pixels.

``startY``(int): The y left-top position of the image, in pixels.

``width``(int): The width of the image, in pixels. (Default: Image Real Width)

``height``(int): The height of the image, in pixels. (Default: Image Real Height)

``isInstantly``(int **(not bool)**): Whether the image should be shown instantly. (Default: 0(false))

``duration``(float): The duration of the fade-in/out animation, in seconds. (Default: 0.5s)

Examples:

- Show a picture file ({Project Base Folder}/Arcade/Special/Images/blackBorder.png) in left-top position (0, 0) and the full size (raw size: 1920x1080) by 3.25s:

```cs
special(%time%, image, in, blackBorder, 0, 0, 1920, 1080, 0, 3.25);
```

- Show a picture file ({Project Base Folder}/Arcade/Special/Images/arrow.png) in left-top position (500, 350) and the scaled size (scaled to 150x150) by 2.15s:

```cs
special(%time%, image, in, arrow, 500, 350, 150, 150, 0, 2.15);
```

- Show a picture file ({Project Base Folder}/Arcade/Special/Images/caution.png) in left-top position (0, 0) and the full size (raw size: 3840x2160) instantly
  and hide it after 1.5s, by 0.75s:

```cs
special(%time%, image, in, caution, 0, 0, 3840, 2160, 1);
special(%time%+1500, image, out, caution, 0.75);
```

#### **5. Edit UI**

Updated on 2.1.0 (12.25.2022)

This statement can edit the value of the UI component in the game dynamically.

Usage:

```cs
special(%time%, uiedit, <type>, <value>);
```

``type``(int): The type of the UI component, could be one of the following values:

- `0`: Difficulty Class ("Past"/"Present"/"Future"/"Beyond")

* `1`: Difficulty Rating ("rating10"(means "10")/"rating9plus"(means "9+"))
* `2`: Full Difficulty String ("Beyond_rating12"(means "Beyond 12")/"Future_rating9plus"(means "Future 9+"))

``value``(string): The value of the UI component.

Caution:

- Noted that ``value`` is string type, so if there is only rating number in the value, you should add ``rating`` prefix, such as: ``rating10``(will be displayed as "10").
- Noted that ``value`` cannot have special symbols, such as ``+``(except ``_``, see below). If you want to show plus rating, you should add ``plus`` suffix, such as: ``rating9plus``(will be displayed as "9+").
- Noted that there cannot be space character in the ``value``, so use ``_`` to replace the space, such as: ``Beyond_rating12``(will be displayed as "Beyond 12").

  - ``_`` is a value seperator, so every part of the value which seperated by ``_`` should also follow the rules above.

Examples:

- Change rating to 10+, leave difficulty alone to Future

```cs
special(%time%, uiedit, 1, rating10plus);
```

- Change difficulty to Beyond, leave rating alone to 10

```cs
special(%time%, uiedit, 0, Beyond);
```

- Change difficulty from "Beyond 10" (Original) to "Beyond 12"

```cs
special(%time%, uiedit, 2, Beyond_rating12);
```

- Change difficulty from "Beyond 10" (Original) to "Survive 4+" ([Preview Video Link](https://www.bilibili.com/video/BV1h8411H7zg))

```cs
special(%time%, uiedit, 2, Survive_rating4plus);
```

- Change rating to 'R', leave difficulty alone to Beyond

```cs
special(%time%, uiedit, 1, R); // This is not start with a number, so we don't need to add 'rating' prefix.
```

---

Last Update: Sunday, December 25, 2022  
Corresponding Arcade-Chan Version: 2.1.0 LTS (Updated on 12.25.2022)
