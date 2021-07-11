# Yammit

A command line interface to Yamaha A/V products (receivers, home theater systems)

Set the hostname of your device in `~/.config/yammit/env` like so:

```sh
YAMMIT_RECEIVER_HOST=RX-V581-DC2176.local
```

Finding the device's hostname is an exercise for the user.

Once you have checked out this repository, add `zsh` tab completion:

```sh
source _yammit
```

`yammit` is written in `zsh` and relies on `curl` and `jq`.
You may need to install these packages yourself.

This is a partial implementation of the Yamaha Extended Control API calls.
If there's tab completion for it, it's supported.

Examples to try:

```sh
./yammit setPower main toggle
./yammit setInput main spotify
./yammit setPlayback pause
./yammit setPlayback play
./yammit setVolume main up
./yammit setVolume main down
```
