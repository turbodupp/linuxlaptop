Switching to Awesome
====  
- install Awesome through pamac or pacman
- packages you want:
* awesome
* awesome-freedesktop
* awesome-terminal-fonts
* lain-git

# Theme it hard!
* [awesome copycats](https://github.com/lcpz/awesome-copycats)
* Clone the repo above
* backup old rc.lua from ~/.conf/awesome
* mv awesome-copycats/* .conf/awesome

Så kommer finjusteringen

* edit rc.lua and change the default run launcher to rofi 

* `awful.key({ modkey }, "F2", function () awful.screen.focused().mypromptbox:run() end,`   
you need to edit the run key to something other than R, and then you can add the follow lines above it:
- `awful.key({ modkey }, "r", function () awful.util.spawn("rofi -show run", false) end),`  

- `awful.key({ modkey }, "l", function () awful.util.spawn("i3lock-fancy -gpf Meslo-LG-S-Regular -- scrot -z", false) end),`  

# Autorun.sh  
```
#!/usr/bin/env bash

function run {
  if ! pgrep $1 ;
    then
        $@&
          fi
          }
run nm-applet          
run pa-applet
run update-checker
exec /usr/lib/polkit-gnome/polkit-gnome-authentication-agent-1
```

# lockscreen
* i3lock-fancy-git / i3lock-fancy-rapid
* Lock function is described above autorun
* Choose one to use. i3lock-fancy-rapid is faster

```
awful.key({ modkey }, "l", function () awful.util.spawn("i3lock-fancy-rapid 10 5", false) end),
```

# Extra stuff to remember
* pamac-manager giving you authentication griefs? Check if you have an authentication agent running. If not, try using something like:  
`exec /usr/lib/polkit-gnome/polkit-gnome-authentication-agent-1 & `

* Monitors got messed up/missing layout? Check out ArandR  
Make and save a layout (.sh file)  
get it to run somehow! awesome autorun.sh doesnt seem to be able to call it.  
I should check out xinitrc?

* Network and bluetooth tray icons?  
Just run nm-applet and blueman-manager

* Laptop monitor not sutting off when closing lid and connected to dock?  
I have not figured this one out yet, still todo

<p align="center">

<h3>Things I tried to make it work

</p>