*Notice:* I did a rewrite in python which can handle more players (probably your
 favorite among them) by default and is also able to handle multiple players
 running at the same time (like if you're watching a video in your browser and
 listening to music on your spotify or whatever you do). It's still an early
 release and I'd be happy if you gave it a try and let me know if something
 doesn't work for you.

 You can visit the [github page](https://github.com/folixg/python-pauseonlock)
 or just install via `pip install pauseonlock`

![logo](header.png)

# pause-on-lock

Automatically pause your music player when the screen gets locked and resume
playback, once the screen is unlocked again.

## Supported desktop environments

Currently [Unity](https://launchpad.net/unity),
[Cinnamon](https://github.com/linuxmint/Cinnamon),
[GNOME](https://www.gnome.org/), [MATE](https://mate-desktop.org/),
[KDE](https://kde.org/), [POP!\_OS](https://pop.system76.com) and
[XFCE](https://www.xfce.org) are supported. The currently running desktop is
detected using `$XDG_CURRENT_DESKTOP`.

## Installation

Download the executable for the [latest
release](https://github.com/folixg/pause-on-lock/releases/download/v2.1.0/pause-on-lock)
and run

```
sudo install pause-on-lock /usr/local/bin/

# make user service
cp pauseonlock.service $HOME/.config/systemd/user/pauseonlock.service

    413  systemctl --user enable pauseonlock.service 
    540* systemctl --user restart pauseonlock.service                                                                                                         
    541* systemctl --user status pauseonlock.service
    
```

If you don't have sudo rights or don't want a system-wide installation, change
the install destination directory to e.g. `$HOME/bin` (and make sure that that
folder is in your `$PATH`).

## Usage

