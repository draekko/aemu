# Android emulator tools #

Scripts added as I go along.

## aemu-hosts ##

Syncs your `/etc/hosts` with your Android virtual devices.

### Why is this needed? ###

Unlike the iOS simulator, the Android emulator ignores your system's hosts file.

### Usage ###

You'll need Bash 4. OS X < 10.8 comes with Bash 3, so you'll need to [upgrade](http://apple.stackexchange.com/a/24635/28699).

```bash
git clone git@github.com:mattcg/aemu.git
cd aemu/
./aemu-hosts -h
```

Without `-a`, you'll be prompted to select a virtual device by name.

With `-e`, your `$VISUAL` editor should open the hosts file for last minute editing. Remember to use `10.0.2.2` instead of `127.0.0.1`.

Save the file and exit to push the changes.

## aemu-sms ##

Send an SMS directly to the running virtual device.

### Why is this needed? ###

Using the shell is annoying.

### Usage ###

```bash
./aemu-sms -h
```

Use `-m` to specify the message and the optional `-n` for the phone number.

## License ##

Copyright © 2013 Matthew Caruana Galizia, licensed under an [MIT license](http://mattcg.mit-license.org/).
