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

## Good packages to install
* `pandoc`

## Yakuake

1. Install the Yakuake drop down terminal using the distro's package manager.
2. Open Yakuake and it will prompt you that it can be opened with F12, so do that
3. Press `Ctrl+Shift+,` to open the configuration
4. Under width, change to `100%`
5. Go to `appearance`, then `get new skins` and install the Materia Dark theme, and enable it
6. Go to `Autostart` in the system settings and enable Yakuake to autostart

## Fonts
1. Install the JetBrains Mono font found [here](https://www.jetbrains.com/lp/mono/)

## Hostname

1. Run `sudo nano /etc/hostname` and edit the file to contain the desired hostname
2. Run `sudo nano /etc/hosts` and change from the old to new hostname
3. Reboot to ensure the changes take effect

## Dolphin

1. Open Dolphin
2. Right click on the panel and change the icon size to large
3. Under `Configure Toolbars` add the terminal to the Toolbars
4. Create two folders in documents, `University` and `Personal Projects`

## Double click to open folders

Under `General Behaviour` in the system settings, change the option for opening a folder from single click to double click.

## NAS

1. Open Dolphin, under `Network`, use `Add Network Folder` to add the NAS
2. Add the created folder to the Places sidebar

## GPG Key

1. Install KGPG using the package manager
2. Add the GPG key (note that the GPG cannot be copied directly from a NAS, it must first be copied to the local file system)

## Git LFS
Install `git-lfs` using your package manager

## Firefox

1. Open Firefox and log in
2. Let all the extensions install and log in to them all
3. Under `Customize` enable the bookmark bar

## Calendar

1. Open KOrganiser
2. Under settings, go to `Configure KOrganiser`
3. Go to `Calendars` under `General` and click `Add`
4. Proceed with the steps to add Google Calendar
5. In the system tray, turn off notifications for the KOrganiser Daemon.

## Panel

1. Right click on the clock to change the time and date settings
2. Change the time format to 24 hours
3. Enable showing the date
4. Enable the PIM events plugin
5. Enable google calendar showing
6. Open the system tray settings
7. Disable the clipboard

## KRunner

To set up Krunner to open when the super key is pressed, add the following to the bottom of `~/.config/kwinrc`

```
[ModifierOnlyShortcuts]
Meta=org.kde.krunner,/App,,display
```

## Show Desktop

1. Go to `KWin Scripts` and enable the script titled `MinimiseAll`
2. In `Global Shortcuts` reassign `MinimiseAll` to `Super+D`

## LaTeX

1. Install the full version of `TexLive` using the package manager
2. Install `TexStudio` using the package manager
3. If available install `LanguageTool`
4. In the TexStudio settings under `Editor`, change to show all line numbers
5. Remove all unnecessary toolbars

## Flatpak

1. Install flatpak for your distribution using the instructions [here](https://flatpak.org/setup/)
2. Use it to install GitKraken, Spotify and Minecraft and sign in

## GitKraken

1. Open GitKraken and sign in using your GitHub credentials
2. Under preferences set up the GPG key you set up earlier
3. Clone in whatever repositories you are currently working on

## NodeJS

- Install NodeJS using the package manager
- Install Vercel using `npm i -g vercel`
- Log in using `vc login`
- Install Gatsby using `npm i -g gatsby-cli`
- Install prettier using `npm i -g prettier`

## Hugo
- Install hugo using your package manager

## Atom

1. If it is available for your distribution, install Atom using the instructions [here](https://flight-manual.atom.io/getting-started/sections/installing-atom/)
2. If it is not available install it using Flatpak
3. Install the `prettier-atom` plugin
4. In the prettier settings enable format on save
5. Go to the `autocomplete-plus` package settings and change the keymap for confirming a suggestion to `tab always`
6. Also in the `autocomplete-plus` settings, blacklist `*.md` files.
7. Under Packages, disable `Wrap Guide`, this removes the vertical line at 80 characters

## Visual Studio Code

1. VS Code can be installed using the instructions [here](https://code.visualstudio.com/docs/setup/linux)#
2. Install the following extensions:
  - Prettier
  - ESLint
  - Tailwind CSS IntelliSense
  - Headwind
  - GitLens

## Flameshot

1. Flameshot should be in the repos, if not check the website for an installer
2. Follow the instructions [here](https://flameshot.js.org/#/key-bindings?id=on-kde-plasma-desktop) to integrate with the Plasma Desktop

## Snap

1. Install Snap using the instructions [here](https://snapcraft.io/docs/installing-snapd)
2. Install MathPix Snipping tool using the command `sudo snap install mathpix-snipping-tool` and log in

## Python

- Most distros will have python and pip installed, so I'm skipping over that
- Install the black code formatter using `pip install black`

## Chromium

1. Install chromium using the package manager
2. Run the `widevine.sh` script to enable widevine for watching Netflix

## zsh
1. Install zsh using the package manager
2. Run `chsh -s $(which zsh)` to change the shell to zsh
3. Install oh my zsh using `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
4. Install bat using the package manager
5. Copy my dotfiles from my dotfiles repo https://github.com/samrobbins85/dotfiles
