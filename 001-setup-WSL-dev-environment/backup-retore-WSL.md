# Export a WSL distribution

Export a distribution as a VHD file.

```PowerShell
wsl --export --vhd <distribution name> <vhdx file path> 
```

# Import a WSL distribution

Import a dsitribution from a VHD file.

```PowerShell
wsl --import-in-place <distribution name> <vhdx file path>
```

# Unregister a WSL distribution

> [!CAUTION]
> This will erase the existing distribution's file
> Ensure you exported the deistribution prior else it could cause data loss

```PowerShell
wsl --unregister <distribution name>
```

# For more information check Microsoft documentations:

* [import and export a distribution](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#import-and-export-a-distribution)
* [Import a distribution in place](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#import-a-distribution-in-place)
* [Unregister or uninstall a Linux distribution](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#unregister-or-uninstall-a-linux-distribution)
