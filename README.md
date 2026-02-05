# Azuretha
*A hush of rose, softened for touch*

This is customized BeautyLine theme variation used in my [Rice](https://github.com/VaccuumDev/Archlinux-rice) 
This repository also contains a copy of [BeautyLine](https://www.gnome-look.org/p/1425426/).

### Troubleshooting

In most versions, there is a badly named file that causes the following error.

```shell
gtk-update-icon-cache: The generated cache was invalid.
```

Renaming it should fix the issue.

```shell
$ mv apps/scalable/goa-account-msn.svg\n.svg apps/scalable/goa-account-msn.svg
```

Though, it could be any other file name.

#### Find problematic filename

```console
$ ls -a -R * > filenames
$ vim filenames
```

Once in Vim, use search and replace to discard symlinks.

```
:%s/ -> /***/g
```

Then replace white spaces.

```
:%s/ /@@@/g
```

Now searching for `@@@` should hopefully point to the problematic (s) file (s).

```
$ mv apps/scalable/keysmith\ 1.svg apps/scalable/keysmith_1.svg
```
