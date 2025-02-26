RuneLite automatically enables hardware acceleration for Java 2D rendering. This can cause artifacting of the side panel, particularly on Windows, and can be fixed by doing one of the following:


# Windows

## Update the launcher

Launcher version 2.4.0+ blocks common applications which cause the artifacting issue, updating to it by redownloading RuneLite from https://runelite.net may fix the problem. If you still experience the issue after installing a launcher newer than 2.4.0, tell us in `#support` on https://runelite.net/discord and we will look into it further.

## Removing external programs that interfere with RuneLite

Many GPU overlay programs cause this problem, usually removing them is the best option. The below programs are known to cause this problem:

* rivatuner
* sonic suite
* cFosSpeed
* alienware command center
* LogiOverlay
* NZXT CAM (must be closed and computer restarted)
* Wallpaper engine
* NVIDIA GeForce Experience
* Nahimic
* Sonic Studio
* MSI Afterburner
* Sonic radar 3
* GPU TWEAK III - ASUS

## Disabling hardware acceleration

### Method 1: Creating a shortcut

You can create desktop shortcut with ` --mode=OFF` at the end of the target box. make sure there is a space before the `--`! (Video below)

[![Client View](https://thumbs.gfycat.com/DamagedWealthyKoalabear-size_restricted.gif)](https://gfycat.com/DamagedWealthyKoalabear)

### Method 2: Starting the launcher with HW accel disabled from CMD
(requires launcher version 2.4+)

Run cmd.exe (Windows Key + R) and paste this into the command prompt:
```
"%localappdata%\RuneLite\RuneLite.exe" --mode=OFF
```


You can create a batch file to run this automatically when executed.  Copy the text below, paste it into notepad, and save as a .bat file.  
```
start "" "%localappdata%\RuneLite\RuneLite.exe" --mode=OFF
exit
``` 

Be sure to change "Save as type" to "All Files"

![](https://i.imgur.com/SeTB5Tl.png)



# All platforms

If you downloaded the `.jar` version of the launcher, run this:

```
java -jar Location-of-RuneLite.jar --mode=OFF
```
