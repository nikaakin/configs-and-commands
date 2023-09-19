# I3 setup:
I3 is a tiling window manager, completely written from scratch. The target platforms are GNU/Linux and BSD operating systems, our code is Free and Open Source Software (FOSS) under the BSD license.

## Usage:

- Put `config` and `i3status.conf` in `~/.config/i3/` directory.
- Put `picom.conf` in `~/.config/picom/` directory.

#### More info what each of them are:

- `config` is main config file for i3wm. There are all keyboard variations and more stuff for i3vm setup (as well as loading the statusbar, setting background image, switching languages and so on.)
- `i3status.conf` is configuration about status bar.
- `picom.conf` includes configuration for i3wm composition package `picom`. In my case VScode had split second flash of white screen each time switching window to it. this configuration fixes it and adds more smooth animations.

#### Debugging:

- `i3-msg reload` or `i3-msg restart` to resource them. (If its not resourcing the config file `i3-msg exit` or `reboot`). All those commands have keyboard combinations as well.
- If something is not resourcing change `exec` with `exec_always` and remove `--no-startup-id` as well.
