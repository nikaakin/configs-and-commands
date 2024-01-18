# I3 setup:

I3 is a tiling window manager, completely written from scratch. The target platforms are GNU/Linux and BSD operating systems, our code is Free and Open Source Software (FOSS) under the BSD license.

## Usage:

- Put `netspeed.sh`, `config` and `i3status.conf` in `~/.config/i3/` directory.
- Put `picom.conf` in `~/.config/picom/` directory.

#### More info what each of them are:

- `config` is main config file for i3wm. There are all keyboard variations and more stuff about i3vm workflow (as well as loading the statusbar, setting background image, switching languages and so on.)
- `i3status.conf` is configuration about status bar.
- `picom.conf` includes configuration for i3wm composition package picom. In my case vs code had split second flash of white screen each time switching window to it. this configuration fixes it and add more smooth animations.
- `netspeed.sh` is a script to display network speed in statusbar. this script is calling the i3status command with i3status.conf file and adding network speed to it. (i3status.conf is calling this script as well.). This script itself is called in `config` file from `bar { ... }` . if you dont want network speed to be displayed on the bar open `config` and go down to here:

```
bar {
   # status_command i3status
    status_command sh ~/.config/i3/netspeed.sh
    position top
    
    colors {
        background          $bg
        statusline          $fg
        separator           $hi
        focused_workspace   $gn        $bg        $ac
        active_workspace    $gn        $ac        $tx
        inactive_workspace  $bg        $bg        $ia
        urgent_workspace    $rd        $bg        $ac
    }
}

```

remove the comment from  ` status_command i3status` line  and comment the following line like so :     `#status_command sh ~/.config/i3/netspeed.sh`

#### Debugging:

- `i3-msg reload` or `i3-msg restart` to resource them. (If its not resourcing the config file `i3-msg exit` or `reboot`). All those commands have keyboard combinations as well.
- If something is not resourcing change `exec` with `exec_always` and remove `--no-startup-id` as well.
