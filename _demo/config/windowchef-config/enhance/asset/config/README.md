
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
├── style
│   ├── bar
│   │   └── windowchef-bar-clock.sh
│   └── picom
│       └── picom.conf
├── apps.conf
├── autostart
├── environment
├── key.conf
└── rc.conf

3 directories, 7 files
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
