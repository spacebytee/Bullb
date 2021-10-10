# Bullb
Program to turn web apps into windows applications (Similar to Electron) created with Visual Studio C#, and CefSharp, has it's own "Scripting language" using .bullbscript and .bullbform files or by directly Running Code from the js console
# Docs
Documentation for bullbscript
# OpenFile
OpenFile is very straight forward, log OpenFile, and then whatever process name you want, by default it will go from the directory the exe is running in, and you can use slashes to go itno folders from ther,e or you can type the exact directory.
Example: 
```sh
console.log('OpenFile,Program2.exe');
```
This should open Program2.exe in the same directory as your main exe file.
# Browser Control Commands
With these, you can do basic tasks with the brwoser, such as refresh, go back, or forward
Example: Refreshes The Current Page
```sh
console.log('BulbRefresh;');
```
Example: Goes Back one page
```sh
console.log('BulbBack;');
```
Example: Goes Forward one page
```sh
console.log('BulbForward;');
```
# CloseBulbApp
This commands closes the application
```sh
console.log('CloseBulbApp;');
```
# CloseProcessByName
Shuts down any windows process given it's name (Does not include file type such as .exe
Example:
```sh
console.log('CloseProcessByName,Audacity');
```
Closes Audacity
# ChangeBulbFormTitle
This commands changes the form title, however if you have SiteTitleChanges enabled in your .bulbsettings file, it will reset when a new page is loaded
```sh
console.log('ChangeBulbFormTitle,New Title!!');
```
# Bulb Form Icon Commands
This command changes the form icon to a file located in your resources folder
Example:
```sh
console.log('ChangeBulbFormIconFromResources,favicon2.ico');
```
This command changes the form icon to a file in a general location
Example:
```sh
console.log('ChangeBulbFormIconByLoc,C:/favicon.ico');
```
Should change the form icon to a file named 'favicon' in your C drive
# SetResizable
This command will set if your program is able to be resized, if this is false, the maximize button will be disable and you wont be able to resize the program on the edges with your Cursor
Example:
```sh
console.log('SetResizable,false');
```
Sets the program to not be resizable
# Show Minimize/Maximize boxes
Allows you to individually change if  the minimize and maximize boxes are enable or disabled, doesn't effect resizing  the window normally.
Example:
```sh
console.log('ShowMinimizeBox,false');
```
Hides the minimize box
# RunBatchCmdAsAdmin
Runs a single batch command as an administrator
```sh
console.log('RunBatchCmdAsAdmin,echo Hello World');
```
# RunBullbScript
At the moment, this only works for Bullb Forms, as BullbScript FILES arent implemented yet. However this runs bullb script from a file, which for normal bullb script is useful for executing a bunch of scripts at once
Example:
```sh
console.log('RunBullbScript,/Resources/form.bullbform');
```
