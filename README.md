# FakeVirusesForFriends
👻 FakeVirusesForFriends 👾 | Harmless PC Pranks • Custom Fake Error Spams • Matrix Rain • Fake Loading Screens • 100% Safe VBS/Batch Scripts for fun with friends!


# Customization Guide for Ultimate Prank Builder

This guide explains how to edit and customize the `prank_builder.bat` file to create your own personalized jokes. You can open the `.bat` file with any text editor (like Notepad) to make these changes.

---

## 1. Changing the Colors
Windows Command Prompt uses color codes. You can find the color command in the script (e.g., `color 0A`). 
* The **first character** changes the background color.
* The **second character** changes the text color.

### Common Color Codes:
* `0` = Black
* `2` = Green
* `4` = Red
* `7` = White
* `A` = Light Green
* `C` = Light Red

**Example:** To make the screen look like a red warning system (Black background, Red text), change `color 0A` to:
```cmd
color 0C
```

---

## 2. Customizing the Pop-up Message Boxes
The popup windows are generated using VBScript. The line in the script looks like this:
```cmd
echo msgbox "Your Message Here", 64, "Window Title" > "%temp%\filename.vbs"
```

### What you can modify:
1. **The Text:** Change `"A completely harmless prank error has occurred!"` to whatever you want.
2. **The Window Title:** Change `"Prank Alert"` to something like `"Windows Defender"` or `"System Error"`.
3. **The Icon (The Number):**
   * `16` = Critical Error Icon (Red "X")
   * `32` = Help/Question Icon (Blue "?")
   * `48` = Warning Icon (Yellow "!")
   * `64` = Information Icon (Blue "i")

**Example for a scary-looking error:**
```cmd
echo msgbox "Critical threat detected! Please restart.", 16, "System Critical Error" > "%temp%\harmless.vbs"
```

---

## 3. Adjusting the Amount of Window Spam
In the `:errorspam` section, the script uses a loop to open multiple windows at the same time:
```cmd
for /L %%i in (1,1,10) do (
```
The number **`10`** at the end defines how many windows will pop up simultaneously. 

* If you want a mild joke, keep it at `5` or `10`.
* If you want a massive window flood, you can increase it to `30` or `40`. 
*(Note: Do not set it too high, or the computer will lag while closing them!)*

---

## 4. Editing the Fake Progress Bar Text
In the `:fakeprogress` section, you can change the text to simulate different scenarios. 
Look for the `echo` lines:
```cmd
echo Initializing database purge simulation...
```
You can change this to something like:
```cmd
echo Downloading more RAM...
echo Deleting System32 folder...
```
*Tip: The `timeout /t 1 >nul` command creates a 1-second delay between the lines. You can increase the number to make the waiting time longer.*

