# Escaping from KIOSKs

## Check for possible actions inside the GUI application

* Close/Close as
* Open/Open with
* Print
* Export/Import
* Search
* Scan

You should check if you can:

* Modify or create new files
* Create symbolic links
* Get access to restricted areas
* Execute other apps

Maybe using a _Open with_ option you can open a _cmd.exe, command.com, Powershell/Powershell ISE, mmc.exe_

If you can execute something with commands you can execute binaries like _rundll32.exe, at.exe, schtasks.exe, regedit.exe, qwinsta.exe, systeminfo.exe, msinfo32.exe, msconfig.exe, wmic.exe, eventvwr.exe_

## Bypassing path restrictions

* **Environment variables**: There are a lot of environment variables that are pointing to some path
* **UNC paths**: Paths to connect to shared folders. You should try to connect to the C$ of the local machine \("\\127.0.0.1\c$\Windows\System32"\)
* **Other protocols**: _about:, data:, ftp:, file:, mailto:, news:, res:, telnet:, view-source:_
* **Symbolic links**
* **Shortcuts**: CTRL+N \(open new session\), CTRL+R \(Execute Commands\), CTRL+SHIFT+ESC \(Task Manager\),  Windows+E \(open explorer\), CTRL-B, CTRL-I \(Favourites\), CTRL-H \(History\), CTRL-L, CTRL-O \(File/Open Dialog\), CTRL-P \(Print Dialog\), CTRL-S \(Save As\)
  * Hidden Administrative menu: CTRL-ALT-F8, CTRL-ESC-F9
* **Shell URIs**: _shell:Administrative Tools, shell:DocumentsLibrary, shell:Librariesshell:UserProfiles, shell:Personal, shell:SearchHomeFolder, shell:Systemshell:NetworkPlacesFolder, shell:SendTo, shell:UsersProfiles, shell:Common Administrative Tools, shell:MyComputerFolder, shell:InternetFolder_

## Download Binaries

