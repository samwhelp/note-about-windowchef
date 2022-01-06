
# Boot

## Subject

* [Xsession](#xsession)
* [Autostart](#autostart)
* [Howto](#howto)


## Xsession

| Path | Note |
| --- | --- |
| [/usr/share/xsessions/windowchef-session.desktop](xsessions/windowchef-session.desktop) | start here |
| [/usr/share/windowchef/xsessions/windowchef-session](xsessions/windowchef-session) | windowchef-session.desktop call this script |


## Autostart

> Not using system wild if user file exists.

### System Wild

| Path |
| --- |
| [/usr/share/windowchef/config/windowchef/environment](config/windowchef/environment) |
| [/usr/share/windowchef/config/windowchef/autostart](config/windowchef/autostart) |


### Per User

| Path |
| --- |
| [~/.config/windowchef/environment](../asset/config/environment) |
| [~/.config/windowchef/autostart](../asset/config/autostart) |


## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```
