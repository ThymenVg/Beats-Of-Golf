# <Beats of Golf Automation>

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
|3|reposition and resize a program|name of target program as seen in task manager|x-coordinate|y-coordinate|width|height|3;firefox;0;0;1500;1500
| 4|double left mouse click|x-coordinate|y-coordinate|N/A|N/A|N/A|4;250;142
|5|single left mouse click|x-coordinate|y -coordinate|N/A|N/A|N/A|5;750;374
|6|drag left mouse click|starting x-coordinate|starting y-coordinate|the ammount of pixels you want to move on the x-axis|the ammount of pixels you want to move on the y-axis|N/A|6;1250;900;0;100

when finished writing the config file make sure to save the file

## Example

``` 
HELLO
```

## Trouble-Shooting

## Usage

## Credits

Special thanks to Aäron Leman (https://www.linkedin.com/in/a%C3%A4ronleman/), he helped me brainstorm :P
