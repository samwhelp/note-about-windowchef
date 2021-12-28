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


install: autostart-install config-install picom-install panel-install
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
	install -Dm755 ./windowchef/style/tint2/tint2rc ~/.config/windowchef/style/tint2/tint2rc
.PHONY: panel-install

picom-install:
	install -Dm644 ./windowchef/style/picom/picom.conf ~/.config/windowchef/style/picom/picom.conf
.PHONY: picom-install




remove: autostart-remove config-remove picom-remove panel-remove
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

picom-remove:
	rm -f  ~/.config/windowchef/style/picom/picom.conf
.PHONY: picom-remove



test:
	./xephyr-run-windowchef.sh
.PHONY: test

stop:
	killall -9 bash
.PHONY: stop
