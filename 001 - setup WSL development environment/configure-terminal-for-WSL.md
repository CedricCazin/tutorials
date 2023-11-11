# Configure PowerShell on Terminal

Terminal should automaticaly setup PowerShell profile, but don't hesitate to modify it.

To configure the profile on Terminal, Open sthe settings GUI
* Edit a prfile
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
            "font": 
            {
                "face": "CaskaydiaCove Nerd Font Mono"
            }
        },
        "list": 
        [
            {
                "__comment__": "DUPLICATE FROM A PROFILE WSL Ubuntu-22.04",
                "colorScheme": "Campbell",
                "commandline": "C:\\Windows\\system32\\wsl.exe -d Ubuntu-22.04",
                "guid": "{c391a90c-4ee9-4989-a02e-95ae2c5827b4}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/{9acb9455-ca41-5af7-950f-6bca1bc9722f}.png",
                "name": "Ubuntu-22.04",
                "startingDirectory": "~"
            },
            {
                "__comment__": "DUPLICATE FROM A PROFILE WSL Ubuntu-20.04",
                "colorScheme": "Campbell",
                "commandline": "C:\\Windows\\system32\\wsl.exe -d Ubuntu-20.04",
                "guid": "{9ec9e8ef-9b92-4a47-9d17-26305ff47f0f}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/{9acb9455-ca41-5af7-950f-6bca1bc9722f}.png",
                "name": "Ubuntu-20.04",
                "startingDirectory": "~"
            },
            {
                "__comment__": "DUPLICATE FROM A PROFILE Ubuntu-20.04",
                "colorScheme": "Ubuntu-20.04-ColorScheme",
                "commandline": "ubuntu2004.exe",
                "cursorShape": "filledBox",
                "font": 
                {
                    "size": 13.0
                },
                "guid": "{4b78dc20-0f4c-4bcf-9f6f-7c9bfce0d8d2}",
                "hidden": false,
                "icon": "https://assets.ubuntu.com/v1/49a1a858-favicon-32x32.png",
                "name": "Ubuntu 20.04.6 LTS (Copier)",
                "tabTitle": "Ubuntu 20.04.6 LTS"
            },
            {
                "__comment__": "DUPLICATE FROM A PROFILE WSL Ubuntu-22.04",
                "colorScheme": "Ubuntu-22.04-ColorScheme",
                "commandline": "ubuntu2204.exe",
                "cursorShape": "filledBox",
                "font": 
                {
                    "size": 13.0
                },
                "guid": "{001daa8e-6e60-4b84-8d47-5320ea7687ee}",
                "hidden": false,
                "icon": "https://assets.ubuntu.com/v1/49a1a858-favicon-32x32.png",
                "name": "Ubuntu 22.04.2 LTS (Copier)",
                "tabTitle": "Ubuntu 22.04.2 LTS"
            }
            ...
        ],
    },
    ...
},
```
