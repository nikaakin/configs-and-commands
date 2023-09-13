
# I3 setup:

## Usage:

- Put `config` and  `i3status.conf` in ```~/.config/i3/``` directory.
- Put `picom.conf` in ```~/.config/picom/``` directory.

#### More info what each of them are:

- `config` is main config file for i3wm. There are all keyboard variations and more stuff about i3vm workflow (as well as loading the statusbar, setting background image, switching languages and so on.)
- `i3status.conf` is configuration about status what is displayed there and how.
- `picom.conf` includes configuration for i3wm composition package picom. In my case vs code had split second flash of white screen each time switching window to it. this configuration fixes it and add more smooth animations.

#### Debugging:

- `i3-msg reload` or `i3-msg restart` to resource them. (If its not resourcing the config file `i3-msg exit` or `reboot`). All those commands have keyboard combinations as well.
- If something is not resourcing change `exec` with `exec_always` and remove `--no-startup-id` as well.
