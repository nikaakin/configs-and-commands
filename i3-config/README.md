
# I3 setup:

## Usage:

- Put `config` and  `i3status.conf` in ```~/.config/i3/``` directory.
- Put `picom.conf` in ```~/.config/picom/``` directory.

#### More info what each of them are:

- `config` is main config file for i3wm. There are all keyboard variations and more stuff about i3vm workflow (as well as loading the statusbar, setting background image, switching languages and so on.)
- `i3status.conf` is configuration about status bar, what is displayed there and how.
- `picom.conf` includes configuration for i3wm composition package picom. VS Code had split second flash of white screen each time switching window to it. this configuration fixed it and added more smooth animations.
- Both (`picom.conf` and `i3status.conf`) are used in config as this is the starting point of i3wm. 

#### Debugging:

- Use `i3-msg reload` or `i3-msg restart` to see changes you made in config files. (If there is no difference `i3-msg exit` or `reboot`). All those commands have keyboard combinations as well defined in `config`.
- If some changes are still not visible after `i3-msg reload` or `i3-msg restart` then change`exec` with `exec_always` and remove `--no-startup-id` as well.
