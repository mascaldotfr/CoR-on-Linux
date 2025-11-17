# General troubleshooting

## No textures

You had a blank page at character selection screen, and now ingame you get something like that:

![](img/troubleshooting.md/1.jpg)

You will need to nerf your GPU to make it a 2009 one. Don't worry, it only applies to the game!

You can modify your launcher icon to use this command line instead :

```sh
/usr/bin/env MESA_EXTENSION_MAX_YEAR=2009 /where/is/regnum/rolauncher
```

## Limited FPS

On Linux, vsync is usually the default, whatever you put in the game options.

You can modify your launcher icon to use this command line instead :

```sh
/usr/bin/env vblank_mode=0 /where/is/regnum/rolauncher
```

## Weird thousands separators

The game is in [latin1](https://en.wikipedia.org/wiki/ISO/IEC_8859-1), but modern Linuces use UTF8.

It's mostly a French thing. Check your operating system docs to make the non UTF8 (usually ISO-8859-1) locale available.

Once done, you can modify your launcher icon to use this command line instead (example for French) :

```sh
/usr/bin/env LANG=fr_FR.ISO-8859-1 /where/is/regnum/rolauncher
```

Known working locales changes below.

### Debian and derivatives

```shell
sudo dpkg-reconfigure locales
# tick your language, for exemple fr_FR for French
# validate the change
# Ensure the locale is well installed
locale -a
```
