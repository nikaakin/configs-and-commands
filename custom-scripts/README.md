in your .bashrc or .zshrc file add the following line to execure custom scripts from anywhere in the terminal:

```bash
export PATH="$HOME/bin":$PATH
```

In case if the custom is command is a single file like `screen_off` in here put that in the ~/bin directory and make it executable by running `chmod +x screen_off` and then you can run the command from anywhere in the terminal.

Otherwise if the command has assets then make a directory in home for example named `bin-assets` and another directory `bin`.
In `bin-assets` put all your custom scripts and in `bin` make a file maching the name the command you want to execute for example file named `alarm-notification` and inside the file put the following code:

```bash
#!/bin/bash
/home/user/bin-assets/alarm-notification/alarm-notification $@
```

update the path to actual script on your machine respcetively.

Then make the file executable by running `chmod +x ~/bin/alarm-notification` and then you can run the command from anywhere in the terminal.
