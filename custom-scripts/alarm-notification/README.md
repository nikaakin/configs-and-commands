# Alarm Notification

Timer to alarm you when time is up with popup notification. First argument is the time in minutes from now you want the notification to be fired.

## Prerequisite:

- [at](https://linux.die.net/man/1/at) - `at` and `batch` read commands from standard input or a specified file which are to be executed at a later time.
- [notify-send](https://man.archlinux.org/man/notify-send.1.en) - With `notify-send` you can send desktop notifications to the user via a notification daemon from the command line.

## Usage:

- Source the executable `alarm-notification` file and you will get the access to `alarm-notification` command.
- First argument of the command is the time you want the notification to run notify you. Without providing this argument notification will be fired instantly. 
- Second argument is option it just modifies the text on the notification.

## Customize:

- For now there is no argument responsible for advenced customization of text. So you might need to change the text from file itself for now.
- If you wish to store .wav and .png files somewhere else update the path in the command file respectivle for command to work properly and source command again.

## Examples:

- Alarm will be up in 1 minute : `alarm-notification 1`.
- View all prepared notification by : `atq`. Which will show something like this : `48	Sun Sep 17 21:46:00 2023 a user` meaning there is one notification which will be fired at the time specified there.
- If you wish to remove the specific notification `atrm <id>`. id in our case is `48` from  here `48	Sun Sep 17 21:46:00 2023 a user`.  

