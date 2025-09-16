<div align = center>
  
<a href="https://discord.gg/9bAVTCNZ">
    <img alt="Dynamic JSON Badge" src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscordapp.com%2Fapi%2Finvites%2Fyour-invite-code%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&suffix=%20members&style=for-the-badge&logo=discord&logoSize=auto&label=WehttamSnaps%20Community&labelColor=ebbcba&color=8A2BE2">
</a>

###### _<div align="right"><a id=-design-by-t2></a><sub>// design by t2</sub></div>_

![hyde_banner](Source/assets/hyde_banner.png)

<div align="center">
  
[![Twitch](https://img.shields.io/badge/Twitch-WehttamSnaps-9146FF?style=for-the-badge&logo=twitch)](https://www.twitch.tv/wehttamsnaps)
[![YouTube](https://img.shields.io/badge/YouTube-WehttamSnaps-FF0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@WehttamSnaps)
[![GitHub](https://img.shields.io/badge/GitHub-Crowdrocker-181717?style=for-the-badge&logo=github)](https://github.com/Crowdrocker)

</div>

<div align="center">

# Description

This is my daily driver configuration that I use on both my laptop and desktop for coding, gaming, trading, browsing the web, etc., with Dvorak in mind. I am constantly adding new features and improvements.

I use Arch BTW.. :)

> **Feel free to open an issue ♡ (anything you can think of)!**

# Discord

New official [Discord](https://discord.gg/9bAVTCNZ) server.

# See Wiki

> The README as an organized [WIKI](https://archeclipse-wiki.vercel.app/)

# Design Philosophy

- Enhanced productivity
- Faster responsiveness
- Smooth animations
- Vibrant color schemes
- It just works

# Features

- **Dynamic wallpapers** based on workspaces: Custom scripts & [Hyprpaper](https://github.com/hyprwm/hyprpaper)
- **Dynamic color schemes** based on current wallpaper: Custom scripts & [PyWal](https://github.com/dylanaraps/pywal)
- **Global Theme switcher (Light/Dark)**: Custom scripts
- **Ags V2 widgets** ~~(Eww replaced)~~: _these are just some of the features_
  - Color scheme based on current wallpaper
  - Main bar
    - Dark/light modes
    - Bandwidth speed monitor
  - Application launcher ~~(Rofi replaced)~~
    - App launcher
    - Emojis
    - Arithmetics
    - Url forwarding to default browser
    - custom commands
  - Wallpaper switcher for each workspace
  - Media player
  - Right Panel
    - Waifu display -- using [Danbooru](https://danbooru.donmai.us) and [Gelbooru](https://gelbooru.com) APIs
    - Media Player
    - Notification history - filter
    - Calendar
  - Left Panel
    - Chat Bot -- multiple APIs + image generation
    - Booru Viewer -- using [Danbooru](https://danbooru.donmai.us) and [Gelbooru](https://gelbooru.com) APIs
  - Hyprland Settings widget
  - User Panel (logout etc...)
- **High-quality wallpapers** from [Danbooru](https://danbooru.donmai.us), [Yandere](https://yande.re), and [Gelbooru](https://gelbooru.com)

# Current Workflow

> **Important:** Screenshots below ⊽

| W1  | W2      | W3  | W4                                                  | W5                                           | W6                                                  | W7                                                                            | W8  | W9  | W10   |
| --- | ------- | --- | --------------------------------------------------- | -------------------------------------------- | --------------------------------------------------- | ----------------------------------------------------------------------------- | --- | --- | ----- |
| --- | Browser | --- | [Spotify](https://wiki.archlinux.org/title/spotify) | [Btop](https://github.com/aristocratos/btop) | [Discord](https://wiki.archlinux.org/title/Discord) | [Steam](https://wiki.archlinux.org/title/steam)/[Lutris](https://lutris.net/) | --- | --- | Games |

- **W`id`**: Workspace with corresponding ID.
- **`---`**: Placeholder, any app can go here.
- **`name`**: Application that opens automatically in its designated workspace.

# To-Do List

- **Users: Any suggestions or issues?**
- AGS V2 bundling
- AGS V2: GTK-3 --> GTK-4
- Make sure the dot-files work for every machine not just mine **(WIP)**
- Add tutorials for each part of the dot-files **(WIP)**
- Continuous improvements and polishing **(INDEFINITELY)**

# KeyBinds

KeyBinds are displayed and organized [Here](https://raw.githubusercontent.com/Crowdrocker/Snaps-ArchEclipse/refs/heads/master/.config/hypr/configs/keybinds.conf), be sure to check them out!

# Installation and Update

## Required Dependencies and packages

- [Arch Linux](https://archlinux.org/) (I use Arch linux BTW)
- [Hyprland](https://hyprland.org/)
- [Necessary packages](https://github.com/Crowdrocker/Snaps-ArchEclipse/blob/master/.config/hypr/pacman/pkglist.txt) (do not worry they will be installed automatically)

## Installation Guide

> Run this one liner in the terminal -- Say `Yes` to everything

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Crowdrocker/Snaps-ArchEclipse/refs/heads/master/.config/hypr/maintenance/INSTALL.sh)"
```

## Update Guide

> To update the config and its related pkgs Simply run `update` in the terminal

```bash
update
```

# Tips

- User Icon is stored in `$HOME/.face.icon`
- Press `SUPER + w` to select the wallpaper you like
- Custom wallpapers should be added in `$HOME/.config/wallpapers/custom`
- Custom hyprland configuration should be put in `$HOME/.config/hypr/configs/custom`
- Most functionalities have associated [keybinds](https://raw.githubusercontent.com/Crowdrocker/Snaps-ArchEclipse/refs/heads/master/.config/hypr/configs/keybinds.conf). Check them out!

> **Important**: If you encounter any problems, no matter how small, please feel free to open an issue. I’m happy to help! :)

# Additional Notes

- Machines with batteries (aka: laptops) require `upower` to be installed for battery monitoring to work properly.

# Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Crowdrocker/hyprland-conf&type=Date)](https://star-history.com/#Crowdrocker/hyprland-conf&Date)

# Visuals

## Application Launcher

| Apps                                                                                                                | Emojis                                                                                    | Arithmetics                                                                               | URLs                                                                                      |
| ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| ![clipboard_image_20241013_132106](https://github.com/user-attachments/assets/20f9ed91-79cf-41e7-bf5e-dacad8f3933b) | ![image](https://github.com/user-attachments/assets/a0ee2cb8-129a-4f38-b4f2-0636351a0c69) | ![image](https://github.com/user-attachments/assets/8449ae19-0d81-4505-9d58-7241da8dfd48) | ![image](https://github.com/user-attachments/assets/77cabaf7-1233-4f5f-9f56-c27e6e5e1ea5) |

## Right Panel

> You can customize the widget layout however you want!

| Example Layout                                                                            | Example Layout                                                                            |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| ![image](https://github.com/user-attachments/assets/0e8865aa-9e3e-4b20-af7c-cce5d7cd9206) | ![image](https://github.com/user-attachments/assets/bec585c9-aece-4517-bc09-6d739a7994e9) |

## Left Panel

| Chat Bot                                                                                  | Booru Viewer                                                                              |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| ![image](https://github.com/user-attachments/assets/7e8a472b-8195-4438-abd4-03e694b54352) | ![image](https://github.com/user-attachments/assets/f5ad3ee1-4c0a-4052-ad92-9b49b0123d11) |

## Media Player

![image](https://github.com/user-attachments/assets/1be9e780-88cd-4d9f-ba12-252784986bec)

## Wallpaper Switcher

![image](https://github.com/user-attachments/assets/55aea0b2-dea0-46f2-bb33-84ce66b4cb16)

## Theme Switching

| Dark Theme + Custom colors based on wallpaper                                             | Light Theme + Custom colors based on wallpaper                                            |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| ![image](https://github.com/user-attachments/assets/f3ff78c1-5243-4c00-9e03-898c517cccac) | ![image](https://github.com/user-attachments/assets/7b158721-38fa-4405-9cda-7864c1bc7818) |

## User Panel

![image](https://github.com/user-attachments/assets/d88f9a5e-c7da-4e31-80db-38073dc0278c)

# Tutorials

## App launcher

- `>` `[name]` : Custom Apps
- `emoji` `[name]` : emojis
- `translate` `[text]` `>` `fr|en|es|jp...` : translate text into other languages
- `[...1+2...]` : arithmetics (maths)
- `[link]` : open the link in browser
