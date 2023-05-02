# Neovim Configuration for Windows
This repo is based on Lunix (see fork repo) and makes changes to run Neovim with many plugins in Windows. Idea is to configure an ICer or FPGA working enviroment limited by company's OS 😂

## Get Start
The entire toolchain includes items below:
* **Neovim** - fundation
* **Alacritty** - terminal tool
* **MYSY2** - unix complier env for windows
* **Ripgrep** - support telescope nvim plugin
* **Nerd Font** - support nvim tree plugin
* **Many Plugins** - all handled by the packer inside neovim repo

Feel free to change any of them if you have a better solution!

## Neovim
Download and install nvim-win64.msi
- [Neovim](https://github.com/neovim/neovim/releases/tag/stable)
It can add to your user PATH automatically. Run ```nvim -v``` in a terminal (ect. powershell) to check installation success.
Clone this git repo to (~\AppData\Local\) in your windows. After that, you can run ``` :checkhealth ``` in your Neovim to check configuration.

## Alacritty
Download and install Alacritty-v0.12.0-installer.msi (new version prefered)
- [Alacritty](https://github.com/alacritty/alacritty/releases)
Alacritty can work well with nvim-tree plugin and faster. Please copy those 2 files to ....
Launch Run App in windows and type ``` %APPDATA% ```, create alacritty folder under this path ( *%APPDATA%\alacritty\alacritty.yml* ) and put the configuration files.

## Nerd Font
This type of Font is necessary to dispaly all signs from nvim-tree. Suggest Hack Nerd Font.
- [Nerd Font](https://www.nerdfonts.com/font-downloads)
Copy files to (C:\Windows\Fonts) in your windows. I only use HackNerdFont-Regular.ttf 
