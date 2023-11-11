# Install PowerShell

Just follow Microsoft articles:
* [Installing PowerShell on Windows](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows)
* [github PowerShell/readme.md Get PowerShell /](https://github.com/PowerShell/PowerShell/blob/master/README.md#get-powershell) 

# Configure PowerShell on Terminal

Terminal should automaticaly setup PowerShell profile, but don't hesitate to modify it.
It should look like this:

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
                "guid": "{fb8fefc7-0090-4173-8922-add87ba50790}",
                "name": "PowerShell",
                "commandline": "\"C:\\Program Files\\PowerShell\\7\\pwsh.exe\"",
                "icon": "ms-appx:///ProfileIcons/pwsh.png",
                "colorScheme": "Solarized Dark",
                "hidden": false,
                "startingDirectory": "%USERPROFILE%"
            },
        ],
    },
    ...    
},
```

# Install and configure OhMyPosh and pimp plugins

* [Customize PowerShell prompt with OhMyPosh](https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup)
* [Install Cascadia Code font](https://learn.microsoft.com/en-us/windows/terminal/cascadia-code)
* [Install Terminal Icons](https://github.com/devblackops/Terminal-Icons#installation)

![image](https://github.com/CedricCazin/tutorials/assets/26877462/f0cab309-c98d-4b4e-9ca7-93640d17fa08)

# Install PowerShell Pluggins

* [posh-git](https://github.com/dahlbyk/posh-git)

