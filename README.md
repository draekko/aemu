# Android emulator hosts file syncing #

Syncs your `/etc/hosts` with your Android virtual devices.

## Why is this needed? ##

Unlike the iOS simulator, the Android emulator ignore's your system's hosts file.

## Install ##

You'll need Bash 4. OS X < 10.8 comes with Bash 3, so you'll need to [upgrade](http://apple.stackexchange.com/a/24635/28699).

```bash
git clone git@github.com:mattcg/android-hosts.git
cd android-hosts/
./android-hosts
```

You'll be prompted to select a virtual device by name. After that, your `$VISUAL` editor should open the hosts file for last minute editing. Remember to use `10.0.2.2` instead of `127.0.0.1`.

Save the file and exit to push the changes.

Symlink or copy the script into `/usr/local/bin` if you want to call it more easily.

```bash
ln -s ./android-hosts /usr/local/bin/ahosts
ahosts
```

## Options ##

All options will be passed to `emulator`. This is useful if for example you want to enable HTTP proxying in the emulator.

```bash
./android-hosts -http-proxy http://127.0.0.1:8888
```

## License ##

Copyright © 2013 Matthew Caruana Galizia, licensed under an [MIT license](http://mattcg.mit-license.org/).
