# Configure Terminal

Terminal should automatically setup PowerShell profile, but don't hesitate to modify it.

To configure the profile on Terminal, Open the settings GUI

* Edit a profile
* Create a new profile base on a profile found by Terminal (WSL distribution, Ubuntu, PowerShell...)
* Open the settings.json file

![image](https://github.com/CedricCazin/tutorials/assets/26877462/55224545-3ba6-4572-a30d-47a67aa0611b)

The file settings.json should look like this:

```json
{
    "$help": "https://aka.ms/terminal-documentation",
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "defaultProfile": "{fb8fefc7-0090-4173-8922-add87ba50790}",
    "profiles": 
    {
        "defaults": 
        {
            "__comment__": "CONFIGURATION FOR ALL PROFILES",
            "font": 
            {
                "__comment__": "FONT FACE NEEDED TO DISPLAY ICONS",
                "face": "CaskaydiaCove Nerd Font Mono",
                "size": 12.0
            }
        },
        "list": 
        [
            {
                "__comment__": "POwERSHELL 5",
                "altGrAliasing": true,
                "antialiasingMode": "grayscale",
                "closeOnExit": "automatic",
                "colorScheme": "Campbell",
                "commandline": "%SystemRoot%\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
                "cursorShape": "bar",
                "guid": "{acbf4777-f746-4a15-b5e3-9729d76534c6}",
                "hidden": false,
                "historySize": 9001,
                "icon": "ms-appx:///ProfileIcons/{61c54bbd-c2c6-5271-96e7-009a87ff44bf}.png",
                "name": "Windows PowerShell",
                "padding": "8, 8, 8, 8",
                "snapOnInput": true,
                "startingDirectory": "%USERPROFILE%",
                "useAcrylic": false
            },
            {
                "__comment__": "POwERSHELL 7",
                "colorScheme": "Solarized Dark",
                "commandline": "\"C:\\Program Files\\PowerShell\\7\\pwsh.exe\"",
                "guid": "{fb8fefc7-0090-4173-8922-add87ba50790}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/pwsh.png",
                "name": "PowerShell",
                "startingDirectory": "%USERPROFILE%"
            },                        
            {
                "__comment__": "A PROFILE WSL Ubuntu-22.04",
                "colorScheme": "Campbell",
                "commandline": "C:\\Windows\\system32\\wsl.exe -d Ubuntu-22.04",
                "guid": "{c391a90c-4ee9-4989-a02e-95ae2c5827b4}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/{9acb9455-ca41-5af7-950f-6bca1bc9722f}.png",
                "name": "Ubuntu-22.04",
                "startingDirectory": "~"
            },
            {
                "__comment__": "A WSL WSL Ubuntu-20.04",
                "colorScheme": "Campbell",
                "commandline": "C:\\Windows\\system32\\wsl.exe -d Ubuntu-20.04",
                "guid": "{9ec9e8ef-9b92-4a47-9d17-26305ff47f0f}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/{9acb9455-ca41-5af7-950f-6bca1bc9722f}.png",
                "name": "Ubuntu-20.04",
                "startingDirectory": "~"
            },
            ...
        ],
    },
    ...
},
```
