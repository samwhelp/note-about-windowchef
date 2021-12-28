
# User Config


## Subject

* [User Config Dir Path](#user-config-dir-path)
* [User Config File List](#user-config-file-list)
* [Howto](#howto)


## User Config Dir Path

* [~/.config/windowchef](./)

## User Config File List

run

``` sh
tree --dirsfirst ~/.config/windowchef
```

show

```
/home/user/.config/windowchef
├── bin
│   ├── windowchef-wallpaper-ctrl-default
│   └── windowchef-wallpaper-ctrl-shuf
├── style
│   ├── picom
│   │   └── picom.conf
│   └── tint2
│       └── tint2rc
├── autostart
├── environment
├── sxhkdrc
└── windowchefrc

4 directories, 8 files
```

## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```
