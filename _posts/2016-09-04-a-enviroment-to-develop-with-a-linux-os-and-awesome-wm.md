---
layout: post
section-type: post
title: "Awesome WM for a nice Linux experience"
category: tech
tags: ['tutorial', 'linux', 'awesome']
---

Linux is not only a very convenient enviroment to develop but also is the best way to take adventange of all posibilities provided for a personal computer. An operative system based on Linux allow customize the enviroment and the use of a very complete compedium of tools. On the other hand, Awesome Windows Manager is a level more to get the best experience with your system and your activity with Linux. This one is a dynamic window manager for the X Window System developed in the C and Lua programming languages. Lua is also used for configuring and extending the window manager. Its development began as a fork of dwm. It aims to be extremely small and fast, yet extensively customizable and make it possible for the user to productively manage windows with the use of keyboard. It is another world.

![image](/img/included/awesomewm.jpg "My Awesome WM")


### Install [XUbuntu](http://xubuntu.org/getxubuntu/mirrors/): 

As operative system based on Unix is possible use anyone but he most convenient would be an OS the most ligth as possible. For this reason I have choosen [XUbuntu](https://help.ubuntu.com/community/Installation?action=show&redirect=InstallingXubuntu){:target="_blank"}, an operative system derivated of Ubuntu. This one uses the Xfce desktop environment, instead of Ubuntu's Unity. It is recommended the last LTS version with all software updated to not be any problem with the wifi driver.

### Install browser, in my case Google Chrome:

Download package (64bits):

     wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

Install the package, forcing install of dependencies:

     sudo dpkg -i --force-depends google-chrome-stable_current_amd64.deb
     
In case any dependencies didn't install (you would have a warning or failure message for this), you can force them via:

     sudo apt-get install -f     
     
Just before install the new WM, it is interesting uninstall those apps not usefull to keep clean the OS.


### Install Awesome WM:

Install package:

     sudo apt-get install awesome awesome-extra
     
Remove XUbuntu desktop:

     sudo apt-get autoremove --purge xubuntu-* && sudo apt-get autoremove --purge xfce*
     
Set Awesome as the default windows manager:

     sudo xfconf-query -c xfce4-session -p /sessions/Failsafe/Client0_Command -t string -s "awesome" -a
     
Restart lightdm service:

     sudo service lightdm restart
     
Copy awesome WM config file yo home directory:

	mkdir -p ~/.config/awesome/
	sudo cp /etc/xdg/awesome/rc.lua ~/.config/awesome/
	sudo chown YOURUSERNAME ~/.config/awesome/rc.lua

Finally, to get Awesome WM start automatically:

Open:

	nano ~/.bash_profile
	
and include:

	# startx automatically
	if [ -z "$DISPLAY" ] &amp;&amp; [ $(tty) = /dev/tty1 ]; then
  		startx
  	fi
  	
And open:

	nano ~/.xinitrc
	
including:

	# ~/.xinitrc	
	# This file is sourced when running 	startx and
	# other programs which call xinit
 
	# Start the window manager
	exec awesome

Reboot:

	sudo reboot
	
After of this, you can enjoy with your new system.


# Customizing the aparience:

The most interesting feature of awesome windows manager is the possibility to be customized freely. Awesome 3 uses a configuration file based on the Lua language. Lua is a simple language but very powerful becuse offers more control. Firstly it maybe intimidate but finally it is enough a litle bit number of notions to start to include changes in the original file. 

In my case I don't have include many changes firstly. Specially I have focused in widgets for my tool bar. 

In order to customize the windows manager it is necessary edit the file *rc.lua*. This one is normally stored in *~/.config/awesome/* but also it is possible access browsing into the default menu: *menu > awesome > edit config*

Before working with this file it is recommended check it previously to understand specially different parts of code to know where includes the piece of code of our new feature. These parts are fundamentally:

- Libraries definition
- Error handling
- Variables definition
- Widgets definition
- Layouts, menu options and tags definition for the tool bar
- Wibox of widgets addition
- Buttons and shortcuts functionality
- Signal definition for mouse

After including any change is required update. For this is possible reboot or use in the default menu the option: *menu > awesome > reboot*

Currently, this is my [rc.lua](https://github.com/jmquintana79/my_awesomewm/blob/master/rc.lua){:target="_blank"} file but now it is very simple. 

	
# Interesting tools:

Awesome WM it is possible be used with a convencional way (mouse, graphical file manager, etc) but really the most interesting way is use terminal and keyboard (shortcuts). OS based on Unix provide many tools to work from a terminal and Awesome WM allow to configure many terminals in the same screen.

For me, these maybe some interesting tools to start to operate with this system. 

### Install htop for tasks/memory usage monitoring and eog for open pictures

	sudo apt-get install htop
	sudo apt-get install eog # open pictures

This tooll allow open any picture from terminal.
	
### Install mdcharm: Markdown editor

    # a possible dependece
    sudo apt-get install libhunspell-1.3-0 libhunspell-dev
    # download package
    wget https://github.com/zhangshine/MdCharm/releases/download/1.2.0/mdcharm_1.2_amd64.deb
    # install
    sudo dpkg -i mdcharm_1.2_amd64.deb 
    sudo apt-get -f install

This tool for me is one of the best Markdown editor. It is easy to use and the markdown conversor is really good.

### Install sublime_text3

    sudo add-apt-repository -y ppa:webupd8team/sublime-text-3
    sudo apt-get update; sudo apt-get install -y sublime-text-installer

I think it is not necessary speak about this text editor. It is so good.

### Install notify-send: customizing OS notifications
    
    sudo apt-add-repository ppa:izx/askubuntu
    sudo apt-get update
    sudo apt-get install libnotify-bin

This tool launch customized OS reminders or advices setup for the user. For example, I use to remember me the time o'clock after to be included in CRON.     
    
### Install multitail: monitoring of logs

    sudo apt-get install multitail

This is a very interesting tool. It is the same than command 'tail' but also allow the possibility to show in the same time several files. This one is very useful for monitoring sevelar logs of several applications running in streaming.   

### Install how2 library: stackoverflow from terminal Linux

    #Install node: 
    sudo apt-get install nodejs npm 
    #Make a symlink: 
    sudo ln -s /usr/bin/nodejs /usr/bin/node 
    #Then install how2: 
    npm install -g how2
    
[Stackoverflow](http://stackoverflow.com/) is a website reference for developers. In order to fix any code problem or remember any forgotten command, this is a good place to be consulted. So, how2 it is very interesting because provide a very simple way to consult in Stackoverflow from terminal. 

### Install telegram for terminal

Despite of [Telegram](https://telegram.org/) is not the most used messenger tool, I think many people know about this one. For me is the best.  

Requeriments:

    sudo apt-get update 
    sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev sudo apt-get install libevent-dev 
    sudo apt-get install libjansson*
    
Install:

    sudo apt-get install git
    # download package
    git clone --recursive https://github.com/vysheng/tg.git
    # enter in folder and install
    ./configure
    make
        
The executable is inside of 'bin' folder.

### Install speedometer: network monitoring

Install:

    sudo apt-get install speedometer

Usage from terminal:

    speedometer -l  -r <<name_network>> -t <<name_network>> -m $(( 1024 * 1024 * 3 / 2 ))
    
This tool allow monitoring our network very easily. There are very similar tools available, any of these, sure more powerful, but speedometer keep the best equilibrium between easiness and usefulness.

### Install Nautilus

    sudo apt-get install nautilus
    sudo apt-get install nautilus-open-terminal
    sudo apt-get install nautilus-actions

Working with terminal, it is not necessary use service as Nautilus, but for me, sometimes, it is confortable.     
    
###  Install MegaSync: cloud storage

For many years, users prefer work with their information storaged into own hard-drive. But, currently and I think in the future, the use of cloud storage service will be extended and our personal computers will be more slim, more ligth and with a bigger connectivity. Mega cloud services provide free 50GB, the possibility to be used from browser or directly from our file manager after installing any extension. Work and sincronize very good. Of course, it is necessary [donwload](http://ubuntuhandbook.org/index.php/2014/09/install-mega-client-ubuntu-linux/) any packages.

 Install:
 
    sudo apt-get install libcrypto++9 
    sudo dpkg -i megasync-xUbuntu_14.04_amd64.deb 
    sudo dpkg -i nautilus-megasync-xUbuntu_14.04_amd64.deb
    
Now it is neccesary launch 'megasync' and logging to add in Nautilus the "Mega" folder and syncronize with cloud.


### Install any translater for ONLINE use by terminal:

Firstly is necessary install:

    sudo apt-get install libtranslate-bin


This library use online the google translate engine.

Usage:

    echo "what are you doing" | translate-bin -s google -f en -t es
    #" onmouseover="this.style.backgroundColor='#ebeff9'" onmouseout="this.style.backgroundColor='#fff'">Qué estás haciendo


But maybe this bash command is not easy to remember or write every time. For this reason it is possible iinclude a function alias into .bashrc file.

    ## translater
    mytranslater() {
        echo $3 | translate-bin -s google -f $1 -t $2
    }
    alias translate=mytranslater # $1=language 1 / $2=language 2 / $3=text to be tr$


For this function alias, the usage would be:

    translate en es "what are you doing"
    #" onmouseover="this.style.backgroundColor='#ebeff9'" onmouseout="this.style.backgroundColor='#fff'">Qué estás haciendo

