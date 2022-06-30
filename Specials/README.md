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
special(%time%, ui, out); // Hide Game UI. (Fade-Out Duration: 0.5s)
special(%time%, ui, in); // Show Game UI. (Fade-In Duration: 0.5s)
```

**REMEMBER: Every** `out` **statement should have the corresponding** `in` **statement, or may occurr something which is unexpected;
For this type of effects, you must put the `out` statement before the first `in` statement, or may occurr something which is also unexpected.**
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

---

Last Update: Thursday, June 17th, 2022
Corresponding Arcade-Chan Version: 1.5.1 LTS (Updated on 6.17.2022)
