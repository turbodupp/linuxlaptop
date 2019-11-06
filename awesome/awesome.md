~~~Switching to Awesome~~~
====  
- install Awesome through pamac or pacman
- packages you want:
* awesome
* awesome-freedesktop
* awesome-terminal-fonts
* lain-git

# Theme it hard!
* [awesome copypats](https://github.com/lcpz/awesome-copycats)
* Clone the repo above
* backup old rc.lua from ~/.conf/awesome
* mv awesome-copycats/* .conf/awesome

Så kommer finjusteringen

* edit rc.lua and change the default run launcher to rofi 

* `awful.key({ modkey }, "F2", function () awful.screen.focused().mypromptbox:run() end,`   
you need to edit the run key to something other than R, and then you can add the follow lines above it:
- `awful.key({ modkey }, "r", function () awful.util.spawn("rofi -show run", false) end),`  

    `awful.key({ modkey }, "l", function () awful.util.spawn("i3lock-fancy -gpf Meslo-LG-S-Regular -- scrot -z", false) end),`