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
                "__comment__": "One version I created based on WSL cli",
                "colorScheme": "Campbell",
                "commandline": "C:\\Windows\\system32\\wsl.exe -d Ubuntu-20.04",
                "guid": "{9b2fbcb9-ddf8-4be7-a8a1-d179c46623de}",
                "hidden": false,
                "icon": "ms-appx:///ProfileIcons/{9acb9455-ca41-5af7-950f-6bca1bc9722f}.png",
                "name": "Ubuntu-20.04",
                "startingDirectory": "~"
            },
            {
                "__comment__": "Default one by ",
                "guid": "{17bf3de4-5353-5709-bcf9-835bd952a95e}",
                "hidden": false,
                "name": "Ubuntu-22.04",
                "source": "Windows.Terminal.Wsl"
            },
            {
                "__comment__": "Default one",
                "guid": "{d7b20cea-47a9-518c-95a4-c8bd91e2e1c6}",
                "hidden": false,
                "name": "Ubuntu 22.04.2 LTS",
                "source": "CanonicalGroupLimited.Ubuntu22.04LTS_79rhkp1fndgsc"
            },
            ...
        ],
    },
    ...
},
```
