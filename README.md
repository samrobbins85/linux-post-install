# Post Install Instructions
## What you should have before this
A distro set up with KDE Plasma Desktop
## Update
Perform the distro update mechanism to ensure all packages are up to date
## Drivers
If on an Nvidia machine, follow the distro instructions to set up the NVidia drivers.
## Libraries
Follow the distro instructions to install graphics libraries such as `ffmpeg`
## Reboot
At this point, a reboot is good to load in the new drivers and packages
## Yakuake
1. Install the Yakuake drop down terminal using the distro's package manager.
2. Open Yakuake and it will prompt you that it can be opened with F12, so do that
3. Press `Ctrl+Shift+,` to open the configuration
4. Under width, change to `100%`
5. Go to `appearance`, then `get new skins` and install the Materia Dark theme, and enable it
6. Go to `Autostart` in the system settings and enable Yakuake to autostart

## Hostname
1. Run `sudo nano /etc/hostname` and edit the file to contain the desired hostname
2. Run `sudo nano /etc/hosts` and change from the old to new hostname
3. Reboot to ensure the changes take effect

## Dolphin
1. Open Dolphin
2. Right click on the panel and change the icon size to large
3. Under `Configure Toolbars` add the terminal to the Toolbars
4. Create two folders in documents, `University` and `Personal Projects`
