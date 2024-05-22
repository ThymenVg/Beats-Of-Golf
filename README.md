# <Beats of Golf Automation>
**A NEWER VERSION WILL BE RELEASED IN 2026, THIS VERSION WILL BE COMPLETE FOR ENTERPRISE USE**

## Description

This application is developed to automate the startup of the needed software for golf simulators. You can use this application for other purposes aswell. It's functionality is not dedicated to golf simulator software. Because of this application employees have to spend less time making sure every simulator is up and running. During development I learned how to use windows API's in C# and use those API's to manipulate mouse inputs and window handlers.

## Table of Contents

- [Installation](#installation)
- [Config](#config)
- [Example](#example)
- [Trouble shooting](#trouble-shooting)
- [Usage](#usage)
- [Credits](#credits)

## Installation

You need to download **two** things:
1. **.NET runtime 6.0.29** https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-6.0.29-windows-x64-installer
2. **This project**'s zipped repository


**.NET runtime**
- run the installer
- complete the wizard

**This project**
- extract the zip

## Config

**The zipped folder contains a file named _config.txt_ this file must at all times, be present in the same directory as the executable.**
to config the executable open the _config.txt_ file in your preferred text editor. With the config file openend write your commands line by line. Commands are written in following format: _Command-Number;Parameter1; . . . ;Parameter-n_.
In total there are 6 different commands all represented by a command number.

| command number     | command purpose |parameter 1 |parameter 2|parameter 3 |parameter 4| parameter 5|example|
| ----------- | ----------- |------------------------|------------------------|-------------------------------|-----------|------------|--------|
|1|open a program|directory of executable|N/A|N/A|N/A|N/A|1;C:\Program Files\7-Zip\7z.exe
|2|delay the next command|duration in ms|N/A|N/A|N/A|N/A|2;5000
|3|**focus** the window, reposition and resize a program|name of target program as seen in task manager|x-coordinate|y-coordinate|width|height|3;firefox;0;0;1500;1500
| 4|double left mouse click|x-coordinate|y-coordinate|N/A|N/A|N/A|4;250;142
|5|single left mouse click|x-coordinate|y -coordinate|N/A|N/A|N/A|5;750;374
|6|drag left mouse click|starting x-coordinate|starting y-coordinate|the ammount of pixels you want to move on the x-axis|the ammount of pixels you want to move on the y-axis|N/A|6;1250;900;0;100

when finished writing the config file make sure to save the file

## Example
Let's say you'd for some reason want to configurate the program to automatically open youtube and play a youtube short...

- Here is an example of what the config file could look like.
``` 
1;C:\Program Files\Mozilla Firefox\firefox.exe
2;2500
3;firefox;-2;0;2570;1440
2;1000
5;230;100
2;3000
6;2555;200;0;500
5;1000;1000
3;firefox;0;0;750;1000
```
- This is the result when executed.

https://github.com/ThymenVg/Beats-Of-Golf/assets/78809977/4e8cdf89-fd73-4241-acfb-b58d011c261d

- Lastly, this is the terminal after finishing the execute.
  
![terminal after execute](https://github.com/ThymenVg/Beats-Of-Golf/assets/78809977/39b29d1e-9eb4-480b-8e37-10574882b183)

## Trouble-Shooting
Because this is a prototype a few issues may arise. Almost everytime a issue happens the terminal will close and all further commands will be stopped. Here as some of the most common reasons:
- When using _command 1_ and giving an incorrect filepath or the filepath isn't an executable
- When using _command 3_ and giving a wrong or non existant window name, make sure always to give the name as shown in task manager
- When empty lines are present in the config file
- Not enough or incorrect parameters
- Redudent spaces in commands 

## Usage
Some program requires admin priv. and as a result give a pop up this disturbs the flow of the program. To bypass this disable these notifications **DO SO AT YOUR OWN RISK**
1. Open windows search
2. type "change user account control setting"
3. drag the slider all the way down to "never notify"
4. click "ok"

If you wish the program to automatically start when the computer boots, follow these steps:
1. Open the locally downloaded repository folder
2. Copy the full path of the executable (.exe)
3. Press window+R
4. Enter "shell:startup"
5. Press enter
6. In the startup folder right click -> new -> shortcut
7. Paste the executable's full path
8. Click "next"
9. Give the shortcut a name to your desire
10. finally click "finish"

shell startup starts the program when the PC is booted. Not when the user logs in, this can create issues for the click commands. To fix this you can disable the windows user authentication as explained in the following video: https://www.youtube.com/watch?v=_WSGqnKHZsI make sure to use your password in NETPLWIZ en not your pincode, otherwise it won't work.
## Credits

Special thanks to Aäron Leman (https://www.linkedin.com/in/a%C3%A4ronleman/), he helped me brainstorm :P
