Manjaro XFCE edition
===========

- * [Install](#Install)
- * [Conf](#Conf)
- * [Use](#Use)
- * [Issues and workarounds](#issues)
- * [awesome wm](#awesome)

<a name="issues"/>

### 1. Issues and workarounds

1.1: Unable to git push, ssh, key error  
  Start the sshkey-agent:  

  `eval "$(ssh-agent -s)"`  
  
  add the ssh key:  

  `ssh-add ~/%pubkey%`  

  
1.2: High fan speed/temp  
Check out [throttled](https://github.com/erpalma/throttled)


1.3: Volume hotkeys not changing volume for bluetooth device?  
Open sound settings(pavucontrol) in tab Output switch output to integrated audio and then back to Bluetooth Headphones

<a name="Awesome"/>

### 2. Awesome


[How to awesome WM!](/awesome/awesome.md)
