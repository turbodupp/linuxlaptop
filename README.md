# linuxlaptop
Processes and workarounds for using linux as main OS @ work

Current itteration is specificly for running POP!_os 19.04 @ thinkpad x1 6th gen
NOTE: currently running 19.10 after an upgrade

##### Table of Contents
[Setting up power management and S3 sleep](#powersleep)

[Outlook, teams, rocketchat](#franz)

[Anyconnect VPN](#vpn)

[Shell environment](#shell)

[Other stuff](#other)

[Untested](#nottested)

[Links](#links)


<a name="powersleep"/>

### 0. Proper power management and s3 sleep

IMPORTANT: To enable s3 sleep you need to flash your BIOS to a newer version. Unsure the specific version at this point, but as of 15. SEP. 2019 the newest BIOS was able to do s3 sleep no problem.

Only thing you have to change is <b> sleep settings in bios, change from windows to other/linux </b>

<a name="franz"/>

### 1. Communication suite. Getting outlook, teams and rocketchat up and running.

To get rocketchat working just a self-hosted variant, the rest is self-explanatory.
Same goes with outlook o365/teams, just add and log in.


<a name="vpn"/>

### 2. Anyconnect VPN

https://faq.oit.gatech.edu/content/how-do-i-install-cisco-anyconnect-client-linux
this was relevant, but HER MÅ DET MER INFO SENERE
 
 
<a name="shell"/>
 
### 3. Shell env

Currently running ZSH with powerlevel10k theme


#### 3.2 Plugins
Plugins im currently using:
git
zsh-autosuggestions | git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

kubectl

kube-ps1

colored-man-pages

zsh-syntax-highlighting

helm
