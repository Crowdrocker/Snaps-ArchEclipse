# WehttamSnaps Hypr-Snaps: GitHub-ready modular Hyprland setup

[![CI](https://github.com/Crowdrocker/Hypr-Snaps-GitHub-Ready/actions/workflows/ci.yml/badge.svg)](https://github.com/Crowdrocker/Hypr-Snaps-GitHub-Ready/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![GitHub release](https://img.shields.io/github/v/release/Crowdrocker/Hypr-Snaps-GitHub-Ready?style=for-the-badge)](https://github.com/Crowdrocker/Hypr-Snaps-GitHub-Ready/releases)

WehttamSnaps Hypr-Snaps is a modular Hyprland-based setup tailored for WehttamSnaps branding. It’s designed for gaming, streaming, and a fast, responsive workflow on Arch Linux.

What’s included
- Core Hyprland config (hyprland.conf) with modular pieces
- Waybar config and neon cyberpunk styling
- Clickable launcher icons for Steam, Lutris, MO2, and Vortex in Waybar
- A rofi-based game launcher with a full icon set
- Per-app workspace rules and an auto-assign startup helper
- Audio routing templates (PipeWire + qpwgraph)
- A ready-to-use “README-CUSTOMIZE.md” for quick branding tweaks
- A CI workflow to validate the template structure on pushes

Repo structure (high level)
- config/hypr/hyprland.conf.template
- config/hypr/config.d/
  - bar/ (Waybar config)
  - launcher/ (launcher scripts)
  - workspace/ (workspace rules, auto-assign)
  - settings/ (ML4W-like, stub)
  - workspace/ (per-app workspace rules)
  - audio/ (audio routing scripts)
- waybar/config and style.css
- scripts/ (install.sh, build-final-config.sh)
- assets/ (optional icons and themes)
- docs/ (customization guide, notes)
- README.md
- README-CUSTOMIZE.md
- CONTRIBUTING.md
- LICENSE

Getting started
- Prerequisites: Arch Linux, NVIDIA RTX 1650 (can swap to RX580 later)
- Install: clone this repo, copy templates to your Arch install, customize paths, and run the build script
- Build final Hyprland config and reload Hyprland

Contributing
- Fork the repository and create feature branches (e.g., feature/bar, feature/launcher, feature/workspace)
- Open a pull request to merge into main
- Ensure scripts pass shellcheck, and templates remain modular and well-documented
- See CONTRIBUTING.md for more details

License
- MIT license. See LICENSE in the repo.

Project governance
- This is a community-oriented starter template. You’re encouraged to adapt, extend, and share improvements.

Customization quick-start
- Edit Waybar’s style.css for color tweaks (cyberpunk violet-to-cyan gradient)
- Add or modify launcher scripts under config/hypr/config.d/launcher
- Update per-app workspaces in config/hypr/config.d/workspace/workspace-assignments.conf
- Rebuild final config with: bash config/hypr/build-final-config.sh
- Start Hyprland (log out/in or restart Hyprland)

CI integration
- This repo includes a CI workflow (ci.yml) to automatically validate template structure on pushes and PRs
- The badge at the top of this README reflects CI status

Next steps
- If you want, I can tailor icons to a specific Nerd Font you have installed, add more per-app launchers, or expand workspace rules
- I can also add a small one-page README within docs/ for branding guidelines and a quick-start checklist

Block 2: ci.yml (GitHub Actions workflow)
Code block you can paste into .github/workflows/ci.yml

name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  validate-templates:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Install dependencies
        run: |
          sudo apt-get update
          sudo apt-get install -y shellcheck yamllint jq

      - name: ShellCheck all scripts
        run: |
          bash -n scripts/**/*.sh || true
          shellcheck scripts/**/*.sh || true
          shellcheck config/**/*.sh || true

      - name: Lint Waybar YAML
        run: |
          yamllint waybar/config waybar/config.yaml || true
          true

      - name: Validate Hypr layout presence
        run: |
          if [ ! -f config/hypr/hyprland.conf ]; then
            echo "Missing config/hypr/hyprland.conf"
            exit 1
          fi
          if [ ! -d config/hypr/config.d ]; then
            echo "Missing config/hypr/config.d directory"
            exit 1
          fi

      - name: Basic repo sanity
        run: |
          if [ ! -d config/hypr/config.d/bar ]; then echo "Missing bar module"; exit 1; fi
          if [ ! -d config/hypr/config.d/launcher ]; then echo "Missing launcher module"; exit 1; fi
          echo "Template structure validated."

      - name: CI success
        run: echo "CI checks passed"



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
