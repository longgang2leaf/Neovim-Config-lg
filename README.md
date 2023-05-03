# Neovim Configuration for Windows
This repo is based on Lunix (see fork repo) and makes changes to run Neovim with many plugins in Windows. Idea is to configure an ICer or FPGA working enviroment limited by company's OS 😂

## Get Start
The entire toolchain includes items below:
* **Python**
* **Neovim** - fundation
* **Alacritty** - terminal tool
* **MYSY2** - unix complier env for windows
* **Ripgrep** - support telescope nvim plugin
* **Nerd Font** - support nvim tree plugin
* **Many Plugins** - all handled by the packer inside neovim repo
* **HDL-checker** - ```pip3 install hdl-checker --upgrade```

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

Run in git bash and set some alias. C:\Program Files\Git\etc\profile.d\aliases.sh 
``` alias vtags='python D:/Software/Tools/vtags-3.11/vtags.py' ```

## Nerd Font
This type of Font is necessary to dispaly all signs from nvim-tree. Suggest Hack Nerd Font.
- [Nerd Font](https://www.nerdfonts.com/font-downloads)

Copy files to (C:\Windows\Fonts) in your windows. ect: HackNerdFont-Regular.ttf 

Or you can run ```Add-Font "C:\Windows\Fonts\fontfile.ttf"``` in Powershell as administrator

## Ripgrep
The ripgrep supports telescope nvim plugin.
- [Scoop](https://scoop.sh/#/)
Run following commands in Powershell to install Scoop (not in Admin mode):
```bash
$ Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
$ irm get.scoop.sh | iex
```
- [ripgrep](https://github.com/BurntSushi/ripgrep#installation)
```$ scoop install ripgrep```

## MSYS2
- [MSYS2](https://www.msys2.org/)

After installation, run ``` $ pacman -S mingw-w64-ucrt-x86_64-gcc ```in MSYS2 shell.

Add C:\msys64\ucrt64\bin to PATH and check with ``` $ gcc --version ```
