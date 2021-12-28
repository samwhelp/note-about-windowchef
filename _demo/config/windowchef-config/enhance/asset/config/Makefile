default: help
.PHONY: default

help:
	@echo 'Usage:'
	@echo '	$$ make [action]'
	@echo
	@echo 'Example:'
	@echo '	$$ make'
	@echo '	$$ make help'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo
	@echo '	$$ make test'
	@echo

.PHONY: help


install: autostart-install config-install compositor-install panel-install wallpaper-install
#	tree --dirsfirst ~/.config/windowchef
.PHONY: install

autostart-install:
	install -Dm644 ./windowchef/environment ~/.config/windowchef/environment
	install -Dm755 ./windowchef/autostart ~/.config/windowchef/autostart
.PHONY: autostart-install

config-install:
	install -Dm755 ./windowchef/windowchefrc ~/.config/windowchef/windowchefrc
	install -Dm644 ./windowchef/sxhkdrc ~/.config/windowchef/sxhkdrc
.PHONY: config-install

panel-install:
	install -Dm644 ./windowchef/style/tint2/tint2rc ~/.config/windowchef/style/tint2/tint2rc
.PHONY: panel-install

compositor-install:
	install -Dm644 ./windowchef/style/picom/picom.conf ~/.config/windowchef/style/picom/picom.conf
.PHONY: compositor-install

wallpaper-install:
	install -Dm755 ./windowchef/bin/windowchef-wallpaper-ctrl-shuf ~/.config/windowchef/bin/windowchef-wallpaper-ctrl-shuf
	install -Dm755 ./windowchef/bin/windowchef-wallpaper-ctrl-default ~/.config/windowchef/bin/windowchef-wallpaper-ctrl-default
.PHONY: wallpaper-install




remove: autostart-remove config-remove compositor-remove panel-remove wallpaper-remove
#	tree --dirsfirst ~/.config/windowchef
.PHONY: remove

autostart-remove:
	rm -f ~/.config/windowchef/environment
	rm -f ~/.config/windowchef/autostart
.PHONY: autostart-remove

config-remove:
	rm -f ~/.config/windowchef/rc.conf
	rm -f ~/.config/windowchef/key.conf
	rm -f ~/.config/windowchef/apps.conf
.PHONY: config-remove

panel-remove:
	rm -f  ~/.config/windowchef/style/tint2/tint2rc
.PHONY: panel-remove

compositor-remove:
	rm -f  ~/.config/windowchef/style/picom/picom.conf
.PHONY: compositor-remove

wallpaper-remove:
	rm -f  ~/.config/windowchef/bin/windowchef-wallpaper-ctrl-shuf
	rm -f  ~/.config/windowchef/bin/windowchef-wallpaper-ctrl-default
.PHONY: wallpaper-remove


test:
	./xephyr-run-windowchef.sh
.PHONY: test

stop:
	killall -9 bash
.PHONY: stop
