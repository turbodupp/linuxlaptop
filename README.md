# linuxlaptop
Processes and workarounds for using linux as main OS @ work

Current itteration is specificly for running Manjaro XFCE 18.1 @ thinkpad x1 6th gen
NOTE: for old POP!os setup, check [here](popos.md)

##### Table of Contents
- [Setting up disk encryption](#encryption)

- [Outlook, teams, rocketchat](#franz)

- [Anyconnect VPN](#vpn)

- [Terminal environment](#shell)

- [Gnome shell](#Gnomeshell)

- [Other stuff](#other)

- [Untested](#nottested)

- [Links](#links)


<a name="encryption"/>

### 0. Disk Encryption

Just use LUKS, you get the option during install

<a name="franz"/>

### 1. Communication suite. Getting outlook, teams and rocketchat up and running.

- **USE FRANZ**
To get rocketchat working just a self-hosted variant, the rest is self-explanatory.
Same goes with outlook o365/teams, just add and log in.


<a name="vpn"/>

### 2. Openconnect

VPN connections can be handled with openconnect, so no need to hunt down an outdated anyconnect version, just install these packages instead:

1. openconnect
2. networkmanager-openconnect

Congratulations, all you need to connect now is add the address: `%vpn address here%`
 
 
<a name="shell"/>
 
### 3. Terminal env

Currently running ZSH with powerlevel10k theme. ZSH comes default on manjaro, but to install p10k do:

`sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`  
  
`git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`  

then edit ~/.zshrc and change ZSH_THEME to powerlevel10k/powerlevel10k

next time you restart shell it should start the powerlevel10k install

However you do need propper fonts for it to display properly. Currently im using meslo LGS, which you can get here:  
- [MesloLGS NF Regular.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Regular.ttf)  
- [MesloLGS NF Bold.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Bold.ttf)  
- [MesloLGS NF Italic.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Italic.ttf)  
- [MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Bold%20Italic.ttf)  

or alternatively, install with pacman:  
`sudo pacman -S ttf-meslo`  
or if you want more fonts:  
`sudo pacman -S nerd-fonts-complete`  

- [syntax highlighting in nano](https://github.com/scopatz/nanorc)

#### 3.1 Guake + byobu

- *install Guake*
- *install byobu*
- *set startup command in terminal profile to launch byobu*
- *edit pulldown shortcut key for byobu*

#### 3.2 Wayland-Yutani custom startup

- [weyland-yutani.bashrc](https://gist.github.com/NoraCodes/ffef855e204da213d6f9)
- [weyland-yutani.sh](https://gist.github.com/NoraCodes/adeb3f9eff67ae07b877)

#### 3.3 Plugins

Plugins im currently using:

- **git**
- **kubectl**
- **kube-ps1**
- **colored-man-pages**
- **helm**

- <b>zsh-autosuggestions</b>  
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

- <b>fast-syntax-highlighting</b>  
`git clone https://github.com/zdharma/fast-syntax-highlighting.git \
  ~/.oh-my-zsh/custom/plugins/fast-syntax-highlighting`

#### 3.4 Cloud SDK's

- **Gcloud sdk**
`curl https://sdk.cloud.google.com | bash`  
`gcloud init`

- **IBM Cloud cli**
`curl -sL https://ibm.biz/idt-installer | bash`  
`ibmcloud login`


<a name="Gnomeshell"/>

#### 4. Gnome shell
dont

#### 4.1 Lock screen gone?
'gsettings get org.gnome.desktop.lockdown disable-lock-screen'

#### 4.2 Shell extensions
- *~~[KStatusNotifierItem]~~(https://extensions.gnome.org/extension/615/appindicator-support/) - ~~since topicons plus stopped working with 19.10~~
- *[Dash-to-Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
- *[Shelltile](https://extensions.gnome.org/extension/657/shelltile/)
- *[Openweather](https://extensions.gnome.org/extension/750/openweather/)
- *[Pomodoro](https://extensions.gnome.org/extension/53/pomodoro/)
- *[TopIcons-Plus](https://github.com/phocean/TopIcons-plus) bruk manual installation enn så lenge

<a name="links"/>

### 7. Links ETC

- *Manjaro XFCE4 setup
[Sepparate howto page](manjaro.md)