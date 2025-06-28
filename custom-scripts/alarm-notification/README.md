# Alarm Notification

#### A simple shell script to notify you when your timer is up using a popup notification and optional sound alert.

---

## ✅ Features

- Set a timer in minutes that runs in the background
- Get a desktop popup notification when time is up
- Optional sound alarm
- Supports both **Linux** and **macOS**

---

## 📦 Prerequisites

### ▶️ Linux

- [`at`](https://linux.die.net/man/1/at) — used to schedule a future job
- [`notify-send`](https://man.archlinux.org/man/notify-send.1.en) — sends popup notifications
- [`aplay`](https://linux.die.net/man/1/aplay) — plays `.wav` audio files

### ▶️ macOS

- `sleep` and backgrounding `(& disown)` — used instead of at to delay and detach jobs.
- `terminal-notifier` — replacement for notify-send, used to show macOS-native notifications.
- `afplay` — built-in macOS command-line audio player (used instead of aplay).

## Examples:

- Alarm will be up in 1 minute : `alarm-notification 1`.
- View all prepared notification by : `atq`. Which will show something like this : `48	Sun Sep 17 21:46:00 2023 a user` meaning there is one notification which will be fired at the time specified there.
- If you wish to remove the specific notification `atrm <id>`. id in our case is `48` from here `48	Sun Sep 17 21:46:00 2023 a user`.

## Usage On Different Platforms

- `alarm-notification` file includes scripts for both Linux and macOS. Comment out the one you don't need.

## Limitations

- On Mac custom notification image wont work. To make it work user -sender option on terminal-notifier command. -sender should be an application bundle identifier.

## Structure

alarm-notification/
├── alarm-notification # ← executable script
├── alarm-notification.wav # ← optional sound
├── alarm-notification.png # ← optional icon
├── README.md
└── LICENCE

## License

This project is licensed under the MIT License - see the [LICENCE](./LICENCE) file for details.
