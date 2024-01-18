Recommended way to use custom scripts is to make a directory in home for example named `bin-assets` and another directory `bin`.
In `bin-assets` put all your custom scripts and in `bin` make a file maching the name the command you want to execute for example file named `alarm-notification` and inside the file put the following code:

```bash
#!/bin/bash
source /home/nika/bin-assets/alarm-notification/alarm-notification
```

update the path to actual script on your machine respcetively.

after this in you .bashrc or .zshrc file add the following line:

```bash
source $HOME/bin/*
```

to source all command you add in bin directory.
