# Keyboard Layout

![macOS](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/macos.svg)
![Windows](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/windows.svg)

Custom Russian keyboard layout with Symbols from Swiss German layout.

## Installation

### macOS

![macOS](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/macos.svg)

1. Download [`RUS_CH.keylayout`](https://raw.githubusercontent.com/weibeld-setup/install-keyboard-layout/main/macos/RUS_CH.keylayout) and [`RUS_CH.icns`](https://raw.githubusercontent.com/weibeld-setup/install-keyboard-layout/main/macos/RUS_CH.icns)
1. Copy both files to `/Library/Keyboard Layouts` (to find the folder use shift+cmd+G in finder)
1. Log out of macOS and log in again
1. Go to **_System Preferences > Keyboard > Text Input > Edit... > [+] > Others_**
1. Locate the **Russian Swiss Symbols** keyboard layout in the list and add it
1. Reboot 

### Windows

![Windows](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/windows.svg)

> Tested on Windows 11.

To install the keyboard layout, you must build a setup package from the [`RUCH.klc`](windows/RUCH.klc) file and then install this package:

1. Download and install the [Microsoft Keyboard Layout Creator (MSKLC)](https://www.microsoft.com/en-us/download/details.aspx?id=102134)
1. Download the [`RUCH.klc`](windows/RUCH.klc) file
1. In MSKLC, go to _**File > Load Source File...**_ and select the `RUCH.klc` file
1. Click on _**Project > Build DLL and Setup Package**_
   > This creates a directory called `RUCH` in the current working directory. There may be a dialog notifying about warnings during the build which can be ignored.
1. Run `setup.exe` in the `customsw` directory
   >  This installs the keyboard layout as `RUCH.dll` to `C:\Windows\System32` and creates the necessary registry entries to make the layout available to the system. If `setup.exe` doesn't work for some reason, try executing `RUCH_amd64.msi`. If you get error 1625:
   - Open Windows Security
   - Go to App & browser control
   - Open Smart App Control settings
   - Turn Smart App Control to Off
   - Reboot

Run your setup.exe again as administrator

1. In Windows, go to **_Settings > Time & Language > Language > Keyboard > Override for default input method_** and activate the **Russian Swiss Symbols** keyboard layout

> **Important:** after the installation, keep the `RUCH` directory somewhere on the system. This is because the contained `setup.exe` file allows to cleanly uninstall the keyboard layout. Uninstallation is necessary if you want to make changes to the keyboard layout (i.e. by editing the `.klc` file and rebuilding the DLL and setup package as described above) and then reapply it. The reason that the keyboard layout must be uninstalled before making changes is that MSKLC refuses to export a keyboard layout with the same name as an already installed keyboard layout.

## Notes

### Mappings

The keyboard layout is based on the Logitech Swiss German layout.


