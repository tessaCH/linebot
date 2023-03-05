# linebot
## Environment
* Windows 10
* Windows Terminal (Window PowerShell)
* .Net 3.1
* VSCode

## Setup Line Developer account for Message API
Goto https://developers.line.biz/
1. create account
2. create Messaging API

## Test using line.cli (.Net 3.1)
1. install line.cli<br>
   `dotnet tool install --global line.cli`
2. set channel access token (at the bottom of 'Messaging API' tag)<br>
   `line config -t [channel access token]`
3. test send message (use 'Your user ID' at the bottom of 'Basic settings' tag)<br>
   `line push -u [userId] -m [message]`
4. test send sticker<br>
   `line push -u [userId] -s [STKPKGID,STKID (ref: https://www.arduinoall.net/arduino-tutor/sticker_list.pdf)]`
5. test send photo<br>
   `line push -u [userId] -i [image html (start with https://)]`

## Create linebot project
1. Create project folder<br>
   `md [project]`<br>
   `cd [project]`

2. Init dotnet project and add linebot sdk<br>
   `dotnet new console`<br>
   `dotnet add package linebotsdk`<br>
   `dotnet build` (test)<br>
   `code .` (open VSCode)
