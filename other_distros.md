# Non Debian-based distro, running the native client

Oh, so you chose the **VERY** hard way.

Given it's 2025, we assume you are using the 64bit client

## Download and execute the installer

1. [Download the game](https://www.championsofregnum.com/index.php?l=1&sec=6)
2. Make the installer executable:
   - either through a right click on your installation file, then (usually) properties, then setting it executable for the user
   - or easier, in a terminal: `chmod 0700 ~/Downloads/ROInstall_64`
3. Execute the installer:
   - just (double) click on it
   - you can also run it from the terminal: `~/Downloads/ROInstall_64`
  
## Installing packages and necessary symbolic links

See also https://github.com/mascaldotfr/cor-debian-packages

It's where your mileage may vary. Technically you need to:

1. Install the `gtk2` and `libtinfo` packages (`ncurses` is most likely already installed)
2. Symlink:
   - `libncursesw.so.6` to `libncursesw.so.5`
   - `libtinfo.so.6` to `libtinfo.so.5`

Some known working infos are presented below.

### Void Linux

```sh
sudo ln -s /usr/lib64/libncursesw.so.6 /usr/lib64/libncursesw.so.5
sudo xbps-install ncurses-libtinfo-libs
sudo ln -s /usr/lib64/libtinfo.so.6 /usr/lib64/libtinfo.so.5
```

### Nobara

At least one player reported to be able to run the game without further modifications.

## Have fun

You may get further issues after running the game, see [the troubleshooting version](troubleshooting.md) if it occurs.