Console: [https://sourceforge.net/projects/console/](https://sourceforge.net/projects/console/)  
Explorer: [https://sourceforge.net/projects/explorerplus/files/Explorer%2B%2B/](https://sourceforge.net/projects/explorerplus/files/Explorer%2B%2B/)  
Registry editor: [https://sourceforge.net/projects/uberregedit/](https://sourceforge.net/projects/uberregedit/)

## Accessing filesytem from the browser

### Windows

| File:/C:/windows | File:/C:/windows/ | File:/C:/windows\ | File:/C:\windows |
| :--- | :--- | :--- | :--- |
| File:/C:\windows\ | File:/C:\windows/ | File://C:/windows | File://C:/windows/ |
| File://C:/windows\ | File://C:\windows | File://C:\windows/ | File://C:\windows\ |
| C:/windows | C:/windows/ | C:/windows\ | C:\windows |
| C:\windows\ | C:\windows/ | %WINDIR% | %TMP% |
| %TEMP% | %SYSTEMDRIVE% | %SYSTEMROOT% | %APPDATA% |
| %HOMEDRIVE% | %HOMESHARE |  |   |

## Abusing Common Dialogs

**Common Dialogs** are those options of **saving a file**, **opening a file**, selecting a font, a color... Most of them will **offer a full Explorer functionality**. This means that you will be able to access Explorer functionalities if you can access these options.

## Browsers tricks

Backup iKat versions:

[http://swin.es/k/](http://swin.es/k/)  
[http://www.ikat.kronicd.net/](http://www.ikat.kronicd.net/)  


## Internet Explorer Tricks

### 'Image Toolbar'

It's a toolbar that appears on the top-left of image when it's clicked. You will be able to Save, Print, Mailto, Open "My Pictures" in Explorer. The Kiosk needs to be using Internet Explorer.

### Shell Protocol

Type this URLs to obtain an Explorer view:

* `Shell:Profile`
* `Shell:ProgramFiles`
* `Shell:System`
* `Shell:ControlPanelFolder`
* `Shell:Windows`
* `shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}` --&gt; Control Panel
* `shell:::{20D04FE0-3AEA-1069-A2D8-08002B30309D}` --&gt; My Computer
* `shell:::{{208D2C60-3AEA-1069-A2D7-08002B30309D}}` --&gt; My Network Places
* `shell:::{871C5380-42A0-1069-A2EA-08002B30309D}` --&gt; Internet Explorer

## iPad

### Gestures and bottoms

#### Swipe up with four \(or five\) fingers / Double-tap Home button

To view the multitask view and change App

#### Swipe one way or another with four or five fingers

In order to change to the next/last App

#### Pinch the screen with five fingers / Touch Home button / Swipe up with 1 finger from the bottom of the screen in a quick motion to the up

To access Home

#### Swipe one finger from the bottom of the screen just 1-2 inches \(slow\)

The dock will appear

#### Swipe down from the top of the display with 1 finger

To view your notifications

#### Swipe down with 1 finger the top-right corner of the screen

To see iPad Pro's control centre

#### Swipe 1 finger from the left of the screen 1-2 inches

To see Today view

#### Swipe fast 1 finger from the centre of the screen to the right or left

To change to next/last App

#### Press and hold the On/**Off**/Sleep button at the upper-right corner of the **iPad +**  Move the Slide to **power off** slider all the way to the right,

To power off

#### Press the  On/**Off**/Sleep button at the upper-right corner of the **iPad and the Home button for a few second**

To force a hard power off

#### Press the  On/**Off**/Sleep button at the upper-right corner of the **iPad and the Home button quickly**

To take a screenshot that will pop up in the lower left of the display. Press both buttons at the same time very briefly as if you hold them a few seconds a hard power off will be performed.

### Shortcuts

You should have an iPad keyboard or a USB keyboard adaptor. Only shortcuts that could help escaping from the application will be shown here.

| Key | Name |
| :--- | :--- |
| ⌘ | Command |
| ⌥ | Option \(Alt\) |
| ⇧ | Shift |
| ↩ | Return |
| ⇥ | Tab |
| ^ | Control |
| ← | Left Arrow |
| → | Right Arrow |
| ↑ | Up Arrow |
| ↓ | Down Arrow |

#### System shortcuts

These shortcuts are for the visual settings and sound settings, depending on the use of the iPad.

| Shortcut | Action |
| :--- | :--- |
| F1 | Dim Sscreen |
| F2 | Brighten screen |
| F7 | Back one song |
| F8 | Play/pause |
| F9 | Skip song |
| F10 | Mute |
| F11 | Decrease volume |
| F12 | Increase volume |
| ⌘ Space | Display a list of available languages; to choose one, tap the space bar again. |

#### iPad navigation

| Shortcut | Action |
| :--- | :--- |
| ⌘H | Go to Home |
| ⌘⇧H \(Command-Shift-H\) | Go to Home |
| ⌘ \(Space\) | Open Spotlight |
| ⌘⇥ \(Command-Tab\) | List last ten used apps |
| ⌘~ | Go t the last App |
| ⌘⇧3 \(Command-Shift-3\) | Screenshot \(hovers in bottom left to save or act on it\) |
| ⌘⇧4 | Screenshot and open it in the editor |
| Press and hold ⌘ | List of shortcuts available for the App |
| ⌘⌥D \(Command-Option/Alt-D\) | Brings up the dock |
| ^⌥H \(Control-Option-H\) | Home button |
| ^⌥H H \(Control-Option-H-H\) | Show multitask bar |
| ^⌥I \(Control-Option-i\) | Item chooser |
| Escape | Back button |
| → \(Right arrow\) | Next item |
| ← \(Left arrow\) | Previous item |
| ↑↓ \(Up arrow, Down arrow\) | Simultaneously tap selected item |
| ⌥ ↓ \(Option-Down arrow\) | Scroll down |
| ⌥↑ \(Option-Up arrow\) | Scroll up |
| ⌥← or ⌥→ \(Option-Left arrow or Option-Right arrow\) | Scroll left or right |
| ^⌥S \(Control-Option-S\) | Turn VoiceOver speech on or off |
| ⌘⇧⇥ \(Command-Shift-Tab\) | Switch to the previous app |
| ⌘⇥ \(Command-Tab\) | Switch back to the original app |
| ←+→, then Option + ← or Option+→ | Navigate through Dock |

#### Safari shortcuts

| Shortcut | Action |
| :--- | :--- |
| ⌘L \(Command-L\) | Open Location |
| ⌘T | Open a new tab |
| ⌘W | Close the current tab |
| ⌘R | Refresh the current tab |
| ⌘. | Stop loading the current tab |
| ^⇥ | Switch to the next tab |
| ^⇧⇥ \(Control-Shift-Tab\) | Move to the previous tab |
| ⌘L | Select the text input/URL field to modify it |
| ⌘⇧T \(Command-Shift-T\) | Open last closed tab \(can be used several times\) |
| ⌘\[ | Goes back one page in your browsing history |
| ⌘\] | Goes forward one page in your browsing history |
| ⌘⇧R | Activate Reader Mode |

#### Mail shortcuts

| Shortcut | Action |
| :--- | :--- |
| ⌘L | Open Location |
| ⌘T | Open a new tab |
| ⌘W | Close the current tab |
| ⌘R | Refresh the current tab |
| ⌘. | Stop loading the current tab |
| ⌘⌥F \(Command-Option/Alt-F\) | Search in your mailbox |

### References

* [https://www.macworld.com/article/2975857/6-only-for-ipad-gestures-you-need-to-know.html](https://www.macworld.com/article/2975857/6-only-for-ipad-gestures-you-need-to-know.html)
* [https://www.tomsguide.com/us/ipad-shortcuts,news-18205.html](https://www.tomsguide.com/us/ipad-shortcuts,news-18205.html)
* [https://thesweetsetup.com/best-ipad-keyboard-shortcuts/](https://thesweetsetup.com/best-ipad-keyboard-shortcuts/)
* [http://www.iphonehacks.com/2018/03/ipad-keyboard-shortcuts.html](http://www.iphonehacks.com/2018/03/ipad-keyboard-shortcuts.html)
